# **SESSION 6/8 — Distribution, publication, installation, intégration et consommation des ressources logicielles**

Cette session définit les exigences relatives à la mise à disposition, à la publication, à la distribution, à l'installation et à l'exploitation des ressources logicielles constituant le patrimoine de la plateforme.

Elle constitue le prolongement naturel des sessions précédentes. Après avoir défini les besoins concernant l'acquisition de ressources provenant de plusieurs sources, leur organisation, la maîtrise de leurs codes sources, leur personnalisation, leur création, leur prévisualisation et leur validation, il faut maintenant déterminer comment ces ressources pourront être utilisées concrètement en dehors de leur espace de gestion.

L'objectif est de permettre à une ressource de dépasser son environnement de création et de devenir un élément exploitable dans différents projets, applications, bibliothèques, environnements de développement et contextes de distribution.

La plateforme ne doit donc pas seulement permettre de stocker des composants, de modifier leur code source ou de les présenter dans un catalogue. Elle doit également permettre de les rendre disponibles selon différents modes de consommation, tout en préservant leur identité, leur provenance, leur historique, leurs conditions d'utilisation, leurs dépendances et leurs possibilités d'évolution.

Il faut notamment répondre à une distinction fondamentale : **gérer une ressource dans un patrimoine logiciel et distribuer cette ressource pour qu'elle soit utilisée dans un autre environnement sont deux responsabilités différentes, mais étroitement liées.**

Une ressource peut être conservée dans une bibliothèque interne sans être publiée. Elle peut être publiée dans un registre privé sans être accessible publiquement. Elle peut être distribuée sous forme de code source, de paquet installable, de collection ou de bibliothèque complète. Elle peut également être rendue disponible à travers un mécanisme de récupération et d'intégration directe dans un projet.

Ces possibilités ne doivent pas être confondues.

La plateforme doit permettre de choisir le mode de mise à disposition correspondant à la nature de la ressource, à sa destination, aux droits associés et aux besoins de ses utilisateurs.

Elle doit également garantir que les ressources distribuées restent maîtrisables. Une modification apportée à une ressource dans son environnement d'origine ne doit pas nécessairement modifier immédiatement toutes les copies déjà utilisées dans les projets consommateurs. De même, une mise à jour disponible ne doit pas être assimilée à une mise à jour automatiquement appliquée.

La distribution doit ainsi préserver l'équilibre entre disponibilité, autonomie, contrôle des versions, liberté de personnalisation et maîtrise des évolutions.

## **1. Un système de distribution indépendant de l'environnement de création**

La plateforme doit être capable de gérer la distribution des ressources sans rendre leur utilisation dépendante de l'interface de gestion dans laquelle elles ont été créées ou personnalisées.

Un utilisateur doit pouvoir créer une ressource, la valider, la publier et l'exploiter dans un autre projet sans devoir obligatoirement conserver un lien permanent avec l'environnement de création.

Cette indépendance est importante pour plusieurs raisons.

Premièrement, une ressource peut être destinée à un projet qui utilise ses propres outils, son propre environnement de développement et ses propres mécanismes de gestion des dépendances.

Deuxièmement, les utilisateurs doivent pouvoir conserver le code source et les fichiers nécessaires à l'exploitation de leurs ressources, même lorsqu'ils ne travaillent plus directement dans la plateforme.

Troisièmement, la distribution doit pouvoir s'adapter à plusieurs modes de consommation, sans imposer un modèle unique à toutes les ressources.

La plateforme doit donc permettre de distinguer clairement :

- Le patrimoine interne de ressources.
- Les ressources préparées pour une distribution.
- Les ressources effectivement publiées.
- Les ressources disponibles dans un catalogue.
- Les ressources installables.
- Les ressources récupérables sous forme de code source.
- Les ressources intégrables dans un projet.
- Les ressources distribuées à des utilisateurs ou organisations.
- Les versions effectivement consommées.
- Les versions qui ne sont plus recommandées ou qui ne sont plus maintenues.

Cette distinction doit être conservée dans l'ensemble du cycle de distribution.

### **1.1. Distribution sans dépendance obligatoire à la plateforme**

Une ressource distribuée doit pouvoir être utilisée indépendamment de la plateforme lorsque sa nature et ses conditions d'utilisation le permettent.

Par exemple, un composant créé dans la plateforme doit pouvoir être récupéré sous forme de fichiers sources et intégré dans un projet externe.

L'utilisateur ne doit pas être obligé de consulter continuellement la plateforme pour que le composant continue de fonctionner.

Il faut donc permettre la récupération des éléments nécessaires à l'utilisation de la ressource :

- Fichiers sources.
- Fichiers de configuration.
- Styles.
- Assets.
- Définitions de types.
- Informations sur les dépendances.
- Métadonnées nécessaires.
- Documentation.
- Exemples d'utilisation.
- Informations de version.
- Informations de licence.

La plateforme doit éviter de créer une dépendance artificielle entre les ressources distribuées et son propre environnement de gestion.

### **1.2. Plusieurs modes de distribution pour une même ressource**

Une même ressource peut nécessiter plusieurs formes de distribution.

Un composant peut, par exemple, être distribué sous forme de code source directement récupérable, mais également sous forme de paquet installable lorsque cela est pertinent.

Une collection peut être proposée comme ensemble de ressources indépendantes, ou comme un ensemble destiné à être récupéré en une seule opération.

Une bibliothèque peut être distribuée comme un ensemble structuré de fichiers ou comme un paquet versionné.

Il faut donc permettre à une même ressource de disposer de plusieurs modalités de distribution, sans créer artificiellement plusieurs identités pour ce qui constitue fondamentalement la même ressource.

Les différentes modalités doivent rester liées à l'identité de la ressource, à ses versions et à ses conditions d'utilisation.

### **1.3. Distribution adaptée à la nature des ressources**

Il ne faut pas imposer un mécanisme unique à toutes les catégories.

Un composant React, une collection d'icônes, une feuille de styles, une fonction utilitaire, un ensemble de templates ou une bibliothèque complète ne présentent pas les mêmes besoins.

La plateforme doit pouvoir déterminer et proposer des modes de distribution adaptés à la nature des ressources.

Elle doit notamment distinguer les ressources qui peuvent être installées directement, celles qui nécessitent une intégration dans un projet, celles qui peuvent être récupérées comme fichiers et celles qui exigent des opérations de configuration complémentaires.

L'objectif est d'éviter de présenter une ressource comme directement installable lorsque son utilisation nécessite en réalité plusieurs étapes ou adaptations.

## **2. Publication des ressources**

La publication représente le passage entre une ressource gérée dans le patrimoine et une ressource rendue disponible pour une consommation définie.

Elle doit constituer une opération maîtrisée, traçable et réversible selon les possibilités du mode de distribution concerné.

Une ressource ne doit pas être automatiquement publiée dès qu'elle est créée, importée ou modifiée.

L'utilisateur doit pouvoir décider quand elle devient disponible, à qui elle est destinée et sous quelles conditions elle peut être consommée.

### **2.1. Préparation à la publication**

Avant sa publication, une ressource doit pouvoir faire l'objet d'une préparation spécifique.

Cette préparation doit permettre de vérifier que les éléments destinés aux utilisateurs sont présents et cohérents.

Il faut notamment examiner :

- L'identité de la ressource.
- Son nom.
- Sa description.
- Sa catégorie.
- Sa version.
- Son origine.
- Son auteur ou son propriétaire.
- Sa licence.
- Ses conditions d'utilisation.
- Sa documentation.
- Ses dépendances.
- Ses fichiers distribuables.
- Ses environnements compatibles.
- Ses éventuelles limitations.
- Son état de validation.
- Les informations nécessaires à son installation ou à son intégration.

La plateforme doit permettre d'identifier les éléments manquants avant la publication.

Elle doit également éviter de confondre les informations internes utilisées pour gérer la ressource avec les informations destinées aux utilisateurs qui la consomment.

### **2.2. Publication d'une version précise**

La publication doit toujours être rattachée à une version identifiable.

Lorsqu'un utilisateur publie une ressource, il doit être possible de savoir exactement quelle version a été rendue disponible.

