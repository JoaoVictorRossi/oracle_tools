# ODI Studio - Interface de Desenvolvimento
Ferramenta gráfica pra desenvolvimento de pipelines ETL/ELT da Oracle.
## Composição da Ferramenta
A ferramenta é composto por 4 principais módulos/navegadores.
- Topologia (Utilizado para visualizar e manipular a topologia do banco de dados e infraestrutura).
- Segurança (Oferece recurso de controle de segurança, como usuários e permissões).
- Designer (Local para desenvolver os mapeamentos das pipelines).
- Operador (Monitoramento das pipelines e armazenamento de Logs).
![Composição ODI Studio](../Imgs/composicao-odi-studio.png)
## Arquitetura ODI

A ferramenta contém uma arquitetura de repositórios **vinculados entre si**, responsável por armazenar os **metadados** das operações, configurações de ambiente, fontes de dados entre outras necessidades da ferramenta.
- **Master**, contém informações de segurança, usuários, topologia e versões de objeto.
- **Work**, armazena objetos de desenvolvimento, como mapeamentos, pacotes, entre outros, possuindo dois tipos:
    - Development Work Repository: usado para o desenvolvimento e design dos fluxos de dados.
    - Execution Work Repository: Exclusivo para a execução de cargas.
   
---
**[Voltar](../orcl_data_integrator.md)**