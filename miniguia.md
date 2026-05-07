# Miniguia: ServiceNow ITSM e Gestão de Incidentes

## 1. O que é ITSM?

ITSM significa IT Service Management, ou Gerenciamento de Serviços de TI.

Ele representa um conjunto de práticas utilizadas para planejar, entregar, operar e melhorar serviços de tecnologia dentro de uma organização.

O objetivo do ITSM é garantir que os serviços de TI atendam às necessidades do negócio, com qualidade, controle e melhoria contínua.

## 2. O que é ServiceNow ITSM?

ServiceNow ITSM é uma solução da plataforma ServiceNow voltada para a gestão de serviços de TI.

Ela permite centralizar, automatizar e acompanhar processos como:

- Incidentes;
- Problemas;
- Mudanças;
- Requisições;
- Base de conhecimento;
- SLAs;
- Catálogo de serviços.

## 3. O que é Incident Management?

Incident Management, ou Gestão de Incidentes, é o processo responsável por restaurar a operação normal de um serviço o mais rápido possível.

Um incidente pode ser uma falha, interrupção ou degradação de um serviço.

Exemplos:

- Sistema indisponível;
- Erro ao acessar uma aplicação;
- Lentidão em um serviço;
- Falha de integração;
- Problema em equipamento ou rede.

## 4. Objetivo da Gestão de Incidentes

O principal objetivo da gestão de incidentes é reduzir o impacto negativo para o usuário e para o negócio.

Esse processo busca:

- Registrar corretamente os incidentes;
- Classificar e priorizar atendimentos;
- Direcionar para o grupo responsável;
- Resolver dentro do prazo acordado;
- Manter o usuário informado;
- Documentar a solução aplicada.

## 5. Ciclo de Vida de um Incidente no ServiceNow

### 5.1 Registro

O incidente é criado no ServiceNow por um usuário, analista, portal de atendimento, integração ou automação.

Boas práticas:

- Preencher descrição clara.
- Informar serviço afetado.
- Registrar usuário impactado.
- Anexar evidências quando possível.

### 5.2 Categorização

O incidente deve ser classificado por categoria e subcategoria.

Exemplo:

| Campo | Exemplo |
|---|---|
| Categoria | Software |
| Subcategoria | Acesso |
| Serviço afetado | Portal Corporativo |

### 5.3 Priorização

A prioridade geralmente é definida a partir da combinação entre impacto e urgência.

| Impacto | Urgência | Prioridade |
|---|---|---|
| Alto | Alta | Crítica |
| Alto | Média | Alta |
| Médio | Média | Moderada |
| Baixo | Baixa | Baixa |

### 5.4 Atribuição

Após o registro e classificação, o incidente é direcionado para um grupo responsável.

Exemplo:

- Service Desk;
- Suporte N2;
- Infraestrutura;
- Redes;
- Aplicações;
- Segurança.

### 5.5 Investigação e Diagnóstico

O grupo responsável analisa o incidente, verifica evidências, consulta histórico, pesquisa soluções conhecidas e identifica a causa provável.

### 5.6 Resolução

Após identificar a solução, o analista aplica a correção e registra as informações no chamado.

A resolução deve conter:

- O que foi feito;
- Qual foi a causa identificada;
- Como o serviço foi restaurado;
- Evidências, quando necessário.

### 5.7 Encerramento

O incidente é encerrado após a confirmação da resolução ou após o prazo definido pela política do processo.

Boas práticas:

- Validar com o usuário.
- Registrar solução clara.
- Relacionar artigo de conhecimento, se existir.
- Garantir que os campos obrigatórios estejam preenchidos.

## 6. Boas Práticas para Gestão de Incidentes

- Manter descrições claras e objetivas.
- Usar categorias padronizadas.
- Definir corretamente impacto e urgência.
- Atribuir o chamado ao grupo correto.
- Cumprir os SLAs definidos.
- Comunicar o usuário durante o atendimento.
- Utilizar base de conhecimento.
- Evitar encerramentos sem descrição de solução.
- Monitorar indicadores de atendimento.
- Revisar incidentes recorrentes para possível abertura de problema.

## 7. Indicadores Importantes

Alguns indicadores úteis para acompanhar a gestão de incidentes são:

| Indicador | Objetivo |
|---|---|
| Volume de incidentes | Medir quantidade de chamados abertos |
| Tempo médio de resolução | Avaliar eficiência do atendimento |
| Cumprimento de SLA | Verificar aderência aos prazos |
| Incidentes reabertos | Identificar falhas na resolução |
| Incidentes por categoria | Identificar áreas com maior demanda |
| Backlog | Acompanhar chamados pendentes |

## 8. Relação com Base de Conhecimento

A base de conhecimento ajuda a acelerar a resolução de incidentes.

Ela pode conter:

- Procedimentos conhecidos;
- Soluções para erros recorrentes;
- Orientações para usuários;
- Scripts de diagnóstico;
- Passos de troubleshooting.

## 9. Conclusão

O ServiceNow ITSM permite estruturar e automatizar processos de atendimento de TI, trazendo mais controle, rastreabilidade e eficiência.

A gestão de incidentes é uma das práticas mais importantes dentro do ITSM, pois atua diretamente na restauração dos serviços e na redução de impactos ao negócio.

Este miniguia consolida os principais conceitos, etapas e boas práticas para apoiar estudos, revisões e desenvolvimento profissional na área de ServiceNow.