Une modification ultérieure du code source ne doit pas altérer silencieusement le contenu d'une version déjà publiée.

Cette exigence est essentielle pour garantir la stabilité des projets qui consomment les ressources.

La plateforme doit donc distinguer :

- La version en cours de travail.
- La version préparée.
- La version soumise à publication.
- La version publiée.
- La version remplacée par une nouvelle publication.
- La version retirée de la distribution.
- La version archivée.

Une publication doit conserver un lien explicite avec les fichiers, les dépendances et les métadonnées correspondant à l'état publié.

### **2.3. Publication initiale et publications successives**

La plateforme doit permettre de publier une ressource pour la première fois, puis de publier de nouvelles versions au fur et à mesure de son évolution.

Chaque nouvelle publication doit pouvoir être identifiée et documentée.

Il doit être possible de préciser :

- Ce qui a changé.
- Pourquoi la modification a été effectuée.
- Les nouvelles fonctionnalités.
- Les corrections apportées.
- Les incompatibilités éventuelles.
- Les changements de dépendances.
- Les éventuelles migrations nécessaires.
- Les limitations connues.

La publication ne doit pas être considérée comme une simple opération de remplacement des fichiers précédents.

Elle doit préserver l'historique des versions distribuées.

### **2.4. Publication contrôlée**

Il doit être possible de soumettre une ressource à un processus de publication comportant plusieurs étapes.

Par exemple, une ressource peut être préparée par son créateur, examinée par un responsable, puis rendue disponible après validation.

Les règles de publication doivent pouvoir être adaptées au contexte.

Une bibliothèque personnelle peut être publiée directement par son propriétaire, tandis qu'une bibliothèque institutionnelle peut nécessiter une validation préalable.

La plateforme doit permettre de représenter ces différences sans imposer un processus identique à tous les utilisateurs.

### **2.5. Retrait d'une publication**

Il doit être possible de retirer une ressource de la distribution lorsque cela devient nécessaire.

Ce retrait peut être justifié par :

- Une erreur importante.
- Une vulnérabilité.
- Un problème de licence.
- Une incompatibilité.
- Une publication accidentelle.
- Une version défectueuse.
- Une décision du propriétaire.
- L'abandon de la ressource.

Le retrait d'une publication ne doit pas nécessairement supprimer la ressource du patrimoine.

Il faut distinguer le fait de ne plus distribuer une version du fait de supprimer définitivement les fichiers et l'historique associés.

Lorsqu'une ressource a déjà été consommée par d'autres projets, la plateforme doit permettre de conserver une information sur son retrait et ses raisons.

## **3. Registres et catalogues de distribution**

La plateforme doit pouvoir organiser les ressources publiées dans des espaces de distribution structurés.

Ces espaces doivent permettre aux utilisateurs de découvrir les ressources, de comprendre leur destination et de déterminer comment les consommer.

Il faut distinguer le catalogue, qui sert à découvrir et à consulter les ressources, du registre, qui représente un espace dans lequel les ressources publiées peuvent être identifiées et récupérées selon un mécanisme de distribution.

Une plateforme peut avoir besoin de plusieurs catalogues et de plusieurs espaces de distribution.

### **3.1. Catalogue public**

Le catalogue public doit permettre de rendre certaines ressources accessibles à un public extérieur.

Il doit permettre de consulter les informations pertinentes sans nécessairement accéder à l'ensemble des fonctionnalités de gestion interne.

Un utilisateur doit pouvoir découvrir une ressource, consulter sa description, examiner ses versions disponibles, comprendre ses conditions d'utilisation et connaître les modalités de récupération.

Les ressources privées ou restreintes ne doivent pas apparaître dans un catalogue public lorsque leurs règles de visibilité ne l'autorisent pas.

### **3.2. Catalogue privé**

La plateforme doit également permettre de gérer des catalogues réservés à des utilisateurs, des équipes ou des organisations.

Ces catalogues peuvent contenir :

- Des composants internes.
- Des bibliothèques propres à une organisation.
- Des ressources expérimentales.
- Des ressources non publiées publiquement.
- Des collections réservées à certains projets.
- Des ressources soumises à des règles d'accès particulières.

L'accès à ces catalogues doit respecter les droits associés aux ressources et aux espaces concernés.

### **3.3. Catalogues spécialisés**

Il doit être possible de créer des catalogues correspondant à des catégories ou à des domaines d'utilisation.

Par exemple :

- Catalogue de composants d'interface.
- Catalogue de systèmes de design.
- Catalogue d'icônes.
- Catalogue de templates.
- Catalogue de ressources graphiques.
- Catalogue de composants de formulaires.
- Catalogue de ressources destinées à React.
- Catalogue de bibliothèques partagées.

Ces regroupements doivent faciliter la découverte sans imposer une organisation rigide.

Une même ressource peut appartenir à plusieurs catégories ou apparaître dans plusieurs catalogues lorsque les règles de distribution le permettent.

### **3.4. Organisation des catalogues**

Les catalogues doivent permettre de retrouver facilement les ressources.

Il faut notamment pouvoir organiser les informations selon :

- Les catégories.
- Les technologies.
- Les sources d'origine.
- Les auteurs.
- Les propriétaires.
- Les bibliothèques.
- Les collections.
- Les versions.
- Les niveaux de validation.
- Les licences.
- Les environnements compatibles.
- Les dates de publication.
- Les statuts de maintenance.

Les utilisateurs doivent pouvoir rechercher et filtrer les ressources selon plusieurs critères simultanément.

### **3.5. Découverte d'une ressource**

La consultation d'une ressource publiée doit permettre de comprendre rapidement ce qu'elle contient et comment elle peut être utilisée.

Une fiche de distribution doit notamment pouvoir présenter :

- Le nom.
- La description.
- Les usages prévus.
- Les aperçus disponibles.
- Les variantes.
- La version actuelle.
- Les versions précédentes.
- Les informations de provenance.
- Les conditions d'utilisation.
- Les dépendances.
- Les environnements compatibles.
- La documentation.
- Les exemples d'intégration.
- Les résultats de validation disponibles.
- Les éventuelles limitations.
- Les modalités de récupération.

Il ne faut pas obliger l'utilisateur à récupérer le code source avant de comprendre ce qu'il s'apprête à utiliser.

## **4. Gestion de plusieurs espaces et registres de distribution**

La plateforme doit pouvoir prendre en charge plusieurs espaces de publication et de distribution.

Cette capacité est importante pour les utilisateurs qui gèrent des ressources destinées à différents projets, équipes ou organisations.

### **4.1. Espaces personnels**

Un utilisateur doit pouvoir disposer d'un espace dans lequel il publie ses propres ressources.

Cet espace peut servir à distribuer des composants personnels, des expérimentations finalisées, des collections ou des bibliothèques.

Il doit être possible de contrôler la visibilité de ces ressources et de déterminer qui peut les consulter ou les consommer.

### **4.2. Espaces d'équipe**

Une équipe doit pouvoir disposer d'un espace de distribution commun.

Cet espace peut regrouper des ressources créées par plusieurs membres, tout en conservant leur provenance et leur historique.

Il doit être possible de gérer les responsabilités relatives à la publication, à la validation et à la maintenance.

### **4.3. Espaces organisationnels**

Une organisation peut avoir besoin d'un catalogue commun pour ses projets.

Cet espace doit permettre de centraliser les ressources qu'elle souhaite mettre à disposition de ses équipes.

Il doit notamment être possible de distinguer :

- Les ressources accessibles à tous les membres.
- Les ressources réservées à certaines équipes.
- Les ressources destinées à des projets spécifiques.
- Les ressources expérimentales.
- Les ressources approuvées pour un usage général.

### **4.4. Espaces de distribution spécialisés**

La plateforme doit pouvoir prendre en compte des espaces ayant des finalités différentes.

Par exemple, un espace peut être destiné à la distribution de composants validés, tandis qu'un autre sert à partager des ressources expérimentales.

Il doit être possible de définir les règles de publication et d'accès correspondant à chaque espace.

