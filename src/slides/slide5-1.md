#### Ports Entrants (Driving/Primary)

**Ce que l'application EXPOSE**

```typescript
// Port entrant : Use Case
interface CreateUserUseCase {
  execute(userData: UserData): Promise<User>;
}

// Implémenté par le domaine
class CreateUserService implements CreateUserUseCase {
  execute(userData: UserData): Promise<User> {
    // Logique métier
  }
}
```

