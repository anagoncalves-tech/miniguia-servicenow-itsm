# Engenharia de Prompts e Cicatrizes

Este documento registra os prompts utilizados durante o estudo, os objetivos de cada prompt, as dificuldades encontradas e os ajustes realizados.

---

## Prompt 1

Explique de forma simples e estruturada o que é ITSM e como ele se relaciona com o ServiceNow.

### Retorno Prompt 1:

ITSM (IT Service Management ou Gestão de Serviços de TI) e o ServiceNow são conceitos que andam juntos, onde o primeiro representa a estratégia e o segundo a ferramenta que a torna operacional
. Abaixo, apresento uma explicação estruturada sobre essa relação.

1. O que é ITSM?
De forma simples, ITSM é como as equipes de TI gerenciam a entrega completa de serviços aos usuários, garantindo que a tecnologia apoie os objetivos do negócio
- Foco no Serviço: Diferente do suporte técnico tradicional (focado apenas em consertar hardware), o ITSM trata a TI como um serviço, focando nas necessidades do usuário final e no ciclo de vida completo desse serviço: desde o planejamento e design até a operação e melhoria contínua
- Processos Principais: O ITSM é composto por diversas "práticas" ou processos, como o gerenciamento de incidentes (restaurar falhas rápidas), problemas (investigar causas raízes), mudanças (minimizar riscos em atualizações) e solicitações (pedidos de novos softwares ou equipamentos)
- Framework de Referência: A maioria das organizações utiliza o ITIL 4 como guia de boas práticas para implementar o ITSM

2. O que é o ServiceNow?
O ServiceNow é uma plataforma baseada em nuvem projetada para automatizar fluxos de trabalho e consolidar ferramentas de TI em um único lugar. Ele é considerado o líder de mercado para soluções de gestão de serviços.

3. Como o ITSM se relaciona com o ServiceNow?
A relação é de teoria versus prática: enquanto o ITSM (e o ITIL) fornece os conceitos e diretrizes, o ServiceNow fornece o "motor de execução" que transforma essa teoria em fluxos de trabalho digitais reais.
- Concepção Baseada em Padrões: O ServiceNow foi construído nativamente em torno das orientações do ITIL. Isso significa que, ao abrir a plataforma, você já encontra módulos prontos para gerenciar incidentes, problemas e mudanças com campos e estados que seguem os padrões mundiais de TI
- Orquestração de Dados (CMDB): No coração dessa relação está o CMDB (Banco de Dados de Gestão de Configuração) do ServiceNow. Ele centraliza as informações de todos os componentes de TI (servidores, softwares, serviços) e seus relacionamentos, permitindo que os processos de ITSM sejam inteligentes e saibam exatamente o que será impactado por uma falha ou mudança
- Automação e Inteligência: O ServiceNow eleva o ITSM para além de simples chamados. Ele utiliza Inteligência Artificial (como o Now Assist) para resumir incidentes, sugerir resoluções e automatizar tarefas repetitivas, o que aumenta drasticamente a produtividade das equipes

4. Vantagens da União ITSM + ServiceNow
Quando uma empresa utiliza o ServiceNow para fazer sua gestão de ITSM, ela obtém:
- Visibilidade Única: Todos os processos de TI rodam em uma única base de dados, acabando com os silos de informação
- Agilidade e Resiliência: Detecção proativa de erros (antes mesmo do usuário reclamar) e restauração mais rápida de serviços
- Melhoria Contínua: Dashboards em tempo real (como o Performance Analytics) que mostram onde o serviço está falhando e onde pode ser otimizado

Em resumo, o ITSM é a estratégia de gestão, e o ServiceNow é a plataforma tecnológica que permite executar essa estratégia de forma automatizada, escalável e inteligente

--------------------------------------------------------------------------------

## Prompt 2

Crie um resumo sobre o processo de Incident Management no ServiceNow, incluindo registro, categorização, priorização, atribuição, resolução e encerramento.

### Retorno Prompt 2:

O gerenciamento de incidentes no ServiceNow é projetado para restaurar a normalidade do serviço o mais rápido possível, minimizando o impacto negativo nas operações de negócio. O processo segue um fluxo estruturado baseado nas melhores práticas da ITIL 4.

Abaixo está o resumo das etapas principais:

1. Registro (Identification and Logging)
Um incidente começa quando uma interrupção ou redução na qualidade do serviço é detectada. O registro pode ser feito de forma omnichannel, incluindo o Portal de Autoatendimento (Service Portal), e-mail, telefone, chat ou automaticamente através de ferramentas de monitoramento e AIOps. No registro, são capturadas informações fundamentais como o usuário afetado (Caller) e uma descrição do problema.

2. Categorização (Categorization)
Os incidentes são categorizados e subcategorizados com base na área de TI ou do negócio que sofreu a interrupção. Uma boa prática é associar o incidente diretamente a um Serviço ou Item de Configuração (CI) no CMDB, em vez de usar apenas categorias genéricas. Isso permite que a plataforma identifique automaticamente quem é o dono do serviço e qual equipe técnica deve ser mobilizada.

3. Priorização (Prioritization)
A prioridade determina a ordem de atendimento e os prazos de resolução. No ServiceNow, ela é calculada automaticamente através de uma matriz de prioridade baseada em dois fatores:
- Impacto: A extensão do dano ao negócio ou número de usuários afetados.
- Urgência: Quão rápido o negócio precisa da restauração antes que o impacto seja sentido. 
A prioridade resultante (ex: P1 - Crítica a P5 - Planejamento) define as metas dos Acordos de Nível de Serviço (SLAs).

4. Atribuição (Routing and Assignment)
O incidente é encaminhado para um Grupo de Atribuição (Assignment Group) responsável pela área técnica. Com o alinhamento ao CSDM (Common Service Data Model), o ServiceNow pode herdar regras de atribuição diretamente do dono do serviço ou CI afetado, reduzindo o tempo de triagem manual. Uma vez no grupo, um técnico específico é designado como o dono do chamado (Assigned to).

5. Resolução (Resolution)
Ocorre quando o técnico aplica um contorno (workaround) ou uma solução definitiva para restaurar o serviço. Ao mover o incidente para o estado "Resolvido", o sistema geralmente exige o preenchimento obrigatório de códigos de resolução e notas técnicas para fins de auditoria e alimentação da base de conhecimento. Neste estágio, o cronômetro do SLA de resolução para de contar.

6. Encerramento (Closure)
O estado final é o encerramento, que ocorre após o usuário confirmar que o serviço foi restaurado e que está satisfeito com a solução. Muitos ambientes são configurados para o encerramento automático após um período de inatividade (ex: 7 dias) se o usuário não reabrir o chamado. O fechamento torna o registro um histórico imutável para análises de tendência e melhoria contínua.

Aumento de Eficiência com IA: O ServiceNow utiliza o Predictive Intelligence para automatizar a categorização e o roteamento, além do Now Assist (IA Generativa) para resumir históricos de chamados e sugerir notas de resolução, acelerando todo o ciclo de vida

--------------------------------------------------------------------------------

## Prompt 3

Crie um resumo sobre o processo de Incident Management no ServiceNow, incluindo registro, categorização, priorização, atribuição, resolução e encerramento.

## Retorno Prompt 3:

--------------------------------------------------------------------------------

## Prompt 4

Crie um resumo sobre o processo de Incident Management no ServiceNow, incluindo registro, categorização, priorização, atribuição, resolução e encerramento.

### Retorno Prompt 4:

--------------------------------------------------------------------------------

## Prompt Reutilizáveis

### - Explique o conceito de [TEMA] de forma simples, estruturada e com exemplo prático aplicado ao ServiceNow.
### - Crie um resumo sobre [PROCESSO] no ServiceNow, incluindo objetivo, etapas, papéis envolvidos, boas práticas e riscos comuns.
### - Monte uma tabela comparando [CONCEITO 1] e [CONCEITO 2], destacando definição, uso prático e exemplo.

--------------------------------------------------------------------------------