### **4.5. Relations entre les espaces**

Une même ressource peut être gérée dans un espace principal et distribuée dans plusieurs autres espaces autorisés.

La plateforme doit permettre de conserver le lien entre ces différentes représentations.

Il faut notamment éviter qu'une même ressource soit considérée comme totalement indépendante dans chaque catalogue alors qu'elle partage une origine, un historique ou une version commune.

## **5. Distribution sous forme de code source**

La récupération du code source constitue un besoin central du produit.

L'utilisateur doit pouvoir obtenir les fichiers réels d'une ressource, les examiner et les intégrer librement dans son projet, dans les limites des droits associés.

Il ne faut pas réduire la distribution à la fourniture d'un paquet compilé ou à une référence vers une ressource distante.

### **5.1. Récupération complète du code source**

Pour une ressource distribuable sous forme de code source, il doit être possible de récupérer l'ensemble des fichiers nécessaires à son utilisation.

Cela peut inclure :

- Les fichiers de composants.
- Les fichiers de styles.
- Les fichiers de configuration.
- Les fichiers de types.
- Les fichiers utilitaires.
- Les fichiers d'assets.
- Les fichiers de documentation.
- Les fichiers de définition.
- Les éventuels fichiers d'exemples.

La récupération doit préserver autant que possible la structure nécessaire à la compréhension et à l'utilisation de la ressource.

### **5.2. Préservation de la structure des fichiers**

La plateforme ne doit pas détruire l'organisation des fichiers lors de leur distribution.

Une ressource composée de plusieurs fichiers doit pouvoir être récupérée avec une structure cohérente.

Les relations entre les fichiers doivent être conservées.

Il faut également éviter de regrouper arbitrairement plusieurs fichiers indépendants lorsque cette opération rendrait la ressource difficile à maintenir ou à personnaliser.

### **5.3. Récupération d'une ressource individuelle**

Il doit être possible de récupérer uniquement une ressource précise.

Par exemple, un utilisateur qui souhaite obtenir un bouton ne doit pas être obligé de récupérer une bibliothèque entière contenant des dizaines de composants.

La récupération individuelle doit être possible lorsque la ressource est suffisamment autonome et que ses dépendances peuvent être identifiées.

Si des fichiers supplémentaires sont nécessaires, la plateforme doit les signaler.

### **5.4. Récupération d'un ensemble de ressources**

Il doit également être possible de récupérer plusieurs ressources dans une même opération.

Par exemple :

- Plusieurs composants sélectionnés.
- Une collection complète.
- Une famille de composants.
- Un ensemble de ressources associées.
- Une bibliothèque entière.

La plateforme doit préserver les relations entre les éléments récupérés.

### **5.5. Récupération d'une version précise**

Il doit être possible de récupérer une version déterminée plutôt que systématiquement la dernière version publiée.

Cette capacité est essentielle pour les utilisateurs qui souhaitent reproduire un environnement existant ou conserver la stabilité d'un projet.

La version récupérée doit être identifiable sans ambiguïté.

### **5.6. Récupération avec ou sans éléments complémentaires**

Selon les besoins, l'utilisateur doit pouvoir choisir entre plusieurs périmètres de récupération :

- Code source uniquement.
- Code source avec dépendances documentées.
- Code source avec assets.
- Code source avec documentation.
- Ressource complète.
- Ensemble complet incluant les ressources nécessaires.

Ces possibilités doivent être présentées clairement afin d'éviter les récupérations incomplètes.

## **6. Distribution par mécanismes de registre et de paquets**

Certaines ressources ont vocation à être distribuées sous forme de paquets installables.

La plateforme doit pouvoir prendre en compte ce mode de consommation lorsque la nature de la ressource le permet.

Ce mode ne doit toutefois pas remplacer la possibilité de récupérer les codes sources lorsque celle-ci est nécessaire ou souhaitée.

### **6.1. Distribution sous forme de paquet**

Pour les ressources compatibles avec ce mode de distribution, il doit être possible de produire ou de publier un paquet identifiable et versionné.

Le paquet doit contenir les éléments nécessaires à son utilisation dans l'environnement prévu.

Il doit également disposer d'informations permettant de connaître :

- Son nom.
- Sa version.
- Son contenu.
- Ses dépendances.
- Ses prérequis.
- Son environnement cible.
- Ses conditions d'utilisation.
- Sa provenance.

### **6.2. Compatibilité avec les écosystèmes de paquets**

La plateforme doit pouvoir prendre en compte les différents environnements de distribution utilisés par les technologies prises en charge.

Par exemple, selon la nature des ressources :

- Écosystèmes npm.
- Environnements Yarn.
- Environnements pnpm.
- Autres registres de paquets compatibles avec les ressources distribuées.

Il ne faut pas supposer qu'un mécanisme de distribution unique convient à toutes les technologies.

### **6.3. Publication vers des registres externes**

La plateforme doit pouvoir prendre en compte la publication vers des registres externes lorsque cela est autorisé et pertinent.

L'objectif est de ne pas enfermer les ressources dans un registre interne.

Une ressource préparée dans la plateforme pourrait ainsi être rendue disponible dans un environnement de distribution externe, tout en conservant les informations nécessaires à sa traçabilité.

La plateforme doit permettre de distinguer la publication interne de la publication externe.

### **6.4. Gestion des versions publiées**

Les paquets doivent conserver une identité et une version précises.

La publication d'une nouvelle version ne doit pas modifier rétroactivement les paquets déjà distribués.

Il doit être possible de consulter les versions disponibles et de comprendre leurs différences.

### **6.5. Informations relatives à l'installation**

La fiche de distribution doit fournir les informations nécessaires à l'installation.

Cela peut comprendre :

- Le nom du paquet.
- La version recommandée.
- Les instructions d'installation.
- Les dépendances requises.
- Les prérequis.
- Les éventuelles configurations supplémentaires.
- Les conditions de compatibilité.

Les instructions doivent correspondre à la version effectivement publiée.

## **7. Distribution de composants à la manière des registres de composants**

La plateforme doit pouvoir répondre aux besoins de distribution de composants sous forme de ressources récupérables directement dans les projets.

Le besoin ne se limite pas à publier une bibliothèque complète.

Un utilisateur doit pouvoir sélectionner un composant dans un catalogue, le récupérer dans son projet et disposer de ses fichiers sources.

Cette capacité est particulièrement importante pour les modèles de distribution dans lesquels les composants sont copiés ou ajoutés directement au code source du projet consommateur.

### **7.1. Distribution individuelle de composants**

Un composant doit pouvoir être publié indépendamment des autres composants de sa bibliothèque lorsque cela est possible.

L'utilisateur doit pouvoir le découvrir, le prévisualiser, examiner ses propriétés, consulter ses dépendances et récupérer uniquement les éléments nécessaires.

### **7.2. Distribution de collections de composants**

Il doit être possible de publier des collections composées de plusieurs composants.

L'utilisateur doit pouvoir récupérer l'ensemble ou sélectionner uniquement les éléments qui l'intéressent.

La plateforme doit préserver les relations entre les composants et identifier les dépendances partagées.

### **7.3. Dépendances entre composants**

Certains composants nécessitent d'autres composants.

Par exemple, un composant de sélection avancé peut dépendre d'un composant de base, d'une fonction utilitaire ou d'un ensemble de styles.

La plateforme doit permettre de déterminer les dépendances nécessaires avant la récupération.

Elle doit également distinguer les dépendances obligatoires des dépendances facultatives.

### **7.4. Personnalisation après récupération**

Un composant récupéré dans un projet doit pouvoir être modifié par le développeur selon les conditions de sa licence.

La plateforme doit tenir compte du fait que la copie locale peut évoluer indépendamment de la version publiée.

Il ne faut donc pas supposer que toute modification effectuée dans le projet consommateur sera automatiquement synchronisée avec le patrimoine d'origine.

### **7.5. Suivi des versions des composants distribués**

Il doit être possible d'identifier la version du composant qui a été récupérée.

Cette information est importante lorsqu'une nouvelle version est publiée et que le développeur souhaite déterminer si une mise à jour est pertinente.

