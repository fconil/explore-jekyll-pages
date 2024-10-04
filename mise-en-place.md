# Utilisation GitHub Pages

Pour un repository de projet (pas pour l'utilisateur / l'organisation)

<https://pages.github.com/>

1. Créer un repository
2. Aller sur `Settings`
3. Aller dans le menu `Code and automation` > `Pages`

> GitHub Pages is currently disabled. You must first add content to your
> repository before you can publish a GitHub Pages site.

4. Ajouter un contenu pour que le repository ne soit pas vide, ici `mise-en-place.md`

5. On peut alors choisir la branche à publier, par défaut `main` et indiquer un
   dossier source pour la documentation. Par défaut, il prend la racine du
   projet `/(root)` mais propose l'utilisation de `/docs` ce que je vais faire.

   <https://docs.github.com/fr/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site>

> Votre site GitHub Pages sera **toujours déployé avec une exécution d’un
> workflow GitHub Actions**, même si vous avez configuré votre site GitHub
> Pages pour être créé à l’aide d’un autre outil CI. La plupart des workflows
> CI externes se « déploient » sur GitHub Pages en validant la sortie de build
> sur la branche `gh-pages` du référentiel, et incluent généralement un fichier
> `.nojekyll`. Lorsque cela se produit, le workflow GitHub Actions détecte
> l’état que la branche n’a pas besoin d’une étape de build et exécute
> uniquement les étapes nécessaires pour déployer le site sur les serveurs
> GitHub Pages.

6. Cliquer sur le bouton `Save`, à côté des paramètres "branche" et "dossier"

Un workflow est lancé et échoue puisque le dossier `/docs` n'existe pas

Il y a un lien "Learn how to [add a Jekyll theme](https://docs.github.com/fr/pages/setting-up-a-github-pages-site-with-jekyll/adding-a-theme-to-your-github-pages-site-using-jekyll) to your site"

**Je pensais que GitHub Pages créait une structure (scafolding) pour un site
Jekyll. Apparemment non, il faut installer Ruby et Jekyll sur sa machine et
créer le site soi-même.**

<https://docs.github.com/fr/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll>

> **Nous recommandons d’utiliser Jekyll avec GitHub Pages**. Si vous préférez,
> **vous pouvez utiliser d’autres générateurs de sites statiques** ou
> personnaliser votre propre processus de génération en local ou sur un autre
> serveur. Pour plus d’informations, consultez « [À propos de GitHub Pages](https://docs.github.com/fr/pages/getting-started-with-github-pages/about-github-pages#static-site-generators) ».

> Si vous utilisez un processus de génération personnalisé ou un générateur de
> site statique autre que Jekyll, vous pouvez écrire une action GitHub Actions
> pour générer et publier votre site. GitHub fournit des modèles de workflow
> pour plusieurs générateurs de sites statiques. Pour plus d’informations, 
> consultez « [Configuration d’une source de publication pour votre site GitHub Pages](https://docs.github.com/fr/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site) ».

=> Permettrait malgré tout de partager l'édition des pages entre personnes ayant un compte GitHub

## Création d’un site GitHub Pages avec Jekyll

<https://docs.github.com/fr/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll>

Avant de pouvoir utiliser Jekyll pour créer un site GitHub Pages, vous devez installer Jekyll et Git.

Pour plus d’informations, consultez [Installation](https://jekyllrb.com/docs/installation/) dans la documentation de Jekyll et « Configurer Git ».

Nous vous recommandons d’utiliser [Bundler](https://bundler.io/) pour installer et exécuter Jekyll. Bundler gère les dépendances de gemme Ruby, réduit les erreurs de build Jekyll et empêche les bogues liés à l’environnement. Pour installer Bundler :

1. Installer Ruby Pour plus d’informations, consultez « [Installation de Ruby](https://www.ruby-lang.org/en/documentation/installation/) » dans la documentation de Ruby.
2. Installez Bundler. Pour plus d’informations, consultez « Bundler ».

## À propos de GitHub Pages : Limites d'utilisation

<https://docs.github.com/fr/pages/getting-started-with-github-pages/about-github-pages#limites-relatives-%C3%A0-lutilisation-de-github-pages>

### Limites d’utilisation

Les sites GitHub Pages sont soumises aux limites d’utilisation suivantes :

- Les dépôts sources GitHub Pages ont une limite recommandée de 1 Go. Pour plus d’informations, consultez « À propos des fichiers volumineux sur GitHub »
- Les sites publiés GitHub Pages ne peuvent ne pas avoir une taille supérieure à 1 Go.
- Les déploiements GitHub Pages expirent s’ils prennent plus de 10 minutes.
- Les sites GitHub Pages ont une limite de bande passante souple de 100 Go par mois.
- Les sites GitHub Pages ont une limite souple de 10 builds par heure. Cette limite ne s’applique pas si vous générez et publiez votre site avec un flux de travail GitHub Actions personnalisé.

Afin de fournir une même qualité de service pour tous les sites GitHub Pages,
des limites de débit peuvent être appliquées. Ces limites de débit ne doivent
pas interférer avec les utilisations légitimes de GitHub Pages. Si votre
demande déclenche une limitation du débit, vous recevrez une réponse contenant
le code d’état HTTP 429, ainsi qu’un corps HTML informatif.

Si votre site dépasse ces quotas d’utilisation, il se peut que nous ne
puissions pas le servir ou que vous receviez un e-mail poli de Support GitHub
suggérant des stratégies de réduction de l’impact de votre site sur nos
serveurs, dont la mise en place d’un réseau de distribution de contenu tiers
(CDN) devant votre site, l’utilisation d’autres fonctionnalités GitHub telles
que les versions, ou le passage à un autre service d’hébergement susceptible de
mieux répondre à vos besoins.

