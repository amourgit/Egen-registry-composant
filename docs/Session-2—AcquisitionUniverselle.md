# SESSION 2/8 — EXPRESSION EXHAUSTIVE DES BESOINS
# ACQUISITION UNIVERSELLE, DÉCOUVERTE MULTISOURCE ET IMPORTATION INTELLIGENTE

## 1. OBJET ET FINALITÉ DE CETTE PARTIE

Cette partie approfondit exclusivement les exigences relatives à la découverte, à l'acquisition et à l'importation des ressources logicielles dans la plateforme.

Elle complète le document de vision globale en précisant l'étendue des sources que le produit doit pouvoir prendre en charge, les différents modes d'acquisition attendus, les capacités d'exploration des ressources externes et les exigences relatives à leur récupération.

L'objectif est de définir un système d'acquisition extrêmement riche, ouvert, polyvalent et évolutif.

Il ne faut pas considérer l'acquisition comme une simple opération technique consistant à télécharger un fichier ou à cloner un dépôt. Elle doit être envisagée comme un ensemble de fonctionnalités permettant de découvrir des ressources, de comprendre leur organisation, d'identifier les éléments intéressants, de déterminer leur nature, de récupérer les fichiers nécessaires et de préparer leur intégration dans le patrimoine central de la plateforme.

La plateforme doit pouvoir travailler avec des sources très différentes, qui ne possèdent pas nécessairement les mêmes structures, les mêmes formats, les mêmes métadonnées ou les mêmes possibilités d'accès.

Certaines sources seront parfaitement structurées et exposeront des catalogues exploitables automatiquement. D'autres ne seront que des dépôts de code classiques. Certaines proposeront des fichiers isolés, tandis que d'autres présenteront leurs composants dans une documentation, une galerie interactive ou des exemples de démonstration.

Le système doit pouvoir s'adapter à ces situations.

**L'exigence fondamentale est de ne pas rendre l'acquisition dépendante d'un seul fournisseur, d'un seul format de publication ou d'un seul mode de récupération.**

---

# 2. UNE CAPACITÉ D'ACQUISITION MULTISOURCE SANS ENFERMEMENT

La plateforme doit pouvoir travailler avec une diversité importante de sources.

Il ne faut pas limiter cette capacité aux sources déjà connues lors du développement initial.

L'écosystème logiciel évolue constamment. De nouvelles plateformes, de nouveaux catalogues, de nouveaux registres et de nouveaux mécanismes de publication apparaissent régulièrement.

Le système doit donc être suffisamment ouvert pour accueillir de nouvelles origines et de nouveaux modes de récupération.

## 2.1. Sources officielles de composants et de bibliothèques

La plateforme doit pouvoir prendre en charge les sources qui publient directement des composants ou des bibliothèques de ressources.

Cela comprend notamment :

- Les catalogues officiels de composants.
- Les bibliothèques de composants open source.
- Les collections de composants communautaires.
- Les bibliothèques de primitives d'interface.
- Les collections de composants animés.
- Les bibliothèques de visualisation.
- Les bibliothèques de composants spécialisés.
- Les collections de blocs d'interface.
- Les catalogues de templates.
- Les bibliothèques de thèmes et de styles.
- Les collections d'éléments graphiques.
- Les systèmes de design distribuables.

Quelques exemples de sources que nous souhaitons pouvoir intégrer :

- shadcn/ui.
- Radix UI.
- Aceternity UI.
- Magic UI.
- Origin UI.
- React Bits.
- Cult UI.
- Animate UI.
- Tremor.
- Park UI.
- Ark UI.
- Headless UI.
- DaisyUI.
- Flowbite.
- Preline UI.
- Autres bibliothèques et collections pertinentes.

Cette liste ne constitue pas une liste fermée de fournisseurs.

Le système doit pouvoir découvrir et prendre en charge d'autres sources présentant des caractéristiques similaires.

Il faut également distinguer les sources qui distribuent des fichiers sources directement de celles qui proposent uniquement des packages, des exemples ou des ressources accessibles sous certaines conditions.

## 2.2. Registries spécialisées

La plateforme doit accorder une attention particulière aux registres de composants et aux mécanismes de distribution structurés.

Nous voulons pouvoir travailler avec :

- Les Registries compatibles shadcn.
- Les Registries hébergées sur GitHub.
- Les Registries hébergées sur des serveurs indépendants.
- Les Registries exposant des fichiers JSON.
- Les Registries exposant une API.
- Les Registries possédant un catalogue dynamique.
- Les Registries privées.
- Les Registries publiques.
- Les Registries communautaires.
- Les Registries internes à une organisation.
- Les futurs systèmes de distribution de ressources structurées.

La documentation de référence de shadcn doit servir de point de départ pour comprendre les possibilités offertes par les Registries :

https://ui.shadcn.com/docs/registry

https://ui.shadcn.com/docs/registry/github

https://ui.shadcn.com/docs/registry/registry-json

https://ui.shadcn.com/docs/registry/registry-item-json

https://ui.shadcn.com/docs/registry/namespaces

La plateforme doit être capable de consommer les Registries compatibles, de parcourir leurs catalogues, d'identifier leurs éléments et de récupérer les ressources sélectionnées.

Mais elle ne doit pas supposer que toutes les Registries utilisent exactement le même format.

Une Registry propriétaire ou communautaire pourra nécessiter un mécanisme d'adaptation particulier.

