# 📜 Slide 3 : Histoire de l'Architecture Hexagonale

## Origine : Alistair Cockburn (2005)

### Le nom original : "Ports & Adapters"

En **2005**, **Alistair Cockburn** publie un article décrivant un pattern architectural qu'il nomme **"Ports and Adapters"**.

**Objectif initial** :
> "Permettre à une application d'être pilotée de manière égale par des utilisateurs, des programmes, des tests automatisés ou des scripts batch, et d'être développée et testée de manière isolée de ses bases de données et autres services externes."

### Pourquoi "Hexagonale" ?

Le terme **"Architecture Hexagonale"** est un **surnom** donné par la communauté par la suite.

**Raisons du surnom** :
- 🔷 La forme **hexagonale** dans les diagrammes est **symbolique**
- 🔷 Elle permet de représenter **plusieurs côtés** (pas limité à 6 !)
- 🔷 Chaque côté peut avoir **un ou plusieurs ports**
- 🔷 Plus visuel et mémorable que "Ports & Adapters"

> ⚠️ **Important** : "Hexagonale" n'est qu'une métaphore visuelle. Le nombre de côtés n'a aucune importance !

## Les deux noms sont corrects

Aujourd'hui, les deux termes sont utilisés de manière interchangeable :
- ✅ **Ports & Adapters** (nom original, plus descriptif)
- ✅ **Architecture Hexagonale** (surnom populaire, plus visuel)

## Évolution et adoption

Depuis 2005, ce pattern a été :
- 📚 Documenté dans de nombreux livres (Clean Architecture, DDD)
- 🏢 Adopté par de nombreuses entreprises
- 🔧 Implémenté dans divers langages et frameworks
- 🎓 Enseigné dans les formations d'architecture logicielle

## Concepts clés inchangés depuis 2005

1. **Isolation du domaine** des détails techniques
2. **Inversion de dépendances** (Dependency Inversion Principle)
3. **Ports** = Interfaces définies par le domaine
4. **Adapters** = Implémentations techniques des ports
5. **Testabilité** complète sans infrastructure

---

### Références

- 📄 [Article original d'Alistair Cockburn](https://alistair.cockburn.us/hexagonal-architecture/)
- 📘 "Clean Architecture" - Robert C. Martin (2017)
- 📙 "Implementing Domain-Driven Design" - Vaughn Vernon (2013)

# Slide 4 : Les couches

## Le domaine :
- La logique métier pure désigne l’ensemble des traitements et opérations 
qui traduisent le fonctionnement du domaine, 
indépendamment de toute technologie ou infrastructure (base de données, interface, etc.). 
Elle est centrée sur le « comment » du métier.
- Les règles métier sont les contraintes, conditions et invariants 
qui doivent toujours être respectés dans le domaine : elles définissent le « quoi » 
(ce qui est permis ou interdit, les validations, les calculs, etc.).