La plateforme doit également permettre de comprendre les différences entre la version installée et la version disponible.

## **8. Installation et intégration dans les projets consommateurs**

La distribution ne doit pas s'arrêter à la disponibilité des ressources.

La plateforme doit également faciliter leur intégration dans les projets.

Un utilisateur doit pouvoir comprendre comment utiliser une ressource dans son environnement réel, avec les prérequis et les éventuelles adaptations nécessaires.

### **8.1. Identification de l'environnement cible**

Avant de proposer une méthode d'intégration, il faut pouvoir identifier l'environnement concerné.

Par exemple :

- Projet React.
- Projet Next.js.
- Projet Vue.
- Projet Nuxt.
- Projet Svelte.
- Projet Angular.
- Projet utilisant uniquement HTML, CSS et JavaScript.
- Bibliothèque de composants.
- Projet utilisant un environnement de styles particulier.

La plateforme doit présenter les méthodes adaptées à la technologie concernée.

Elle ne doit pas proposer une instruction d'installation générique qui serait incorrecte pour l'environnement cible.

### **8.2. Informations de compatibilité avant intégration**

Avant qu'une ressource soit intégrée, l'utilisateur doit pouvoir connaître les conditions nécessaires.

Il faut notamment indiquer :

- Les versions minimales ou prises en charge.
- Les dépendances obligatoires.
- Les dépendances facultatives.
- Les prérequis de configuration.
- Les éventuelles incompatibilités connues.
- Les adaptations nécessaires.
- Les limites de la ressource.

L'objectif est de réduire les erreurs d'intégration et les mauvaises surprises.

### **8.3. Instructions d'intégration**

La plateforme doit pouvoir fournir des instructions adaptées à chaque mode de consommation.

Ces instructions peuvent inclure :

- Installation.
- Récupération des fichiers.
- Importation.
- Configuration.
- Déclaration des dépendances.
- Utilisation dans un composant.
- Utilisation dans une page.
- Chargement des styles.
- Configuration des assets.
- Paramétrage des thèmes.

Les exemples doivent être cohérents avec la version distribuée.

### **8.4. Exemples d'utilisation**

Chaque ressource doit pouvoir être accompagnée d'exemples concrets.

Pour un composant, il peut s'agir de montrer :

- Son utilisation minimale.
- Son utilisation avec des propriétés personnalisées.
- Ses différentes variantes.
- Son utilisation avec des événements.
- Son utilisation avec des données.
- Son intégration dans un ensemble de composants.

Ces exemples doivent permettre à l'utilisateur de comprendre rapidement comment exploiter la ressource.

### **8.5. Gestion des configurations nécessaires**

Certaines ressources nécessitent des configurations particulières.

La plateforme doit permettre de les documenter clairement.

Il peut s'agir :

- De configurations de styles.
- De paramètres de thème.
- De variables d'environnement.
- De chemins d'assets.
- De paramètres d'exécution.
- De configurations liées à un framework.
- De dépendances externes.
- De paramètres spécifiques au projet.

Il faut distinguer les configurations obligatoires des configurations facultatives.

### **8.6. Détection des conflits d'intégration**

Lorsque cela est possible, la plateforme doit permettre d'identifier les conflits susceptibles d'apparaître lors de l'intégration.

Par exemple :

- Dépendances déjà présentes dans le projet.
- Versions incompatibles.
- Noms de fichiers déjà utilisés.
- Conflits de styles.
- Conflits de configuration.
- Ressources dupliquées.
- Incompatibilités entre bibliothèques.

L'objectif est d'éviter qu'une intégration apparemment simple introduise des problèmes dans le projet consommateur.

## **9. Consommation des ressources selon plusieurs modes**

La plateforme doit prendre en charge plusieurs manières d'utiliser les ressources distribuées.

Il ne faut pas imposer un seul modèle de consommation.

Certaines équipes préfèrent intégrer directement les fichiers sources dans leur projet. D'autres préfèrent utiliser des paquets versionnés. D'autres encore ont besoin de récupérer des collections ou des ressources depuis un registre.

### **9.1. Consommation par copie de code source**

Dans ce modèle, les fichiers d'une ressource sont récupérés et intégrés directement au projet consommateur.

Le développeur possède alors une copie locale qu'il peut adapter selon les conditions d'utilisation.

La plateforme doit permettre de conserver l'identification de l'origine de cette copie.

Il doit également être possible de retrouver la version initiale à partir de laquelle elle a été récupérée.

### **9.2. Consommation par paquet installé**

Dans ce modèle, le projet utilise une ressource distribuée sous forme de paquet.

Le développeur dépend alors d'une version publiée et de ses règles de distribution.

La plateforme doit permettre de consulter les informations nécessaires à la gestion de cette dépendance.

### **9.3. Consommation par récupération d'une collection**

Un projet peut nécessiter plusieurs ressources appartenant à une même collection.

Il doit être possible de récupérer cet ensemble en conservant sa cohérence et ses relations internes.

La plateforme doit également permettre de ne récupérer qu'une partie de la collection lorsque cela est possible.

### **9.4. Consommation de ressources composées**

Certaines ressources peuvent être constituées de plusieurs éléments interdépendants.

Il faut pouvoir les consommer comme un ensemble cohérent lorsque leur fonctionnement l'exige.

La plateforme doit clairement identifier les éléments qui composent l'ensemble et les conditions nécessaires à leur utilisation.

### **9.5. Consommation depuis plusieurs projets**

Une même ressource peut être utilisée dans plusieurs projets.

La plateforme doit permettre d'identifier ces différents usages lorsque les projets consommateurs sont connus ou déclarés.

Cela facilite le suivi des versions et l'analyse de l'impact des évolutions.

## **10. Gestion des mises à jour et des évolutions distribuées**

La distribution ne peut pas être considérée comme une opération ponctuelle.

Les ressources évoluent, leurs dépendances changent et de nouvelles versions sont publiées.

La plateforme doit donc permettre de gérer les mises à jour sans compromettre les projets qui consomment les ressources.

### **10.1. Détection des nouvelles versions**

Lorsqu'une nouvelle version d'une ressource est publiée, il doit être possible de l'identifier par rapport aux versions précédemment distribuées.

La plateforme doit pouvoir présenter :

- La version actuelle.
- La nouvelle version disponible.
- Les modifications.
- Les corrections.
- Les nouvelles fonctionnalités.
- Les changements de dépendances.
- Les incompatibilités éventuelles.
- Les éventuelles migrations nécessaires.

### **10.2. Mise à jour volontaire**

La disponibilité d'une nouvelle version ne doit pas entraîner automatiquement son adoption par tous les projets.

L'utilisateur doit pouvoir décider s'il souhaite effectuer la mise à jour.

Cette décision doit être prise en tenant compte de la stabilité du projet, des changements introduits et des résultats de compatibilité disponibles.

### **10.3. Mise à jour de composants copiés dans un projet**

Les ressources récupérées sous forme de fichiers sources présentent une particularité : le projet consommateur peut les modifier indépendamment de leur origine.

Il faut donc éviter de supposer qu'une mise à jour peut simplement remplacer les fichiers locaux.

La plateforme doit permettre de distinguer :

- La version originale récupérée.
- La copie locale.
- Les modifications locales.
- La nouvelle version publiée.
- Les différences entre les deux états.
- Les éventuels conflits.
- Les modifications pouvant être reprises.

L'objectif est de permettre aux développeurs de bénéficier des améliorations sans perdre leurs personnalisations.

### **10.4. Mise à jour des paquets**

Pour les ressources distribuées sous forme de paquets, il doit être possible de consulter les versions disponibles et de comprendre les changements avant d'adopter une mise à jour.

La plateforme doit pouvoir présenter les éventuelles ruptures de compatibilité et les conditions nécessaires à la migration.

### **10.5. Mises à jour de plusieurs ressources**

Une mise à jour peut concerner plusieurs composants d'une même collection ou d'une bibliothèque.

La plateforme doit permettre d'identifier les ressources concernées et d'évaluer les conséquences d'une mise à jour groupée.