Nous voulons donc une prise en charge aussi large que possible des systèmes de distribution existants.

## 2.3. Plateformes d'hébergement de code source

L'acquisition ne doit pas être limitée aux plateformes de publication de composants.

Elle doit également pouvoir exploiter les plateformes qui hébergent des projets logiciels complets.

Les sources à considérer comprennent notamment :

- GitHub.
- GitLab.
- Bitbucket.
- Codeberg.
- SourceHut.
- Gitea.
- Forgejo.
- Instances Git auto-hébergées.
- Autres plateformes compatibles avec Git.
- Serveurs proposant des archives ou des répertoires téléchargeables.

Le système doit pouvoir travailler avec des dépôts publics, mais aussi avec des dépôts privés lorsque l'utilisateur dispose des autorisations nécessaires.

Il doit être possible de renseigner un dépôt, de consulter son contenu, de parcourir ses branches, ses tags et ses répertoires, puis de sélectionner précisément les éléments à récupérer.

Il ne faut pas imposer le téléchargement complet d'un dépôt lorsqu'une sélection partielle suffit.

## 2.4. Documentation et catalogues de ressources

Certaines ressources sont publiées principalement à travers une documentation technique.

Il peut s'agir de documentations qui présentent :

- Des composants.
- Des exemples de code.
- Des démonstrations interactives.
- Des variantes.
- Des propriétés.
- Des fichiers de configuration.
- Des instructions d'installation.
- Des exemples de composition.
- Des dépendances.
- Des ressources complémentaires.

La plateforme doit pouvoir envisager l'acquisition depuis ces environnements.

Elle doit notamment pouvoir explorer une documentation, identifier les éléments pertinents, récupérer les exemples de code accessibles et, lorsque cela est techniquement possible, reconstituer les fichiers nécessaires à partir des ressources présentées.

Il faut distinguer le code réellement disponible du rendu simplement affiché dans une démonstration.

Le système ne doit jamais prétendre avoir récupéré un code source original lorsqu'il n'a récupéré qu'une représentation ou un extrait incomplet.

## 2.5. Autres sources potentielles

Le système doit également pouvoir envisager :

- Les archives ZIP et TAR.
- Les packages npm et autres registres de packages.
- Les archives de releases.
- Les fichiers téléchargeables.
- Les répertoires partagés.
- Les dépôts miroirs.
- Les sources accessibles par URL directe.
- Les sources exposant des manifests.
- Les catalogues possédant leur propre API.
- Les sources documentées à travers des fichiers Markdown.
- Les collections de ressources publiées dans des projets indépendants.
- Les sources internes à une organisation.
- Les sources fournies manuellement par les utilisateurs.

La plateforme doit rester ouverte à toute autre origine légalement accessible et techniquement exploitable.

---

# 3. MULTIPLICITÉ DES MODES D'ACQUISITION

Une même source peut proposer plusieurs manières d'accéder à ses ressources.

Inversement, plusieurs sources différentes peuvent utiliser le même mécanisme de récupération.

Il faut donc éviter de confondre le fournisseur d'une ressource avec la manière dont cette ressource est acquise.

Nous voulons disposer d'une véritable diversité de modes d'importation.

## 3.1. Acquisition à partir d'une Registry

Lorsque la source expose une Registry compatible, le système doit pouvoir :

- Identifier la Registry.
- Lire son catalogue.
- Récupérer les informations générales.
- Explorer les éléments disponibles.
- Identifier les catégories.
- Consulter les métadonnées.
- Identifier les dépendances déclarées.
- Examiner les fichiers associés.
- Identifier les éléments nécessaires à d'autres éléments.
- Sélectionner un élément individuel.
- Sélectionner plusieurs éléments.
- Récupérer une collection.
- Récupérer les ressources dépendantes.
- Vérifier les informations disponibles avant importation.

Il faut également prendre en charge les Registries qui nécessitent un namespace, une URL spécifique ou des paramètres d'accès.

L'utilisateur doit pouvoir ajouter une Registry comme source connue de la plateforme et la réutiliser lors de futures acquisitions.

## 3.2. Acquisition depuis un dépôt Git

Le système doit pouvoir récupérer des ressources depuis un dépôt Git classique.

Les opérations attendues comprennent :

- Identification du dépôt.
- Exploration de son arborescence.
- Consultation des branches.
- Consultation des tags.
- Sélection d'un commit.
- Sélection d'un répertoire.
- Sélection de plusieurs fichiers.
- Récupération d'un sous-ensemble du dépôt.
- Récupération du dépôt complet lorsque nécessaire.
- Identification des fichiers importants.
- Conservation des informations relatives au commit d'origine.

Il doit être possible d'importer une ressource depuis une branche spécifique sans perdre la possibilité de retrouver ultérieurement la version exacte qui a été récupérée.

Le système doit également pouvoir distinguer une importation depuis la branche principale d'une importation depuis une branche de développement ou une release.

## 3.3. Acquisition par URL directe

L'utilisateur doit pouvoir fournir directement une URL.

Cette URL peut pointer vers :

- Un fichier source.
- Un fichier JSON.
- Un fichier CSS.
- Un fichier SVG.
- Une archive.
- Un manifest.
- Un package.
- Une ressource graphique.
- Une documentation.
- Une page présentant un composant.
- Un endpoint de Registry.
- Un répertoire ou une ressource accessible à travers une plateforme externe.

