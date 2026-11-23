# SESSION 3/8 — EXPRESSION EXHAUSTIVE DES BESOINS
# PATRIMOINE LOGICIEL, GESTION INTÉGRALE DES CODES SOURCES, ORGANISATION DES RESSOURCES ET CYCLE DE VIE

---

# 1. OBJECTIF ET IMPORTANCE DU PATRIMOINE LOGICIEL

Cette partie définit les exigences relatives à la conservation, à l'organisation, à la maîtrise et à l'évolution des ressources logicielles acquises par la plateforme.

Nous voulons constituer un patrimoine logiciel centralisé, durable, structuré et exploitable, qui puisse accueillir une quantité importante de ressources provenant de sources différentes et dont les caractéristiques techniques peuvent être très variées.

Ce patrimoine doit devenir le point de référence pour toutes les ressources que la plateforme récupère, crée, personnalise, transforme, compose ou publie.

Il ne doit pas être considéré comme un simple répertoire de fichiers.

Il doit représenter une véritable bibliothèque de ressources logicielles, dans laquelle chaque élément possède une identité, une description, une origine, un contenu, des relations, des versions et un cycle de vie.

Une ressource doit pouvoir être retrouvée, consultée, comprise, comparée, modifiée, dupliquée, transformée, regroupée, publiée et réutilisée indépendamment des conditions dans lesquelles elle a été initialement acquise.

L'utilisateur doit pouvoir retrouver une ressource importée plusieurs mois auparavant, connaître son origine exacte, consulter son code initial, examiner les modifications qui lui ont été apportées, retrouver ses dépendances et identifier les projets dans lesquels elle est utilisée.

Nous voulons également éviter que la plateforme devienne progressivement un ensemble désorganisé de fichiers, de copies et de versions difficiles à distinguer.

La gestion du patrimoine doit donc être pensée dès le départ comme une capacité centrale et particulièrement approfondie.

**Le patrimoine constitue la mémoire technique, documentaire et historique de l'ensemble des ressources gérées par la plateforme.**

---

# 2. DISTINCTION ENTRE LES DIFFÉRENTES NOTIONS DE RESSOURCES

La plateforme doit être capable de distinguer plusieurs niveaux d'organisation.

Il est important de ne pas considérer qu'un composant correspond systématiquement à un fichier ou qu'une collection correspond nécessairement à un ensemble de composants indépendants.

Nous voulons une représentation suffisamment riche pour prendre en charge des structures complexes.

## 2.1. La ressource logicielle

La notion de ressource logicielle constitue la catégorie générale.

Elle peut représenter n'importe quel élément que la plateforme souhaite conserver, exploiter ou distribuer.

Il peut s'agir :

- D'un composant.
- D'un ensemble de composants.
- D'un hook.
- D'une fonction.
- D'un service.
- D'un module.
- D'une bibliothèque.
- D'un template.
- D'un bloc fonctionnel.
- D'un système de design.
- D'un thème.
- D'une collection d'assets.
- D'une configuration.
- D'un ensemble de ressources interdépendantes.
- D'une implémentation destinée à un environnement particulier.

Le système ne doit donc pas limiter sa gestion patrimoniale à une catégorie unique.

## 2.2. Le composant logique

Un composant logique représente une unité fonctionnelle ou visuelle identifiable.

Par exemple, un Button représente une ressource logique, même s'il est constitué de plusieurs fichiers.

Cette identité doit pouvoir être conservée indépendamment de son organisation physique.

Un composant logique peut disposer :

- D'un nom.
- D'un identifiant.
- D'une description.
- D'une catégorie.
- D'une documentation.
- De propriétés.
- De variantes.
- D'une ou plusieurs implémentations.
- De ressources associées.
- De dépendances.
- D'un historique.

## 2.3. L'implémentation

Une implémentation représente une réalisation technique particulière d'une ressource logique.

Par exemple, un même composant Button peut posséder plusieurs implémentations :

- React.
- Vue.
- Angular.
- Svelte.
- Web Components.
- React Native.

Ces implémentations peuvent être indépendantes techniquement tout en représentant une même intention fonctionnelle.

Il faut pouvoir les regrouper sous une identité commune sans prétendre qu'elles partagent automatiquement le même code.

## 2.4. Le fichier source

Un fichier représente une unité physique contenant du code, des styles, une configuration, des données ou une autre ressource.

Un composant peut utiliser plusieurs fichiers.

Un fichier peut également contenir plusieurs composants ou déclarations.

Le système doit pouvoir conserver cette réalité sans imposer une relation systématique d'un fichier pour un composant.

## 2.5. L'ensemble composite

Un ensemble composite représente plusieurs ressources réunies pour constituer une unité plus complexe.

Par exemple :

- Un système de navigation.
- Un tableau de données complet.
- Un formulaire avancé.
- Un tableau de bord.
- Une interface d'authentification.
- Une collection de composants de gestion documentaire.

Il doit être possible de conserver cet ensemble comme une ressource identifiable, tout en maintenant les identités de ses éléments constitutifs.

## 2.6. La collection

Une collection regroupe des ressources selon une logique particulière.

Elle peut être organisée par :

- Catégorie.
- Technologie.
- Fournisseur.
- Domaine fonctionnel.
- Style visuel.
- Utilité.
- Projet.
- Organisation.
- Système de design.
- Préférence personnelle.

Une collection ne doit pas nécessairement posséder les mêmes contraintes qu'un package.

Elle peut simplement représenter un regroupement logique de ressources réutilisables.

---

# 3. CONSTITUTION D'UNE BIBLIOTHÈQUE CENTRALE DE RESSOURCES

Nous voulons disposer d'une bibliothèque centrale dans laquelle toutes les ressources acquises et créées peuvent être conservées.

Cette bibliothèque doit pouvoir accueillir des ressources de différentes origines, technologies, catégories et niveaux de complexité.

Elle doit devenir le point d'entrée principal pour retrouver les éléments disponibles.

## 3.1. Catalogue général

L'utilisateur doit pouvoir consulter un catalogue global de toutes les ressources présentes dans le patrimoine.

