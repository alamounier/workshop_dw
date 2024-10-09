## ELT Workflow

Este projeto segue um fluxo ELT (Extract, Load, Transform) para buscar dados de commodities, armazenar no PostgreSQL e transformá-los para análises futuras.

```mermaid
graph TD
    A[Início] --> B[Extrair dados de commodities]
    B --> C{Iterar sobre cada símbolo de commodity}
    C -->|Sim| D[Buscar dados históricos de preços]
    D --> E[Carregar dados no DataFrame consolidado]
    E --> F[Carregar no PostgreSQL]
    F --> G[Transformar dados para análises futuras]
    G --> H[Fim]