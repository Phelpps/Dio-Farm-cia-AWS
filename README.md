RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS
Data: 11 de Março de 2026

Empresa: Abstergo Industries

Responsável: Kroo (Game Master & Cloud Developer)

1. Introdução
Este relatório apresenta o processo de implementação de ferramentas na Abstergo Industries. O objetivo principal do projeto foi elencar 3 serviços AWS estratégicos para realizar a diminuição de custos operacionais imediatos, migrando de uma infraestrutura tradicional para um modelo escalável e inteligente.

2. Descrição do Projeto
O projeto foi estruturado para otimizar o armazenamento, a consulta de dados e o processamento, eliminando gastos com servidores ociosos.

Etapa 1: Otimização de Armazenamento
Ferramenta: Amazon S3 (com Intelligent-Tiering)

Foco: Redução de custos de armazenamento de objetos.

Caso de Uso: Armazenamento de logs de transações e backups de sistemas legados. Ao utilizar a classe Intelligent-Tiering, o S3 move automaticamente arquivos não acessados para camadas mais baratas, reduzindo o custo mensal sem intervenção manual ou impacto na performance.

Etapa 2: Consultas de Dados Serverless
Ferramenta: Amazon Athena

Foco: Eliminação de servidores de banco de dados para análise de dados (BI).

Caso de Uso: Em vez de manter um cluster de banco de dados ligado 24/7 para gerar relatórios mensais, utilizamos o Athena para rodar consultas SQL diretamente sobre os arquivos no S3. O custo passa a ser apenas por volume de dados varridos, gerando uma economia imediata ao desligar instâncias de bancos relacionais subutilizadas.

Etapa 3: Computação Eficiente e sob Demanda
Ferramenta: AWS Lambda

Foco: Execução de código sem gerenciamento de servidores.

Caso de Uso: Processamento de gatilhos (triggers) de limpeza de dados e automação de rotinas administrativas. Substituímos instâncias EC2 que rodavam scripts Python agendados por funções Lambda, que cobram apenas pelo tempo de execução (milissegundos), eliminando o custo de infraestrutura ociosa.

3. Conclusão
A implementação das ferramentas na Abstergo Industries tem como esperado a redução de até 40% nos custos mensais de infraestrutura, além de aumentar a escalabilidade dos processos. A transição para uma arquitetura Serverless e de armazenamento inteligente permite que a equipe foque no desenvolvimento de novas funcionalidades, deixando a gestão de hardware para a AWS.

Recomenda-se a continuidade do monitoramento via AWS Cost Explorer para identificar novas oportunidades de otimização.

4. Anexos
Arquitetura da Solução (Diagrama)

Script de Automação Boto3 para Ingestão de Dados

Planilha de Comparativo de Custos (On-Premise vs AWS)
