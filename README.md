﻿# Architecture Hexagonale - Support de Formation
Support de formation sur l'architecture hexagonale créé avec Reveal.js et TypeScript.

## ⚠️ IMPORTANT : Clarification Ports vs Adapters

**Question fréquente** : "À quoi correspondent mon port primaire et mon port secondaire ?"

**Réponse rapide** : Ils n'existent pas ! 👉 **[Lire la réponse complète](./REPONSE_DIRECTE.md)**

### 📚 Documentation Complémentaire

Pour comprendre la distinction entre Ports et Adapters :

- 🎯 **[CHEAT_SHEET.md](./CHEAT_SHEET.md)** - Aide-mémoire rapide (commencez ici !)
- 📖 **[REPONSE_DIRECTE.md](./REPONSE_DIRECTE.md)** - Réponse détaillée avec exemples
- 🔍 **[PORT_VS_ADAPTER.md](./PORT_VS_ADAPTER.md)** - Comparaison approfondie
- 📚 **[README_PORTS_ADAPTERS.md](./README_PORTS_ADAPTERS.md)** - Index complet
- 🧠 **[ARCHITECTURE_EXPLICATION.md](./ARCHITECTURE_EXPLICATION.md)** - Architecture du projet Curtailment

### 🖼️ Schémas Visuels

