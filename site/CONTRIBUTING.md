# Sumário
<!-- o sumário ("table of contents") pode ser gerado e atualizado automaticamente usando a extensão "Markdown All in One" do vscode ou a ferramenta markdown-toc -->

- [1. GitHub](#1-github)
  - [1.1 Commits](#11-commits)
    - [1.1.1 Padrão de commit](#111-padrão-de-commit)
  - [1.1.2 Boas práticas](#112-boas-práticas)
  - [1.2 Pull requests e branches](#12-pull-requests-e-branches)
    - [1.2.1 Nomear branches (remotas)](#121-nomear-branches-remotas)
    - [1.2.2 Code reviews](#122-code-reviews)
    - [1.2.3 Padrão de pull request](#123-padrão-de-pull-request)
  - [1.3 Issues](#13-issues)
    - [1.3.1 Issue templates](#131-issue-templates)
  - [1.5 Releases](#15-releases)
    - [1.5.1 Versioning](#151-versioning)
- [2. Integração e entrega de código](#2-integração-e-entrega-de-código)
  - [2.1 CI/CD](#21-cicd)
    - [2.1.1 Frameworks](#211-frameworks)
  - [2.2 Testes](#22-testes)
    - [2.2.1 Django Rest Framework (DRF)](#221-django-rest-framework-drf)
    - [2.2.2 React Native](#222-react-native)
  - [2.3 Formatação de código](#23-formatação-de-código)
    - [2.3.1 Python](#231-python)
    - [2.3.2 Typescript](#232-typescript)
    - [2.3.3 Dockerfile](#233-dockerfile)
  - [2.4 Ambiente de desenvolvimento](#24-ambiente-de-desenvolvimento)
    - [2.4.1 Documentos de instalação](#241-documentos-de-instalação)
    - [2.4.2 Documentos de execução](#242-documentos-de-execução)
- [3. Comunicação](#3-comunicação)
  - [3.1 GitHub](#31-github)
  - [3.2 WhatsApp](#32-whatsapp)
  - [3.3 Discord](#33-discord)
- [4. Licença(s)](#4-licenças)
  - [4.1 Licença do código](#41-licença-do-código)
- [5. Referências](#5-referências)

# 1. GitHub
## 1.1 Commits
### 1.1.1 Padrão de commit

Commits devem descrever as alterações feitas de forma clara e breve. Todo commit deve estar associado a uma issue.

Regras para escrita das mensagens nos commits:
```
#issueID Mensagem breve descrevendo alterações

Mensagem mais detalhada sobre o que foi feito neste commit. (Opcional)
```

Exemplo:
```
git commit -m "#3 Mensagem breve descrevendo alterações" -m "Mensagem mais detalhada sobre o que foi feito neste commit (Opcional)"
```

## 1.1.2 Boas práticas
**Faça commits atômicos (pequenos):** Faz com que a revisão do código seja elaborada com maior facilidade e se for necessário reverter o código em algum ponto, perde-se menos alterações feitas ou trabalhos.

**Faça commits de funcionalidades prontas e testadas:** Nunca dê commits a códigos incompletos, tenha o hábito de testar o código antes de fazer o commit.

**Escreva sempre mensagens esclarecedoras no commit:** Uma boa mensagem de commit deve responder à questão "Por que este código é necessário?".

## 1.2 Pull requests e branches

### 1.2.1 Nomear branches (remotas)

Com exceção de branches que derivem da main, todas as branches devem começar com o nome da branch da qual elas derivam. Por exemplo, a branch "django-api" é derivada da main, e a branch "django-api-authentication" é derivada da branch "django-api".

"authentication" é o nome da feature que está sendo desenvolvida para ser integrada à branch principal "django-api". Logo, o padrão para nomear branches é "[branch-original]-[feature]".

Por exemplo,
```
branch original: django-api
feature a ser desenvolvida: authentication
nome da branch: django-api-authentication
```

Caso a feature já tenha sido colocada dentro da main, para fazer uma atualização ou consertar um bug, basta realizar as alterações na branch da feature e, depois, especificar no pull request o que foi feito.

```
branch original: django-api
feature que está sendo atualizada ou consertada: authentication
nome da branch: django-api-authentication
```

### 1.2.2 Code reviews
TODO

### 1.2.3 Padrão de pull request
TODO

## 1.3 Issues
### 1.3.1 Issue templates
O GitHub tem uma feature chamada de ["issue templates"](https://docs.github.com/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository). Os nossos templates estão a pasta [".github/ISSUE_TEMPLATE"](https://github.com/fga-eps-mds/2022-1-TiControla-FrontEnd/tree/main/.github/ISSUE_TEMPLATE) no repositório do [frontend](https://github.com/fga-eps-mds/2022-1-TiControla-FrontEnd). Para criar um template novo, basta seguir este guia do github: https://docs.github.com/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository.

O ideal é que todas as issues sigam os templates, porém os templates são só um ponto inicial e não há problema em fugir do padrão.

## 1.5 Releases
### 1.5.1 Versioning
TODO

# 2. Integração e entrega de código
## 2.1 CI/CD 
CI (continuous integration) significa integração contínua, e CD (continuous deployment) significa entrega contínua.

### 2.1.1 Frameworks
Decidimos usar o [GitHub Actions](https://github.com/features/actions) para fazer a integração e a entrega contínua. Não chegamos a explorar alternativas como Jenkins, CircleCI e TravisCI.

## 2.2 Testes
### 2.2.1 Django Rest Framework (DRF)
O DRF auxilia de certa forma a implementação de testes, visto que descreve em sua documentação oficial uma série de classes e recursos com este fim, como a APIClient e APITestCase.

### 2.2.2 React Native
TODO

## 2.3 Formatação de código
### 2.3.1 Python
[PEP 8](https://peps.python.org/pep-0008/) com [autopep8](https://pypi.org/project/autopep8/)

### 2.3.2 Typescript
TODO

### 2.3.3 Dockerfile
[hadolint](https://github.com/hadolint/hadolint)

## 2.4 Ambiente de desenvolvimento
### 2.4.1 Documentos de instalação
Um documento de instalação deve conter as seguintes seções: lista de dependências, troubleshooting, instalação, validação.

**Lista de dependências**: Softwares necessários para instalar o programa. Também é necessário especificar a versão de cada software. Por exemplo: git, python 3.10.5, react v17.0.

**Troubleshooting (opcional)**: Problemas communs que são encontrados ao instalar alguma das dependências ou ao rodar o software em algum sistema operacional.

**Instalação**: Tutorial de como instalar o software. Seja por meio de contêineres ou não, é necessário mostrar os comandos utilizados e explicar o motivo pelo qual cada um está sendo usado.

**Validação**: Como validar se a instalação do software deu certo. Pode ser rodando um script que verifica a instalação, seguindo um passo-a-passo por uma interface ou, até mesmo, executando uma sequência de comandos no terminal: o importante é fazer alguma verificação.

### 2.4.2 Documentos de execução
Esse tipo de documento não se aplica muito ao frontend (aplicativos e sites). O frontend já tem o documento de caso de uso. O documento de "como executar" é mais para softwares que vão ser usados por devs de software (como a "CLI" do [FrankMocap](https://github.com/facebookresearch/frankmocap#a-quick-start)).

Por exemplo, no caso da API, é necessário documentar como o frontend pode utilizar a API. O [Django REST Swagger](https://github.com/axnsan12/drf-yasg) gera uma documentação muito boa, mas falta explicar em que contexto cada uma das requisições HTTP deve ser feita.

# 3. Comunicação
Caso deseje entrar em algum dos canais de comunicação, entrar em contato pelo email "leonardomichalskim@gmail.com".

## 3.1 GitHub
O GitHub é o meio de comunicação padrão.

Armazenamento de código fonte, transparência na realização de tarefas, documentação de interações. É importante que qualquer desenvolvedor que chegue nos nossos repositórios seja capaz de resolver issues e abrir PRs.

## 3.2 WhatsApp
Marcar reuniões de pareamento. Tirar dúvidas rápidas. Avisar que botou algo no GitHub. Decisões de baixíssimo impacto.

Comunicação liberada **somente na semana da release** se necessário para entregar o código.

## 3.3 Discord
Realização — por meio de chamadas de aúdio — de pareamentos, de reviews, de plannings e de dailies.

# 4. Licença(s)
## 4.1 Licença do código
Copyright (c) EPS/MDS. All rights reserved.

Licensed under the [MIT](https://github.com/fga-eps-mds/2022-1-TiControla-FrontEnd/blob/main/LICENSE) license.



# 5. Referências
* [Commit Best Practices](https://microsoft.github.io/code-with-engineering-playbook/source-control/#commit-best-practices)
* [Naming branches](https://microsoft.github.io/code-with-engineering-playbook/source-control/naming-branches/)
* [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/#summary)
* [How to Contribute to Visual Studio Code](https://github.com/microsoft/vscode/wiki/How-to-Contribute)
