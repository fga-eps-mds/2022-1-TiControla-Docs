# Documento de Visão

## 1. Introdução

### 1.1 Propósito

Este documento visa demonstrar claramente as informações ao redor do aplicativo de finanças, incluindo o propósito do software, seu escopo, requisitos e identificar pessoas relevantes ao aplicativo, incluindo as partes interessadas/afetadas, desenvolvedores, *scrum master* (SM), *product owner* (PO).

### 1.2 Escopo

Um aplicativo de celular no qual seja possível monitorar o dinheiro que entrou e que saiu das contas de banco de um usuário, seja possível ver o histórico dos outros meses e controlar os gastos do cartão de crédito.

### 1.3 Definições, Acrônomos e Abreviações

| **Sigla/Termo/Acrônimo** | **Definição** |
| ------------------------ | ------------- |
| MDS | Métodos de Desenvolvimento de <i>Software</i> |
| FGA | Faculdade do Gama |
| UnB | Universidade de Brasília |


## **2. Posicionamento**

Facilitar o gerenciamento das finanças de uma pessoa com a vida financeira ativa por meio de um software.

### 2.1 Oportunidade de negócios

TODO

### 2.2 Descrição do problema

| O problema é | que afeta | uma boa solução seria |
| ------------ | --------- | --------------------- |
| Facilitar o gerenciamento de finanças mensais e anuais de um usuário | pessoas com a vida financeira ativa | um software que auxilie nas finanças do usuário |


### 2.3 Descrição da posição do produto

TODO

## **3. Descrição dos Envolvidos e dos Usuários**

### 3.1 Perfis dos Envolvidos

| Nome | Papel | GitHub | Responsabilidade |
| ---- | ----- | ------ | ---------------- |
| Professora Dra Carla Rocha | Avaliadora | @rochacarla | Avaliar a qualidade do projeto desenvolvido pelos alunos de MDS |
| 1 | Product Owner e Dev Frontend | @... | Tomada de decisões a respeito do produto; Criar e manter documentos; Desenvolver e testar o software |
| 2 | Dev Frontend | @... | Criar e manter documentos; Desenvolver e testar o software |
| 3 | Dev Frontend | @... | Criar e manter documentos; Desenvolver e testar o software |
| 4 | Dev Backend | @... | Criar e manter documentos; Desenvolver e testar o software |
| 5 | Dev Backend | @... | Criar e manter documentos; Desenvolver e testar o software |
| 6 | Dev Backend | @... | Criar e manter documentos; Desenvolver e testar o software |
| 7 | Scrum Master e Dev Backend | @... | Garantir boas práticas do XP e do Scrum; Criar e manter documentos; Desenvolver e testar o software |

### 3.2 Descrição dos Usuários

O "usuário anônimo" é uma pessoa que, por necessidade de organizar sua vida financeira, instalou o app em seu celular e que, por algum motivo (seja por ainda estar testando o app ou por não querer compartilhar o email com o app), ainda não cadastrou o seu email no app. Tal usuário deve poder utilizar todos os recursos do app de forma offline. A partir do momento que tal usuário realiza seu cadastro, ele se torna um "usuário cadastrado" e pode sincronizar seus dados entre diversos aparelhos celulares.

### 4. Alternativas e Concorrentes

TODO

## 5. Restrições

Listagem de restrições externas e outras dependências:

* Ter um aparelho celular.
* Conexão com a internet.

### 5.1 Restrições de Implementação
O sistema será implementado utilizando 2 principais frameworks, sendo eles o Django Rest para o back-end e o React Native para o app front-end.

### 5.2 Restrições de Design
Toda a interação com o software deve ocorrer de forma natural, de modo que o usuário não fique com dúvidas sobre como realizar determinada tarefa. Os recursos cujos usuários tem acesso devem ser de fácil entendimento, de modo que o usuário não desista durante alguma ação. Com a finalidade de alcançar um público maior, a aplicação será desenvolvida para usuários mobile.

### 5.3 Restrições de Confiabilidade
Visando facilitar a manutenção do projeto pela comunidade, os desenvolvedores tem o comprometimento de manter uma cobertura de testes mínima de 90%.

## **6. Requisitos do Produto**

Lista de categorias de prioridades para requisitos

| Tipo | Descrição |
| :- | :- |
| Alta | Requisitos indispensáveis para o funcionamento do sistema |
| Intermediária | Requisitos importantes para o sistema, mas caso não sejam implementados não resultará em um mal funcionamento do sistema |
| Útil | Requisitos que não são usados com tanta frequência e não são tão significativos na satisfação que o usuário tem sobre o sistema |

Lista de requisitos funcionais

<!-- | Identificador | Descrição | Depende de | Prioridade | -->
| Identificador | Descrição | Prioridade |
| --- | --- | --- |
| RF001 | O usuário deve ser capaz de se cadastrar no sistema | Alta |
| RF002 | O usuário deve logar e deslogar no sistema | Alta |
| RF003 | O usuário deve editar o perfil no sistema | Médio |
| RF004 | O usuário deve cadastrar seu próprio gasto, sendo crédito ou débito. | Alto |
| RF014 | CRUD débito | Alto |
| RF015 | CRUD crédito | Alto |
| RF016 | CRUD de gastos fixos | Médio |
| RF005 | O usuário deve ser capaz de cadastrar um limite personalizado para o gasto em cartão de crédito | Médio |
| RF006 | O usuário deve visualizar o seu saldo baseado em seus cadastros de entradas e saídas (débitos) | Alto |
| RF007 | O usuário deve visualizar o total dos seus lançamentos de crédito | Alto |
| RF008 | O usuário deve excluir a própria conta | Baixo |
| RF009 | O usuário deve solicitar recuraperação de senha | Médio |
| RF010 | O usuário deve visualizar o limite geral do gastos dos cartões | Médio |
| RF011 | O usuário deve ser capaz de visualizar os parcelamentos vigentes por ordem de vencimento | Médio |
| RF012 | O sistema deve fornecer um histórico de entradas e saídas de todos meses cadastrados - Débito | Alto |
| RF013 | O sistema deve possibilitar a edição das entradas e saída dos meses | Alto |
| RF017 | O sistema deve fornecer um histórico de lançamentos de todos meses cadastrados - Crétido | Alto |
| RF018 | O sistema deve fornecer/possibilitar visualização do total da fatura de cada cartão apelidado individualmente |  Alto |


## Referências
