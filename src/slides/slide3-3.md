### 📐 Schéma de l'Architecture Hexagonale

```
┌─────────────────────┐                                 ┌─────────────────────┐
│  PRIMARY ADAPTERS   │                                 │ SECONDARY ADAPTERS  │
│    (Driving)        │                                 │     (Driven)        │
├─────────────────────┤                                 ├─────────────────────┤
│  • REST Controller  │                                 │  • PostgreSQL       │
│  • GraphQL API      │                                 │  • MongoDB          │
│  • CLI              │                                 │  • HTTP Client      │
│  • Tests            │                                 │  • SMTP Service     │
└──────────┬──────────┘                                 └──────────▲──────────┘
           │                                                       │
           │ implémentent                           implémentent   │
           │                                                       │
           ▼                                                       │
┌──────────────────────────────────────────────────────────────────────────────┐
│                           DOMAINE (HEXAGONE)                                 │
│                                                                              │
│  ┌─────────────────┐                                 ┌──────────────────┐    │
│  │ PRIMARY PORTS   │                                 │ SECONDARY PORTS  │    │
│  │  (Entrants)     │       ┌─────────────┐           │   (Sortants)     │    │
│  ├─────────────────┤       │   MÉTIER    │           ├──────────────────┤    │
│  │ • Use Cases     │─────▶ │             │─────────▶ │ • Repositories   │    │
│  │ • Services      │       │  Entités    │           │ • Gateways       │    │
│  │ (Interfaces)    │       │  Règles     │           │ • Services       │    │
│  │                 │       │  Logique    │           │ (Interfaces)     │    │
│  └─────────────────┘       └─────────────┘           └──────────────────┘    │
│           ▲                                                     │            │
└───────────┼─────────────────────────────────────────────────────┼────────────┘
            │                                                     │
            │ appellent                          sont appelés par │
            │                                            le domaine
            │                                                     ▼
┌───────────┴──────────┐                                 ┌─────────────────────┐
│  User / External     │                                 │  Infrastructure     │
│  System              │                                 │  Externe            │
└──────────────────────┘                                 └─────────────────────┘

      CÔTÉ GAUCHE (PRIMARY)                           CÔTÉ DROIT (SECONDARY)
   L'application est pilotée                      L'application pilote l'infra
```

**🎯 Les PORTS sont dans le DOMAINE - Les ADAPTATEURS implémentent les PORTS**