Il faut également pouvoir distinguer les mises à jour qui peuvent être réalisées indépendamment de celles qui nécessitent une évolution coordonnée.

## **11. Gestion des différences entre la version distribuée et les copies locales**

La plateforme doit reconnaître qu'une ressource distribuée sous forme de code source peut être modifiée après son intégration dans un projet.

Cette réalité est fondamentale pour le modèle de distribution envisagé.

Contrairement à un paquet installé dont le projet dépend d'une version publiée, une copie de code source peut évoluer indépendamment.

Il faut donc conserver la possibilité de comparer les états.

### **11.1. Identification de la version d'origine**

Lorsqu'une ressource est récupérée, il doit être possible d'enregistrer son origine.

Cette information peut inclure :

- L'identité de la ressource.
- La source de distribution.
- La version récupérée.
- La date de récupération.
- Les fichiers concernés.
- Les dépendances initiales.
- Les éventuelles transformations effectuées.

Cette traçabilité doit permettre de comprendre d'où provient une copie locale.

### **11.2. Détection des modifications locales**

Lorsque cela est possible, la plateforme doit permettre de comparer une copie locale avec sa version d'origine.

Il faut notamment identifier :

- Les fichiers modifiés.
- Les fichiers ajoutés.
- Les fichiers supprimés.
- Les changements de structure.
- Les modifications de dépendances.
- Les différences de configuration.
- Les changements de comportement.

Cette comparaison doit permettre de comprendre dans quelle mesure la copie locale s'est éloignée de la ressource publiée.

### **11.3. Comparaison avec une nouvelle version**

Lorsqu'une nouvelle version est disponible, l'utilisateur doit pouvoir examiner les différences entre :

- La version initialement récupérée.
- La copie locale actuelle.
- La nouvelle version publiée.

Cette comparaison à trois états est particulièrement importante pour éviter de perdre les modifications locales lors d'une mise à jour.

### **11.4. Gestion des conflits**

Certaines modifications locales peuvent entrer en conflit avec les changements introduits dans une nouvelle version.

La plateforme doit permettre de rendre ces conflits visibles.

Elle doit distinguer les changements indépendants, les changements compatibles et les modifications nécessitant une intervention.

L'utilisateur doit pouvoir comprendre les conflits avant de prendre une décision.

### **11.5. Conservation de l'autonomie des copies locales**

Une copie locale ne doit pas être considérée comme une simple représentation temporaire de la ressource d'origine.

Elle peut devenir une implémentation spécifique à un projet.

La plateforme doit donc permettre de préserver son autonomie, tout en conservant les informations nécessaires à la traçabilité de son origine.

## **12. Distribution de systèmes de design et de bibliothèques complètes**

La plateforme doit pouvoir distribuer des ensembles plus larges que des composants individuels.

Un système de design peut comporter plusieurs catégories de ressources qui doivent rester cohérentes entre elles.

Une bibliothèque peut également comprendre des composants, des utilitaires, des styles, des thèmes, des tokens, des assets et de la documentation.

La distribution de ces ensembles nécessite une attention particulière.

### **12.1. Distribution d'une bibliothèque complète**

Il doit être possible de publier une bibliothèque comme un ensemble identifiable et versionné.

L'utilisateur doit pouvoir consulter son contenu et comprendre les ressources qu'elle regroupe.

Il doit également pouvoir récupérer l'ensemble de la bibliothèque ou certains éléments lorsqu'une consommation partielle est autorisée.

### **12.2. Distribution d'un système de design**

Un système de design doit pouvoir être distribué comme un ensemble cohérent.

La distribution doit pouvoir inclure :

- Les tokens.
- Les thèmes.
- Les palettes.
- Les typographies.
- Les règles d'espacement.
- Les composants.
- Les variantes.
- Les assets.
- Les ressources documentaires.
- Les règles d'utilisation.

Il faut préserver les relations entre ces éléments.

### **12.3. Distribution des versions cohérentes**

Lorsque plusieurs composants dépendent d'un même système de design, il faut pouvoir distribuer un ensemble de versions compatibles.

La plateforme doit permettre d'identifier les versions qui ont été conçues pour fonctionner ensemble.

Cela évite de distribuer des composants qui utilisent des tokens ou des conventions incompatibles.

### **12.4. Distribution partielle**

Un utilisateur peut vouloir récupérer uniquement une partie d'un système de design.

Par exemple, il peut souhaiter utiliser les tokens et les thèmes sans récupérer l'ensemble des composants.

La plateforme doit permettre cette distribution partielle lorsque les éléments sélectionnés sont suffisamment autonomes.

Si certains éléments nécessitent des dépendances supplémentaires, celles-ci doivent être identifiées.

### **12.5. Évolution d'un ensemble distribué**

Lorsqu'un système de design évolue, il doit être possible de publier une nouvelle version cohérente.

La plateforme doit permettre de comprendre quels composants ont été modifiés, quelles ressources ont été ajoutées ou supprimées et quelles adaptations peuvent être nécessaires dans les projets consommateurs.

## **13. Distribution de ressources provenant de plusieurs sources**

L'ambition du produit repose notamment sur la possibilité de récupérer et de personnaliser des ressources provenant de différentes sources libres.

La distribution doit donc pouvoir prendre en compte des ressources dont l'origine n'est pas limitée à une seule bibliothèque ou à un seul fournisseur.

### **13.1. Préservation de la provenance**

Lorsqu'une ressource issue d'une source externe est personnalisée puis redistribuée, sa provenance doit rester traçable.

La plateforme doit permettre de conserver les informations sur :

- La source originale.
- L'auteur ou les auteurs connus.
- La licence initiale.
- La version récupérée.
- Les transformations effectuées.
- Les éléments ajoutés.
- Les éléments supprimés.
- Les éventuelles nouvelles dépendances.

Il faut éviter qu'une ressource redistribuée perde artificiellement son historique d'origine.

### **13.2. Redistribution de ressources dérivées**

Lorsqu'une ressource a été personnalisée, il doit être possible de déterminer si sa redistribution est autorisée.

Cette vérification doit tenir compte des licences et des conditions associées aux éléments qui la composent.

La plateforme doit éviter de considérer qu'une modification du code suffit à rendre une ressource juridiquement indépendante de sa source initiale.

### **13.3. Ressources composites issues de plusieurs origines**

Une ressource composite peut réunir des éléments provenant de plusieurs sources.

Il faut donc pouvoir conserver la provenance de chaque partie lorsque cette information est disponible.

Cela permet d'identifier les conditions applicables à l'ensemble et d'éviter les erreurs de redistribution.

### **13.4. Conditions de redistribution**

Avant de publier une ressource dérivée, il doit être possible de consulter les informations relatives à sa redistribution.

La plateforme doit permettre de signaler les situations dans lesquelles :

- La redistribution est autorisée.
- La redistribution est autorisée sous certaines conditions.
- Une attribution est nécessaire.
- Des obligations de conservation de licence existent.
- Une autorisation supplémentaire est nécessaire.
- Les conditions sont inconnues ou insuffisamment documentées.

La plateforme ne doit pas inventer une autorisation lorsque les informations disponibles ne permettent pas de conclure.

### **13.5. Distinction entre publication technique et autorisation juridique**

Le fait qu'une ressource puisse être publiée techniquement ne signifie pas nécessairement que sa redistribution est autorisée.

La plateforme doit conserver cette distinction.

Les mécanismes de publication doivent pouvoir tenir compte des restrictions connues et signaler les situations nécessitant une vérification.

## **14. Distribution privée, publique et à accès contrôlé**

Toutes les ressources ne sont pas destinées à être accessibles au même public.

La plateforme doit permettre de définir plusieurs niveaux de visibilité et d'accès.

### **14.1. Distribution publique**

Une ressource publique peut être découverte et consommée par les utilisateurs autorisés sans restriction d'accès propre à un espace privé.

La plateforme doit permettre de présenter les informations nécessaires à sa découverte et à son utilisation.

### **14.2. Distribution privée**

Une ressource privée doit être accessible uniquement aux utilisateurs ou organisations autorisés.