Le système doit tenter d'identifier la nature de la ressource et déterminer le mode d'acquisition adapté.

Lorsque l'URL ne permet pas une récupération exploitable, il doit expliquer clairement la limitation et proposer les possibilités compatibles avec la source.

## 3.4. Acquisition depuis un package existant

La plateforme doit pouvoir prendre en considération les composants distribués sous forme de packages.

Nous voulons notamment pouvoir :

- Identifier un package.
- Consulter ses versions.
- Examiner ses métadonnées.
- Identifier ses dépendances.
- Récupérer les informations de son manifeste.
- Consulter les fichiers sources lorsqu'ils sont publiés.
- Consulter les fichiers de distribution.
- Identifier les déclarations de types.
- Identifier les ressources CSS.
- Identifier les assets associés.
- Déterminer si le package expose réellement des sources exploitables.

Il est essentiel de distinguer un package compilé d'un package dont les fichiers sources sont disponibles.

L'objectif est de récupérer autant que possible les ressources originales, sans prétendre reconstituer artificiellement un code source qui n'est pas fourni.

## 3.5. Acquisition depuis une archive

L'utilisateur doit pouvoir importer des archives contenant des ressources logicielles.

Les formats à envisager comprennent notamment ZIP, TAR, TAR.GZ et les autres formats courants.

Le système doit pouvoir :

- Lire le contenu de l'archive.
- Explorer son arborescence.
- Identifier les fichiers.
- Identifier les dossiers.
- Reconnaître les structures de projets.
- Détecter les composants potentiels.
- Identifier les fichiers de configuration.
- Identifier les dépendances.
- Permettre une sélection avant intégration.
- Préserver la structure originale lorsque nécessaire.

Il ne faut pas imposer l'intégration de l'intégralité de l'archive.

L'utilisateur doit pouvoir sélectionner les éléments pertinents.

## 3.6. Importation manuelle

Nous voulons également un mode d'importation manuelle.

L'utilisateur doit pouvoir fournir :

- Un ou plusieurs fichiers.
- Un dossier.
- Une collection de fichiers.
- Un ensemble de composants.
- Des fichiers de styles.
- Des ressources graphiques.
- Des configurations.
- Des fichiers de documentation.
- Des manifests.

Il doit pouvoir indiquer ce qu'il importe et compléter les informations qui n'auraient pas pu être détectées automatiquement.

Ce mode est indispensable pour les ressources qui ne proviennent pas d'une plateforme standardisée.

## 3.7. Importation par lots

Le système ne doit pas imposer une acquisition individuelle pour chaque ressource.

Il doit être possible de lancer des importations multiples.

Par exemple :

- Plusieurs composants provenant d'une même Registry.
- Plusieurs dépôts Git.
- Plusieurs fichiers depuis différentes sources.
- Plusieurs collections.
- Plusieurs versions d'un même composant.
- Plusieurs catégories de ressources.
- Plusieurs sources dans une même opération.

L'utilisateur doit pouvoir suivre les opérations, consulter leur progression, identifier les échecs et reprendre les acquisitions interrompues.

---

# 4. EXPLORATION DES SOURCES AVANT IMPORTATION

L'acquisition doit être précédée, lorsque cela est possible, d'une phase d'exploration.

Nous voulons éviter de télécharger inutilement des ressources dont l'utilisateur ne connaît pas encore le contenu.

Le système doit proposer une véritable expérience de découverte.

## 4.1. Exploration d'un catalogue externe

Lorsqu'une source expose un catalogue, l'utilisateur doit pouvoir le parcourir comme une bibliothèque.

Il doit notamment pouvoir :

- Consulter les éléments disponibles.
- Explorer les catégories.
- Rechercher un élément.
- Filtrer les résultats.
- Consulter les descriptions.
- Identifier les technologies.
- Examiner les dépendances.
- Consulter les versions disponibles.
- Identifier les ressources associées.
- Visualiser les démonstrations disponibles.
- Sélectionner les éléments à importer.

## 4.2. Exploration d'un dépôt

Pour un dépôt classique, l'utilisateur doit disposer d'une représentation exploitable de son contenu.

Il doit pouvoir :

- Parcourir les dossiers.
- Développer et réduire les répertoires.
- Identifier les fichiers.
- Consulter les noms et extensions.
- Repérer les fichiers de configuration.
- Identifier les fichiers potentiellement réutilisables.
- Consulter les fichiers sources.
- Identifier les répertoires de composants.
- Repérer les exemples.
- Repérer les tests.
- Identifier les ressources graphiques.
- Comprendre la structure générale du projet.

Le système doit pouvoir présenter une première analyse du dépôt avant toute importation.

## 4.3. Exploration visuelle

Lorsque la source expose des démonstrations ou des captures exploitables, nous voulons pouvoir visualiser les composants avant de les récupérer.

Il faut envisager :

- Les aperçus statiques.
- Les démonstrations interactives.
- Les variantes visuelles.
- Les différents états d'un composant.
- Les exemples de composition.
- Les différentes tailles.
- Les déclinaisons responsive.
- Les animations.
- Les interactions disponibles.

La disponibilité de ces informations dépend de la source.

Il ne faut pas inventer une démonstration lorsque le code ou les ressources nécessaires sont absents.

## 4.4. Sélection granulaire

L'utilisateur doit pouvoir sélectionner précisément ce qu'il souhaite importer.

La sélection peut concerner :

