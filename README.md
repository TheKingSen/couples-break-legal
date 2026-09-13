# Pages légales de Couples Break

Les trois textes que l'application Couples Break rend publics :

| Page | Adresse |
|---|---|
| Politique de confidentialité | [`confidentialite.html`](https://thekingsen.github.io/couples-break-legal/confidentialite.html) |
| Conditions d'utilisation | [`conditions.html`](https://thekingsen.github.io/couples-break-legal/conditions.html) |
| Règles de vie | [`regles.html`](https://thekingsen.github.io/couples-break-legal/regles.html) |

Responsable de traitement : **Sendor Dorcent**.
Contact pour l'exercice des droits : **couplesbreak.privacy@gmail.com**.

## Ces fichiers sont générés, pas écrits à la main

Ne les modifiez jamais directement ici : la prochaine génération les écrasera,
et surtout le texte publié cesserait de dire ce que l'application applique
réellement.

Ils sont produits par `scripts/build-site.mjs` dans le dépôt privé
`Couples-Break`, à partir de `mobile/src/data/privacy.ts` et
`mobile/src/data/legal.ts` : exactement les fichiers dont les écrans de
l'application sont tirés. C'est ce qui garantit qu'un couple lit la même chose
à l'écran et en ligne, et c'est la version en ligne qui est opposable.

Pour corriger un texte : modifiez la source dans le dépôt privé, lancez

```bash
node scripts/build-site.mjs
```

puis remettez les quatre fichiers ici. Un contrôle d'intégration du dépôt privé
échoue si les deux versions divergent.

## Pourquoi un dépôt séparé

Apple et Google exigent une adresse web publique menant à la politique de
confidentialité, accessible sans compte et valide dans la durée. Le dépôt de
l'application est privé, et GitHub ne sert pas de pages publiques depuis un
dépôt privé. Seuls les textes qui doivent être publics le sont donc ; le code
reste privé.

## Comment c'est mis en ligne

GitHub Pages sert ce dépôt depuis la branche `gh-pages`. On n'y touche jamais
à la main : `.github/workflows/pages.yml` la recopie depuis `main` à chaque
push, et la mise en ligne suit d'elle-même en une à deux minutes. Il n'y a donc
qu'une seule branche où écrire, `main`.