Elle peut être utilisée pour distribuer des composants internes, des bibliothèques propriétaires ou des ressources spécifiques à une organisation.

### **14.3. Distribution restreinte**

Il doit être possible de rendre une ressource accessible uniquement à un groupe défini.

Par exemple, une bibliothèque peut être destinée à une équipe particulière ou à certains projets.

### **14.4. Distribution par invitation ou autorisation**

Certains espaces peuvent nécessiter une autorisation préalable avant qu'un utilisateur puisse accéder aux ressources.

La plateforme doit permettre de distinguer la découverte d'une ressource de l'autorisation de la récupérer.

### **14.5. Gestion des droits de consommation**

Les droits peuvent différer selon les actions autorisées.

Il faut pouvoir distinguer :

- Consulter.
- Prévisualiser.
- Télécharger.
- Récupérer le code source.
- Installer.
- Utiliser.
- Modifier.
- Redistribuer.
- Publier une version dérivée.
- Administrer la distribution.

La plateforme doit permettre d'associer ces droits aux règles d'accès pertinentes.

## **15. Distribution vers plusieurs environnements et destinations**

Une ressource peut être destinée à plusieurs environnements de consommation.

La plateforme doit pouvoir gérer ces différentes destinations sans supposer que les mêmes fichiers ou les mêmes modalités conviennent à tous les cas.

### **15.1. Plusieurs destinations pour une même ressource**

Une ressource peut disposer de plusieurs formes adaptées à différents environnements.

Par exemple, une ressource peut être distribuée sous forme de code source pour un environnement et sous forme de paquet pour un autre.

Il faut pouvoir associer ces différentes distributions à la même identité de ressource.

### **15.2. Variantes destinées à des environnements différents**

Lorsque plusieurs implémentations sont nécessaires, elles doivent pouvoir être identifiées séparément.

Par exemple, deux composants peuvent remplir la même fonction, mais avoir des implémentations spécifiques à React et Vue.

La plateforme doit permettre de comprendre qu'ils sont liés fonctionnellement sans les présenter comme un même code source interchangeable.

### **15.3. Gestion des configurations par destination**

Certaines destinations peuvent nécessiter des configurations spécifiques.

Il faut pouvoir documenter ces différences et éviter de mélanger les configurations propres à chaque environnement.

### **15.4. Identification des limites de compatibilité**

La plateforme doit signaler les environnements pour lesquels aucune validation n'a été effectuée.

Elle ne doit pas présenter une ressource comme universellement compatible sur la seule base de sa disponibilité dans un catalogue.

## **16. Documentation destinée aux consommateurs**

La documentation de distribution doit être distincte, autant que nécessaire, de la documentation interne de gestion.

Une personne qui découvre une ressource dans un catalogue doit pouvoir comprendre rapidement comment l'utiliser.

### **16.1. Documentation d'installation**

Elle doit expliquer les conditions nécessaires à l'installation ou à la récupération.

Elle doit être adaptée au mode de distribution.

### **16.2. Documentation d'utilisation**

Elle doit présenter les fonctionnalités disponibles et les principales possibilités de personnalisation.

Pour un composant, cela peut inclure :

- Les propriétés.
- Les événements.
- Les états.
- Les variantes.
- Les exemples.
- Les comportements.
- Les limites connues.

### **16.3. Documentation des dépendances**

Il faut identifier les dépendances nécessaires et les éventuelles configurations complémentaires.

La documentation doit permettre de comprendre les prérequis avant de commencer l'intégration.

### **16.4. Documentation des changements**

Chaque version publiée doit pouvoir être accompagnée d'informations sur son évolution.

Les utilisateurs doivent pouvoir comprendre ce qui a changé depuis la version précédente.

### **16.5. Documentation des migrations**

Lorsqu'une version introduit des modifications qui nécessitent une adaptation du projet consommateur, la plateforme doit pouvoir présenter des instructions de migration.

Ces instructions doivent permettre de comprendre les changements à effectuer et les éventuels impacts sur les usages existants.

### **16.6. Documentation des limitations**

Les limitations connues doivent pouvoir être présentées explicitement.

Il ne faut pas laisser entendre qu'une ressource répond à tous les besoins lorsque certaines restrictions sont connues.

## **17. Suivi de l'utilisation et des projets consommateurs**

La distribution doit pouvoir être accompagnée d'une visibilité sur les usages lorsque les projets consommateurs sont connus et que les informations peuvent être collectées ou déclarées.

L'objectif est de comprendre comment les ressources sont réellement utilisées et d'anticiper les conséquences de leurs évolutions.

### **17.1. Identification des projets consommateurs**

Il doit être possible de connaître les projets qui utilisent une ressource lorsque cette relation est enregistrée.

La plateforme doit pouvoir distinguer :

- Les projets qui utilisent une version donnée.
- Les projets qui utilisent une ancienne version.
- Les projets qui utilisent une variante.
- Les projets qui utilisent une copie personnalisée.
- Les projets qui utilisent une dépendance distribuée sous forme de paquet.

### **17.2. Suivi des versions consommées**

Il doit être possible de connaître les versions utilisées par les différents projets.

Cette information est importante lorsqu'une nouvelle version est publiée ou lorsqu'un problème est détecté.

### **17.3. Analyse de l'impact d'une évolution**

Lorsqu'une ressource est modifiée, la plateforme doit permettre d'identifier les projets potentiellement concernés.

Il faut pouvoir examiner :

- Les versions utilisées.
- Les fonctionnalités concernées.
- Les changements introduits.
- Les incompatibilités possibles.
- Les migrations nécessaires.

Cette capacité doit permettre d'anticiper les conséquences avant de publier ou de recommander une nouvelle version.

### **17.4. Ressources non utilisées**

Il peut également être utile d'identifier les ressources qui sont publiées mais ne sont plus utilisées dans les projets connus.

Cette information peut aider à organiser le patrimoine et à évaluer les besoins de maintenance.

Il faut toutefois distinguer une ressource réellement inutilisée d'une ressource dont les usages ne sont simplement pas suivis par la plateforme.

### **17.5. Respect des limites de visibilité**

Le suivi des projets consommateurs doit respecter les droits d'accès et les règles de confidentialité applicables.

La plateforme ne doit pas exposer les informations internes d'un projet à des utilisateurs qui ne sont pas autorisés à les consulter.

## **18. Gestion de la stabilité et de la continuité des ressources distribuées**

Une ressource publiée peut devenir importante pour plusieurs projets.

Il est donc nécessaire de pouvoir gérer sa stabilité dans le temps.

### **18.1. Ressources stables**

Il doit être possible d'identifier les versions considérées comme suffisamment stables pour les usages prévus.

Cette qualification doit s'appuyer sur des critères explicites et ne doit pas être assimilée à une garantie absolue d'absence de défaut.

### **18.2. Ressources expérimentales**

Il doit également être possible de distribuer des ressources expérimentales.

Ces ressources peuvent être accessibles pour des essais, mais leur statut doit être clairement indiqué.

Les utilisateurs doivent comprendre qu'elles peuvent évoluer rapidement et présenter certaines limitations.

### **18.3. Ressources dépréciées**

Lorsqu'une ressource n'est plus recommandée, il doit être possible de la marquer comme dépréciée.

La plateforme doit permettre d'expliquer :

- Pourquoi elle est dépréciée.
- Depuis quand.
- Quelle ressource peut éventuellement la remplacer.
- Quelles versions sont concernées.
- Quelles précautions doivent être prises.

La dépréciation ne doit pas nécessairement entraîner une suppression immédiate.

### **18.4. Ressources abandonnées**

Une ressource qui n'est plus maintenue doit pouvoir être identifiée comme telle.

Les utilisateurs doivent pouvoir consulter cette information avant de décider de l'utiliser.

### **18.5. Continuité des versions anciennes**

Il doit être possible de conserver l'accès aux versions antérieures lorsque leur distribution reste autorisée et pertinente.

Cette possibilité est importante pour les projets qui ne peuvent pas adopter immédiatement les nouvelles versions.

### **18.6. Retrait définitif et conséquences**