- Un composant.
- Plusieurs composants.
- Un fichier.
- Plusieurs fichiers.
- Un dossier.
- Une catégorie.
- Une collection.
- Un ensemble de composants dépendants.
- Une version.
- Une variante.
- Un sous-ensemble de ressources.

Il faut pouvoir visualiser les conséquences de la sélection.

Par exemple, si l'utilisateur sélectionne un composant qui dépend de plusieurs autres éléments, le système doit lui signaler les dépendances identifiées et lui permettre de décider comment les traiter.

---

# 5. DÉTECTION ET IDENTIFICATION AUTOMATIQUE DES RESSOURCES

Toutes les sources ne disposent pas d'un catalogue proprement structuré.

La plateforme doit donc posséder des capacités de reconnaissance et d'analyse des ressources récupérées.

Nous voulons qu'elle soit capable d'identifier les éléments susceptibles de constituer des ressources réutilisables.

## 5.1. Reconnaissance des technologies

Le système doit pouvoir identifier, dans la mesure du possible :

- Le langage utilisé.
- Le framework.
- La bibliothèque principale.
- Le système de styles.
- Le système de construction.
- Le gestionnaire de packages.
- Les outils de développement.
- Les conventions d'importation.
- Les formats de fichiers.
- Les environnements d'exécution concernés.

Exemples :

- React.
- Next.js.
- Vue.
- Nuxt.
- Angular.
- Svelte.
- SvelteKit.
- SolidJS.
- Astro.
- React Native.
- Flutter.
- HTML.
- CSS.
- JavaScript.
- TypeScript.
- Autres technologies pertinentes.

Cette détection doit pouvoir s'appuyer sur les fichiers de configuration, les manifests, les extensions, les imports et les caractéristiques du code.

## 5.2. Reconnaissance des composants

Le système doit rechercher les éléments susceptibles d'être des composants réutilisables.

Il doit pouvoir identifier :

- Les composants exportés.
- Les composants internes.
- Les sous-composants.
- Les composants composés.
- Les fonctions exportées.
- Les hooks.
- Les services.
- Les modules.
- Les classes.
- Les interfaces.
- Les types.
- Les éléments de configuration.
- Les ressources de styles.
- Les assets associés.

L'objectif n'est pas de supposer qu'un fichier représente toujours un composant.

Un même fichier peut contenir plusieurs éléments, et un même composant peut être réparti dans plusieurs fichiers.

La plateforme doit être capable de représenter cette complexité.

## 5.3. Identification des points d'entrée

Le système doit pouvoir repérer les fichiers et déclarations qui permettent d'accéder à une ressource.

Il doit notamment pouvoir identifier :

- Les exports.
- Les index.
- Les fichiers d'entrée.
- Les manifests.
- Les déclarations de packages.
- Les fichiers de configuration.
- Les chemins d'importation.
- Les points d'entrée des sous-modules.

Cette information est nécessaire pour comprendre comment récupérer et utiliser correctement une ressource.

## 5.4. Identification des ressources associées

Un composant peut dépendre de ressources qui ne sont pas immédiatement visibles.

Le système doit pouvoir rechercher :

- Les styles associés.
- Les fichiers CSS.
- Les tokens.
- Les images.
- Les icônes.
- Les polices.
- Les fichiers SVG.
- Les hooks.
- Les fonctions utilitaires.
- Les autres composants.
- Les fichiers de configuration.
- Les données nécessaires aux exemples.
- Les ressources complémentaires.

L'utilisateur doit pouvoir comprendre ce qui constitue réellement l'ensemble d'une ressource.

---

# 6. IMPORTATION DE COMPOSANTS DEPUIS DES PROJETS COMPLETS

Cette capacité mérite une attention particulière.

Nous voulons pouvoir récupérer un composant depuis un projet logiciel qui n'a jamais été conçu pour être distribué individuellement.

Par exemple, un dépôt GitHub peut contenir une application complète avec plusieurs dizaines de composants, des services, des configurations, des pages et des ressources.

Nous voulons pouvoir identifier un composant intéressant dans ce projet et tenter de l'extraire sans importer inutilement toute l'application.

Le système doit donc envisager une capacité d'extraction sélective.

## 6.1. Extraction d'un composant individuel

L'utilisateur doit pouvoir désigner un composant et demander son extraction.

Le système doit alors rechercher les fichiers nécessaires à son fonctionnement.

Il doit notamment identifier :

- Le fichier principal.
- Les sous-composants.
- Les dépendances internes.
- Les imports relatifs.
- Les fichiers de styles.
- Les hooks.
- Les utilitaires.
- Les assets.
- Les types.
- Les configurations indispensables.

Le résultat doit constituer un ensemble de fichiers cohérent, autant que les informations disponibles le permettent.

## 6.2. Extraction d'un ensemble de composants

Il doit être possible d'extraire plusieurs composants liés entre eux.

Par exemple, un ensemble de composants provenant d'un module de tableau de bord.

Le système doit pouvoir conserver leurs relations et leurs dépendances sans les dissocier arbitrairement.

## 6.3. Extraction depuis une application complète

Nous voulons pouvoir analyser une application et identifier ses ressources réutilisables.

Il peut s'agir de :

- Ses composants UI.
- Ses blocs fonctionnels.
- Ses composants de navigation.
- Ses formulaires.
- Ses tableaux.
- Ses graphiques.
- Ses éléments de présentation.
- Ses hooks.
- Ses utilitaires.
- Ses styles.
- Ses thèmes.