Ce catalogue doit présenter les ressources de manière organisée, avec des informations permettant de les identifier rapidement.

Il doit notamment être possible de consulter :

- Le nom de la ressource.
- Son type.
- Sa catégorie.
- Sa description.
- Son origine.
- Son fournisseur.
- Son framework.
- Son langage.
- Sa version.
- Son état.
- Sa date d'acquisition.
- Sa dernière modification.
- Ses éventuelles variantes.
- Ses dépendances principales.
- Ses collections.
- Son statut de publication.

Les informations présentées doivent pouvoir être adaptées selon la catégorie de ressource.

## 3.2. Organisation par catégories

Nous voulons une organisation permettant de distinguer les différentes familles de ressources.

Quelques catégories indicatives :

**Interface et présentation**
- Éléments fondamentaux.
- Navigation.
- Formulaires.
- Tableaux.
- Dialogues.
- Notifications.
- Cartes.
- Graphiques.
- Tableaux de bord.
- Layouts.
- Blocs.
- Pages.
- Templates.

**Logique et programmation**
- Hooks.
- Fonctions.
- Utilitaires.
- Services.
- Modules.
- Adaptateurs.
- Extensions.
- Plugins.
- Bibliothèques.

**Design et ressources graphiques**
- Thèmes.
- Tokens.
- Icônes.
- Illustrations.
- Images.
- Polices.
- Animations.
- Assets.

**Configuration et documentation**
- Configurations.
- Schémas.
- Manifestes.
- Documentation.
- Exemples.
- Instructions.
- Modèles de projets.

Cette classification doit rester extensible.

L'utilisateur doit pouvoir créer de nouvelles catégories et sous-catégories.

## 3.3. Organisation personnalisée

Il ne faut pas imposer une seule organisation à tous les utilisateurs.

La plateforme doit permettre de créer des espaces de classement personnalisés.

Un utilisateur pourrait, par exemple, constituer :

- Une bibliothèque de composants React.
- Une collection de composants administratifs.
- Une collection de composants pour les applications mobiles.
- Une collection de composants de gestion documentaire.
- Une collection de composants graphiques.
- Une collection de ressources issues de shadcn.
- Une collection de composants personnalisés CIVITAS.
- Une collection de ressources prêtes à être publiées.

Ces regroupements ne doivent pas nécessairement déplacer ou dupliquer les ressources physiques.

Une même ressource doit pouvoir appartenir à plusieurs collections.

## 3.4. Espaces de travail et bibliothèques distinctes

Il faut également envisager plusieurs bibliothèques ou espaces de travail.

L'utilisateur peut avoir besoin de séparer :

- Ses ressources personnelles.
- Les ressources d'une organisation.
- Les ressources d'un projet.
- Les ressources expérimentales.
- Les ressources validées.
- Les ressources destinées à une publication.
- Les ressources archivées.

La plateforme doit pouvoir gérer ces différents contextes sans rendre l'utilisation du patrimoine inutilement complexe.

---

# 4. GESTION INTÉGRALE DES CODES SOURCES

La maîtrise des codes sources constitue l'une des exigences les plus importantes du produit.

Nous voulons pouvoir accéder aux véritables fichiers qui constituent les ressources.

La plateforme ne doit pas être limitée à la conservation d'une référence externe, d'un nom de package ou d'un lien vers un dépôt.

Lorsqu'une ressource source est disponible et que son acquisition est autorisée, nous voulons pouvoir en conserver une copie exploitable.

## 4.1. Conservation des fichiers originaux

Lorsqu'une ressource est importée, le système doit pouvoir conserver les fichiers tels qu'ils ont été récupérés.

Il faut préserver autant que possible :

- Le contenu exact des fichiers.
- Leur nom.
- Leur extension.
- Leur organisation.
- Leur structure de répertoires.
- Les informations de version.
- Les fichiers de configuration.
- Les fichiers de styles.
- Les ressources graphiques.
- Les déclarations de types.
- Les documents associés.
- Les notices de licence.
- Les informations de provenance.

Il ne faut pas modifier silencieusement les fichiers originaux lors de leur acquisition.

Si une normalisation, une transformation ou une adaptation est nécessaire, elle doit être identifiable et ne pas détruire la possibilité de retrouver le contenu initial.

## 4.2. Conservation des structures originales

La plateforme doit pouvoir conserver l'organisation d'origine des projets lorsque cela est pertinent.

Par exemple, si un composant est importé depuis :

```text
src/
  components/
    ui/
      button.tsx
      dialog.tsx
  hooks/
    use-mobile.ts
  lib/
    utils.ts
  styles/
    globals.css
```

Il doit être possible de préserver cette structure.

Cependant, la structure originale ne doit pas nécessairement devenir l'organisation définitive du patrimoine.

Nous voulons pouvoir conserver simultanément les informations relatives à l'organisation d'origine et disposer d'une représentation adaptée à la gestion centralisée.

## 4.3. Consultation du code source

L'utilisateur doit pouvoir ouvrir une ressource et consulter ses fichiers directement depuis la plateforme.

Il doit pouvoir :

- Parcourir les fichiers.
- Ouvrir plusieurs fichiers.
- Rechercher du texte.
- Naviguer entre les fichiers.
- Consulter les imports.
- Examiner les déclarations.
- Consulter les types.
- Identifier les exports.
- Visualiser les styles.
- Examiner les configurations.
- Consulter les fichiers associés.

La consultation doit être adaptée à la nature des ressources.

Il ne faut pas limiter cette expérience aux fichiers TypeScript et JavaScript.

## 4.4. Modification directe des fichiers

L'utilisateur doit pouvoir modifier les véritables fichiers sources.

Les opérations attendues comprennent :

- Modification du contenu.
- Création de fichiers.
- Suppression de fichiers.
- Renommage.
- Déplacement.
- Copie.
- Réorganisation.
- Modification des imports.
- Modification des exports.
- Modification des propriétés.
- Modification des types.
- Modification des styles.
- Modification des configurations.

