# Especificações do Projeto

## Definição do problema

Foi identificado em reunião presencial, que o projeto Contagem Ativa hoje conta com aproximadamente 70 núcleos de promoção do bem-estar através da atividade física, muitos professores de diferentes modalidades e muitos alunos de diversas faixas etárias. E identificou-se que o cadastro das informações pessoais dessas várias pessoas que participam do projeto não é informatizado, sendo este realizado através do preenchimento manual, via papel e caneta, de uma ficha apresentada ao aluno. Os professores precisam guardar as fichas físicas aos montes e consultá-las em um processo de busca pouco prático, não funcional caso precisem resgatar alguma informação médica de algum aluno em caso de emergência.  

Portanto, traçou-se como o objetivo principal e mais crítico do desenvolvimento da aplicação, a solução para o armazenamento e busca das fichas dos alunos. Porém, tem-se como objetivos secundários, disponibilizar aos alunos a lista de locais para realização das atividades físicas, integrações com API’s de geração de mapas e de informações sobre o tempo e levantamento de métricas sobre quantidade de alunos em cada ponto, problemas de saúde reportados entre outras. 

Neste documento serão abordados os artefatos desenvolvidos na etapa de projeto da solução do problema apresentado. Tais como: requisitos do software e diagrama de casos de uso.

## Arquitetura e Tecnologias

Para solução do problema apresentado, a arquitetura proposta foi a arquitetura cliente-servidor, muito indicada para soluções web. O diagrama de implantação combinado com o diagrama de componentes que descrevem a arquitetura utilizada encontram-se a seguir:
![Diagrama de implantação combinado com o diagrama de componentes UML](img/Diagrama_de_implantação_Componentes.png)
Como tecnologias utilizadas nesta arquitetura, podemos citar:
* Serviço de provisão de nuvem da Microsoft: Microsoft Azure. Utilizado na hospedagem do servidor do banco de dados e do servidor da aplicação back-end
* Serviço de hospedagem gratuita de páginas web do Github: Github Pages. Utilizado para hospedar a aplicação web
* C# com Entity Framework para desenvolvimento da aplicação back-end e API
* React e Tailwind CSS para desenvolvimento da aplicação front-end
* Microsoft SQL Server como serviço de banco de dados

## Requisitos

As tabelas que se seguem apresentam os requisitos funcionais e não funcionais que detalham o escopo do projeto.

### Requisitos Funcionais

| Descrição do Requisito | 
|-----------------------------------------|
|RF01 O sistema deverá ter um menu de cadastro de alunos que deverá permitir a consulta de um aluno, pelo nome/sobrenome ou CPF. |
|RF02 O sistema deverá ter uma opção de ordenação da lista de alunos e professores tanto em ordem crescente quanto em ordem decrescente (para que fique a escolha do usuário a forma de ordenação que preferir); |
|RF03 O sistema deverá ter a opção de acessibilidade (visual, auditiva, etc.) para que possa atender ser acessível a todos os alunos |
|RF04 O sistema deve na tela inicial ter uma espécie de “Cards de Acesso rápido”, nos quais deverão ter as opções “Cadastro de Alunos”, “Cadastro de Professores” e outras que julgarem importantes para manter nesse menu. |
|RF05 O sistema deverá ter um menu de cadastro de professores que deverá permitir a consulta de um professor, pelo nome/sobrenome e as. |
|RF06 O sistema deverá ter uma opção de ordenação da lista tanto em ordem crescente quanto em ordem decrescente nos menus de Cadastro de Alunos e Cadastro de Professores (para que fique a escolha do usuário a forma de ordenação que preferir); |
|RF07 O sistema deverá ter um campo para colocar o cargo da pessoa (professor, instrutor ou estagiário) |
|RF08 O sistema deverá, no menu de cadastros de alunos, ter um campo para que o aluno informe quais medicações está tomando. Esse campo deverá ficar visível na listagem de cadastros (sem precisar entrar dentro do cadastro do aluno, pode ser identificado talvez com uma pílula, ou com uma agulha no caso de medicamentos injetáveis) |
|RF09 O sistema deverá, no menu de cadastros de alunos, ter um campo para que o aluno informe pelo menos dois contatos de emergência. |
|RF10 O sistema deverá ter um botão no início e no cadastro de alunos com a nomenclatura “Enviar cadastro de ficha” |
|RF11 No menu de cadastro de professores, deve ter um campo onde ele poderá se vincular a modalidades que ele tem mais experiencia (uma vez que se o professor tiver CREF ele pode dar aula em qualquer modalidade consideraremos que ele poderá escolher as que ele tem mais experiencia ou se sinta melhor lecionando) |
|RF12 O sistema deverá ter um campo para filtrar os professores através das regionais e modalidades em que eles estão vinculados. |
|RF13 O sistema deverá ter uma opção de filtro de professores a partir das modalidades. Ex: Modalidade Natação, tem esses professores que tem experiencia. |
|RF14 O sistema deverá, ter um menu “Gráficos” e nele, deverá ter um relatório “Idade média por regional” onde nesse gráfico o coordenador conseguirá ver a média da idade dos alunos. |
|RF15 Adicionar um gráfico no modelo pizza para essa análise e quando ele for passando o mouse no gráfico, informar qual porcentagem corresponde aquela faixa etária e sua respectiva quantidade; |
|RF016 O sistema deverá, ter um menu “Gráficos” e nele, deverá ter um relatório “Idade média dos Alunos” onde nesse gráfico o coordenador conseguirá ver a média da idade dos alunos inscritos no programa Contagem Ativa. |
|RF17 Na tela inicial do sistema, deverá estar exposto três guias, “Regional” “Polo” e “Modalidade”, na medida que o aluno selecionar uma Regional, por exemplo, fazer um filtro que mostre os polos daquela regional, depois que ele selecionar o polo, mostrar as modalidades disponíveis e horários; caso ele selecione somente a modalidade, fazer o processo inverso, onde, ele informa a modalidade e são mostradas as informações de polo e regional que contemplam aquela modalidade. |
|RF18 O sistema deverá ter uma funcionalidade de Pesquisa de satisfação; |
|RF19 O sistema deverá ter um local para que os alunos possam colocar Sugestões, solicitações, etc.; |

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
