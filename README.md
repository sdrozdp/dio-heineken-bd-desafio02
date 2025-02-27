## Olá, meu nome é Simone D Palma!

### DESAFIO PROPOSTO

### Criar um modelo conceitual de Banco de Dados referente ao gerenciamento de execução de ordens de serviço em uma oficina mecânica.

## OBJETIVO

Cria o esquema conceitual para o contexto de oficina com base na narrativa fornecida.

## Narrativa

* Sistema de controle e gerenciamento de execução de ordens de serviço em uma oficina mecânica;
* Clientes levam veículos à oficina mecânica para serem consertados ou para passarem por revisões  periódicas;
* Cada veículo é designado a uma equipe de mecânicos que identifica os serviços a serem executados e preenche uma OS com data de entrega;
* A partir da OS, calcula-se o valor de cada serviço, consultando-se uma tabela de referência de mão-de-obra;
* O valor de cada peça também irá compor a OSO cliente autoriza a execução dos serviços;
* A mesma equipe avalia e executa os serviços;
* Os mecânicos possuem código, nome, endereço e especialidade;
* Cada OS possui: n°, data de emissão, um valor, status e uma data para conclusão dos trabalhos.

## ESTRATÉGIA UTILIZADA

#### ENTIDADES CRIADAS
    * Cliente: Representa a pessoa que possui o veículo sendo que o cliente pode ser uma pessoa física ou pessoa jurídica. Essa informação pode ser relevante, pois um cliente na pessoa jurídica pode atuar no ramo de aluguel de veículos e a oficina poderia oferecer descontos especiais a estes clientes. Um cliente pode possuir um ou mais veículos. Desta forma, o relacionamento entre Cliente e Veículo e de 1 para n.

    * Veículo: Representa o carro que será avaliado. Veículo está relacionado a Solicitação na cardinalidade 1:N (um veículo pode ter várias revisões ou consertos ao longo do tempo).

    * Equipe: Conjunto de mecânicos designados para avaliar e executar os serviços.

    * Mecânico: Profissionais pertencentes a uma equipe.

    * Solicitação: Registra a chegada do veículo, o problema e o desejo do cliente (realizar uma revisão ou conserto). A solicitação será atribuída a uma equipe que dará seguimento a avalição dos serviços necessários. A solicitação poderá assumir os seguintes estados: “pendente”, “em atendimento”, “concluída”, “cancelada”. 

    * Avaliação Mecânica: Após a atribuição da solicitação a uma equipe, o responsável pela equipe atribuirá aos mecânicos os serviços que deverão ser avaliados. A avaliação mecânica criada para cada mecânico assumirá o status inicial pendente. No momento, que o mecânico iniciar a avalição do veículo, o objeto assumirá o status “em andamento”. Após a avaliação da real necessidade do serviço, a inspeção do técnico poderá ser concluída (estado “concluída”). O mecânico informará a data de conclusão para realização do serviço. Esta entidade registra os serviços necessários identificado pelo mecânico após avaliação do veículo, a descrição do problema identificado e a necessidade do serviço sugerido.

    * Ordem de Serviço (OS): A OS será criada após a avaliação do veículo pela equipe mecânica. A OS será criada com todos os serviços e peças identificados como necessários no processo de avaliação pela equipe técnica. O cliente então deverá aprovar a OS com todos os serviços e peças, ou poderá excluir os itens (serviços e peças) que não entrarão na execução da OS. A OS poderá assumir os seguintes estados: Aguardando aprovação, aprovada, rejeitada, em execução, concluída. A data de conclusão da OS assumirá a data de conclusão do serviço mais demorado na avalição previamente realizada.

    * Serviços associados a OS: Representa todos os serviços que foram avaliados como necessários no processo de avalição do veículo pela equipe técnica. Estes serviços estão vinculados a OS. Cada serviço associado a OS deverá ser aprovado ou não pelo cliente para que possa ser executado em fase posterior.

    * Peças associadas a OS: Representa todas as peças que deverão ser substituídas e consideradas como necessárias pela equipe técnica. Estas peças estão vinculadas a OS. As peças da OS e suas respectivas quantidades deverão ser aprovadas ou não pelo cliente para que as substituições sejam possíveis em fase posterior. Neste modelo não foi contemplado a associação entre serviços e peças, mas poderiam ser considerado uma melhoria futura, visto que a não aprovação de alguma peça pode inviabilizar também a execução de algum serviço.

    * Execução da Ordem de Serviço: Representa a execução de cada serviço aprovado pelo cliente da ordem de serviço pelo mecânico que realizou a avaliação ou outro da mesma equipe técnica. Esta entidade será criada no momento da aprovação da OS e assumirá o estado inicial “pendente”. No momento que o mecânico iniciar o serviço, o objeto assumirá o estado “em andamento” e ao ser concluída assumirá o valor “concluído”.

    * Serviço: Tarefas a serem executadas (ex.: troca de óleo, alinhamento).

    * Peça: Componentes usados na execução dos serviços.

    * Plano Revisão: Representa um conjunto de serviços recomendados para um veículo com base em seu modelo, ano e quilometragem. Um plano de revisão pode ter vários itens de revisão (serviços recomendados).

    
#### PODEMOS NOS CONECTAR ATRAVÉS DO 
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/simone-drozd-palma-813b22280)[![Gmail](https://img.shields.io/badge/Gmail-333333?style=for-the-badge&logo=gmail&logoColor=red)](mailto:sdrozdp@gmail.com)

#### 📁 JÁ DESENVOLVI COM
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white)![PL](https://img.shields.io/badge/PL%2FSQL-FFFFFF?style=for-the-badge&logo=oracle&logoColor=FF0000&labelColor=FFFFFF&color=FF0000)![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

#### 📁 ESTOU ESTUDANDO
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)

#### 📁 FERRAMENTAS
![Git](https://img.shields.io/badge/GIT-E44C30?style=for-the-badge&logo=git&logoColor=white)