La plateforme doit permettre de travailler sur une ressource comme sur un véritable environnement de développement.

Les modifications doivent pouvoir être sauvegardées, comparées et historisées.

## 4.5. Conservation des fichiers non directement exécutables

Il ne faut pas conserver uniquement les fichiers qui participent directement au rendu d'un composant.

Certains fichiers sont essentiels à sa compréhension, sa maintenance ou sa distribution.

Il faut notamment prendre en charge :

- README.
- LICENSE.
- CHANGELOG.
- package.json.
- tsconfig.json.
- Fichiers de configuration.
- Fichiers de test.
- Fichiers de documentation.
- Fichiers d'exemples.
- Fichiers de démonstration.
- Fichiers de génération.
- Fichiers de styles.
- Fichiers d'assets.

Le système doit pouvoir distinguer les fichiers nécessaires à l'utilisation, ceux nécessaires au développement et ceux qui sont purement documentaires.

---

# 5. SÉPARATION ENTRE SOURCES ORIGINALES, MODIFICATIONS ET VERSIONS PUBLIÉES

Nous ne voulons jamais perdre la possibilité de retrouver l'état initial d'une ressource.

Une ressource importée peut être modifiée plusieurs fois, adaptée à différents projets et distribuée sous plusieurs formes.

Il est donc essentiel de distinguer ses différentes représentations.

## 5.1. Source originale

La source originale correspond au contenu récupéré depuis l'origine.

Elle doit être conservée comme référence historique.

Elle ne doit pas être écrasée par les personnalisations ultérieures.

## 5.2. Copie de travail

La copie de travail représente une version sur laquelle l'utilisateur intervient.

Elle peut contenir des modifications non encore validées.

Elle doit permettre d'expérimenter librement sans compromettre les versions déjà conservées.

## 5.3. Version personnalisée

Une version personnalisée représente une évolution volontaire de la ressource originale.

Elle peut inclure :

- Des modifications visuelles.
- Des modifications structurelles.
- Des modifications fonctionnelles.
- Des corrections.
- Des optimisations.
- Des adaptations technologiques.
- Des dépendances supplémentaires.
- Des fonctionnalités nouvelles.

Elle doit conserver une relation avec la ressource dont elle est issue.

## 5.4. Version publiée

Une version publiée représente une version considérée comme prête à être distribuée.

Elle doit être identifiable et stable.

Il doit être possible de publier plusieurs versions sans écraser les précédentes.

## 5.5. Versions dérivées indépendantes

Il doit également être possible de créer une déclinaison indépendante à partir d'une ressource existante.

Par exemple, un Button issu de shadcn peut être adapté pour un design system interne, tandis qu'une autre déclinaison est créée pour un autre environnement.

Ces évolutions ne doivent pas nécessairement être fusionnées.

Il faut pouvoir maintenir plusieurs directions de développement à partir d'une même origine.

---

# 6. IDENTITÉ, MÉTADONNÉES ET DESCRIPTION DES RESSOURCES

Chaque ressource doit disposer d'informations suffisamment riches pour être identifiée, comprise et exploitée.

Nous voulons dépasser les simples noms de fichiers.

## 6.1. Identité

Une ressource doit pouvoir posséder :

- Un identifiant stable.
- Un nom.
- Un nom technique.
- Un nom d'affichage.
- Une description.
- Une catégorie.
- Des sous-catégories.
- Des mots-clés.
- Des tags.
- Un auteur.
- Un propriétaire.
- Une date de création.
- Une date d'importation.
- Une date de modification.

Il faut pouvoir distinguer son identité interne de son nom d'origine.

Une même ressource peut être renommée dans le patrimoine sans perdre sa correspondance avec la source initiale.

## 6.2. Informations techniques

Les informations techniques doivent notamment comprendre :

- Langage.
- Framework.
- Bibliothèques utilisées.
- Version du framework.
- Environnement cible.
- Gestionnaire de packages.
- Système de styles.
- Outils de construction.
- Points d'entrée.
- Exports.
- Types.
- Dépendances.
- Contraintes de compatibilité.

Ces informations peuvent être détectées automatiquement, renseignées manuellement ou complétées progressivement.

## 6.3. Documentation propre à la ressource

Une ressource doit pouvoir posséder sa propre documentation.

Il faut pouvoir conserver :

- Sa description générale.
- Son objectif.
- Ses cas d'utilisation.
- Ses prérequis.
- Ses propriétés.
- Ses paramètres.
- Ses événements.
- Ses variantes.
- Ses exemples.
- Ses limitations.
- Ses dépendances.
- Ses instructions d'installation.
- Ses instructions de personnalisation.
- Ses notes de maintenance.

Cette documentation doit pouvoir évoluer indépendamment du code, tout en restant associée à la bonne version de la ressource.

## 6.4. Métadonnées personnalisées

L'utilisateur doit pouvoir ajouter des informations complémentaires.

Il ne faut pas enfermer le système dans une structure de métadonnées entièrement prédéfinie.

Il doit être possible de définir des attributs personnalisés adaptés aux besoins d'une organisation ou d'un domaine particulier.

---

# 7. GESTION DES VERSIONS ET DE L'HISTORIQUE

Le versionnement doit être une capacité fondamentale du patrimoine.

Une ressource peut connaître de nombreuses évolutions et il faut pouvoir en comprendre l'histoire.

## 7.1. Historique complet

Le système doit pouvoir enregistrer les opérations importantes :

- Création.
- Importation.
- Modification.
- Ajout de fichier.
- Suppression de fichier.
- Renommage.
- Déplacement.
- Modification de métadonnées.
- Modification des dépendances.
- Création de variante.
- Duplication.
- Publication.
- Archivage.
- Restauration.
- Synchronisation avec la source.

Chaque opération doit pouvoir être associée à son contexte et, lorsque pertinent, à son auteur.

## 7.2. Comparaison de versions

L'utilisateur doit pouvoir comparer deux versions d'une même ressource.

La comparaison doit pouvoir concerner :