La plateforme doit pouvoir présenter les ressources détectées et permettre à l'utilisateur de sélectionner celles qu'il souhaite récupérer.

## 6.4. Extraction assistée

Certaines extractions seront complexes.

Le système doit pouvoir signaler les dépendances difficiles à isoler, les configurations spécifiques à l'application, les imports non résolus et les éléments qui nécessitent une adaptation.

Il doit pouvoir proposer une extraction assistée plutôt que de présenter un résultat incomplet comme étant directement utilisable.

L'utilisateur doit pouvoir intervenir pour préciser les fichiers à conserver, les dépendances à remplacer et les éléments à exclure.

---

# 7. ANALYSE DES DÉPENDANCES AVANT ET PENDANT L'IMPORTATION

L'acquisition ne doit pas produire des composants isolés de leur contexte technique.

Il faut comprendre les dépendances nécessaires à leur fonctionnement.

## 7.1. Dépendances externes

Le système doit identifier autant que possible :

- Les packages npm.
- Les packages de développement.
- Les bibliothèques tierces.
- Les dépendances optionnelles.
- Les dépendances nécessaires à l'exécution.
- Les dépendances liées aux styles.
- Les dépendances de construction.
- Les versions déclarées.

## 7.2. Dépendances internes

Il faut également identifier les relations entre les ressources d'une même source.

Par exemple :

Un composant DataTable peut dépendre d'un Checkbox, d'un DropdownMenu, d'un Button, d'un système de pagination et de plusieurs fonctions utilitaires.

Le système doit pouvoir identifier ces relations et déterminer quelles ressources doivent être récupérées pour constituer un ensemble exploitable.

## 7.3. Dépendances indirectes

Il faut également prendre en compte les dépendances transitives.

Un composant peut dépendre d'un autre composant qui dépend lui-même de plusieurs ressources.

La plateforme doit pouvoir explorer ces relations et présenter une vision aussi complète que possible.

## 7.4. Dépendances manquantes

Lorsqu'une dépendance n'est pas disponible, le système doit le signaler.

Il doit être capable de distinguer :

- Les dépendances disponibles.
- Les dépendances récupérables.
- Les dépendances déjà présentes dans le patrimoine.
- Les dépendances manquantes.
- Les dépendances incompatibles.
- Les dépendances optionnelles.
- Les dépendances dont la version est incertaine.

Il ne faut jamais déclarer qu'une ressource est entièrement autonome lorsque des dépendances indispensables n'ont pas été récupérées.

## 7.5. Réutilisation des dépendances existantes

Lorsqu'une ressource importée dépend d'un élément déjà présent dans le patrimoine, le système doit pouvoir identifier cette correspondance.

Il faut éviter de multiplier inutilement les copies de ressources identiques.

Cependant, il faut aussi préserver la possibilité de conserver une dépendance dans sa version d'origine lorsque sa substitution par une version interne risquerait de modifier le comportement du composant.

---

# 8. GESTION DES VERSIONS ET DES VARIANTES LORS DE L'ACQUISITION

L'acquisition doit permettre de sélectionner précisément la version d'une ressource.

Le système doit prendre en compte :

- Les versions sémantiques.
- Les releases.
- Les tags Git.
- Les branches.
- Les commits.
- Les versions de packages.
- Les versions d'une Registry.
- Les révisions propres à une source.

Lorsqu'une source expose plusieurs versions, l'utilisateur doit pouvoir les consulter.

Il doit être possible de récupérer une version stable, une version expérimentale ou une révision particulière lorsque la source le permet.

Le système doit également pouvoir détecter les variantes d'un même composant.

Par exemple :

- Variantes visuelles.
- Variantes fonctionnelles.
- Variantes responsive.
- Variantes adaptées à différents frameworks.
- Variantes utilisant différentes bibliothèques.
- Variantes destinées à différents environnements.

Ces variantes ne doivent pas être confondues avec les versions historiques d'un même composant.

---

# 9. GESTION DES LICENCES ET DE LA PROVENANCE DES SOURCES

La plateforme doit intégrer la question des droits dès la phase d'acquisition.

Une ressource publiquement accessible n'est pas nécessairement librement modifiable ou redistribuable.

Nous voulons donc que chaque acquisition puisse conserver les informations relatives à son origine et à ses conditions d'utilisation.

## 9.1. Identification des licences

Le système doit rechercher les informations de licence disponibles dans :

- Les fichiers LICENSE.
- Les fichiers COPYING.
- Les manifests.
- Les métadonnées de packages.
- Les déclarations des Registries.
- Les informations du dépôt.
- Les notices de copyright.
- Les documentations officielles.

Il doit notamment pouvoir identifier les licences courantes, telles que :

- MIT.
- Apache-2.0.
- BSD.
- ISC.
- MPL.
- GPL.
- LGPL.
- AGPL.
- Licences propriétaires.
- Licences commerciales.
- Conditions spécifiques à certains catalogues.

## 9.2. Traçabilité de provenance

Pour chaque ressource importée, nous voulons pouvoir retrouver :

- La source d'origine.
- L'URL d'origine.
- Le propriétaire ou l'auteur lorsque disponible.
- Le dépôt d'origine.
- La version récupérée.
- Le commit correspondant.
- La date d'acquisition.
- Le mode d'acquisition.
- La licence identifiée.
- Les éventuelles notices à conserver.
- Les modifications apportées ultérieurement.

