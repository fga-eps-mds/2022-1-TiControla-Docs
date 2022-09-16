# Documento de Arquitetura

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

<<<<<<< HEAD
### 2.1.1. [Django REST Framework](https://www.django-rest-framework.org/)
TODO: Escrever pra que serve o framework e por qual motivo o framework foi escolhido. 

### 2.1.2. [MySQL](https://www.mysql.com/)
TODO: Escrever pra que serve o framework e por qual motivo o framework foi escolhido.

### 2.1.3. [Gunicorn](https://gunicorn.org/)
O comando padrão do DRF para começar um servidor ("python manage.py runserver") não foi feito para ser usado na produção. Ele não passou por testes de segurança nem testes de performance. Além disso, os desenvolvedores do DRF atualmente não tem intenção de fazer um comando que crie um servidor seguro ([fonte](https://docs.djangoproject.com/en/4.0/ref/django-admin/#runserver)). Logo, tivemos que substituir tal comando e decidimos usar o gunicorn pela grande quantidade de tutoriais disponíveis na internet que o utilizam.
=======
### 2.1.1. Django REST Framework
Django é um framework web Python de alto nível que permite o rápido desenvolvimento de sites seguros e de fácil manutenção. Com isto dito, o Django REST Framework ou DRF é uma biblioteca que permite a construção de APIs REST utilizando a estrutura do Django. O foco aqui é o desenvolvimento de [web API's](https://pt.wikipedia.org/wiki/Interface_de_programa%C3%A7%C3%A3o_de_aplica%C3%A7%C3%B5es) de forma simples e ágil. Segundo [a documentação oficial](https://www.django-rest-framework.org/#:~:text=Django%20REST%20framework%20is%20a,toolkit%20for%20building%20Web%20APIs.&text=The%20Web%20browsable%20API%20is,and%20non%2DORM%20data%20sources.), o Django Rest gera uma API navegável que auxilia na usabilidade para os desenvolvedores. Além disso, possui um sistema de autenticação e [serialização](https://cursos.alura.com.br/forum/topico-serializacao-e-desserializacao-110845) dos dados.

Utilizamos essa biblioteca para o desenvolvimento, pois ela é gratuita e de código aberto, tem uma comunidade próspera e ativa, ótima documentação e muitas opções de suporte gratuito e pago. Além de ser completa, versátil e segura.
### 2.1.2. MySQL
O MySQL é um sistema gerenciador de banco de dados relacional de código aberto usado na maioria das aplicações gratuitas para gerir suas bases de dados. Possui flexibilidade, facilidade de uso e alto desempenho.

Visto que o projeto é de código aberto utilizamos o MySQL como gerenciador dos bancos de dados do sistema.
>>>>>>> rascunhos


### 2.2. Aplicativo mobile
Responsável pela visualização de dados e interação com o usuário.

<<<<<<< HEAD
### 2.2.1. [React Native](https://reactnative.dev/)
TODO: Escrever pra que serve o framework e por qual motivo o framework foi escolhido.

### 2.2.2. [Expo](https://expo.dev/)
TODO: Escrever pra que serve o framework e por qual motivo o framework foi escolhido.
=======
### 2.2.1. React Native
Baseado no [React](https://pt-br.reactjs.org), framework JS para desenvolvimento web, o [React Native](https://reactnative.dev) possibilita a criação de aplicações móvel multiplataforma (Android e iOS) utilizando apenas Javascript. Porém, diferente de outros frameworks com esta mesma finalidade (Cordova, por exemplo), todo o código desenvolvido com o React Native é convertido para linguagem nativa do sistema operacional, o que torna o app muito mais fluido.

Levando em consideração que o núcleo do projeto é um aplicativo para smartphones o react native é ferramenta base para o projeto.
### 2.2.2. Expo
O [Expo](https://expo.dev) é uma ferramenta que facilita no desenvolvimento de aplicativos mobile com **React Native**, já que ele abstrai todas as partes complexas de configuração do ambiente e te permite acesso rápido e fácil a várias API’s nativas. Com ele é possível usar a API de câmera e notificações, por exemplo, sem muita dificuldade, já que não é necessário fazer nenhuma configuração de API.
>>>>>>> rascunhos

Utilizamos o expo para auxiliar o React Native no uso dos módulos dos smartphones.

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

![Diagrama Corrigido](/2022-1-TiControla-Docs/site/docs/assets/diagrama_corrigido.png)

### 4.2 Diagrama de pacotes
<img src="/docs/images/diagrama_corrigido.png" alt="Diagrama_2" style="height: 100px; width:100px;"/>

### 5.1 Banco de Dados

#### 5.1.1 Entidades

Entidades Confirmadas:

| Despesas | Usuários |
| --- | --- |
| R$ 10 | usuario_teste |

#### 5.1.2 Atributos

Lista de atributos principais das entidades necessárias para o projeto.

# Usuário (user e user_data, no código):

| Usuário       | Tipos  |
| --- | --- |
| ID            | int    |
| Nome          | string |
| Email         | string |
| Senha         | string |
| Saldo         | double |
| Limite Máximo | double |
| Limite Mínimo | double | 

# Cartão (cartao, no código):

| Despesa           | Tipos  |
| --- | --- |
| ID                | int    |
| Código            | string |
| Tipo              | string |
| Apelido do Cartão | string |
| Data              | double |
| Categoria         | double |
| Descrição         | double |
| Valor             | double |
| Parcelas          | string |

     

#### 5.1.2 Relacionamentos
#### 5.1.3 Diagrama Entidade-Relacionamento
![](/images/Diagrama%20-%20ER%20-%20TiControla%20-%20Diagrama%20ER%20de%20banco%20de%20dados%20(p%C3%A9%20de%20galinha).png)

## Referências

[https://developer.mozilla.org/pt-BR/docs/Learn/Server-side/Django/Introduction](https://developer.mozilla.org/pt-BR/docs/Learn/Server-side/Django/Introduction)

[https://www.treinaweb.com.br/blog/o-que-e-o-django-rest-framework?gclid=Cj0KCQjw94WZBhDtARIsAKxWG-80JjWyWQVb1KCv-4lr8wl0swBakAsPIv8WiMEPDZK--RuKNQwlFXAaAmyYEALw_wcB](https://www.treinaweb.com.br/blog/o-que-e-o-django-rest-framework?gclid=Cj0KCQjw94WZBhDtARIsAKxWG-80JjWyWQVb1KCv-4lr8wl0swBakAsPIv8WiMEPDZK--RuKNQwlFXAaAmyYEALw_wcB)

[https://www.alura.com.br/artigos/django-django-rest-diferencas#:~:text=Django Rest Framework,autenticação e serialização dos dados](https://www.alura.com.br/artigos/django-django-rest-diferencas#:~:text=Django%20Rest%20Framework,autentica%C3%A7%C3%A3o%20e%20serializa%C3%A7%C3%A3o%20dos%20dados).

[https://www.hostinger.com.br/tutoriais/o-que-e-mysql#Por_que_o_MySQL_e_tao_popular](https://www.hostinger.com.br/tutoriais/o-que-e-mysql#Por_que_o_MySQL_e_tao_popular)

[https://www.treinaweb.com.br/blog/o-que-e-o-react-native?gclid=Cj0KCQjw94WZBhDtARIsAKxWG--4M-KvsAlD9iyTjyEujB7-MXN4LhODiP1Gp9bbvA7C2nM1yGlCagkaAiBCEALw_wcB](https://www.treinaweb.com.br/blog/o-que-e-o-react-native?gclid=Cj0KCQjw94WZBhDtARIsAKxWG--4M-KvsAlD9iyTjyEujB7-MXN4LhODiP1Gp9bbvA7C2nM1yGlCagkaAiBCEALw_wcB)

[https://www.alura.com.br/artigos/como-fazer-a-migracao-do-expo-para-react-native-cli#:~:text=O Expo é uma ferramenta,fácil a várias API's nativas](https://www.alura.com.br/artigos/como-fazer-a-migracao-do-expo-para-react-native-cli#:~:text=O%20Expo%20%C3%A9%20uma%20ferramenta,f%C3%A1cil%20a%20v%C3%A1rias%20API%27s%20nativas).