- Le contenu des fichiers.
- Les fichiers ajoutés.
- Les fichiers supprimés.
- Les fichiers modifiés.
- Les changements de structure.
- Les dépendances.
- Les métadonnées.
- Les configurations.
- Les propriétés.
- Les interfaces publiques.

Il doit être possible d'identifier précisément ce qui a changé.

## 7.3. Historique des modifications du code

Nous voulons une expérience de comparaison adaptée aux fichiers sources.

Elle doit permettre de visualiser les différences entre deux états.

Il doit être possible de consulter les modifications ligne par ligne, de retrouver l'état précédent d'un fichier et de restaurer une version lorsque nécessaire.

## 7.4. Branches et évolutions parallèles

Le système doit pouvoir envisager plusieurs évolutions parallèles d'une même ressource.

Par exemple :

- Une branche expérimentale.
- Une branche de personnalisation.
- Une branche de maintenance.
- Une branche destinée à une version particulière d'un projet.

L'utilisateur doit pouvoir travailler sur une évolution sans perturber une autre.

## 7.5. Restauration

Il doit être possible de restaurer :

- Un fichier.
- Un ensemble de fichiers.
- Une version complète.
- Des métadonnées.
- Une configuration.
- Une variante.
- Une publication précédente.

La restauration doit être traçable et ne pas effacer silencieusement l'historique des opérations précédentes.

## 7.6. Versionnement sémantique

La plateforme doit pouvoir prendre en charge les conventions de versionnement courantes, notamment Semantic Versioning.

Elle doit pouvoir distinguer les évolutions correctives, les évolutions fonctionnelles et les changements susceptibles de casser la compatibilité.

Il faut cependant éviter d'imposer une numérotation sémantique à toutes les ressources, notamment aux fichiers ou aux ressources qui possèdent leur propre logique de versionnement.

---

# 8. GESTION DES VARIANTES ET DES DÉCLINAISONS

Une ressource peut exister sous plusieurs formes.

Nous voulons pouvoir gérer ces différences sans multiplier artificiellement les composants indépendants.

## 8.1. Variantes visuelles

Un composant peut posséder différentes présentations.

Exemples :

- Bouton primaire.
- Bouton secondaire.
- Bouton destructif.
- Bouton fantôme.
- Bouton avec icône.
- Bouton compact.
- Bouton pleine largeur.

Il doit être possible de conserver ces variantes et leurs caractéristiques.

## 8.2. Variantes fonctionnelles

Un composant peut posséder plusieurs comportements.

Par exemple :

- Un menu simple.
- Un menu avec recherche.
- Un menu avec sélection multiple.
- Un menu avec chargement dynamique.

Ces variantes doivent être identifiables et documentées.

## 8.3. Variantes technologiques

Une même ressource logique peut posséder des implémentations destinées à différents frameworks.

Il faut pouvoir les associer sans confondre leurs fichiers sources ou leurs dépendances.

## 8.4. Variantes propres à un environnement

Un composant peut également posséder des adaptations destinées à différents contextes.

Par exemple :

- Interface desktop.
- Interface mobile.
- Interface tactile.
- Interface destinée à un environnement administratif.
- Interface destinée à un environnement public.

Ces adaptations doivent pouvoir être conservées et sélectionnées selon le contexte d'utilisation.

## 8.5. Gestion des relations entre variantes

Le système doit pouvoir identifier :

- La variante principale.
- Les variantes secondaires.
- La variante expérimentale.
- La variante stable.
- La variante abandonnée.
- Les variantes dérivées.
- Les variantes partageant une origine commune.

L'utilisateur doit pouvoir créer, modifier, dupliquer, comparer et supprimer des variantes selon les règles de gestion applicables.

---

# 9. GESTION DES DÉPENDANCES ET DES RELATIONS INTERNES

Le patrimoine doit être capable de représenter les relations entre les ressources.

Nous voulons éviter une bibliothèque dans laquelle les composants sont conservés comme des éléments indépendants sans compréhension de leurs relations.

## 9.1. Relations entre composants

Il doit être possible de savoir qu'un composant utilise un autre composant.

Exemple :

Un DataTable peut utiliser :

- Button.
- Checkbox.
- DropdownMenu.
- Pagination.
- Input.
- Tooltip.

Ces relations doivent pouvoir être consultées.

## 9.2. Dépendances entre fichiers

Le système doit également connaître les relations entre les fichiers qui constituent une ressource.

Par exemple :

- Un fichier principal importe un hook.
- Le hook utilise un utilitaire.
- Le composant importe une feuille de style.
- La feuille de style utilise des variables.
- Une configuration déclare un alias de chemin.

Ces relations doivent être conservées lorsque les informations sont disponibles.

## 9.3. Dépendances externes

Il faut conserver les relations avec les packages et bibliothèques externes.

Le système doit pouvoir identifier les versions utilisées et les contraintes associées.

## 9.4. Graphe de dépendances

Nous voulons pouvoir disposer d'une représentation globale des dépendances.

L'utilisateur doit pouvoir explorer les relations d'une ressource et comprendre les conséquences de sa modification.

Il doit être possible d'identifier :

- Les ressources utilisées par un composant.
- Les ressources qui utilisent un composant.
- Les dépendances directes.
- Les dépendances indirectes.
- Les dépendances partagées.
- Les dépendances optionnelles.
- Les dépendances manquantes.
- Les dépendances incompatibles.

## 9.5. Gestion des impacts

Lorsqu'une ressource est modifiée, la plateforme doit pouvoir identifier les autres ressources potentiellement affectées.

Par exemple, une modification de l'API d'un composant Button peut affecter plusieurs composants composites qui l'utilisent.

Le système doit pouvoir signaler ces impacts avant qu'une évolution soit publiée.

## 9.6. Gestion des cycles et des relations complexes

Il faut également pouvoir représenter les situations dans lesquelles des dépendances forment des relations complexes.

Le système doit pouvoir identifier les cycles éventuels et distinguer les relations réellement nécessaires de celles qui sont simplement documentaires ou organisationnelles.

---

# 10. DÉTECTION DES DOUBLONS ET GESTION DES IDENTITÉS

