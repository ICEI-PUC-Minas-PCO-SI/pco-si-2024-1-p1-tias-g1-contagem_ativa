# Especificações do Projeto

## Definição do problema

Foi identificado em reunião presencial, que o projeto Contagem Ativa hoje conta com aproximadamente 70 núcleos de promoção do bem-estar através da atividade física, muitos professores de diferentes modalidades e muitos alunos de diversas faixas etárias. E identificou-se que o cadastro das informações pessoais dessas várias pessoas que participam do projeto não é informatizado, sendo este realizado através do preenchimento manual, via papel e caneta, de uma ficha apresentada ao aluno. Os professores precisam guardar as fichas físicas aos montes e consultá-las em um processo de busca pouco prático, não funcional caso precisem resgatar alguma informação médica de algum aluno em caso de emergência.  

Portanto, traçou-se como o objetivo principal e mais crítico do desenvolvimento da aplicação, a solução para o armazenamento e busca das fichas dos alunos. Porém, tem-se como objetivos secundários, disponibilizar aos alunos a lista de locais para realização das atividades físicas, integrações com API’s de geração de mapas e de informações sobre o tempo e levantamento de métricas sobre quantidade de alunos em cada ponto, problemas de saúde reportados entre outras. 

Neste documento serão abordados os artefatos desenvolvidos na etapa de projeto da solução do problema apresentado. Tais como: requisitos do software e diagrama de casos de uso.

## Arquitetura e Tecnologias

Descreva brevemente a arquitetura definida para o projeto e as tecnologias a serem utilizadas. Sugere-se a criação de um diagrama de componentes da solução.
Para solução do problema apresentado, a arquitetura proposta foi a arquitetura cliente-servidor, muito indicada para soluções web. O diagrama de implantação combinado com o diagrama de componentes que descrevem a arquitetura utilizada encontram-se a seguir:

## Requisitos

As tabelas que se seguem apresentam os requisitos funcionais e não funcionais que detalham o escopo do projeto.

### Requisitos Funcionais

| Descrição do Requisito | 
|-----------------------------------------|
| Permitir que o usuário cadastre tarefas |
| Emitir um relatório de tarefas no mês  |

### Requisitos não Funcionais

| Descrição do Requisito |
|-------------------------|
| O sistema deve ser responsivo para rodar em um dispositivos móvel |
| Deve processar requisições do usuário em no máximo 3s |

> **Links Úteis**:
> - [O que são Requisitos Funcionais e Requisitos Não Funcionais?](https://codificar.com.br/requisitos-funcionais-nao-funcionais/)
> - [O que são requisitos funcionais e requisitos não funcionais?](https://analisederequisitos.com.br/requisitos-funcionais-e-requisitos-nao-funcionais-o-que-sao/)

## Diagrama de Casos de Uso

O diagrama de casos de uso é o próximo passo após a elicitação de requisitos, que utiliza um modelo gráfico e uma tabela com as descrições sucintas dos casos de uso e dos atores. Ele contempla a fronteira do sistema e o detalhamento dos requisitos funcionais com a indicação dos atores, casos de uso e seus relacionamentos. 

As referências abaixo irão auxiliá-lo na geração do artefato “Diagrama de Casos de Uso”.

> **Links Úteis**:
> - [Criando Casos de Uso](https://www.ibm.com/docs/pt-br/elm/6.0?topic=requirements-creating-use-cases)
> - [Como Criar Diagrama de Caso de Uso: Tutorial Passo a Passo](https://gitmind.com/pt/fazer-diagrama-de-caso-uso.html/)
> - [Lucidchart](https://www.lucidchart.com/)
> - [Astah](https://astah.net/)
> - [Diagrams](https://app.diagrams.net/)

## Diagrama UML

Apresente os diagramas UML de maior importância do projeto (exceto os de caso de uso, que serão apresentados no tópico acima).

> **Links Úteis**:
> - [Diagrama UML](https://www.lucidchart.com/pages/pt/o-que-e-uml)

## Projeto da Base de Dados (se aplicável)

O projeto da base de dados corresponde à representação das entidades e relacionamentos identificadas no Modelo ER, no formato de tabelas, com colunas e chaves primárias/estrangeiras necessárias para representar corretamente as restrições de integridade.