Lorsqu'une ressource doit être retirée définitivement, la plateforme doit permettre d'identifier les conséquences de cette décision.

Il faut distinguer le retrait du catalogue, l'arrêt de publication de nouvelles versions et l'indisponibilité des anciennes versions.

Ces opérations n'ont pas nécessairement les mêmes conséquences pour les consommateurs.

## **19. Exportation, sauvegarde et autonomie des distributions**

La plateforme doit permettre de récupérer les ressources distribuées dans des formats et des structures qui préservent leur exploitabilité.

L'utilisateur ne doit pas dépendre exclusivement d'un mécanisme de récupération propriétaire.

### **19.1. Exportation individuelle**

Il doit être possible d'exporter une ressource et les éléments nécessaires à sa réutilisation.

### **19.2. Exportation de collections**

Il doit être possible d'exporter plusieurs ressources en conservant leur organisation et leurs relations.

### **19.3. Exportation de bibliothèques complètes**

Une bibliothèque doit pouvoir être exportée avec ses fichiers, ses métadonnées et les informations nécessaires à sa reconstruction.

### **19.4. Exportation des informations de distribution**

L'exportation ne doit pas se limiter au code.

Lorsque cela est pertinent, elle doit également préserver :

- Les versions.
- Les descriptions.
- Les dépendances.
- Les licences.
- Les informations de provenance.
- Les documentations.
- Les relations entre ressources.
- Les informations de compatibilité.
- Les résultats de validation disponibles.

### **19.5. Récupération indépendante**

Il doit être possible de conserver une copie exploitable des ressources distribuées sans avoir à maintenir un accès permanent à leur catalogue d'origine.

Cette capacité participe à l'autonomie des utilisateurs et à la continuité de leurs projets.

## **20. Gouvernance de la publication et de la distribution**

La distribution des ressources peut impliquer plusieurs personnes et plusieurs niveaux de responsabilité.

La plateforme doit donc permettre d'organiser les responsabilités liées à la publication et à la maintenance.

### **20.1. Propriétaire de la distribution**

Il doit être possible d'identifier le propriétaire ou le responsable d'un espace de distribution.

Cette personne ou organisation doit pouvoir définir les règles applicables aux ressources publiées dans cet espace.

### **20.2. Responsables de publication**

Il doit être possible de distinguer les personnes qui peuvent préparer une publication de celles qui sont autorisées à l'approuver ou à la rendre disponible.

### **20.3. Responsables de maintenance**

Une ressource distribuée peut nécessiter un suivi continu.

Il doit être possible d'identifier les personnes ou équipes responsables de son évolution et de sa maintenance.

### **20.4. Historique des opérations**

Les opérations importantes doivent pouvoir être retracées.

Cela concerne notamment :

- La publication.
- Le remplacement d'une version.
- Le retrait.
- La modification de visibilité.
- Le changement de propriétaire.
- La modification des conditions de distribution.
- La gestion des accès.
- Les décisions de validation.

### **20.5. Continuité en cas de changement de responsable**

La distribution ne doit pas devenir impossible à maintenir lorsqu'une personne quitte une équipe ou cesse de gérer une ressource.

Il doit être possible de transférer les responsabilités selon les règles applicables à l'espace concerné.

## **21. Expérience utilisateur de la distribution**

Les fonctions de distribution doivent être compréhensibles, même pour les utilisateurs qui ne connaissent pas tous les mécanismes techniques associés aux registres et aux paquets.

La plateforme doit proposer une expérience cohérente depuis la consultation d'une ressource jusqu'à son intégration dans un projet.

### **21.1. Vue d'une ressource publiée**

La fiche d'une ressource publiée doit permettre de comprendre rapidement :

- Ce qu'est la ressource.
- À quoi elle sert.
- À qui elle est destinée.
- Quelle version est disponible.
- Comment la récupérer.
- Comment l'installer ou l'intégrer.
- Quelles sont ses dépendances.
- Quelles sont ses conditions d'utilisation.
- Quels sont ses environnements compatibles.
- Quelles validations ont été effectuées.

### **21.2. Actions de distribution clairement identifiées**

Selon les possibilités de la ressource, l'utilisateur doit pouvoir accéder aux actions correspondantes :

- Prévisualiser.
- Consulter le code source.
- Récupérer les fichiers.
- Télécharger.
- Installer.
- Copier les instructions.
- Consulter les versions.
- Examiner les dépendances.
- Consulter la documentation.
- Consulter les conditions d'utilisation.

Il ne faut pas afficher des actions qui ne sont pas réellement prises en charge par la ressource.

### **21.3. Parcours de consommation simplifié**

Un utilisateur qui souhaite intégrer un composant doit pouvoir comprendre rapidement les étapes nécessaires.

Il ne doit pas être obligé de parcourir toutes les informations internes de gestion pour utiliser une ressource déjà publiée.

### **21.4. Parcours avancé**

Les utilisateurs qui souhaitent examiner les détails doivent pouvoir accéder à des informations plus complètes.

Cela concerne notamment les développeurs, les responsables de bibliothèques et les personnes chargées de la maintenance.

La plateforme doit donc permettre une lecture simple sans supprimer la profondeur des informations techniques.

## **22. Exigences fondamentales à respecter**

Les capacités de cette session doivent respecter les principes suivants.

**1. La publication ne doit pas être confondue avec la création.**

Une ressource créée n'est pas nécessairement destinée à être distribuée.

**2. Une publication doit correspondre à une version identifiable.**

Les fichiers d'une version publiée doivent rester associés à leur état exact.

**3. La distribution doit être indépendante de l'environnement de création.**

Les ressources doivent pouvoir être exploitées ailleurs lorsque leur nature et leurs conditions d'utilisation le permettent.

**4. Plusieurs modes de distribution doivent pouvoir coexister.**

La plateforme ne doit pas imposer un mécanisme unique aux composants, aux bibliothèques, aux collections et aux autres catégories de ressources.

**5. La distribution du code source doit être pleinement prise en compte.**

La récupération des fichiers sources ne doit pas être considérée comme une fonctionnalité secondaire.

**6. Les ressources individuelles et les ensembles complets doivent pouvoir être distribués.**

Il faut préserver la possibilité de récupérer uniquement ce qui est nécessaire.

**7. Les dépendances doivent être clairement identifiées.**

Une ressource ne doit pas être présentée comme autonome lorsque son fonctionnement exige d'autres éléments.

**8. Les mises à jour ne doivent pas écraser automatiquement les personnalisations locales.**

Les copies de code source peuvent évoluer indépendamment de leur origine.

**9. Les versions anciennes doivent rester identifiables.**

Il faut préserver la traçabilité et la continuité des projets consommateurs.

**10. Les conditions de redistribution doivent être respectées.**

La possibilité technique de publier ne constitue pas une autorisation juridique.

**11. La visibilité et les droits d'accès doivent être maîtrisés.**

Les catalogues publics, privés et restreints doivent respecter les règles de leurs espaces.

**12. Les distributions doivent rester exportables et exploitables.**

L'utilisateur ne doit pas être enfermé dans un environnement propriétaire.

**13. La distribution doit préserver la provenance.**

Les ressources dérivées doivent conserver les informations disponibles sur leurs origines et transformations.

**14. Les compatibilités doivent être présentées honnêtement.**

Une compatibilité non vérifiée ne doit pas être présentée comme garantie.

**15. Le suivi des consommateurs doit respecter les droits et la confidentialité.**

La visibilité sur les usages doit rester limitée aux informations effectivement accessibles.

## **23. Scénarios d'utilisation représentatifs**

### **Scénario 1 — Publication d'un composant personnalisé**

Un utilisateur récupère un composant depuis une source externe, le personnalise et le valide.

Il souhaite ensuite le rendre disponible pour d'autres développeurs.

La plateforme doit lui permettre de :

1. Sélectionner la version qu'il souhaite publier.
2. Vérifier les informations descriptives.
3. Examiner les dépendances.
4. Vérifier les conditions de redistribution.
5. Préparer la documentation.
6. Choisir un espace de distribution.
7. Déterminer les conditions d'accès.
8. Effectuer les contrôles nécessaires.
9. Publier la version.
10. Rendre le composant consultable et récupérable.