Le patrimoine peut progressivement accueillir plusieurs ressources similaires provenant de sources différentes.

Il faut donc éviter les duplications incontrôlées.

## 10.1. Détection des doublons exacts

Le système doit pouvoir identifier des fichiers ou des ressources dont le contenu est strictement identique.

Il doit pouvoir comparer leurs empreintes et identifier les correspondances.

## 10.2. Détection des ressemblances

Il doit également pouvoir identifier des ressources similaires sans supposer qu'elles sont identiques.

Par exemple, deux composants Button peuvent avoir une structure très proche mais des comportements ou des propriétés différents.

La plateforme doit pouvoir présenter ces correspondances comme des similarités, et non comme des doublons certains.

## 10.3. Origines multiples

Une ressource similaire peut exister dans plusieurs sources.

Il doit être possible de conserver les différentes origines et de comparer leurs versions.

## 10.4. Regroupement des ressources apparentées

L'utilisateur doit pouvoir associer plusieurs ressources comme variantes, forks, adaptations ou alternatives.

Il ne faut pas supprimer automatiquement une ressource au motif qu'une autre lui ressemble.

## 10.5. Réutilisation contrôlée

Lorsque deux ressources possèdent réellement un contenu commun, le système peut proposer une mutualisation ou une référence partagée.

Cette opération doit cependant préserver l'intégrité des ressources et éviter de créer des dépendances cachées.

---

# 11. GESTION DES LICENCES ET DE LA TRAÇABILITÉ DANS LE PATRIMOINE

Les informations de provenance et de licence doivent rester attachées aux ressources pendant toute leur durée de vie.

Elles ne doivent pas disparaître lorsque l'utilisateur renomme, modifie, déplace ou publie un composant.

## 11.1. Conservation des informations d'origine

Chaque ressource doit conserver son origine et les informations disponibles sur son auteur.

Il faut pouvoir retrouver la source initiale même après plusieurs transformations.

## 11.2. Historique des dérivations

Lorsqu'une ressource est créée à partir d'une autre, le système doit pouvoir représenter cette relation.

Exemple :

- Composant initial provenant de shadcn.
- Première personnalisation.
- Nouvelle variante.
- Adaptation pour un projet.
- Version publiée dans une collection interne.

Il doit être possible de remonter cette chaîne.

## 11.3. Gestion des licences héritées

Les transformations ne doivent pas entraîner la perte des obligations de licence applicables.

Le système doit pouvoir conserver les notices et informations nécessaires à chaque dérivation.

## 11.4. Ressources composites

Un ensemble composite peut contenir plusieurs composants provenant de sources différentes.

Il faut pouvoir conserver les informations de provenance de chaque élément constitutif.

La licence de l'ensemble ne doit pas être considérée comme remplaçant automatiquement les licences des composants qui le constituent.

## 11.5. Publication et redistribution

Avant une publication, le système doit pouvoir examiner les ressources concernées et présenter les informations relatives à leurs licences.

Il doit signaler les incompatibilités et les situations nécessitant une vérification.

---

# 12. GESTION DES ASSETS ET DES RESSOURCES ASSOCIÉES

La plateforme ne doit pas séparer artificiellement les composants de leurs ressources complémentaires.

Un composant peut dépendre de plusieurs éléments qui ne sont pas du code source au sens strict.

Il faut donc pouvoir gérer un patrimoine d'assets.

## 12.1. Ressources graphiques

- Images.
- Illustrations.
- Icônes.
- Fichiers SVG.
- Logos.
- Arrière-plans.
- Textures.
- Ressources vectorielles.

## 12.2. Ressources typographiques

- Polices.
- Familles typographiques.
- Variantes de graisse.
- Fichiers de fontes.
- Configurations typographiques.

## 12.3. Ressources animées

- Animations CSS.
- Fichiers Lottie.
- Animations SVG.
- Vidéos de démonstration.
- Ressources interactives.
- Autres formats compatibles.

## 12.4. Ressources de style

- CSS.
- SCSS.
- Variables.
- Tokens.
- Thèmes.
- Presets.
- Configurations de design.

## 12.5. Gestion des relations entre assets et composants

Un composant doit pouvoir référencer ses ressources complémentaires.

Il faut pouvoir identifier les assets nécessaires, optionnels ou utilisés uniquement dans des exemples.

La plateforme doit également permettre de visualiser les assets associés à une ressource.

---

# 13. GESTION DES COLLECTIONS ET DES ENSEMBLES DE RESSOURCES

Nous voulons pouvoir constituer des bibliothèques cohérentes.

Une collection peut représenter une sélection de ressources qui répondent à un objectif particulier.

## 13.1. Collections thématiques

Exemples :

- Collection de composants administratifs.
- Collection de composants de navigation.
- Collection de formulaires.
- Collection de graphiques.
- Collection de composants d'IA.
- Collection de composants mobiles.
- Collection de ressources de gestion documentaire.

## 13.2. Collections technologiques

Exemples :

- Collection React.
- Collection Vue.
- Collection Angular.
- Collection Next.js.
- Collection React Native.
- Collection CSS.
- Collection de ressources multiplateformes.

## 13.3. Collections de fournisseurs

Il doit être possible de regrouper les ressources selon leur origine.

Exemples :

- Collection shadcn.
- Collection Aceternity.
- Collection Magic UI.
- Collection communautaire.
- Collection CIVITAS.

## 13.4. Collections personnalisées

L'utilisateur doit pouvoir créer ses propres collections et y associer des ressources provenant de plusieurs sources.

Une collection ne doit pas obligatoirement être homogène sur le plan technologique.

## 13.5. Collections versionnées

Il doit être possible de publier une collection comme un ensemble cohérent.

Une collection peut posséder ses propres versions et conserver les références exactes aux versions de ses composants.

Il faut éviter qu'une mise à jour individuelle d'un composant modifie silencieusement une collection déjà publiée.

---

# 14. GESTION DU CYCLE DE VIE DES RESSOURCES

