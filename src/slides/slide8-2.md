#### Flux Complet (Front-end)

1. **Événement utilisateur** (clic, formulaire) dans le composant Vue
2. Le composant appelle le `CreateUserUseCase` (port entrant)
3. Le use case contient la **logique métier**
4. Le use case utilise `UserRepository` (port sortant)
5. L'implémentation `HttpUserRepository` (adaptateur sortant) appelle l'API backend
6. La réponse remonte à travers les couches vers le composant

**Le composant UI ne connaît ni l'API HTTP ni la logique métier !**