- **[port-vs-adapter.svg](./public/images/port-vs-adapter.svg)** - Distinction Port/Adapter
- **[hexagonal-architecture.svg](./public/images/hexagonal-architecture.svg)** - Architecture complète (corrigée)
## 🚀 Démarrage rapide
### Installation
```bash
npm install
```
### Lancement en mode développement
```bash
npm run dev
```
### Build pour la production
```bash
npm run build
```
## 📊 Structure de la présentation
### 1. **Introduction** (Slide 1)
Titre et présentation générale de la formation
### 2. **Le Problème** (Slide 2)
- Architecture traditionnelle en couches
- Problèmes de couplage fort
- Difficultés de test et d'évolution
### 3. **Qu'est-ce que l'Architecture Hexagonale ?** (Slide 3 + sous-slides)
- Définition et origine (Alistair Cockburn, 2005)
- **Sous-slide 3.1** : Principe fondamental
- **Sous-slide 3.2** : Pourquoi "hexagonale" ?
- **Sous-slide 3.3** : 📐 Schéma détaillé de l'architecture avec Primary/Secondary
### 4. **Les 3 Couches Principales** (Slide 4 + sous-slides)
- Introduction aux 3 couches
- **Sous-slide 4.1** : 1️⃣ Le Domaine (Domain) - Entités, règles métier
- **Sous-slide 4.2** : 2️⃣ Les Ports - Interfaces et contrats
- **Sous-slide 4.3** : 3️⃣ Les Adaptateurs - Implémentations concrètes
### 5. **Ports & Adaptateurs : Détails** (Slide 5 + sous-slides)
- Introduction aux ports
- **Sous-slide 5.1** : Ports entrants (Driving/Primary) avec exemple TypeScript
- **Sous-slide 5.2** : Ports sortants (Driven/Secondary) avec exemple TypeScript
- **Sous-slide 5.3** : Adaptateurs côté gauche (Driving/Primary)
- **Sous-slide 5.4** : Adaptateurs côté droit (Driven/Secondary)
### 6. **Structure de Projet** (Slide 6)
Organisation recommandée des fichiers et dossiers avec arborescence complète
### 7. **Exemple Concret** (Slide 7 + sous-slides)
- Cas d'usage : Création d'un utilisateur
- **Sous-slide 7.1** : 💡 Flux complet (Backend) - HTTP Request → Controller → UseCase → Repository → PostgreSQL
- **Sous-slide 7.2** : 💡 Flux complet (Front-end) - Événement UI → Composant → UseCase → Repository → API HTTP
### 8. **Avantages & Inconvénients** (Slide 8 + sous-slides)
- Titre principal ⚖️
- **Sous-slide 8.1** : ✅ Avantages (Testabilité, Flexibilité, Gestion des dépendances, Maintenabilité, etc.)
- **Sous-slide 8.2** : ⚠️ Inconvénients et Défis (Complexité initiale, Courbe d'apprentissage, etc.)
- **Sous-slide 8.3** : 🎯 Au-delà de la complexité métier - Structure, dépendances contrôlées, évolution
### 9. **Points Clés à Retenir** (Slide 9)
Résumé des 6 concepts clés et ressources pour aller plus loin
---
**Total : 9 slides principales avec de nombreuses sous-slides verticales**
## 📁 Structure du projet
```
archi-hexa-introduction/
├── src/
│   ├── Slides/           # Fichiers Markdown des slides
│   │   ├── slide1.md     # Titre
│   │   ├── slide2.md     # Le problème
│   │   ├── slide3.md     # Définition
│   │   ├── slide3-1.md   # └─ Principe fondamental
│   │   ├── slide3-2.md   # └─ Pourquoi hexagonale
│   │   ├── slide3-3.md   # └─ Schéma architecture
│   │   ├── slide4.md     # Les 3 couches
│   │   ├── slide4-1.md   # └─ Le Domaine
│   │   ├── slide4-2.md   # └─ Les Ports
│   │   ├── slide4-3.md   # └─ Les Adaptateurs
│   │   ├── slide5.md     # Ports & Adaptateurs
│   │   ├── slide5-1.md   # └─ Ports entrants
│   │   ├── slide5-2.md   # └─ Ports sortants
│   │   ├── slide5-3.md   # └─ Adaptateurs Primary
│   │   ├── slide5-4.md   # └─ Adaptateurs Secondary
│   │   ├── slide6.md     # Structure de projet
│   │   ├── slide7.md     # Exemple concret
│   │   ├── slide7-1.md   # └─ Flux Backend
│   │   ├── slide7-2.md   # └─ Flux Front-end
│   │   ├── slide8.md     # Avantages & Inconvénients
│   │   ├── slide8-1.md   # └─ Avantages
│   │   ├── slide8-2.md   # └─ Inconvénients
│   │   ├── slide8-3.md   # └─ Au-delà complexité métier
│   │   └── slide9.md     # Conclusion
│   ├── main.ts           # Configuration Reveal.js
│   └── style.css
├── index.html            # Point d'entrée
├── package.json
└── README.md
```
## 🎮 Navigation
- **← →** : Navigation horizontale entre les slides principales
- **↑ ↓** : Navigation verticale dans les sous-slides
- **Esc** : Vue d'ensemble de toutes les slides
- **S** : Mode présentateur avec notes
- **F** : Plein écran
## 🎯 Points Forts de cette Présentation
- ✅ **Schéma visuel** de l'architecture avec Primary/Secondary
- ✅ **Exemples de code TypeScript** pour les ports et adaptateurs
- ✅ **Flux complets** Backend ET Front-end
- ✅ **Équilibre** entre avantages et inconvénients
- ✅ **Structure de projet** concrète et applicable
- ✅ **Navigation verticale** pour approfondir chaque concept
## 🛠️ Technologies utilisées
- **Reveal.js** : Framework de présentation
- **TypeScript** : Langage de programmation
- **Vite** : Build tool et dev server
- **Markdown** : Format des slides
## 📚 Ressources
- [Hexagonal Architecture - Alistair Cockburn](https://alistair.cockburn.us/hexagonal-architecture/)
- [Clean Architecture - Robert C. Martin](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html)
- [Domain-Driven Design (DDD)](https://martinfowler.com/tags/domain%20driven%20design.html)
## 📝 Personnalisation
Les slides sont au format Markdown dans le dossier `src/Slides/`. Vous pouvez :
- Modifier le contenu de chaque slide individuellement
- Ajouter de nouvelles slides en créant de nouveaux fichiers `.md`
- Changer le thème dans `src/main.ts` (moon, black, white, league, etc.)
- Personnaliser les styles dans `src/style.css`
## 💡 Concepts Clés Abordés
1. **Isolation du domaine** - Le métier au centre, protégé
2. **Inversion de dépendances** - Les dépendances pointent vers le domaine
3. **Ports & Adaptateurs** - Contrats définis par le domaine
4. **Primary vs Secondary** - Distinction claire entre pilotage et infrastructure
5. **Testabilité** - Mock facile des ports pour les tests
6. **Flexibilité** - Changement d'infrastructure sans impact sur le métier
## 📄 Licence
Projet éducatif - Libre d'utilisation pour la formation