Chaque ressource doit pouvoir suivre un cycle de vie identifiable.

Il ne faut pas supposer qu'une ressource importée est immédiatement prête à être distribuée.

Nous voulons pouvoir distinguer différents états.

## 14.1. Ressource nouvellement acquise

La ressource vient d'être récupérée.

Elle doit pouvoir être examinée et analysée.

## 14.2. Ressource en cours de vérification

Des informations peuvent manquer ou nécessiter une intervention.

La ressource peut être conservée sans être considérée comme pleinement exploitable.

## 14.3. Ressource validée

Les informations essentielles ont été examinées et les conditions d'exploitation ont été suffisamment vérifiées pour son usage prévu.

## 14.4. Ressource en personnalisation

La ressource fait l'objet de modifications.

Elle peut comporter des évolutions non encore publiées.

## 14.5. Ressource expérimentale

Une ressource peut être utilisée à titre expérimental.

Il doit être possible de conserver des versions instables sans les confondre avec les versions validées.

## 14.6. Ressource publiée

Une version a été rendue disponible à travers un mécanisme de distribution.

## 14.7. Ressource dépréciée

Une ressource peut ne plus être recommandée.

Elle doit rester consultable pour les projets qui l'utilisent encore.

## 14.8. Ressource archivée

Une ressource peut être conservée sans être activement utilisée.

L'archivage ne doit pas entraîner la perte de ses informations historiques.

## 14.9. Ressource abandonnée

Une ressource peut être définitivement abandonnée par son propriétaire ou son responsable.

Il faut pouvoir conserver les informations nécessaires à sa traçabilité et aux projets qui en dépendent.

Les différents états doivent être configurables et suffisamment souples pour s'adapter aux besoins du produit.

---

# 15. SYNCHRONISATION AVEC LES SOURCES D'ORIGINE

Une ressource acquise peut continuer à évoluer sur sa source initiale.

La plateforme doit pouvoir détecter ces évolutions et permettre leur prise en compte.

## 15.1. Surveillance des sources

Il doit être possible de vérifier périodiquement si une ressource a connu de nouvelles versions.

Les vérifications peuvent concerner :

- Les releases.
- Les tags.
- Les commits.
- Les branches.
- Les versions de packages.
- Les versions de Registries.

## 15.2. Détection des modifications

Lorsque la source originale évolue, la plateforme doit pouvoir identifier les changements.

Elle doit pouvoir comparer la nouvelle version avec celle initialement acquise.

## 15.3. Présentation des mises à jour

L'utilisateur doit pouvoir consulter :

- Les nouveaux fichiers.
- Les fichiers modifiés.
- Les fichiers supprimés.
- Les modifications de dépendances.
- Les modifications de métadonnées.
- Les changements de licence lorsqu'ils sont détectables.
- Les évolutions de compatibilité.

## 15.4. Mise à jour sans perte des personnalisations

C'est une exigence majeure.

Une ressource personnalisée ne doit pas être écrasée automatiquement par une nouvelle version de sa source originale.

Le système doit pouvoir distinguer les modifications d'origine et les modifications locales.

Il doit pouvoir proposer une comparaison et, lorsque cela est possible, une fusion assistée.

## 15.5. Fusion des évolutions

L'utilisateur doit pouvoir examiner les changements et décider :

- De conserver sa version.
- D'adopter la version originale.
- De fusionner les modifications.
- De récupérer certains changements uniquement.
- De créer une nouvelle variante.
- De conserver les deux évolutions séparément.

Il faut prendre en compte les conflits de code et les conflits de métadonnées.

---

# 16. RECHERCHE ET EXPLORATION DU PATRIMOINE

Le patrimoine doit pouvoir être exploré efficacement même lorsqu'il contient un très grand nombre de ressources.

Nous voulons disposer de capacités de recherche approfondies.

## 16.1. Recherche générale

L'utilisateur doit pouvoir rechercher par :

- Nom.
- Description.
- Catégorie.
- Tags.
- Technologie.
- Framework.
- Langage.
- Fournisseur.
- Auteur.
- Version.
- Origine.
- Date.
- État.

## 16.2. Recherche technique

Il doit également être possible de rechercher des ressources selon leurs caractéristiques techniques.

Par exemple :

- Tous les composants React utilisant Tailwind CSS.
- Tous les composants utilisant Radix UI.
- Tous les composants possédant une variante sombre.
- Toutes les ressources utilisant une dépendance particulière.
- Tous les composants compatibles avec une version donnée d'un framework.

## 16.3. Recherche dans les codes sources

Nous voulons pouvoir rechercher du contenu directement dans les fichiers.

Cela peut inclure :

- Des noms de fonctions.
- Des noms de composants.
- Des propriétés.
- Des classes CSS.
- Des imports.
- Des exports.
- Des types.
- Des variables.
- Des chaînes de caractères.

Il doit être possible de retrouver une ressource à partir d'un élément présent dans son code.

## 16.4. Recherche sémantique

Il faut également envisager une recherche fondée sur la signification et l'utilité des ressources.

Par exemple, l'utilisateur pourrait rechercher :

« Un composant de sélection de fichiers avec aperçu des images et possibilité de supprimer les éléments sélectionnés. »

Le système devrait pouvoir identifier des ressources qui répondent à cette intention, même si leur nom technique ne contient pas ces termes.

## 16.5. Filtres combinés

Les filtres doivent pouvoir être combinés.

L'utilisateur doit pouvoir affiner les résultats selon plusieurs critères simultanément.

Il doit également pouvoir enregistrer des recherches et retrouver ses critères favoris.

---

# 17. INTÉGRITÉ, QUALITÉ ET VALIDATION DU PATRIMOINE

Le patrimoine doit rester fiable dans le temps.

Nous voulons éviter les ressources dont le contenu est incomplet, incohérent ou difficile à exploiter.

## 17.1. Intégrité des fichiers

Le système doit pouvoir vérifier que les fichiers conservés sont intègres.

Il doit notamment pouvoir détecter les corruptions, les fichiers manquants et les modifications inattendues.

