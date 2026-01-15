### 📦 Structure de Projet

```text
src/
├── domain/
│   ├── entities/
│   │   └── Program.ts
│   ├── usecases/
│   │   └── ProgramSearchService.ts
│   └── ports/
│       ├── primary/
│       │   └── ProgramSearchPort.ts (Primary Port)
│       └── secondary/
│           └── ProgramRepositoryPort.ts (Secondary Port)
├── infrastructure/
│   ├── primary/ (Primary Adapters)
│   │   └── components/
│   │       └── SearchProgram.vue
│   └── secondary/ (Secondary Adapters)
│       ├── ProgramRepositoryAdapter.ts
│       └── ProgramResponse.ts
└── main.ts (Bootstrap / Injection de dépendances)
```

<!--
NOTES POUR LE PRÉSENTATEUR :
- Le domaine contient les entités, use cases et ports
- Les ports sont organisés en domain/ports/primary/ et domain/ports/secondary/
- Les ports primaires (primary/) définissent ce que l'application expose (API)
- Les ports secondaires (secondary/) définissent ce dont l'application a besoin (SPI)
- L'infrastructure est séparée en primary (Primary Adapters) et secondary (Secondary Adapters)
- primary/ contient les adapters qui pilotent l'application (UI, composants Vue)
- secondary/ contient les adapters pilotés par l'application (APIs, BDD)
- Le fichier main.ts à la racine de /src contient le bootstrap (injection de dépendances)
- ProgramResponse est un DTO de l'infrastructure, jamais importé dans le domaine
-->

