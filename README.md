# AWS

#  RELATORIO DE IMPLEMENTAÇAO DE SERVIÇOS AWS

Data: 10/12/2025
Empresa: Abstergo Industries
Responsável: Thabata Lia 

#  Introdução 
Este relatorio apresenta o processo de implementaçao de ferramentas na empresa Abstergo Industries, realizado por Thabata Lia.
O objetivo do projeto foi elencar 3 servicos aws, com finalidade de realizar diminuição de custos imediato.

##  Descrição do porjeto
O projeto de implementação de ferramentas foi dividido em 3 etapas, cada uma com seus objetivos especiais 
seguir, serão descritas as etapas do projeto:

Etapa 1:
- Nome da Ferramenta: Amazon Aurora
- Foco da Ferramenta: Banco de dados gerenciado, escalável, com alta performance e disponibilidade.
- Descrição de Uso: Antes da implementação, a empresa utilizava um banco de dados MySQL on-premises (local) para gerenciar dados de vendas, 
clientes e inventário. Esse sistema apresentava:
Problemas de lentidão e quedas inesperadas;
Altos gastos com infraestrutura física (compra de hardware, energia e refrigeração);
Necessidade de backups manuais, que consumiam muito tempo e eram arriscados.
Com a migração para o Amazon Aurora, foi possível resolver esses problemas com os seguintes benefícios:
Backup automático, segurança da base de dados e alta disponibilidade.
Consultas processadas em milissegundos, acelerando os sistemas de vendas e aplicativos móveis quando consultam ou atualizam informações de clientes.
Escalabilidade automática, sem interrupção dos serviços, para aumentar a capacidade de acordo com a demanda.
Resultado Prático:
O banco de dados da empresa agora suporta até 10 vezes mais consultas simultâneas, sustentando o crescimento da base de dados sem exigir constantes upgrades. 
A manutenção foi reduzida em 40%, já que backups, atualizações e segurança são gerenciados automaticamente pela AWS.

Etapa 2:
- Nome da Ferramenta: Amazon S3
- Foco da Ferramenta: Armazenamento escalável, confiável e seguro para dados estruturados e não estruturados.
- Descrição de Uso: Anteriormente, a empresa utilizava servidores físicos para armazenar backups e arquivos internos, como:
Contratos legais, registros de funcionários, relatórios financeiros e logs;
Esses servidores ocupavam uma sala inteira, consumiam altos níveis de energia e tinham um custo elevado de manutenção.
Além disso, havia o risco significativo de perda de dados devido a falhas nos discos rígidos.
Com a implementação do Amazon S3:
Todos os arquivos e contratos foram migrou-se para o S3, ficando disponíveis para acesso interno por meio de integrações simples;
Dados mais antigos, como logs e contratos expirados, foram automaticamente arquivados no Amazon S3 Glacier,
resultando em menor custo para armazenamento de informações raramente acessadas.
Resultado Prático:
A empresa eliminou o investimento necessário em servidores físicos e reduziu os custos de energia e refrigeração.
A economia foi de cerca de 50% nos gastos com armazenamento anual, enquanto garantiu proteção contra perda de dados com backups automáticos.

Etapa 3:
- Nome da Ferramenta: AWS Lambda
- Foco da Ferramenta: Processamento de código sob demanda (serverless) para automação de tarefas pontuais e event-driven.
- Descrição de Uso: Antes, algumas tarefas simples (como automações de upload e notificações) exigiam servidores dedicados que ficavam a maior parte do tempo ociosos,
resultando em custos desnecessários. Por exemplo:
Um servidor processava uploads de arquivos enviados pelos clientes, mas só era utilizado poucas vezes por dia;
Outro servidor enviava notificações automáticas por e-mail ou SMS para clientes e equipes internas.
Com o AWS Lambda:
Quando um cliente envia um arquivo (como contratos assinados), o Lambda verifica se o documento está correto e processa o upload;
Outra função do Lambda envia notificações por e-mail sempre que um pedido urgente é registrado pelo time de vendas.
O código só executa quando necessário, eliminando custos de infraestrutura contínua.
Resultado Prático:
As tarefas ficaram mais rápidas, seguras e totalmente automatizadas. A empresa agora economiza cerca de 70% nos custos operacionais,
já que só paga pelo tempo real de execução das funções (em milissegundos), sem necessidade de um servidor dedicado.