## 17.2. Cohérence des ressources

Il doit pouvoir signaler :

- Les références manquantes.
- Les dépendances absentes.
- Les fichiers orphelins.
- Les exports introuvables.
- Les imports non résolus.
- Les ressources incompatibles.
- Les configurations manquantes.
- Les métadonnées incohérentes.

## 17.3. Validation technique

Il faut pouvoir effectuer des contrôles adaptés aux ressources.

Selon leur nature, cela peut inclure :

- Vérification syntaxique.
- Vérification des types.
- Vérification des imports.
- Vérification des dépendances.
- Vérification de compilation.
- Vérification des configurations.
- Exécution de tests.
- Contrôle des ressources associées.

Il ne faut pas imposer une compilation à des ressources qui ne sont pas destinées à être compilées individuellement.

## 17.4. Contrôle de qualité

Le système doit pouvoir présenter des indicateurs de qualité et signaler les problèmes connus.

Il doit distinguer les contrôles effectués, les contrôles non applicables et les contrôles qui n'ont pas pu être exécutés.

## 17.5. Conservation de l'intégrité historique

Les contrôles et modifications ne doivent pas détruire les états historiques.

Il doit être possible de retrouver les contenus précédemment conservés.

---

# 18. GESTION DES PROJETS QUI UTILISENT LES RESSOURCES

Une ressource du patrimoine peut être utilisée dans plusieurs projets.

Nous voulons pouvoir connaître les utilisations et les dépendances externes.

Il doit être possible d'associer une ressource à un ou plusieurs projets consommateurs.

Pour chaque utilisation, la plateforme devrait pouvoir conserver, lorsque les informations sont disponibles :

- Le projet concerné.
- La ressource utilisée.
- La version utilisée.
- La variante utilisée.
- La date d'intégration.
- Le mode de distribution.
- Les dépendances associées.
- Les éventuelles personnalisations locales.
- Les informations de compatibilité.

Cette connaissance doit permettre d'identifier les conséquences d'une évolution.

Par exemple, si un composant Button est utilisé dans cinq projets, une modification importante de son API doit pouvoir déclencher une information sur les projets potentiellement concernés.

Il faut également pouvoir identifier les projets qui utilisent une version ancienne ou une variante dépréciée.

La plateforme doit pouvoir présenter ces relations sans prétendre contrôler automatiquement des projets externes dont elle ne connaît pas l'état réel.

---

# 19. GESTION DES ESPACES, DES PROPRIÉTAIRES ET DES RESPONSABILITÉS

Le patrimoine peut être utilisé par une personne seule, une équipe ou une organisation.

Il faut donc envisager plusieurs contextes de propriété et de responsabilité.

Une ressource peut appartenir :

- À un utilisateur.
- À une équipe.
- À une organisation.
- À un espace de travail.
- À un projet.
- À une collection administrée.

Le système doit pouvoir distinguer :

- Le créateur de la ressource.
- Son importateur.
- Son propriétaire interne.
- Son responsable de maintenance.
- Ses contributeurs.
- Ses validateurs.
- Ses utilisateurs.

Il faut également pouvoir gérer des droits différents selon les opérations.

Par exemple :

- Consultation.
- Téléchargement.
- Modification.
- Duplication.
- Création de variantes.
- Validation.
- Publication.
- Archivage.
- Administration.

Une organisation doit pouvoir contrôler son patrimoine sans empêcher l'utilisation de ressources publiques auxquelles ses membres ont légalement accès.

---

# 20. GESTION DES NOTES, COMMENTAIRES ET DOCUMENTATION COLLABORATIVE

Le patrimoine doit également pouvoir conserver des informations humaines relatives aux ressources.

Il peut s'agir de :

- Notes techniques.
- Commentaires.
- Instructions particulières.
- Décisions de personnalisation.
- Informations de maintenance.
- Avertissements.
- Retours d'expérience.
- Suggestions d'amélioration.
- Informations de compatibilité.
- Historique de validation.

Il doit être possible d'associer ces informations à une ressource, une version, un fichier ou une modification précise.

Dans un contexte collaboratif, les membres doivent pouvoir discuter d'une ressource et documenter les décisions prises.

---

# 21. EXPORTATION ET SAUVEGARDE DU PATRIMOINE

La plateforme ne doit pas enfermer les ressources dans son propre environnement.

Nous voulons pouvoir récupérer les données et les fichiers qui constituent le patrimoine.

Il faut prévoir des possibilités d'exportation.

L'utilisateur doit pouvoir exporter :

- Une ressource individuelle.
- Plusieurs ressources.
- Une collection.
- Un ensemble composite.
- Une version précise.
- Les fichiers originaux.
- Les fichiers personnalisés.
- Les métadonnées.
- Les informations de provenance.
- Les informations de dépendances.
- La documentation.
- Les historiques lorsque le format le permet.

Les formats d'exportation doivent être adaptés à la nature des ressources.

Il faut également envisager la sauvegarde et la restauration de bibliothèques complètes.

La plateforme doit pouvoir préserver la cohérence entre les fichiers, les métadonnées et les relations.

L'utilisateur doit pouvoir récupérer son patrimoine dans des formats exploitables sans dépendre exclusivement de l'interface de la plateforme.

---

# 22. ÉVOLUTIVITÉ ET CROISSANCE DU PATRIMOINE

Nous voulons que le patrimoine puisse grandir considérablement sans devenir difficile à administrer.

La plateforme doit envisager la gestion :

- De quelques composants.
- De milliers de composants.
- De dizaines de milliers de ressources.
- De nombreuses collections.
- De plusieurs implémentations par ressource.
- De multiples versions.
- De nombreux fichiers associés.
- De ressources provenant de centaines de sources.

Il faut prendre en considération les volumes, les opérations de recherche, les comparaisons, les relations et les sauvegardes.

La croissance du patrimoine ne doit pas obliger l'utilisateur à changer complètement ses habitudes d'organisation.

Il faut pouvoir conserver une expérience claire et exploitable malgré l'augmentation du nombre de ressources.

---

