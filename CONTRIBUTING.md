# Sumário
1. GitHub
    1. Commits
        1. Padrão de commit
        1. Boas práticas

    1. Pull requests e branches
        1. Nomear branches
        1. Code reviews
        1. Padrão de pull request

    1. Issues
        1. Issue templates

    1. Releases
        1. Versioning

1. Integração e entrega de código
    1. CI/CD
        1. Frameworks

    1. Testes
        1. Django Rest Framework
        1. React Native

    1. Formatação de código
        1. Python
        1. Typescript
        1. Dockerfile

    1. Ambiente de desenvolvimento
        1. Documento de instalação
        1. Documento de execução

1. Comunicação
    1. GitHub
    1. WhatsApp
    1. Discord

1. Licença(s)
    1. Licença do código

# 1. GitHub
## 1.1 Commits
### 1.1.1 Padrão de commit

Commits devem descrever as alterações feitas de forma clara e breve.

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

### 1.2.3 Padrão de pull request

## 1.3 Issues
### 1.3.1 Issue templates
O GitHub tem uma feature chamada de ["issue templates"](https://docs.github.com/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository). Os nossos templates estão a pasta [".github/ISSUE_TEMPLATE"](https://github.com/fga-eps-mds/2022-1-TiControla-FrontEnd/tree/main/.github/ISSUE_TEMPLATE) no repositório do [frontend](https://github.com/fga-eps-mds/2022-1-TiControla-FrontEnd). Para criar um template novo, basta seguir este guia do github: https://docs.github.com/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository.

O ideal é que todas as issues sigam os templates, porém os templates são só um ponto inicial e não há problema em fugir do padrão.

## 1.5 Releases
### 1.5.1 Versioning

# 2. Integração e entrega de código
## 2.1 CI/CD 
CI (continuous integration) significa integração contínua, e CD (continuous deployment) significa entrega contínua.

### 2.1.1 Frameworks

## 2.2 Testes
### 2.2.1 Django Rest Framework (DRF)
O DRF auxilia de certa forma a implementação de testes, visto que descreve em sua documentação oficial uma série de classes e recursos com este fim, como a APIClient e APITestCase.

### 2.2.2 React Native

## 2.3 Formatação de código
### 2.3.1 Python
### 2.3.2 Typescript
### 2.3.3 Dockerfile

## 2.4 Ambiente de desenvolvimento
### 2.4.1 Documentos de instalação
### 2.4.2 Documentos de execução

# 3. Comunicação
## 3.1 GitHub
Armazenamento de código fonte, transparência na realização de tarefas, documentação de interações.

## 3.2 WhatsApp
Diálogo diaŕio e decisões de baixo impacto.

## 3.3 Discord
Realização — por meio de chamadas de aúdio — de pareamentos, de reviews, de plannings e de dailies.

# 4. Licença(s)
## 4.1 Licença do código


### Referências
* [Commit Best Practices](https://microsoft.github.io/code-with-engineering-playbook/source-control/#commit-best-practices)
* [Naming branches](https://microsoft.github.io/code-with-engineering-playbook/source-control/naming-branches/)
* [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/#summary)
