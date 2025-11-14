#### Flux Complet

1. **HTTP Request** arrive au `UserController` (adaptateur entrant)
2. Le controller appelle le `CreateUserUseCase` (port entrant)
3. Le use case contient la **logique métier**
4. Le use case utilise `UserRepository` (port sortant)
5. L'implémentation `PostgresUserRepository` (adaptateur sortant) sauvegarde en BDD
6. La réponse remonte à travers les couches

**La logique métier ne connaît ni HTTP ni PostgreSQL !**

