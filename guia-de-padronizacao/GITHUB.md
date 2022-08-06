# Guia de padronização usado no Git/GitHub

O objetivo deste guia é de apresentar de forma resumida os padrões/convenções de versionamento que serão utilizador pela nossa equipe, durante o desenvolvimento do nosso projeto, de modo a melhorar a 
se criar harmonia, providenciar um repositório mais organizado e permitir a fácil leitura . 


## Branches

### Nomenclatura de branch remota

Para a nomenclatura de uma (branch)[https://git-scm.com/docs/git-branch] **remota** , utilizamos a seguinte convenção:

*<feature/fix/update>/<epico>*

em que:

* *feature* corresponde a uma funcionalidade nova;
* *fix* corresponde a correção de uma funcionalidade que teve algum problema/bug;
* *update* corresponde a atualização de uma funcionalidade já existente;
* *epico* corresponde ao épico;

#### Exemplos:

Para adicionar uma funcionalidade (que seja num épico), abra o terminal e digite:

```
git clone <repositorio>
cd <repositorio>
git checkout -b feature/acesso_usuario
git push origin feature/acesso_usuario

```
Lembrando que o épico *acesso_usuario* pode ser sub-dividido em *login_usuario*, *cadastro_usuario*, e *esqueceu_senha_usuario*, por exemplo.

### Nomenclatura de branch local

Para a nomenclatura de uma (branch)[https://git-scm.com/docs/git-branch] **local** , utilizamos a seguinte convenção:

*<nome_utilizador>/<feature/fix/update>/<epico/>/<historia_usuario>*

em que:

* *nome_utilizador* corresponde ao nome do usuário da conta do GitHub;
* *historia_usuario* corresponde a uma determinada história do usuário , ou seja, a funcionalidade mais atômica/simples;

#### Exemplos:

Para adicionar uma funcionalidade (que seja uma história do usuário), abra o terminal e digite:

```
git clone <repositorio>
cd <repositorio>
git ls-remote
```
Após a listagem das branches remotas, escolha a branch que corresponde ao épico.

```
git switch feature/acesso_usuario
git checkout -b roddas/feature/acesso_usuario/cadastro_usuario
...(faça as alterações necessárias, com todos os commits)
git checkout feature/acesso_usuario
git pull
git merge roddas/feature/acesso_usuario/cadastro_usuario
git push
```

## Workflow

Para o desenvolvimento do projeto:

* Todas as branches que correspondem histórias do usuário deverão ser incluídas nas branches que correspondem aos épicos;
* Todas as branches que correspondem aos épicos deverão ser incluídas na *develop*;
* No processo de lançamento da *release* a branch develop deverá ser incluída na *main*;

Ou seja, as branches menores serão incluídas nas branches maiores seguindo a ordem de uma pirâmide .


#### Exemplo:


```
LOCAL                                                      REMOTO (no GitHub)      
-----------------------------------------------------------------------------------------------------
roddas/feature/acesso_usuario/login_usuario           
roddas/feature/acesso_usuario/cadastro_usuario        ->  feature/acesso_usuario  ->  develop ->  main
roddas/feature/acesso_usuario/esqueceu_senha_usuario      feature/outra_feature
```


## Commits

Para a criação de um commit, seguimos a seguinte convenção:

*<nome_utilizador>/<feature/fix/update>/<historia_usuario> : <descricao>*

#### Exemplo:

```
git commit -m 'roddas/feature/cadastro_usuario : Criação do método que elabora a requisição AJAX com o servidor'
git commit -m 'roddas/update/cadastro_usuario : Adicionado um método que valida os dados antes do envio dos mesmos para o banco de dados'
```

### Boas práticas 

* **Faça commits atômicos (pequenos):** Faz com que a revisão do código seja elaborada com maior facilidade e se for necessário reverter o código em algum ponto, perde-se menos alterações feitas ou trabalhos. 

* **Faça commits de funcionalidades prontas e testadas:**  Nunca dê commits a códigos incompletos, tenha o hábito de testar o código antes de fazer o commit.

* **Escreva sempre mensagens esclarecedoras no commit:**

Uma boa mensagem de commit deve responder a seguinte questão:

* Por que este código é necessário ? Pode resolver um bug, adicionar uma feature ou para melhorar o desempenho. 

Uma boa estrutura da mensagem do commit :

* Separar o assunto do corpo da mensagem com uma linha em branco.
* O assunto deve contar no máximo 50 caracteres.
* A primeira letra do assunto deve ser sempre maiúscula
* Usar o modo imperativo na linha do assunto
* O corpo da mensagem deve conter no máximo 72 caracteres
* O corpo da mensagem deve explicar **o quê** e **porquê** e **como**.

Exemplo de uma mensagem de commit bem estruturada:

```
Adicionar o código de testes do login de usuário

- Ajuda o time a depurar o código
- Ajuda o time de revisão a documentar o código
```

### Referências
* (Commit Best Practices)[https://microsoft.github.io/code-with-engineering-playbook/source-control/#commit-best-practices]
* (Naming branches)[https://microsoft.github.io/code-with-engineering-playbook/source-control/naming-branches/]
* (Conventional Commits)[https://www.conventionalcommits.org/en/v1.0.0/#summary]