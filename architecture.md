# Documento de arquitetura

## 1. Introdução

### 1.1 Objetivo
Este documento tem como finalidade uma breve apresentação da arquitetura do projeto, descrevendo como as diferentes partes interagem entre si e como funcionam num todo.

### 1.2 Escopo

A arquitetura do projeto é totalmente fundamentada e detalhada, para moldar uma base para a equipe de desenvolvimento, apresentando como será o comportamento do sistema. Este documento contem os registros e tópicos importantes relacionados à arquitetura do sistema, dando diretrizes, e total apoio para o uso de suas tecnologias .

### 1.3 Definições, Acrônimos e Abreviações

| **Sigla/Termo/Acrônimo** | **Definição** |
| ------------------------ | ------------- |
| MDS | Métodos de Desenvolvimento de <i>Software</i> |
| FGA | Faculdade do Gama |
| UnB | Universidade de Brasília |
| DRF | Django Rest Framework |
| MTV | Model Template View |
| JSON | JavaScript Object Notation |
| HTTP | Hypertext Transfer Protocol |
| HTTPS | Hypertext Transfer Protocol Secure |
| CI | Integração contínua |
| CD | Desenvolvimento contínuo ||
| GitHub Actions | Framework de CI/CD |
| REST | Representational State Transfer |
| API | Application Programming Interface |

## 2. Representação arquitetural

A aplicação possui vários núcleos independentes e os mesmos interajem-se entre si enviando requisições por intermédio do HTTP/HTTPS e cada núcleo foi desenvolvido usando tecnologias diferentes. Pelo fato de cada núcleo possuir uma determinada tecnologia distinta, o sistema no geral possui arquitetura de microsserviços.

### 2.1. Servidor central
Responsável pelo recebimento e processamento das demandas realizadas pelos usuários do frontend.

### 2.1.1. [Django REST Framework](https://www.django-rest-framework.org/)
TODO: Escrever pra que serve o framework e por qual motivo o framework foi escolhido. 

### 2.1.2. [MySQL](https://www.mysql.com/)
TODO: Escrever pra que serve o framework e por qual motivo o framework foi escolhido.

### 2.1.3. [Gunicorn](https://gunicorn.org/)
O comando padrão do DRF para começar um servidor ("python manage.py runserver") não foi feito para ser usado na produção. Ele não passou por testes de segurança nem testes de performance. Além disso, os desenvolvedores do DRF atualmente não tem intenção de fazer um comando que crie um servidor seguro ([fonte](https://docs.djangoproject.com/en/4.0/ref/django-admin/#runserver)). Logo, tivemos que substituir tal comando e decidimos usar o gunicorn pela grande quantidade de tutoriais disponíveis na internet que o utilizam.


### 2.2. Aplicativo mobile
Responsável pela visualização de dados e interação com o usuário.

### 2.2.1. [React Native](https://reactnative.dev/)
TODO: Escrever pra que serve o framework e por qual motivo o framework foi escolhido.

### 2.2.2. [Expo](https://expo.dev/)
TODO: Escrever pra que serve o framework e por qual motivo o framework foi escolhido.


## 3. Metas e Restrições arquiteturais

3.1 **Suportabilidade**

Suportar que celulares? Que sistemas operacionais (android, ios, windows phone)? A partir de que versão de cada sistema operacional?

3.2 **Usabilidade**

O sistema deverá ser intuitivo e de simples uso, de forma que a curva de aprendizado para utilizar a aplicação não seja um impedimento para usar o sistema.

3.3 **Ferramentas de Desenvolvimento**

Por enquanto, o frontend só tem o aplicativo mobile. Talvez, façamos um site eventualmente. O app está em Typescript utilizando os frameworks React Native e Expo.

O backend se baseia em uma API REST e no banco de dados. A API está em Python utilizando o framework Django Rest. O banco de dados está em MySQL.

A infraestrutura do backend é baseada em contêineres Docker (tanto para a API quanto para o banco de dados). Utilizar contêineres facilita tanto a entrega contínua da aplicação ao ambiente de produção quanto a execução da aplicação em ambientes de desenvolvimento.

3.4 **Confiabilidade**

O sistema deve ter uma cobertura mínima de testes de 90%, buscando garantir que suas funcionalidades foram suficientemente testadas.

## 4. Visão Lógica

### 4.1 Visão Geral

![https://user-images.githubusercontent.com/9947506/176018987-5ac04711-7778-4571-850d-b674dda9ab3e.png](https://user-images.githubusercontent.com/9947506/176018987-5ac04711-7778-4571-850d-b674dda9ab3e.png)


### 4.2 Diagrama de pacotes
TODO

### 5.1 Banco de Dados

#### 5.1.1 Entidades
TODO

#### 5.1.2 Atributos
TODO

#### 5.1.2 Relacionamentos
TODO

#### 5.1.3 Diagrama Entidade-Relacionamento
TODO

#### 5.1.4 Diagrama Lógico de Dados
TODO

## Referências