## 9.3. Restrictions et avertissements

Le système doit signaler les situations dans lesquelles les droits sont incertains, incomplets ou incompatibles avec l'utilisation envisagée.

Il doit distinguer la possibilité technique de récupérer une ressource de la possibilité juridique de la modifier, de la redistribuer ou de l'intégrer à un produit commercial.

Il doit notamment prendre en considération les licences qui imposent des obligations particulières en matière de redistribution, de conservation des notices, de mise à disposition des modifications ou de publication du code dérivé.

L'utilisateur doit disposer des informations nécessaires pour prendre une décision éclairée avant l'importation et avant toute publication.

## 9.4. Absence de licence identifiable

Lorsqu'aucune licence n'est détectée, le système ne doit pas supposer que la ressource est libre.

Il doit conserver son statut comme indéterminé et signaler les limites d'utilisation qui en résultent.

---

# 10. GESTION DES SOURCES PRIVÉES ET DES ACCÈS AUTHENTIFIÉS

L'acquisition doit pouvoir fonctionner avec des sources publiques et privées.

Il faut envisager les situations dans lesquelles l'utilisateur souhaite connecter ses propres comptes ou accéder à des dépôts qui nécessitent une authentification.

Les sources concernées peuvent notamment être :

- Des dépôts privés GitHub.
- Des dépôts privés GitLab.
- Des Registries privées.
- Des serveurs Git internes.
- Des API protégées.
- Des espaces de stockage privés.
- Des plateformes internes à une organisation.

Le système doit permettre les mécanismes d'accès appropriés, dans le respect des autorisations accordées.

Il faut distinguer les différentes permissions :

- Lecture.
- Exploration.
- Téléchargement.
- Accès aux métadonnées.
- Accès aux versions.
- Accès aux ressources privées.

Les identifiants, jetons et autres informations sensibles ne doivent jamais être exposés dans les fichiers importés, les logs ou les manifests distribués.

L'utilisateur doit pouvoir révoquer les accès et gérer les sources connectées.

---

# 11. GESTION DES IMPORTATIONS COMPLEXES ET DES CAS PARTICULIERS

Nous voulons que le système soit suffisamment robuste pour ne pas fonctionner uniquement avec des sources parfaitement organisées.

Il doit envisager des situations réelles et parfois difficiles.

### 11.1. Source incomplète

Une source peut contenir des composants dont certains fichiers manquent.

Le système doit pouvoir identifier les éléments absents et présenter les limites de l'importation.

### 11.2. Source mal structurée

Un projet peut posséder une organisation inhabituelle, sans convention claire.

Le système doit pouvoir explorer les fichiers et proposer une interprétation, éventuellement avec l'intervention de l'utilisateur.

### 11.3. Source contenant plusieurs technologies

Un dépôt peut réunir React, Vue, des scripts Python, des ressources CSS et des outils de construction.

Le système ne doit pas supposer que l'intégralité du dépôt correspond à un seul environnement technologique.

### 11.4. Ressources dupliquées

Plusieurs sources peuvent proposer des composants identiques ou très similaires.

Le système doit pouvoir identifier les doublons potentiels sans supprimer automatiquement des ressources qui pourraient posséder des différences importantes.

### 11.5. Versions incompatibles

Un composant peut dépendre d'une version ancienne d'une bibliothèque ou d'un framework.

Le système doit pouvoir identifier cette situation et présenter les contraintes connues.

### 11.6. Ressources partiellement accessibles

Certaines sources peuvent limiter l'accès à certains fichiers, certaines versions ou certaines ressources.

Le système doit distinguer ce qui a été récupéré de ce qui demeure inaccessible.

### 11.7. Sources indisponibles

Lorsqu'une source ne répond plus, le système doit pouvoir signaler l'indisponibilité, conserver les informations déjà obtenues et permettre de reprendre l'opération ultérieurement.

### 11.8. Importation interrompue

Les opérations longues doivent pouvoir être suivies et, lorsque les conditions techniques le permettent, reprises sans devoir recommencer intégralement.

---

# 12. AUTOMATISATION ET INTELLIGENCE DANS L'ACQUISITION

L'acquisition doit pouvoir bénéficier de capacités d'automatisation avancées.

Nous voulons notamment pouvoir fournir une URL et laisser le système effectuer une première exploration.

À partir d'une source, il doit pouvoir :

- Identifier la nature de la source.
- Déterminer le mode d'acquisition approprié.
- Explorer les ressources disponibles.
- Identifier les composants potentiels.
- Détecter les frameworks.
- Analyser les dépendances.
- Identifier les métadonnées.
- Rechercher les informations de licence.
- Identifier les fichiers associés.
- Détecter les ressources similaires.
- Proposer une sélection d'éléments intéressants.
- Présenter les informations détectées.
- Signaler les incertitudes.
- Préparer une opération d'importation.

Nous voulons également envisager une assistance IA capable d'aider à comprendre des projets complexes.

Cette assistance pourrait notamment :

- Expliquer la structure d'un dépôt.
- Identifier les composants intéressants.
- Distinguer les composants des pages complètes.
- Expliquer les relations entre les fichiers.
- Proposer les fichiers nécessaires à une extraction.
- Identifier des dépendances non déclarées.
- Expliquer les limitations d'une importation.
- Aider à compléter les métadonnées.
- Proposer des regroupements cohérents.

