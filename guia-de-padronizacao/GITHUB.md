# Guia de padronização usado no Git/GitHub

O objetivo deste guia é de apresentar de forma resumida os padrões/convenções de versionamento que serão utilizador pela nossa equipe, durante o desenvolvimento do nosso projeto, de modo a melhorar a 
se criar harmonia, providenciar um repositório mais organizado e permitir a fácil leitura . 


## Branches
### Nomenclatura de branch remota

Para a nomenclatura de uma (branch)[https://git-scm.com/docs/git-branch] **remota** , utilizamos a seguinte convenção:

*<feature/bug/update>/<epico>*

em que:

* *feature* corresponde a uma funcionalidade nova;
* *bug* corresponde a correção de uma funcionalidade que teve algum problema/bug;
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

*<nome_utilizador>/<feature/bug/update>/<epico/>/<historia_usuario>*

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
