# Contribuer à Lumiqo

Merci de l'intérêt que vous portez à ce projet ! Voici comment contribuer efficacement.

---

## Avant de commencer

- Vérifiez que votre idée ou bug n'est pas déjà signalé dans les [Issues](https://github.com/chtitus/lumiqo/issues)
- Pour les changements importants, ouvrez d'abord une Issue pour en discuter avant de coder

---

## Signaler un bug

Ouvrez une [Issue](https://github.com/chtitus/lumiqo/issues/new) en précisant :

1. **Description** — que se passe-t-il exactement ?
2. **Reproduction** — étapes pour reproduire le bug
3. **Comportement attendu** — ce qui devrait se passer
4. **Environnement** — navigateur, OS, mode d'ouverture (file:// ou serveur local)
5. **Capture d'écran** si pertinent

---

## Proposer une fonctionnalité

Ouvrez une [Issue](https://github.com/chtitus/lumiqo/issues/new) avec le label `enhancement` en décrivant :

- Le besoin concret (contexte d'audit, référentiel concerné)
- La solution envisagée
- Les alternatives éventuelles

---

## Contribuer du code

### Types de contributions bienvenues

- 🐛 **Corrections de bugs**
- 🌍 **Nouvelles traductions** (allemand, espagnol, italien, néerlandais...)
- 📝 **Amélioration des formulations types** — pour des secteurs spécifiques (finance, industrie, collectivités...)
- 📋 **Nouvelles questions d'entretien** — compléter ou affiner les questions existantes
- 🎨 **Améliorations UI/UX** — accessibilité, responsive, ergonomie
- 📄 **Documentation** — README, guides d'utilisation, tutoriels

### Ce qui n'est pas accepté

- Modifications des 117 mesures ISO 27001:2022 ou de leur numérotation — celles-ci sont normatives
- Dépendances externes supplémentaires (l'outil doit rester un fichier HTML autonome)
- Fonctionnalités nécessitant un backend (hors scope du projet actuel)

---

## Processus de contribution

### 1. Fork et clone

Cliquez sur **Fork** en haut à droite du dépôt, puis :

```bash
git clone https://github.com/[votre-pseudo]/lumiqo.git
cd lumiqo
```

### 2. Créez une branche

```bash
git checkout -b fix/description-du-bug
# ou
git checkout -b feature/nom-de-la-fonctionnalite
```

Convention de nommage :
- `fix/` — correction de bug
- `feature/` — nouvelle fonctionnalité
- `i18n/` — traduction
- `content/` — amélioration du contenu (formulations, questions)
- `docs/` — documentation uniquement

### 3. Faites vos modifications

Tout le code se trouve dans le fichier unique `lumiqo.html`.

**Points d'attention :**
- Testez dans Firefox ET Chrome (via `npx serve .`)
- Vérifiez que le chiffrement/déchiffrement fonctionne toujours après vos modifications
- Assurez-vous que vos ajouts fonctionnent en FR et EN
- Évitez les apostrophes françaises dans les chaînes JavaScript — utilisez des versions sans accent ou échappez-les

### 4. Testez

Avant de soumettre, vérifiez :

- [ ] Ouverture du fichier dans Firefox (file://)
- [ ] Ouverture via `npx serve .` dans Chrome
- [ ] Création d'un client et saisie de données
- [ ] Chiffrement/déchiffrement (fermer et rouvrir l'outil)
- [ ] Export Word fonctionnel
- [ ] Pas d'erreurs dans la console du navigateur (F12)
- [ ] Interface cohérente en FR et EN

### 5. Commitez

```bash
git add lumiqo.html
git commit -m "fix: description concise du changement"
```

Convention des messages de commit :
- `fix:` — correction de bug
- `feat:` — nouvelle fonctionnalité
- `i18n:` — traduction
- `content:` — contenu (formulations, questions)
- `docs:` — documentation
- `style:` — CSS uniquement

### 6. Ouvrez une Pull Request

Poussez votre branche et ouvrez une Pull Request en décrivant :
- Ce que vous avez modifié et pourquoi
- Comment tester vos changements
- Capture d'écran si la modification est visuelle

---

## Ajouter une traduction

Le système i18n se trouve dans l'objet `TRANSLATIONS` dans le fichier HTML.

Pour ajouter une nouvelle langue (ex: allemand) :

1. Dupliquez le bloc `en: { ... }` et renommez-le `de: { ... }`
2. Traduisez toutes les valeurs
3. Créez les équivalents de `CONTROLS_EN`, `DOMAINS_EN`, `QUESTIONS_EN`, `TEMPLATES_EN`, `DOC_REVIEW_EN` pour la nouvelle langue
4. Ajoutez l'option dans le toggle de langue

---

## Questions

Ouvrez une [Issue](https://github.com/chtitus/lumiqo/issues/new) avec le label `question` — nous répondons dans les meilleurs délais.

---

## Code de conduite

Ce projet accueille des contributions de tous horizons. Soyez respectueux, constructif et bienveillant dans vos échanges. Les contributions inappropriées seront ignorées.

---

*Merci de contribuer à rendre l'audit ISO 27001 plus accessible à tous !*