# 23. SCÉNARIOS D'UTILISATION DU PATRIMOINE

## Scénario A — Retrouver une ressource ancienne

L'utilisateur souhaite retrouver un composant importé plusieurs mois auparavant.

Il effectue une recherche, retrouve la ressource, consulte son origine, sa version et ses fichiers.

Il peut retrouver l'état exact de la ressource au moment de son acquisition.

## Scénario B — Personnaliser une ressource sans perdre l'original

L'utilisateur importe un composant depuis shadcn.

Il crée une copie de travail, modifie son apparence et son comportement, puis conserve une version personnalisée.

La source originale reste accessible.

## Scénario C — Maintenir plusieurs variantes

L'utilisateur crée trois déclinaisons d'un même composant.

Une version est destinée à une application administrative, une autre à une interface publique et une troisième à une application mobile.

Il peut les gérer indépendamment tout en conservant leur origine commune.

## Scénario D — Identifier les dépendances d'un composant

L'utilisateur ouvre un composant complexe.

Il consulte les ressources utilisées, les fichiers associés, les dépendances externes et les autres composants qui en dépendent.

## Scénario E — Comparer une version personnalisée avec sa source

La source d'origine publie une nouvelle version.

L'utilisateur souhaite savoir ce qui a changé et si ces évolutions peuvent être intégrées dans sa version personnalisée.

Le système présente les différences et les conflits éventuels.

## Scénario F — Créer une collection cohérente

L'utilisateur constitue une collection de composants administratifs provenant de plusieurs sources.

Il organise les ressources, ajoute des descriptions, identifie les variantes et prépare une collection destinée à être publiée.

## Scénario G — Identifier l'impact d'une modification

L'utilisateur modifie une ressource utilisée dans plusieurs ensembles composites.

Le système identifie les relations connues et signale les éléments potentiellement affectés.

## Scénario H — Restaurer une version précédente

Une modification récente provoque une régression.

L'utilisateur consulte l'historique et restaure la version antérieure.

L'opération est enregistrée sans supprimer l'historique.

## Scénario I — Exporter une collection complète

L'utilisateur souhaite utiliser son patrimoine en dehors de la plateforme.

Il sélectionne une collection et exporte ses ressources, leurs fichiers, leurs métadonnées et les informations nécessaires à leur réutilisation.

## Scénario J — Identifier les ressources similaires

L'utilisateur recherche un composant de navigation.

La plateforme présente plusieurs ressources similaires provenant de sources différentes, leurs différences techniques et leurs variantes.

L'utilisateur peut les comparer et décider de conserver plusieurs alternatives.

---

# 24. RÉSULTAT GLOBAL ATTENDU

À l'issue de cette partie, nous voulons disposer d'une vision complète de ce que doit représenter le patrimoine logiciel de la plateforme.

Ce patrimoine doit permettre de conserver bien plus que des fichiers.

Il doit préserver les identités des ressources, leurs structures, leurs origines, leurs différentes implémentations, leurs dépendances, leurs variantes, leurs versions, leurs relations et leur historique.

Il doit permettre une véritable maîtrise des codes sources, sans imposer de dépendance permanente à la source d'origine.

Il doit être possible de consulter et modifier les ressources, de créer plusieurs évolutions parallèles, de comparer des versions, de restaurer des états précédents et de synchroniser les personnalisations avec les évolutions des sources externes.

Il doit également être possible de constituer des collections cohérentes, de rechercher des ressources avec des critères avancés, d'identifier les impacts d'une modification et de connaître les projets qui utilisent les ressources lorsque ces informations sont disponibles.

Enfin, l'ensemble du patrimoine doit rester exportable, traçable et exploitable indépendamment de l'interface de gestion.

**Nous voulons un véritable système de gestion du patrimoine logiciel, capable de préserver et de valoriser durablement l'ensemble des ressources acquises, créées et transformées par la plateforme.**

---

# 25. CONSIGNES POUR L'ANALYSE ET LA CONCEPTION ULTÉRIEURES

Cette partie ne doit pas être réduite à un simple système de fichiers, à une base de données de composants ou à un historique rudimentaire.

L'analyse ultérieure devra examiner en profondeur :

1. Les différentes identités des ressources.
2. La distinction entre composants, implémentations, fichiers et ensembles composites.
3. La conservation des sources originales.
4. La gestion des copies de travail.
5. Les versions personnalisées et publiées.
6. Les variantes et les déclinaisons.
7. Les dépendances internes et externes.
8. Les relations entre les ressources.
9. La gestion des doublons et des similarités.
10. La gestion des licences et de la provenance.
11. La synchronisation avec les sources d'origine.
12. La gestion des conflits.
13. La recherche dans les métadonnées et les codes sources.
14. La recherche sémantique.
15. La gestion des assets.
16. Les collections et ensembles composites.
17. Le cycle de vie des ressources.
18. La validation et l'intégrité.
19. Les relations avec les projets consommateurs.
20. Les droits de gestion et les responsabilités.
21. La sauvegarde et l'exportation.
22. La croissance du patrimoine.

Il faudra également identifier les cas particuliers qui n'ont pas été explicitement cités.

Ne pas supposer qu'une ressource possède toujours un seul auteur, une seule origine, un seul langage, un seul fichier ou une seule version.

Ne pas supposer qu'une personnalisation doit obligatoirement rester liée à sa source d'origine.

Ne pas supposer qu'une collection doit être constituée de ressources homogènes.

Ne pas confondre une variante, une version, une implémentation et une copie.

Ne pas imposer une structure de fichiers universelle à toutes les ressources.

Ne pas perdre la possibilité de retrouver les sources originales et les états historiques.

Ne pas réduire la gestion des dépendances à une simple liste de packages.

Enfin, il faut veiller à ce que le patrimoine puisse être exploité aussi bien par l'utilisateur humain que par les mécanismes automatisés de la plateforme.

**Le niveau d'exigence attendu est celui d'un patrimoine logiciel professionnel, durable, extensible, traçable et suffisamment complet pour devenir la base de travail de nombreux projets indépendants.**