La ressource publiée doit conserver son identité, son origine et son historique.

### **Scénario 2 — Récupération d'un composant dans un projet externe**

Un développeur découvre un composant dans un catalogue.

Il souhaite l'intégrer dans son projet React.

La plateforme doit lui permettre de :

1. Consulter le composant.
2. Examiner son aperçu.
3. Consulter ses propriétés.
4. Identifier ses dépendances.
5. Vérifier sa compatibilité.
6. Choisir la version.
7. Récupérer les fichiers nécessaires.
8. Consulter les instructions d'intégration.
9. Comprendre les éventuelles configurations.
10. Utiliser le composant dans son projet.

Il doit pouvoir récupérer le code source et le conserver indépendamment de la plateforme.

### **Scénario 3 — Publication d'une bibliothèque complète**

Une équipe possède une bibliothèque composée de plusieurs dizaines de composants.

Elle souhaite la rendre accessible à plusieurs projets.

La plateforme doit lui permettre de :

1. Sélectionner la version de la bibliothèque.
2. Vérifier les composants inclus.
3. Examiner les dépendances.
4. Contrôler les relations internes.
5. Vérifier les licences.
6. Préparer la documentation.
7. Définir les environnements compatibles.
8. Effectuer une validation globale.
9. Publier la bibliothèque.
10. Rendre ses différentes versions disponibles.

### **Scénario 4 — Distribution privée pour une organisation**

Une organisation développe ses propres composants et souhaite les partager uniquement avec ses équipes.

La plateforme doit lui permettre de :

1. Créer un espace de distribution privé.
2. Définir les ressources accessibles.
3. Gérer les utilisateurs autorisés.
4. Publier les versions.
5. Fournir les instructions d'intégration.
6. Suivre les versions utilisées dans les projets connus.
7. Contrôler les mises à jour.
8. Retirer les ressources qui ne doivent plus être consommées.

Les ressources ne doivent pas devenir visibles publiquement du seul fait de leur publication.

### **Scénario 5 — Mise à jour d'un composant modifié localement**

Un développeur a récupéré un composant et l'a profondément personnalisé dans son projet.

Une nouvelle version du composant original est publiée.

La plateforme doit lui permettre de :

1. Identifier la nouvelle version.
2. Comparer la version d'origine avec la nouvelle version.
3. Examiner ses propres modifications locales.
4. Identifier les fichiers concernés.
5. Détecter les conflits potentiels.
6. Comprendre les améliorations disponibles.
7. Décider des modifications à reprendre.
8. Conserver ses personnalisations.
9. Vérifier le résultat de la mise à jour.

### **Scénario 6 — Distribution d'un système de design**

Une équipe a construit un système de design avec des tokens, des thèmes et plusieurs familles de composants.

Elle souhaite le distribuer à plusieurs projets.

La plateforme doit lui permettre de publier un ensemble cohérent, de documenter les ressources, d'identifier les dépendances, de définir les versions compatibles et de permettre une récupération globale ou partielle.

### **Scénario 7 — Retrait d'une version défectueuse**

Une version publiée présente un problème important.

La plateforme doit permettre de :

1. Identifier la version concernée.
2. Documenter le problème.
3. Retirer ou signaler la version selon les possibilités du registre.
4. Informer les utilisateurs concernés lorsque cela est possible.
5. Préserver l'historique.
6. Identifier une version de remplacement si elle existe.
7. Éviter que les utilisateurs découvrent trop tard le problème.

### **Scénario 8 — Publication d'une ressource issue de plusieurs sources**

Un utilisateur crée un ensemble composite en réunissant plusieurs composants provenant de sources différentes.

Il souhaite distribuer cet ensemble.

La plateforme doit lui permettre de conserver les origines, d'examiner les licences applicables, d'identifier les dépendances et de vérifier les conditions de redistribution de l'ensemble.

Elle ne doit pas considérer automatiquement que toutes les ressources composantes peuvent être redistribuées dans les mêmes conditions.

### **Scénario 9 — Utilisation d'une même ressource dans plusieurs projets**

Une équipe utilise un composant dans plusieurs applications.

Une nouvelle version est publiée.

La plateforme doit permettre de connaître les versions utilisées dans les projets suivis, de comparer les différences et d'identifier les projets susceptibles de nécessiter une mise à jour.

Elle doit également permettre de distinguer les projets qui utilisent une version publiée de ceux qui utilisent une copie locale personnalisée.

## **24. Résultat attendu de cette session**

À travers cette session, l'objectif est de définir un véritable système de distribution des ressources logicielles, capable de prendre en charge plusieurs formes de publication, plusieurs modes de consommation et plusieurs environnements de destination.

La plateforme doit permettre de transformer les ressources gérées dans son patrimoine en éléments réellement exploitables ailleurs.

Un utilisateur doit pouvoir publier un composant individuel, une collection, une bibliothèque ou un système de design, puis rendre ces éléments disponibles selon des règles de visibilité et de distribution adaptées.

Il doit pouvoir proposer la récupération directe du code source, la distribution sous forme de paquets lorsque cela est pertinent, la récupération de plusieurs ressources en une seule opération et l'intégration dans des projets utilisant différentes technologies.

La plateforme doit également maîtriser les évolutions des ressources distribuées.

Elle doit permettre d'identifier les versions, de comparer les modifications, de suivre les mises à jour, de gérer les différences entre les versions publiées et les copies locales, et de préserver les personnalisations effectuées par les développeurs.

Il faut également garantir que la distribution ne détruit pas la traçabilité.

Les ressources doivent conserver leurs informations de provenance, leurs licences, leurs dépendances, leurs versions et leur historique.

Enfin, la plateforme doit préserver l'autonomie des utilisateurs. Le code distribué doit pouvoir être récupéré, conservé et exploité indépendamment de l'environnement dans lequel il a été créé, dans les limites des conditions d'utilisation applicables.

**Le résultat recherché est un environnement dans lequel les ressources ne sont pas simplement enregistrées et consultables, mais réellement publiables, partageables, installables, intégrables, réutilisables et maintenables dans différents projets.**

## **25. Consigne pour l'analyse et la conception ultérieures**

Les exigences de cette session devront être considérées comme un ensemble fonctionnel complet.

Il ne faudra pas réduire la distribution à la mise en place d'un catalogue ou à la publication de paquets.

Il faudra examiner séparément les besoins concernant :

- La publication.
- Les registres.
- Les catalogues.
- Les espaces publics et privés.
- La récupération des codes sources.
- La distribution individuelle.
- La distribution de collections.
- La distribution de bibliothèques.
- Les paquets installables.
- Les mécanismes de récupération de composants.
- L'intégration dans les projets.
- Les instructions d'utilisation.
- La gestion des versions.
- Les mises à jour.
- Les personnalisations locales.
- Les conflits.
- Les licences.
- La provenance.
- Les dépendances.
- Le suivi des projets consommateurs.
- Le retrait des publications.
- L'exportation.
- L'autonomie des utilisateurs.
- La gouvernance des espaces de distribution.

Il faudra notamment éviter plusieurs hypothèses qui pourraient réduire le périmètre du produit :

- Ne pas supposer que toutes les ressources doivent être distribuées sous forme de paquets.
- Ne pas supposer que toutes les ressources doivent être récupérées par copie de fichiers.
- Ne pas supposer qu'une bibliothèque entière doit être récupérée pour utiliser un composant.
- Ne pas supposer qu'une ressource publiée est nécessairement publique.
- Ne pas supposer qu'une copie locale reste identique à sa version d'origine.
- Ne pas supposer que les mises à jour peuvent remplacer automatiquement les personnalisations.
- Ne pas supposer que toutes les ressources provenant de sources différentes ont les mêmes conditions de redistribution.
- Ne pas supposer qu'une ressource compatible avec un environnement l'est automatiquement avec tous les autres.

Les choix techniques et les modalités d'implémentation devront être examinés ultérieurement. Cette session exprime les capacités et les garanties attendues, sans imposer de technologies ou d'architecture particulière.