Toutefois, les résultats de l'analyse automatique ou de l'IA doivent être distingués des informations directement confirmées par la source.

Une hypothèse ne doit jamais être présentée comme une information certaine.

Les opérations sensibles, les importations et les décisions relatives aux droits doivent rester soumises aux contrôles et validations appropriés.

---

# 13. EXPÉRIENCE UTILISATEUR ATTENDUE POUR L'ACQUISITION

L'acquisition doit constituer une expérience complète, et non une succession de formulaires techniques.

Nous voulons que l'utilisateur puisse découvrir et importer des ressources avec une grande simplicité, même lorsqu'il travaille avec des sources complexes.

## 13.1. Point d'entrée centralisé

La plateforme doit proposer un environnement dans lequel l'utilisateur peut initier une acquisition.

Il doit pouvoir choisir une source connue, renseigner une nouvelle origine ou utiliser un mode d'importation adapté à son besoin.

## 13.2. Exploration guidée

Une fois la source identifiée, l'utilisateur doit pouvoir explorer son contenu.

L'interface doit présenter les informations disponibles, les éléments détectés, les catégories, les technologies, les versions et les ressources associées.

## 13.3. Sélection et préparation

L'utilisateur doit pouvoir sélectionner les ressources et examiner le contenu qui sera récupéré.

La plateforme doit présenter les dépendances identifiées, les éventuels conflits, les avertissements de licence et les informations manquantes.

## 13.4. Importation contrôlée

L'utilisateur doit pouvoir confirmer l'importation et suivre son déroulement.

Il doit disposer d'une visibilité sur :

- Les éléments en attente.
- Les éléments en cours de récupération.
- Les éléments récupérés.
- Les éléments analysés.
- Les éléments nécessitant une intervention.
- Les éléments importés avec succès.
- Les éléments en échec.

## 13.5. Résultat de l'importation

À la fin d'une opération, le système doit présenter un compte rendu clair.

Il doit indiquer ce qui a été récupéré, ce qui n'a pas pu l'être, les dépendances détectées, les éventuelles limitations et les informations qui nécessitent une vérification.

---

# 14. GESTION DES SOURCES CONNUES ET DES CONNECTEURS

Nous voulons pouvoir constituer progressivement un répertoire de sources exploitables.

Une source déjà enregistrée ne devrait pas nécessairement devoir être renseignée à nouveau à chaque importation.

La plateforme doit pouvoir gérer un catalogue de sources comprenant notamment :

- Le nom de la source.
- Sa catégorie.
- Son adresse.
- Son propriétaire.
- Son type de publication.
- Ses capacités d'acquisition.
- Les formats pris en charge.
- Les informations de connexion nécessaires.
- Son état de disponibilité.
- Les éventuelles restrictions.
- La date de dernière vérification.
- Les dernières informations de découverte.

L'utilisateur doit pouvoir ajouter une source personnalisée.

Il doit également pouvoir modifier sa configuration, désactiver son utilisation ou la supprimer de son catalogue de sources sans supprimer automatiquement les ressources déjà acquises.

Nous voulons aussi pouvoir envisager des connecteurs développés par des tiers ou par notre organisation.

L'ajout d'un nouveau connecteur ne doit pas nécessiter une refonte du fonctionnement général de l'acquisition.

---

# 15. QUALITÉ, FIABILITÉ ET SÉCURITÉ DES ACQUISITIONS

Le système doit accorder une attention particulière à la qualité des ressources importées.

Il ne suffit pas qu'un fichier ait été téléchargé pour considérer l'acquisition comme réussie.

Il faut pouvoir distinguer plusieurs états :

- Ressource découverte.
- Ressource accessible.
- Ressource récupérée.
- Ressource analysée.
- Ressource identifiée.
- Ressource avec dépendances vérifiées.
- Ressource avec métadonnées complètes.
- Ressource partiellement exploitable.
- Ressource prête à être intégrée.
- Ressource nécessitant une intervention.

Il faut également prendre en considération les risques associés aux sources externes.

Les opérations d'acquisition ne doivent pas exécuter automatiquement du code provenant de sources non fiables.

Les archives doivent être inspectées avant extraction et les chemins dangereux doivent être contrôlés.

Les scripts d'installation, hooks de packages, processus de construction et démonstrations doivent être traités avec prudence.

Il faut également prévenir les situations telles que :

- Les archives malveillantes.
- Les fichiers excessivement volumineux.
- Les chemins de fichiers dangereux.
- Les tentatives de traversal.
- Les liens symboliques problématiques.
- Les dépendances compromises.
- Les scripts d'installation dangereux.
- Les contenus contenant des secrets.
- Les fichiers corrompus.
- Les ressources falsifiées.

La plateforme doit pouvoir isoler les opérations risquées et produire des informations de contrôle avant toute exploitation.

---

# 16. EXEMPLES DE SCÉNARIOS D'ACQUISITION ATTENDUS

Les scénarios suivants permettent d'illustrer l'étendue des capacités attendues.

## Scénario A — Importer un composant depuis shadcn/ui

L'utilisateur souhaite récupérer un composant Button.

Il sélectionne la source officielle, recherche le composant, consulte ses informations, identifie ses dépendances, sélectionne une version et procède à son importation.

Le système récupère les fichiers sources et les informations associées.

## Scénario B — Importer un composant depuis une Registry communautaire

L'utilisateur renseigne une Registry externe.

