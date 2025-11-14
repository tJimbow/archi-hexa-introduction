### 📦 Structure de Projet

```
src/
├── domain/
│   ├── entities/
│   │   └── User.ts
│   ├── usecases/
│   │   └── CreateUserUseCase.ts
│   └── ports/
│       ├── in/
│       │   └── CreateUserPort.ts
│       └── out/
│           └── UserRepositoryPort.ts
├── infrastructure/
│   ├── adapters/
│   │   ├── in/
│   │   │   └── UserController.ts
│   │   └── out/
│   │       └── PostgresUserRepository.ts
│   └── config/
└── main.ts
```