##  Conclusão
A implementação das ferramentas Amazon Aurora, Amazon S3 e AWS Lambda trouxe resultados significativos para a empresa Abstergo Industries, 
atendendo ao principal objetivo do projeto: reduzir custos operacionais de forma imediata com impacto positivo nos processos internos.
O Amazon Aurora modernizou a gestão de banco de dados, oferecendo escalabilidade, alta performance e automação de tarefas antes realizadas manualmente. 
Resultou em uma redução de custos de manutenção em 40% junto a um aumento significativo na capacidade de consultas simultâneas.
O Amazon S3 transformou o armazenamento da empresa, eliminando despesas relacionadas à infraestrutura local e garantindo proteção total dos dados com backups automáticos 
e políticas de arquivamento. A empresa alcançou 50% de economia nos gastos anuais de armazenamento.
O AWS Lambda automatizou processos repetitivos e eliminou servidores ociosos, otimizando os recursos usados e reduzindo os custos com esses processos em 70%, 
ao mesmo tempo que aumentou a agilidade e a segurança das tarefas executadas.
Essas ferramentas resultaram em uma infraestrutura eficiente, escalável e econômica, melhorando a produtividade e alinhando as operações da empresa às melhores práticas tecnológicas.

Recomendação: Com base nos resultados obtidos, sugere-se a continuidade da utilização das ferramentas já implementadas e a realização de novas avaliações para identificar
outros serviços AWS que possam trazer ainda mais benefícios para a organização. A meta é garantir que a Abstergo Industries mantenha sua competitividade e continue evoluindo
no mercado por meio da inovação tecnológica.

##  Anexos
1. Manuais e Documentação Técnica
Amazon Aurora: https://docs.aws.amazon.com/pt_br/AmazonRDS/latest/AuroraUserGuide/aurora-ug.pdf
Amazon S3: [Instruções para criação de buckets, aplicação de políticas de ciclo de vida (ex.: arquivamento no S3 Glacier), e exemplo de integração com o sistema interno.](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html)
AWS Lambda: [Exemplos de funções Lambda implementadas, incluindo o código (em Python, Node.js ou outra linguagem utilizada).](https://docs.aws.amazon.com/lambda/latest/dg/welcome.html)


2. Diagramas de Arquitetura Antes e Depois
Antes da Implementação
Este cenário mostra como era a infraestrutura usada no projeto antes da implementação dos serviços AWS:

Servidor Local - Banco de Dados MySQL:
- Servidor físico armazenava registros de vendas, inventário e clientes.
- Backups dependiam de soluções internas e manutenção manual.

Armazenamento Local:
- Sala cheia de servidores contendo documentos da empresa, contratos e relatórios.
- Arquivos antigos ocupando espaço, sem arquivamento eficiente.

Servidores para Automação:
- Funcionavam 24/7 para tarefas simples (processar uploads e enviar notificações).
- Máquinas ficavam ociosas, mas geravam custos constantes.
Depois da Implementação
Após a transição para os serviços AWS, a arquitetura foi remodelada:

Amazon Aurora:
- Banco de dados escalável substituindo o MySQL local.
- Backups automáticos e alta performance sem esforço adicional.

Amazon S3:
- Toda a infraestrutura de armazenamento foi migrada para o S3.
- Configuração de ciclo de vida com arquivamento automático no S3 Glacier para arquivos antigos.

AWS Lambda:
- Automação de tarefas como notificações e processamento de uploads.
- Funções são executadas sob demanda, com custos baseados no tempo de execução.
(Essa descrição pode ser representada graficamente usando carreiras de blocos/fluxos visuais. Se tiver ferramentas como Lucidchart ou Draw.io, você pode criar imagens para demonstrar os dois modelos.)

3. Cronograma do Projeto de Implementação
Etapa	Atividade	Tempo Necessário
1. Planejamento	Levantamento de dados sobre a infraestrutura atual (ex.: tamanho do banco, dados armazenados, tarefas automatizadas).	1 semana
2. Migração para Amazon Aurora	Configuração inicial do Aurora e migração do banco (testes antes do corte total do MySQL local).	2 semanas
3. Transferência para Amazon S3	Configuração de buckets S3 e S3 Glacier. Transferência dos arquivos locais para os buckets.	1 semana
4. Configuração do AWS Lambda	Criação e deploy das funções automáticas, como processamento de uploads e envio de notificações.	1 semana
Total do Projeto	---	5 semanas

4. Resumo das Etapas de Implementação
1. Migração do Banco de Dados para o Amazon Aurora
Atividade: Migração do banco de dados MySQL local para o Amazon Aurora. Foi realizada a configuração do banco na AWS, criação de réplicas para failover automático e testes. Após a validação, o corte final para o Aurora foi realizado.
Tempo: 2 semanas

2. Transferência de Dados para o Amazon S3
Atividade: Todos os arquivos valiosos da Abstergo Industries (contratos, logs, relatórios financeiros) foram transferidos para buckets S3. Políticas de arquivamento foram configuradas para mover arquivos com pouca frequência de acesso para o S3 Glacier. Isso garantiu um armazenamento mais eficiente e econômico.
Tempo: 1 semana

3. Desenvolvimento e Deploy de Funções AWS Lambda
Atividade: As funções que antes rodavam 24/7 em servidores dedicados (ex.: processamento de uploads e envio de notificações) foram replicadas usando AWS Lambda. Isso permitiu a execução do código sob demanda, eliminando custos com servidores desnecessários.
Tempo: 1 semana


Assinatura do Responsável pelo Projeto:
Thabata Lia 