Le système explore son catalogue, identifie les éléments disponibles et permet leur acquisition.

Il doit pouvoir gérer les namespaces et les dépendances entre éléments lorsque la Registry les expose.

## Scénario C — Importer depuis un dépôt GitHub classique

L'utilisateur fournit l'adresse d'un dépôt.

Le système explore l'arborescence, identifie les technologies, analyse les fichiers et présente les ressources potentiellement intéressantes.

L'utilisateur sélectionne uniquement les composants qu'il souhaite récupérer.

## Scénario D — Extraire un composant d'une application existante

L'utilisateur fournit un dépôt contenant une application complète.

Le système identifie les composants, leurs relations et leurs dépendances.

L'utilisateur sélectionne un composant précis et le système prépare une extraction comprenant ses fichiers nécessaires.

## Scénario E — Importer un package npm

L'utilisateur indique le nom d'un package.

Le système consulte les informations disponibles, identifie les versions, les dépendances et les fichiers publiés.

Il détermine si les sources originales sont accessibles et indique précisément ce qui peut être récupéré.

## Scénario F — Importer une archive

L'utilisateur fournit une archive ZIP.

Le système explore son contenu, détecte une éventuelle structure de projet, identifie les ressources et permet une sélection avant importation.

## Scénario G — Importer plusieurs sources simultanément

L'utilisateur souhaite récupérer des composants provenant de plusieurs catalogues.

Le système permet de préparer une opération groupée, de traiter les différentes sources et de présenter un compte rendu global.

## Scénario H — Importer depuis une documentation

L'utilisateur renseigne une documentation qui présente plusieurs composants.

Le système explore les éléments accessibles, identifie les exemples de code disponibles et distingue les véritables sources récupérables des simples démonstrations.

## Scénario I — Ajouter une source personnalisée

L'utilisateur découvre une nouvelle collection de composants qui n'est pas encore prise en charge.

Il doit pouvoir renseigner sa source et, selon ses caractéristiques, procéder à une acquisition assistée ou proposer son intégration comme nouveau connecteur.

## Scénario J — Réimporter une ressource déjà connue

L'utilisateur retrouve une ressource qui existe déjà dans son patrimoine.

Le système identifie les correspondances, les versions et les différences potentielles avant de proposer une nouvelle acquisition.

Il ne doit pas créer aveuglément des doublons.

---

# 17. RÉSULTAT FONCTIONNEL ATTENDU

À l'issue de cette capacité d'acquisition, nous voulons disposer d'un système qui ne dépend pas exclusivement des sources possédant déjà un mécanisme de distribution standardisé.

Nous voulons pouvoir travailler aussi bien avec des sources structurées qu'avec des sources ordinaires.

Le système doit pouvoir découvrir, explorer, sélectionner, récupérer et analyser des ressources provenant de plusieurs plateformes et de plusieurs formats.

Il doit pouvoir travailler avec des composants isolés, des collections, des packages, des dépôts complets, des archives et des projets logiciels existants.

Il doit pouvoir extraire des ressources depuis des environnements plus complexes, en identifier les relations et préparer leur récupération dans des conditions cohérentes.

Il doit pouvoir gérer des opérations individuelles, multiples, assistées et automatisées.

Il doit préserver la provenance, les versions, les licences et les informations nécessaires à une exploitation ultérieure.

Il doit également être suffisamment ouvert pour accueillir de nouveaux fournisseurs et de nouveaux modes d'acquisition.

**Le résultat attendu est une véritable capacité universelle d'acquisition de ressources logicielles, capable de transformer une grande diversité de sources externes en ressources identifiées, documentées, traçables et potentiellement exploitables dans notre patrimoine central.**

---

# 18. CONSIGNES POUR L'ANALYSE ULTÉRIEURE

Cette partie constitue l'expression du besoin relatif à l'acquisition.

Elle ne constitue pas une décision définitive sur les technologies ou les mécanismes d'implémentation.

Il ne faut pas commencer à réduire ces exigences en choisissant immédiatement quelques connecteurs ou quelques formats.

L'analyse ultérieure devra notamment :

1. Identifier toutes les familles de sources possibles.
2. Distinguer les modes d'acquisition.
3. Identifier les possibilités et limitations de chaque mode.
4. Déterminer les besoins de découverte et d'exploration.
5. Identifier les besoins d'analyse des projets.
6. Définir les différents niveaux d'extraction.
7. Identifier les contraintes de dépendances.
8. Prendre en compte les versions et les licences.
9. Identifier les cas d'acquisition partielle ou incomplète.
10. Déterminer les besoins d'automatisation.
11. Identifier les mécanismes de contrôle et de sécurité.
12. Prévoir l'ajout futur de nouvelles sources.

Les capacités présentées ne doivent pas être considérées comme un plafond fonctionnel.

Toute possibilité supplémentaire pertinente pour atteindre l'ambition du produit doit être examinée.

Il faut rechercher l'exhaustivité sans inventer des capacités techniquement ou juridiquement impossibles.

La distinction entre une fonctionnalité réalisable, une fonctionnalité dépendante des possibilités de la source et une fonctionnalité nécessitant une intervention humaine doit être conservée.

**Nous voulons une plateforme qui puisse acquérir presque toute ressource logicielle légalement accessible, quel que soit son lieu de publication ou son mode de présentation, dès lors qu'une méthode d'accès et de récupération techniquement exploitable existe.**
