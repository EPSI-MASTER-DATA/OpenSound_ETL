# OpenSound_ETL

# Tutoriel Git : travailler avec des branches et avec un fork

Ce guide explique simplement deux façons courantes de collaborer avec Git et GitHub / GitLab :

1. **Travailler avec des branches** sur un dépôt partagé
2. **Travailler avec un fork** lorsque l’on n’écrit pas directement sur le dépôt principal

---

# 1. Travailler avec des branches

## Pourquoi utiliser des branches ?

Les branches permettent de :

- développer une fonctionnalité sans casser la branche principale
- corriger un bug de manière isolée
- travailler à plusieurs sans modifier directement `main`
- relire et valider le code avant intégration

---

## Workflow recommandé

### Étape 1 : se placer sur la branche de base

```bash
git checkout develop
git pull origin develop
```

---

### Étape 2 : créer une nouvelle branche

```bash
git checkout -b feature/ma-feature
```

---

### Étape 3 : travailler et commit (regarder la convention angular)

```bash
git add .
git commit -m "feat: add new feature"
```

---

### Étape 4 : push la branche

```bash
git push origin feature/ma-feature
```

---

### Étape 5 : Pull Request

- Ouvrir une PR / MR
- Faire relire
- Merge dans `develop` ou `main`

---

# 2. Travailler avec un fork

## Définition

Un fork est une copie d’un dépôt dans ton compte.

---

## Workflow

### Étape 1 : fork du dépôt

Via GitHub/GitLab

---

### Étape 2 : clone du fork

```bash
git clone https://github.com/ton-compte/projet.git
cd projet
```

---

### Étape 3 : ajouter upstream

```bash
git remote add upstream https://github.com/original/projet.git
```

---

### Étape 4 : sync avec upstream

```bash
git fetch upstream
git checkout main
git merge upstream/main
```

---

### Étape 5 : créer une branche

```bash
git checkout -b feature/ma-feature
```

---

### Étape 6 : commit et push

```bash
git add .
git commit -m "feat: amélioration"
git push origin feature/ma-feature
```

---

### Étape 7 : Pull Request

- Depuis ton fork vers le repo principal

---

# 3. Bonnes pratiques

- Ne jamais travailler directement sur `main`
- Faire des commits clairs (`feat`, `fix`, `docs`…)
- Mettre à jour régulièrement sa branche
- Faire des PR petites et lisibles

---

# 4. Commandes utiles

```bash
git branch
git checkout -b nom-branche
git pull origin main
git push origin nom-branche
git remote -v
git fetch upstream
```

---

# 5. Résumé

## Branches
- Travail direct sur repo
- Une branche par feature
- PR pour merge

## Fork
- Copie du repo
- Travail sur son fork
- PR vers repo original

---

# Conclusion

- **Branches = travail interne**
- **Fork = contribution externe**

Toujours :
- partir d’une base à jour
- isoler son travail
- faire des commits propres
- passer par une PR

