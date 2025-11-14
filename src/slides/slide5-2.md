#### Ports Sortants (Driven/Secondary)

**Ce dont l'application A BESOIN**

```typescript
// Port sortant : Repository
interface UserRepository {
  save(user: User): Promise<void>;
  findById(id: string): Promise<User | null>;
}

// Implémenté par l'infrastructure
class PostgresUserRepository implements UserRepository {
  async save(user: User): Promise<void> {
    // Appel à la base de données
  }
}
```

