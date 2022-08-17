# TAP

# ✅ Termo de Abertura do Projeto

|Data      |Versão|Descrição     |Autor(es)               |
|----------|------|--------------|------------------------|
|13/08/2022|0.1   |Versão inicial|Mateus de Siqueira Silva|
|          |0.2   |              |                        |
|          |0.3   |              |                        |


## Sumário

1. [Introdução](#intro)
2. [Descrição do Projeto](#desc)
3. [Propósito e justificativa do projeto](#prop)
4. [Requisitos de alto nível](#requi)
5. [Riscos](#risco)
6. [Resumo do Custo estimado](#custo)
7. [Lista das partes interessadas](#stake)
8. [Requisitos para aprovação do Projeto](#requiaprov)
9. [Gerentes do Projeto](#gerente)
10. [Patrocinadores](#patro)

# <a id="intro"></a> 1 - Introdução

Esse documento visa entregar de forma sucinta as principais características do projeto TiControla dentre elas a visão inicial do projeto a forma de desenvolvimento bem como os envolvidos do projeto (stakeholders).

# <a id="desc"></a>2 - Descrição do projeto

Esse projeto foi proposto pelo grupo, mais especificamente pela integrante Lizandra Regis Malta a partir da solicitação da criação de um projeto para ser usado como instrumento de ensino visando o auxilio na aplicação dos conceitos ministrados  pela professora Carla Silva Rocha Aguiar em sala de aula como parâmetro de avaliação da disciplina de Métodos de Desenvolvimento de Software (MDS).

A proposta é um aplicativo de dispositivos móveis (mobile) uma ferramenta que visa um maior controle dos gastos financeiros. A plataforma funcionará como uma agenda de gastos para que os usuários possam relatar cada gasto que fez durante determinado período de tempo. Outro fator importante, é que partir desses dados, o aplicativo fará uma análise e dará avisos e recomendações para que o usuário consiga obter uma economia significativa no final do período.

# <a id="prop"></a>3 - Propósito e justificativa do projeto

O principal propósito da aplicação é que frequentemente nos encontramos com uma falta de controle financeiro. E isso pode nos levar a um acúmulo das dívidas e consequentemente um almento na cobrança de juros em cima destas dívidas. Em determinados casos, a situação pode se agravar e um "simples descontrole financeiro" pode se tornar no comumente conhecido pelo brasileiro como "Bola de neve". Com isso posto, fazendo um controle mais assíduo sob as finanças dos usuários a aplicação TiControla serve como uma ferramenta para evitar esse tipo de problema da socidade brasileira.

# 4 - <a id="requi"></a>Requisitos de alto nível

A plataforma será um aplicativo sendo possível o acesso a partir de smartphones, o acesso será de forma gratuita. Os requisitos de alto nível são:

|Nome      |Descrição|Teste         |
|----------|---------|--------------|
|-         |Configurar a integração do app  dentro das frameworks escolhidas para o projeto (Python Django).|              |
|Inserir dados dos pacientes|Realizar cadastro dos usuários e dados referentes aos gastos.|              |
|Banco de Dados|Permitir a comunicação entre a interface e a base de dados (PostgreSQL) para mostrar o histórico de gastos|              |
|Relatar e avisar|Relatar os gastos e avisar quais os gastos estão sendo mais relevantes|              |

# <a id="risco"></a>5 - Riscos

|Risco     |Ação Preventiva|Ação que será Realizada|
|----------|---------------|-----------------------|
|Falta de conhecimento com as tecnologias de desenvolvimento.|Escolher os alunos que estão dispostos a aprender as ferramentas necessárias.|Procurar cursos ou treinamento sobre tecnologias.|
|Conflitos de horários disponíveis para os integrantes.|Montar uma grade com os horários disponíveis de cada membro|Os pontos das sprints deve ser divido visando a carga horária compatível com o que os integrantes terão na semana, sendo maleável a mudanças(desde que o membro notifique o grupo no planejamento da sprint).|
|Falta de comunicação|Estabelecer ferramentas de comunição entre os membros, realizações de dailys e assuntos pontuais por whatsapp|Sempre deixar principais pontos das sprints em ambientes que os integrantes acessam constantemente.|
|Redefinições do escopo|A partir das dailys e reviews de sprints, a reavaliação de metas pontuais para o projeto.|Elaboração de sprint’s que permita evoluções de funcionalidades do produto.|
|A falta ou desistência de algum membro|Estimular a máxima participação dos membros da equipe.|Adequar os horários e realocar as tarefas entre os membros sem sobrecarregar nenhum membro.|
|Falta de conhecimento sobre DevOps, para configuração do ambiente|Compartilhar links de estudo para o mesmo.|Realizar cursos ou treinamento sobre o assunto.|


# <a id="custo"></a>6 - Resumo do Custo estimado

### Recursos Humanos

Os recursos humanos usados para a realização do projeto fazem referência aos 7 integrantes, sendo 2 deles encarregados do papel de Scrum Master, outro de Product Owner, e um dos Scrum Masters age também como DevOps e os demais como desenvolvedores. O papel de Arquitetura está sendo realizado em conjunto por todos os integrantes da equipe, porém um deles está com maior responsabilidade sobre esse aspecto. Baseando-se no período de dedicação semanal de cada integrante ao projeto, estimamos o custo mensal de cada aluno da Universidade de Brasília (UnB).

As estimativas se baseiam nos seguintes valores:

- 4 horas por dia;
- Durante 5 dias da semana;
- Dentro de 3 meses;

Consideramos que o mês tem 4 semanas, portanto:

**240 horas semanais;**

Consideramos também os dados do Distrito Federal

|Cargo     |Quantidade|Salário/mês (160h total)|Salário/hora|Total       |
|----------|----------|------------------------|------------|------------|
|Desenvolvedores|7         |R$ 3.455                |R21, 60     |R$ 36.228,00|
|Arquiteto |1         |R$ 6.000                |R$ 37,50    |R$ 9.000,00 |
|DevOps    |1         |R$ 7.000                |R$ 43,75    |R$ 10.500,00|
|Scrum Master|2         |R$ 7.666                |R$ 47,91    |R$ 11.498,00|
|Product Owner|1         |R$ 10.000               |R$ 62,50    |R$ 15.000,00|
|Total     |          |                        |            |R$ 82.226   |


### Custo de Equipamentos

|Equipamento|Quantidade|Finalidade    |Valor unitário|Preço       |
|-----------|----------|--------------|--------------|------------|
|Computadores|7 unidades|Desenvolvimento e planejamento|R$ 3.000      |R$ 21.000   |
|Smartphones ou Tablets|Não definido|Desenvolvimento e planejamento|R$ 1.000      |R$ 1.000*n  |
|Energia elétrica|240 horas |Desenvolvimento e planejamento|0,575 R$/KWh  |R$ 138,00   |
|Internet   |3 meses   |Desenvolvimento e planejamento|R$ 100,00[3]  |R$ 300,00   |
|Transporte |2 ou 3 por integrante |Desenvolvimento e planejamento|R$ 2,75       |R$ 3.465,00 |
|Alimentação|1 por dia para cada integrante|Desenvolvimento e planejamento|R$ 10,00      |R$ 4.200,00 |
|Total      |          |              |              |R$ 30.103   |


- Considerando “n” como a quantidade de aparelhos que forem usados e testados.
- Fonte: [http://www.aneel.gov.br/ranking-das-tarifas](https://antigo.aneel.gov.br/ranking-das-tarifas) (Distrito Federal)

### Custo de Ferramentas e Softwares

|Ferramenta|Finalidade|Preço Total   |
|----------|----------|--------------|
|Discord   |Editores de Texto (Visual Studio Code)|R$ 0          |
|Editores de Texto (Visual Studio Code)|Elaboração de documentos e código|R$ 0          |
|Git e GitHub|Versionamento de arquivos|R$ 0          |
|Linux e Android|Ambiente de desenvolvimento|R$ 0          |
|Linguagens de programação|Tecnologias utilizadas para desenvolvimento|R$ 0          |


### Custo Total

|Custo     |Valor Total|
|----------|-----------|
|Recursos Humanos|R$ 82.226  |
|Custo de Equipamentos|R$ 30.103  |
|Ferramentas e Softwares|R$ 0       |
|Total     |R$ 112.329,00|

# <a id="stake"></a>7 - Lista das partes interessadas

## Usuários

Pessoas consumistas que tem dificuldades de manter seus gastos sob controle, pessoas que querem ter uma maior controle de seus gastos, pessoas que querem economizar dinheiro por algum motivo dentre outros.

### Equipe de Desenvolvimento de Software

 A equipe de Desenvolvimento de Software é composta por alunos da disciplina Métodos de Desenvolvimento de Software, do curso Engenharia de Software, do campus do Gama da UnB.

Disciplina ministrada e orientada pela Prof. Carla S. R. Aguiar, do período 2020/2.

|Nome      |Github|Eamil                    |
|----------|------|-------------------------|
|Leonardo Michalski Miranda|http://github.com/leommiranda|leonardomichalskim@gmail.com|
|Milena Beatriz Aires de Santana Dias|https://github.com/MaltaLiz/|mbadsdias@gmail.com      |
|Rodrigo de Andrade Lima Orlandi|https://github.com/OrlandiRodrigo|digoalorlandi@gmail.com  |
|Lizandra Regis Malta|https://github.com/MaltaLiz|lizlrmalta@gmail.com     |
|Henrique Galdino Couto|https://github.com/hgaldino05|hgaldino05@gmail.com     |
|Mateus de Siqueira|https://github.com/mateus-de-siqueira/|mateusiqueira.s@gmail.com|
|Rodolfo Cabral Neves|https://github.com/roddas/|roddas360@gmail.com      |        |


# <a id="requiaprov"></a> 8 - Requisitos para aprovação do Projeto

Para a aprovação do Projeto será necessário a validação da Prof. Carla Silva Rocha Aguiar, que estará avaliando o projeto. O Projeto deverá estar funcionando de acordo com as metas propostas ao longo de sua realização e estarem alinhas com os tópicos de avaliação da professora.

# 9 - <a id="gerente"></a>Gerentes do Projeto

- Nome: Leonardo Michalski Miranda e Milena Beatriz Aires de Santana Dias .
- Responsabilidade: Gerenciar e garantir o desenvolvimento do projeto.
- Nível de autoridade: Alunos da disciplina Métodos de Desenvolvimento de Software, do curso Eng. de Software - UnB, FGA.

# 10 - <a id="patro"></a> Patrocinadores

- Nome: Carla Silva Rocha Aguiar.
- Nível de autoridade: Professora Doutora e Monitora. Avaliadores e orientadores do Projeto.

# <a id="ref"></a>Referências Bibliográficas

EASYBOK. Termo de abertura de projeto. Brasil: Easyhome, 2019. Disponível em: http://www.easybok.com.br/downloads/easyhome-tap/

CheeryUP. Sistema direcionado para psicólogos. Brasil: 2020.2-CheeryUP, 2022. Disponível em: https://fga-eps-mds.github.io/2020.2-CheeryUP/#/https://fga-eps-mds.github.io/2020.2-CheeryUP/#/