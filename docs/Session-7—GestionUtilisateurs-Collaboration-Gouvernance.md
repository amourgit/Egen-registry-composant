# SESSION 7/8 — Gestion des utilisateurs, collaboration, gouvernance, espaces de travail et exploitation collective du patrimoine logiciel

## 1. Objectif général de cette session

La plateforme doit pouvoir être utilisée aussi bien par une personne travaillant seule que par plusieurs utilisateurs, équipes ou organisations qui souhaitent gérer, enrichir, personnaliser et distribuer collectivement des ressources logicielles.

Il ne s'agit donc pas uniquement de permettre à plusieurs personnes de se connecter à un même environnement. Le besoin est de rendre possible une véritable exploitation collective du patrimoine logiciel, dans laquelle les ressources, les bibliothèques, les collections, les systèmes de design, les projets et les publications peuvent être partagés, administrés et faire l'objet de contributions maîtrisées.

Cette dimension collective doit rester cohérente avec les besoins définis dans les sessions précédentes. Une ressource possède une identité, une origine, des versions, des dépendances, des personnalisations et un historique. Lorsqu'elle est utilisée par plusieurs personnes, ces informations doivent rester compréhensibles et exploitables. Les contributions ne doivent pas effacer la provenance d'une ressource, les modifications ne doivent pas rendre les responsabilités indéterminées et le partage ne doit pas entraîner une perte de maîtrise sur le patrimoine.

La plateforme doit ainsi répondre à plusieurs situations :

- Une personne gère seule sa bibliothèque de composants et ses ressources.
- Plusieurs personnes travaillent dans un même espace de travail.
- Une équipe développe et entretient une bibliothèque commune.
- Plusieurs équipes d'une même organisation disposent de patrimoines distincts, mais peuvent partager certaines ressources.
- Une organisation possède un catalogue interne et souhaite publier certaines ressources dans un registre accessible à d'autres utilisateurs.
- Plusieurs organisations collaborent autour de ressources communes sans nécessairement partager l'intégralité de leurs patrimoines.
- Des utilisateurs externes peuvent consulter ou consommer certaines ressources sans disposer des droits nécessaires pour les modifier.
- Des responsables peuvent examiner, approuver ou refuser des contributions avant leur intégration dans une bibliothèque de référence ou leur publication.

L'ensemble doit être conçu autour d'un principe fondamental : **le partage des ressources, la collaboration et la gouvernance doivent être possibles sans supprimer la maîtrise des propriétaires sur leurs patrimoines.**

---

## 2. Gestion des utilisateurs et des comptes

### 2.1. Gestion des utilisateurs

La plateforme doit permettre de gérer les personnes qui utilisent ses fonctionnalités, qu'elles interviennent individuellement ou dans le cadre d'une équipe ou d'une organisation.

Chaque utilisateur doit disposer d'un espace personnel lui permettant de retrouver les ressources auxquelles il a accès, ses bibliothèques personnelles, ses collections, ses projets, ses contributions et les activités qui le concernent.

L'identité d'un utilisateur doit être distinguée des espaces dans lesquels il travaille. Une même personne peut intervenir dans plusieurs équipes ou organisations, avec des responsabilités et des autorisations différentes selon le contexte.

Par exemple, une personne peut être propriétaire de sa bibliothèque personnelle, contributeur dans une équipe de développement et simple lecteur dans une autre organisation. Ces situations ne doivent pas être confondues ni conduire à lui attribuer automatiquement les mêmes droits partout.

### 2.2. Profil utilisateur

Chaque utilisateur doit disposer d'un profil permettant de présenter les informations nécessaires à son identification dans les activités collaboratives.

Le profil peut notamment permettre de retrouver :

- Le nom ou le nom d'affichage.
- Une photo ou un avatar, lorsque cette information est renseignée.
- Une description facultative.
- Les espaces ou équipes auxquels la personne participe, selon les règles de visibilité applicables.
- Les contributions qui peuvent être rendues visibles.
- Les responsabilités qu'elle exerce dans les espaces concernés.

Les informations personnelles ne doivent pas être automatiquement exposées à tous les utilisateurs. Leur visibilité doit dépendre des règles de confidentialité et du contexte de consultation.

### 2.3. Gestion des accès aux comptes

La plateforme doit permettre de gérer les conditions d'accès aux comptes et les situations dans lesquelles un utilisateur ne peut plus intervenir normalement.

Il doit notamment être possible de prendre en compte :

- L'activation ou la désactivation d'un compte.
- La suspension temporaire d'un accès.
- La récupération d'un accès.
- Le changement de certaines informations de compte.
- La fin de participation d'un utilisateur à un espace ou à une organisation.
- La révocation des accès précédemment accordés.

La désactivation d'un compte ne doit pas provoquer automatiquement la suppression des ressources ou des contributions produites par son utilisateur. Les ressources doivent conserver leur historique et leur traçabilité, même lorsque leur auteur n'est plus actif.

Cette distinction est importante : le compte représente une personne qui accède à la plateforme, tandis que les ressources et les contributions produites constituent des éléments du patrimoine qui doivent pouvoir continuer à être gérés.

---

## 3. Gestion des équipes et des organisations

### 3.1. Distinction entre utilisateur, équipe et organisation

La plateforme doit distinguer clairement trois notions.

**L'utilisateur** représente une personne qui accède à la plateforme et intervient sur des ressources.

**L'équipe** représente un groupe de personnes qui travaillent ensemble autour d'un ensemble de ressources, de bibliothèques, de collections ou de projets.

**L'organisation** représente un cadre collectif plus large, qui peut regrouper plusieurs équipes, des espaces de travail et des patrimoines logiciels soumis à des règles communes.

Ces notions ne doivent pas être confondues. Une équipe peut être utilisée indépendamment d'une organisation, et une organisation peut réunir plusieurs équipes ayant des responsabilités distinctes.

La plateforme doit permettre de s'adapter à ces différentes formes d'utilisation sans obliger tous les utilisateurs à adopter une structure organisationnelle complexe.

### 3.2. Création et gestion des organisations

Un utilisateur autorisé doit pouvoir créer ou administrer un espace organisationnel destiné à regrouper les activités de plusieurs personnes.

Une organisation doit pouvoir disposer de ses propres informations descriptives, de ses membres, de ses équipes, de ses espaces de travail et des ressources qu'elle possède ou qu'elle est autorisée à gérer.

Elle doit également pouvoir définir ses propres règles de fonctionnement, notamment en ce qui concerne :

- Les personnes autorisées à rejoindre l'organisation.
- Les responsabilités attribuées aux membres.
- Les conditions de création et de gestion des bibliothèques.
- Les modalités de contribution aux ressources communes.
- Les conditions de validation des modifications.
- Les personnes autorisées à publier des ressources.
- Les règles de partage avec des personnes extérieures.
- Les conditions de consultation des informations internes.

Ces règles doivent pouvoir être adaptées aux besoins de l'organisation, sans imposer un fonctionnement identique à une petite équipe et à une structure regroupant plusieurs départements.

### 3.3. Création et gestion des équipes

Une organisation doit pouvoir regrouper ses membres en équipes selon ses besoins réels.

Une équipe peut être constituée autour d'une activité, d'un domaine de compétences, d'un produit, d'un projet ou d'un ensemble de ressources.

Par exemple, une organisation peut avoir plusieurs équipes chargées respectivement :

- Des composants d'interface.
- Des systèmes de design.
- Des bibliothèques destinées à des applications particulières.
- Des ressources partagées entre plusieurs projets.
- De la documentation et de la maintenance des ressources existantes.

Ces exemples représentent des possibilités d'organisation du travail, et non des catégories obligatoires.

Une équipe doit pouvoir posséder ou gérer un ensemble de ressources, participer à l'entretien d'une bibliothèque commune et collaborer avec d'autres équipes lorsque des ressources sont partagées.

### 3.4. Appartenance multiple

Un même utilisateur doit pouvoir appartenir à plusieurs équipes et organisations, dans la limite des autorisations qui lui sont accordées.

Son appartenance à une organisation ne doit pas lui donner automatiquement accès à toutes les ressources d'une autre organisation à laquelle il participe également.

Les droits doivent être évalués dans leur contexte. Une personne peut être responsable d'une bibliothèque dans une organisation et ne disposer que d'un accès en consultation à une bibliothèque appartenant à une autre.

La plateforme doit rendre ces appartenances compréhensibles afin d'éviter les confusions entre les différents espaces de travail.

---

## 4. Espaces de travail et séparation des patrimoines

### 4.1. Gestion de plusieurs espaces

La plateforme doit permettre à un utilisateur, une équipe ou une organisation de travailler dans plusieurs espaces distincts.

Un espace de travail constitue un contexte dans lequel sont regroupées les ressources, bibliothèques, collections, projets, activités et règles de collaboration correspondant à un besoin déterminé.

Il ne doit pas être considéré comme une simple catégorie de classement. Il doit permettre de définir un périmètre de travail et de partage.

Un utilisateur peut ainsi disposer :

- D'un espace personnel.
- D'un espace de travail partagé avec une équipe.
- D'un espace associé à une organisation.
- D'un espace consacré à un projet particulier.
- D'un espace de collaboration avec des personnes externes.

Ces espaces doivent pouvoir coexister sans que leurs contenus soient automatiquement mélangés.

### 4.2. Séparation des patrimoines

La plateforme doit garantir une distinction claire entre les ressources personnelles, les ressources appartenant à une équipe, les ressources gérées par une organisation et les ressources accessibles par partage.

Cette distinction doit être maintenue dans les opérations de consultation, de modification, de duplication, de transfert et de publication.

Par exemple, lorsqu'un utilisateur partage une ressource personnelle avec une équipe, cela ne signifie pas nécessairement que cette équipe devient propriétaire de la ressource. Elle peut simplement recevoir un droit de consultation ou de contribution.

De la même manière, une ressource appartenant à une organisation ne doit pas devenir automatiquement une ressource personnelle lorsqu'un membre la récupère dans son propre espace.

La plateforme doit donc distinguer explicitement :

- La propriété d'une ressource.
- La responsabilité de sa maintenance.
- Le droit de la consulter.
- Le droit de la modifier.
- Le droit de la dupliquer.
- Le droit de la partager.
- Le droit de la publier.
- Le droit de la retirer d'un espace ou d'un registre.

Ces droits peuvent être accordés à des personnes, à des équipes ou à des organisations, selon les règles définies par le propriétaire ou les responsables autorisés.

### 4.3. Partage entre espaces

Une ressource, une collection ou une bibliothèque doit pouvoir être partagée entre plusieurs espaces lorsque cela est autorisé.

Ce partage doit préserver l'identité et l'origine de l'élément partagé.

Il doit également permettre de comprendre si l'espace destinataire consulte la ressource originale, utilise une copie indépendante ou travaille sur une version partagée dont les modifications peuvent être visibles par les autres participants.

La plateforme doit éviter qu'une opération de partage crée des ambiguïtés sur la propriété, les responsabilités ou les conséquences des modifications.

### 4.4. Déplacement et transfert

La plateforme doit distinguer le partage d'une ressource de son déplacement et de son transfert.

Le partage accorde un accès sans nécessairement modifier la propriété.

Le déplacement change son emplacement ou son espace de rattachement, dans les conditions autorisées.

Le transfert peut modifier la responsabilité ou la propriété de la ressource, lorsque cette opération est permise.

Ces opérations doivent être clairement identifiées et leur conséquence doit être compréhensible avant leur réalisation.

Un transfert ne doit pas entraîner la disparition de l'historique, des versions, des informations de provenance ou des dépendances de la ressource.

---

## 5. Gestion des rôles, responsabilités et permissions

### 5.1. Principe général

La plateforme doit permettre de déterminer précisément ce qu'un utilisateur peut consulter, créer, modifier, supprimer, partager, valider ou publier.

Il ne suffit pas de distinguer un administrateur d'un utilisateur ordinaire. Les responsabilités liées à la gestion d'un patrimoine logiciel sont suffisamment différentes pour nécessiter une gestion plus précise des permissions.

Les droits doivent être adaptés aux ressources et aux opérations concernées.

Un utilisateur peut, par exemple, être autorisé à modifier un composant sans être autorisé à publier une nouvelle version de la bibliothèque dans laquelle il se trouve.

### 5.2. Catégories de responsabilités

La plateforme doit pouvoir prendre en compte plusieurs types de responsabilités, sans imposer que chaque organisation utilise obligatoirement toutes ces catégories.

**Propriétaire**

Le propriétaire est la personne ou l'entité à laquelle appartient une ressource, une bibliothèque ou un patrimoine donné. Il dispose des responsabilités associées à cette propriété, dans les limites des règles applicables.

**Administrateur**

L'administrateur intervient dans la gestion d'un espace, d'une équipe ou d'une organisation. Il peut gérer les membres, les autorisations et les règles de fonctionnement qui relèvent de son périmètre.

**Responsable de ressource ou de bibliothèque**

Cette personne assure le suivi d'un ensemble de ressources. Elle peut être chargée de leur entretien, de leur documentation, de leur cohérence et de leur évolution.

**Contributeur**

Le contributeur participe à la création, à la modification, à la documentation ou à l'amélioration des ressources selon les autorisations accordées.

**Réviseur**

Le réviseur examine les modifications proposées, vérifie leur cohérence et formule des observations avant leur intégration éventuelle.

**Approbateur**

L'approbateur dispose de la responsabilité de valider ou de refuser certaines opérations soumises à validation, conformément aux règles de l'espace concerné.

**Lecteur**

Le lecteur peut consulter les éléments auxquels il a accès sans disposer automatiquement de droits de modification.

**Consommateur**

Le consommateur utilise une ressource distribuée dans un projet ou un environnement donné. Son droit de consommation ne lui confère pas automatiquement des droits sur le patrimoine source.

Ces responsabilités ne doivent pas être considérées comme une hiérarchie universelle. Une même personne peut exercer plusieurs responsabilités, tandis qu'une organisation peut répartir ces fonctions entre plusieurs personnes.

### 5.3. Permissions détaillées

La plateforme doit permettre de gérer les autorisations de manière suffisamment précise pour couvrir les différentes opérations du cycle de vie des ressources.

Les permissions doivent notamment pouvoir concerner :

- La consultation des ressources.
- La consultation des fichiers sources.
- La création de ressources.
- La modification des ressources.
- La création de variantes.
- La duplication des ressources.
- La gestion des versions.
- La suppression ou l'archivage.
- La gestion des collections.
- La gestion des bibliothèques.
- La gestion des dépendances.
- La modification de la documentation.
- Le partage avec d'autres utilisateurs.
- La gestion des membres.
- La validation des contributions.
- La publication dans un registre.
- La gestion des versions publiées.
- Le retrait ou la dépréciation d'une ressource.

La plateforme doit éviter de confondre les droits de consultation, de contribution et d'administration.

### 5.4. Attribution et révocation des permissions

Les responsables autorisés doivent pouvoir accorder, modifier ou retirer des permissions.

Il doit être possible de comprendre qui a accordé une autorisation, à qui elle a été accordée, sur quel périmètre elle porte et quelles opérations elle permet.

La révocation d'une permission doit empêcher les nouvelles opérations non autorisées sans supprimer automatiquement les contributions antérieures de la personne concernée.

La plateforme doit également permettre de vérifier les accès encore actifs afin de limiter les autorisations devenues inutiles.

### 5.5. Permissions héritées et exceptions

Les organisations peuvent souhaiter appliquer des règles communes à plusieurs équipes ou espaces.

La plateforme doit pouvoir prendre en compte cette situation, tout en permettant de définir des autorisations particulières lorsque cela est nécessaire.

Il faut notamment éviter qu'une permission accordée dans un espace soit interprétée comme une autorisation générale sur l'ensemble du patrimoine.

Les éventuelles règles héritées, restrictions et exceptions doivent rester compréhensibles pour les administrateurs.

---

## 6. Collaboration autour des ressources

### 6.1. Collaboration sur une ressource existante

Plusieurs utilisateurs doivent pouvoir participer à l'amélioration d'une même ressource.

La collaboration peut porter sur différents aspects :

- Le code source.
- La structure des fichiers.
- Les propriétés et les comportements.
- L'apparence visuelle.
- Les variantes.
- Les dépendances.
- La documentation.
- Les exemples d'utilisation.
- Les informations de provenance.
- Les éléments nécessaires à sa distribution.

La plateforme doit permettre de comprendre quelles parties ont été modifiées, par qui et dans quel contexte.

Les contributions doivent pouvoir être examinées sans que les autres utilisateurs perdent la possibilité de consulter l'état de référence de la ressource.

### 6.2. Modifications simultanées

La plateforme doit prendre en compte les situations dans lesquelles plusieurs personnes interviennent sur une même ressource au même moment.

Elle doit permettre de distinguer les modifications réalisées par différents contributeurs et d'éviter qu'une intervention écrase silencieusement le travail d'une autre personne.

Lorsqu'il existe un risque de conflit, les utilisateurs concernés doivent être informés de la situation et disposer d'informations suffisantes pour comprendre les modifications concurrentes.

La plateforme doit notamment permettre de gérer les situations suivantes :

- Deux utilisateurs modifient le même fichier.
- Deux utilisateurs modifient des fichiers différents d'une même ressource.
- Plusieurs personnes modifient une même propriété ou configuration.
- Une modification intervient pendant qu'une autre personne examine une version précédente.
- Une ressource est modifiée alors qu'une proposition de contribution est encore en attente.
- Une version de référence évolue pendant qu'un contributeur travaille sur une version dérivée.

La résolution de ces situations doit préserver les modifications pertinentes et permettre de retrouver les états antérieurs.

### 6.3. Travail parallèle

Les utilisateurs doivent pouvoir travailler sur des évolutions différentes sans être obligés de modifier directement la même version de référence.

Cela concerne notamment la création de variantes, les expérimentations, les améliorations indépendantes et les propositions de modification.

Il doit être possible de distinguer :

- La version de référence.
- Le travail en cours.
- Les propositions de modification.
- Les versions expérimentales.
- Les modifications acceptées.
- Les modifications refusées ou abandonnées.

Cette séparation est importante pour permettre à plusieurs personnes de contribuer sans rendre instable le patrimoine commun.

### 6.4. Comparaison des contributions

Avant d'intégrer une modification, les personnes chargées de l'examiner doivent pouvoir comprendre précisément ce qui a changé.

La comparaison doit pouvoir porter sur les fichiers sources, les structures, les propriétés, les dépendances, les variantes et la documentation.

Lorsque cela est pertinent, la plateforme doit également permettre de comparer le rendu visuel avant et après modification.

Une contribution ne doit pas être présentée uniquement comme un ensemble de fichiers modifiés lorsque son impact concerne également le comportement ou l'apparence d'un composant.

L'objectif est de permettre une évaluation suffisamment complète pour éviter d'accepter une modification dont les conséquences ne sont pas comprises.

---

## 7. Contributions, propositions de modification et validation

### 7.1. Contribution structurée

La plateforme doit permettre à un utilisateur de proposer une modification sur une ressource qu'il est autorisé à consulter ou à utiliser, même lorsque ses droits ne lui permettent pas de modifier directement la version de référence.

Cette possibilité est importante dans les bibliothèques partagées et les patrimoines gérés collectivement.

Une contribution doit pouvoir être accompagnée d'une description expliquant :

- Son objectif.
- Le problème qu'elle cherche à résoudre.
- Les éléments concernés.
- Les changements effectués.
- Les conséquences attendues.
- Les éventuelles dépendances ou contraintes.
- Les éléments nécessitant une vérification particulière.

Le contributeur doit pouvoir fournir des explications suffisantes pour que les autres participants comprennent l'intérêt de sa proposition.

### 7.2. Examen des contributions

Les responsables ou réviseurs autorisés doivent pouvoir examiner les propositions reçues.

L'examen ne doit pas se limiter à l'acceptation ou au refus d'une modification. Il doit permettre de formuler des observations, de demander des corrections et de signaler les problèmes identifiés.

Les points examinés peuvent notamment concerner :

- La cohérence avec l'objectif de la ressource.
- La qualité du code.
- La compatibilité avec les environnements visés.
- Les dépendances ajoutées ou modifiées.
- Les éventuelles régressions.
- La cohérence avec les autres ressources de la bibliothèque.
- Le respect des règles de contribution.
- La documentation.
- La provenance et les conditions de licence.

### 7.3. Décisions sur les contributions

La plateforme doit permettre de représenter clairement les différents états d'une proposition.

Une contribution peut notamment être :

- En préparation.
- Soumise.
- En cours de révision.
- En attente de précisions.
- Modifiée par son auteur.
- Approuvée.
- Refusée.
- Intégrée.
- Abandonnée.

Ces états doivent permettre de comprendre où en est une contribution et quelle action est attendue.

La plateforme doit conserver la décision prise et les informations utiles permettant de comprendre cette décision.

### 7.4. Règles de validation

Une organisation doit pouvoir déterminer quelles modifications peuvent être intégrées directement et lesquelles nécessitent une validation.

Toutes les ressources ne présentent pas le même niveau d'importance. Une petite correction documentaire ne nécessite pas nécessairement les mêmes contrôles qu'une modification importante d'un composant partagé par de nombreux projets.

Les règles de validation doivent donc pouvoir être adaptées au contexte.

Il doit être possible de définir des responsabilités d'approbation, de prévoir plusieurs niveaux d'examen lorsque cela est nécessaire et de distinguer la personne qui propose une modification de celle qui l'approuve.

La plateforme doit éviter les validations ambiguës, notamment lorsqu'une personne réalise une modification et l'approuve elle-même alors que les règles de l'organisation prévoient une séparation des responsabilités.

### 7.5. Intégration dans le patrimoine de référence

Lorsqu'une contribution est acceptée, son intégration doit être identifiable dans l'historique de la ressource.

La plateforme doit conserver les informations sur son auteur, les personnes ayant participé à sa révision, la décision prise et la version de référence concernée.

Une contribution acceptée ne doit pas perdre son lien avec la proposition d'origine.

De cette manière, il reste possible de comprendre comment une ressource a évolué et pourquoi certaines décisions ont été prises.

---

## 8. Commentaires, annotations et échanges contextuels

### 8.1. Commentaires associés aux ressources

Les utilisateurs doivent pouvoir échanger autour des ressources sans être obligés de quitter leur contexte de travail.

Les commentaires peuvent porter sur une ressource dans son ensemble, une version particulière, un fichier, une modification proposée ou un élément de documentation.

L'objectif est de conserver les discussions à proximité des éléments auxquels elles se rapportent.

Un commentaire général sur un composant ne doit pas être confondu avec une observation portant sur une modification précise d'un fichier.

### 8.2. Annotations sur les éléments techniques et visuels

Lorsque cela est pertinent, la plateforme doit permettre d'associer une observation à une partie précise d'un élément.

Cela peut concerner une portion de code, une propriété, une zone d'une interface, un comportement ou une partie de la documentation.

Pour les ressources visuelles, il peut être utile de pouvoir formuler des observations sur des éléments précis du rendu.

Ces annotations doivent conserver leur contexte autant que possible. Lorsqu'une modification rend une annotation obsolète, la plateforme doit permettre de comprendre que l'observation concernait un état antérieur.

### 8.3. Discussions et suivi des échanges

Les échanges doivent pouvoir être organisés de manière à conserver le contexte des discussions.

La plateforme doit permettre de répondre à un commentaire, de suivre une discussion et d'identifier les interventions des différents participants.

Il doit également être possible de distinguer les observations encore ouvertes de celles qui ont été traitées ou résolues.

Les commentaires ne doivent pas remplacer l'historique des modifications ni les décisions officielles de validation. Ils constituent un espace d'échange complémentaire.

### 8.4. Documentation collaborative

Plusieurs utilisateurs doivent pouvoir contribuer à la documentation des ressources.

Les contributions documentaires doivent pouvoir être examinées et conservées dans l'historique, au même titre que les autres modifications.

Cela concerne notamment les descriptions, les instructions d'installation, les exemples d'utilisation, les explications des propriétés, les notes de version et les informations relatives aux dépendances.

La documentation doit pouvoir être associée à la version concernée afin d'éviter de présenter des informations anciennes comme si elles décrivaient nécessairement la version actuelle.

---

## 9. Gouvernance du patrimoine logiciel

### 9.1. Principe de gouvernance

La gouvernance représente l'ensemble des règles, responsabilités et décisions qui encadrent la gestion du patrimoine logiciel.

La plateforme doit permettre à chaque espace collectif de définir comment ses ressources sont créées, entretenues, modifiées, validées, partagées et publiées.

Cette gouvernance doit rester proportionnée aux besoins de l'espace concerné.

Une bibliothèque personnelle peut être gérée librement par son propriétaire. Une bibliothèque partagée par plusieurs équipes peut nécessiter des responsables, des règles de contribution et des validations. Un patrimoine organisationnel important peut nécessiter une répartition plus précise des responsabilités.

La plateforme ne doit pas imposer un processus unique à tous les utilisateurs.

### 9.2. Propriété et responsabilité de maintenance

La propriété d'une ressource et sa maintenance doivent être distinguées.

Une organisation peut être propriétaire d'une bibliothèque tout en confiant la maintenance de certains composants à différentes équipes.

De la même manière, un utilisateur peut être l'auteur initial d'une ressource sans rester responsable de son entretien pendant toute sa durée de vie.

La plateforme doit permettre d'identifier les responsables actuels d'une ressource, tout en conservant les informations historiques sur ses auteurs et contributeurs.

Il doit être possible de modifier les responsabilités de maintenance sans effacer l'historique des contributions.

### 9.3. Règles de contribution

Les responsables d'un patrimoine doivent pouvoir définir les conditions dans lesquelles les membres peuvent proposer des modifications.

Ces règles peuvent préciser les informations attendues, les vérifications nécessaires, les responsabilités de révision et les conditions d'intégration.

Elles doivent pouvoir être communiquées aux contributeurs avant qu'ils soumettent leurs modifications.

La plateforme doit également permettre de conserver les règles applicables à un moment donné lorsque cela est nécessaire pour comprendre le traitement historique d'une contribution.

### 9.4. Gouvernance des bibliothèques et collections

Les bibliothèques et collections doivent pouvoir être gérées collectivement.

Les responsables doivent pouvoir déterminer :

- Qui peut ajouter une ressource.
- Qui peut modifier une ressource existante.
- Qui peut créer ou modifier une collection.
- Qui peut retirer une ressource d'une bibliothèque.
- Qui peut gérer les versions de référence.
- Qui peut valider une modification.
- Qui peut rendre une bibliothèque accessible à d'autres espaces.
- Qui peut publier son contenu.

Ces responsabilités doivent pouvoir être attribuées sans obliger une seule personne à gérer toutes les opérations.

### 9.5. Gouvernance des publications

La publication d'une ressource doit être considérée comme une opération distincte de sa modification.

Une personne peut être autorisée à contribuer à une bibliothèque sans avoir le droit de publier ses ressources dans un registre.

Les responsables doivent pouvoir définir les conditions préalables à une publication : version identifiée, documentation suffisante, dépendances connues, licence vérifiée et validations nécessaires.

Les publications doivent conserver leur lien avec le patrimoine dont elles proviennent.

La gouvernance doit également prendre en compte les retraits, les dépréciations, les changements de responsables et la continuité des versions déjà distribuées.

Ces exigences prolongent directement les besoins de la session 6 sur la distribution et la consommation des ressources.

---

## 10. Partage de bibliothèques entre équipes et organisations

### 10.1. Bibliothèques communes

Plusieurs équipes doivent pouvoir utiliser une même bibliothèque lorsque cela correspond à leur activité.

Cette bibliothèque peut contenir des composants, des variantes, des ressources techniques, des systèmes de design ou des collections.

Les équipes utilisatrices doivent pouvoir consulter les ressources et, lorsque cela est autorisé, proposer des améliorations.

Le partage doit permettre de mutualiser les efforts de création et de maintenance sans rendre la gestion de la bibliothèque incontrôlable.

### 10.2. Partage entre organisations distinctes

La plateforme doit pouvoir prendre en charge des collaborations entre organisations indépendantes.

Une organisation peut mettre certaines ressources à disposition d'une autre organisation sans ouvrir l'ensemble de son patrimoine.

Le partage doit préciser son périmètre, ses bénéficiaires et les droits accordés.

Il doit être possible de donner accès à une bibliothèque en consultation, d'autoriser certaines contributions ou de distribuer des ressources sans autoriser la modification du patrimoine d'origine.

### 10.3. Ressources communes et ressources privées

Dans un espace partagé, toutes les ressources ne doivent pas nécessairement avoir la même visibilité.

Certaines peuvent être communes à tous les membres autorisés, tandis que d'autres peuvent rester privées ou limitées à une équipe.

La plateforme doit permettre de distinguer clairement ces situations.

Un utilisateur ne doit pas pouvoir déduire qu'une ressource est accessible à tous simplement parce qu'elle apparaît dans un espace partagé.

### 10.4. Contributions externes

Une organisation doit pouvoir recevoir des contributions de personnes qui ne sont pas membres permanents de son espace.

Cette situation peut notamment se présenter lorsqu'une ressource est partagée avec une communauté externe ou lorsqu'un partenaire propose une amélioration.

Les contributions externes doivent être soumises à des règles explicites.

La possibilité de proposer une modification ne doit pas entraîner automatiquement un accès général à la bibliothèque ou aux informations internes de l'organisation.

---

## 11. Invitations, adhésions et départ des membres

### 11.1. Invitations

Les responsables autorisés doivent pouvoir inviter des utilisateurs à rejoindre un espace, une équipe ou une organisation.

L'invitation doit préciser le contexte dans lequel la personne est invitée et, lorsque cela est prévu, le rôle ou les droits qui lui seront attribués.

La plateforme doit permettre de distinguer les invitations en attente, acceptées, refusées ou expirées.

Une invitation à rejoindre une organisation ne doit pas être interprétée comme une autorisation d'accès illimitée à tous ses patrimoines.

### 11.2. Demandes d'adhésion

Selon les règles de l'espace, les utilisateurs peuvent être autorisés à demander leur intégration dans une équipe ou une organisation.

Les responsables doivent pouvoir examiner ces demandes et prendre une décision.

La plateforme doit conserver un état compréhensible de la demande et permettre à la personne concernée de connaître son résultat lorsque les règles de visibilité le permettent.

### 11.3. Modification des appartenances

Les responsables autorisés doivent pouvoir modifier l'appartenance d'un utilisateur à une équipe ou à un espace.

Cette opération peut entraîner une modification de ses permissions, mais ne doit pas supprimer les contributions réalisées auparavant.

Les changements d'appartenance doivent être traçables.

### 11.4. Départ d'un membre

Lorsqu'un utilisateur quitte une équipe ou une organisation, la plateforme doit permettre de retirer ses accès tout en préservant les ressources et les informations nécessaires à la continuité du travail.

Il faut notamment prendre en compte :

- Les ressources dont il est propriétaire.
- Les ressources dont il assure la maintenance.
- Les contributions en cours.
- Les propositions de modification non traitées.
- Les bibliothèques dont il est responsable.
- Les publications dont il assure le suivi.
- Les projets consommateurs associés à ses activités.

La plateforme doit permettre d'organiser la reprise des responsabilités par d'autres personnes autorisées.

Le départ d'un utilisateur ne doit pas provoquer la disparition d'une bibliothèque, la perte de ses versions ou l'abandon involontaire d'une ressource importante.

### 11.5. Transfert de responsabilités

Les responsables doivent pouvoir transférer certaines responsabilités à un autre utilisateur ou à une équipe.

Le transfert doit être identifiable et traçable.

Il doit être possible de distinguer le responsable actuel de la personne qui a précédemment assuré cette responsabilité.

L'historique des auteurs, des contributeurs et des décisions doit rester intact.

---

## 12. Traçabilité des activités et historique des décisions

### 12.1. Historique des actions

La plateforme doit conserver les informations nécessaires pour comprendre les activités réalisées sur le patrimoine collectif.

Les événements importants doivent pouvoir être associés à leur auteur, leur date, leur contexte et leur objet.

Cela concerne notamment :

- La création d'une ressource.
- La modification d'une ressource.
- La création d'une version.
- La suppression ou l'archivage.
- Le partage ou le retrait d'un partage.
- La modification des permissions.
- L'arrivée ou le départ d'un membre.
- La création ou la modification d'une bibliothèque.
- La soumission d'une contribution.
- L'approbation ou le refus d'une proposition.
- La publication ou le retrait d'une version.
- Le transfert d'une responsabilité.

L'objectif est de pouvoir comprendre ce qui s'est passé, et non de produire uniquement une liste de notifications.

### 12.2. Historique des décisions

Les décisions de gouvernance doivent pouvoir être retrouvées.

Lorsqu'une contribution est refusée, une ressource est dépréciée ou une publication est retirée, il doit être possible de retrouver les informations disponibles sur la décision et son contexte.

Cette traçabilité permet de comprendre l'évolution du patrimoine et d'éviter que les mêmes questions soient systématiquement reprises sans tenir compte des décisions antérieures.

### 12.3. Consultation de l'activité

Les utilisateurs doivent pouvoir consulter les activités qui concernent leurs espaces et les ressources auxquelles ils ont accès.

Les responsables doivent disposer d'une vision adaptée à leurs responsabilités.

La consultation de l'activité doit respecter les permissions : un utilisateur ne doit pas accéder à des informations confidentielles simplement parce qu'elles apparaissent dans un journal global.

### 12.4. Conservation de l'historique

L'historique des activités doit rester cohérent avec les exigences de conservation du patrimoine définies dans la session 3.

La suppression d'un compte, le départ d'un membre ou le changement de propriétaire ne doit pas rendre incompréhensibles les anciennes contributions.

La plateforme doit également permettre de distinguer les événements réellement effectués des informations qui ont été modifiées ultérieurement.

---

## 13. Notifications et suivi des activités collaboratives

### 13.1. Notifications utiles

La plateforme doit permettre aux utilisateurs d'être informés des événements qui nécessitent leur attention.

Les notifications peuvent notamment concerner :

- Une invitation reçue.
- Une demande d'adhésion.
- Une nouvelle contribution.
- Une demande de révision.
- Une observation formulée sur une contribution.
- Une décision d'approbation ou de refus.
- Une modification importante d'une ressource suivie.
- Un changement de responsabilité.
- Une modification des permissions.
- Une publication concernant une bibliothèque suivie.
- Une évolution importante d'une dépendance utilisée.

Les notifications doivent être liées à l'objet concerné afin que l'utilisateur puisse retrouver directement le contexte de l'événement.

### 13.2. Notifications adaptées aux responsabilités

Tous les utilisateurs ne doivent pas recevoir les mêmes notifications.

Un contributeur doit être informé des décisions concernant ses propositions. Un responsable de bibliothèque doit pouvoir suivre les événements importants de son périmètre. Un lecteur n'a pas nécessairement besoin de recevoir les notifications relatives à toutes les modifications internes.

La plateforme doit permettre de limiter les notifications inutiles et de distinguer les informations importantes des événements secondaires.

### 13.3. Suivi des ressources et des espaces

Les utilisateurs doivent pouvoir suivre certaines ressources, bibliothèques ou collections afin d'être informés de leurs évolutions.

Ce suivi doit être distinct d'une permission de modification.

Suivre une ressource signifie recevoir des informations sur son activité, et non obtenir automatiquement des droits supplémentaires.

### 13.4. Activité collective

Les espaces de travail doivent pouvoir présenter une activité collective permettant aux membres de comprendre les changements récents.

Cette activité doit rester pertinente et filtrable selon le périmètre autorisé.

Elle doit notamment permettre de retrouver les modifications récentes, les contributions en attente, les décisions et les événements importants concernant les ressources partagées.

---

## 14. Gestion des projets consommateurs dans un contexte collectif

### 14.1. Projets et responsabilités

Les ressources de la plateforme peuvent être consommées par plusieurs projets, éventuellement gérés par des équipes différentes.

La plateforme doit permettre d'identifier les projets qui utilisent les ressources d'une bibliothèque lorsque ces informations sont disponibles et que leur consultation est autorisée.

Cette visibilité est importante pour évaluer les conséquences d'une modification, d'une nouvelle version, d'une dépréciation ou d'un retrait.

### 14.2. Suivi collectif des dépendances

Une organisation doit pouvoir comprendre quelles ressources sont utilisées par ses différents projets.

Elle doit pouvoir identifier les ressources communes, les dépendances importantes et les situations dans lesquelles plusieurs projets reposent sur une même version.

Cette connaissance permet de mieux organiser les évolutions et de limiter les changements qui pourraient affecter involontairement plusieurs équipes.

### 14.3. Coordination des mises à jour

Lorsque plusieurs projets utilisent une même bibliothèque, les mises à jour doivent pouvoir être suivies dans leur contexte.

Les responsables doivent pouvoir comprendre quels projets sont concernés, quelles versions sont utilisées et quelles modifications pourraient nécessiter une adaptation.

La plateforme doit permettre de coordonner les décisions sans imposer que tous les projets adoptent automatiquement la même version au même moment.

### 14.4. Responsabilités entre producteurs et consommateurs

Les responsabilités du propriétaire d'une ressource doivent être distinguées de celles des équipes qui la consomment.

Le producteur peut être chargé de maintenir et de distribuer la ressource, tandis que les équipes consommatrices restent responsables de son intégration et de son utilisation dans leurs projets.

Cette distinction doit être conservée dans les informations de suivi afin d'éviter les confusions lorsqu'un problème survient.

---

## 15. Collaboration autour des licences et de la provenance

### 15.1. Préservation de la provenance collective

Lorsqu'une ressource est acquise, personnalisée ou enrichie par plusieurs personnes, la plateforme doit conserver les informations relatives à son origine et aux transformations réalisées.

Les contributions doivent pouvoir être reliées à leurs auteurs et aux versions concernées.

Cette exigence prolonge les règles de traçabilité définies dans la session 3.

### 15.2. Contributions issues de plusieurs sources

Une ressource composite peut réunir des éléments provenant de plusieurs sources.

La plateforme doit permettre de conserver les informations relatives à ces origines, même lorsque plusieurs contributeurs participent à sa composition.

Le fait qu'une organisation regroupe les éléments dans une bibliothèque commune ne doit pas effacer les conditions de licence applicables aux différentes parties.

### 15.3. Responsabilité des publications

Avant de publier une ressource issue de plusieurs contributions ou sources, les responsables autorisés doivent pouvoir consulter les informations de provenance et de licence disponibles.

La plateforme doit permettre de signaler les informations manquantes ou les situations qui nécessitent une vérification.

Elle ne doit pas présenter automatiquement une ressource comme librement redistribuable lorsque les conditions applicables ne sont pas établies.

---

## 16. Gouvernance et gestion des conflits

### 16.1. Conflits de modification

Les conflits peuvent résulter de modifications concurrentes, de versions divergentes ou de contributions incompatibles.

La plateforme doit permettre de les identifier et de présenter les éléments nécessaires à leur résolution.

La résolution doit préserver l'historique et permettre de comprendre quelle décision a été retenue.

### 16.2. Désaccords entre contributeurs

Plusieurs contributeurs peuvent proposer des solutions différentes à un même problème.

La plateforme doit permettre de documenter les propositions, les observations et les décisions sans mélanger les différentes versions de travail.

Les responsables autorisés doivent pouvoir arbitrer selon les règles de gouvernance définies dans l'espace concerné.

### 16.3. Désaccords sur la propriété ou la responsabilité

Des situations peuvent apparaître lorsqu'une ressource a été créée dans un espace, puis développée par plusieurs équipes ou transférée vers une organisation.

La plateforme doit conserver les informations relatives à sa propriété et à son historique afin de permettre de comprendre son statut.

Les opérations de transfert doivent être explicites et traçables.

### 16.4. Refus et contestations

Lorsqu'une contribution est refusée ou qu'une décision est prise concernant une ressource, les personnes concernées doivent pouvoir retrouver les informations disponibles sur cette décision.

Selon les règles de l'espace, un mécanisme de réexamen peut être prévu.

Il ne s'agit pas d'imposer une procédure de contestation à toutes les organisations, mais de permettre aux espaces qui en ont besoin de formaliser leur fonctionnement.

---

## 17. Expérience utilisateur dans un environnement collectif

### 17.1. Identification claire du contexte

L'utilisateur doit toujours pouvoir comprendre dans quel espace il travaille et à quel patrimoine appartient la ressource qu'il consulte.

La plateforme doit éviter les confusions entre une bibliothèque personnelle, une bibliothèque d'équipe et une bibliothèque appartenant à une organisation.

Les informations de contexte doivent être suffisamment visibles pour éviter les modifications accidentelles dans un espace collectif.

### 17.2. Compréhension des permissions

Avant une opération importante, l'utilisateur doit pouvoir comprendre s'il est autorisé à effectuer cette opération.

Lorsqu'une action est interdite, la plateforme doit expliquer clairement la limitation et, lorsque cela est pertinent, indiquer quelle responsabilité ou autorisation est nécessaire.

### 17.3. Visibilité des responsabilités

Les utilisateurs doivent pouvoir identifier les personnes ou équipes responsables d'une ressource, d'une bibliothèque ou d'une contribution.

Cette information facilite la collaboration et évite que plusieurs personnes supposent que quelqu'un d'autre assure la maintenance d'un élément.

### 17.4. Expérience adaptée à la taille du collectif

L'expérience ne doit pas devenir inutilement complexe pour une personne qui travaille seule.

Les fonctionnalités collectives doivent apparaître lorsque le contexte les rend nécessaires, sans imposer à chaque utilisateur de gérer des équipes, des organisations ou des processus de validation.

Inversement, les organisations qui gèrent des patrimoines importants doivent pouvoir disposer d'une vision suffisamment complète de leurs membres, de leurs responsabilités, de leurs ressources et de leurs activités.

---

## 18. Exigences fondamentales de cette session

La plateforme devra satisfaire les exigences suivantes :

1. Permettre une utilisation individuelle et collective.
2. Distinguer clairement les utilisateurs, les équipes, les organisations et les espaces de travail.
3. Permettre à une même personne de participer à plusieurs espaces avec des responsabilités différentes.
4. Préserver la séparation des patrimoines personnels, collectifs et organisationnels.
5. Permettre le partage contrôlé des ressources, collections et bibliothèques.
6. Distinguer la propriété, la maintenance, la consultation, la contribution et la publication.
7. Permettre une gestion précise des rôles et des permissions.
8. Préserver les ressources et les contributions lorsqu'un utilisateur quitte un espace.
9. Permettre le travail collaboratif sur une même ressource.
10. Prendre en compte les modifications simultanées et les travaux parallèles.
11. Permettre de comparer et d'examiner les contributions avant leur intégration.
12. Permettre des processus de révision et de validation adaptés aux besoins des espaces.
13. Conserver les commentaires, annotations et échanges dans leur contexte.
14. Permettre la gestion collective des bibliothèques et des collections.
15. Préserver les responsabilités et les décisions de gouvernance.
16. Conserver un historique exploitable des opérations importantes.
17. Informer les utilisateurs des événements qui nécessitent leur attention.
18. Permettre le partage entre organisations indépendantes sans ouverture générale des patrimoines.
19. Maintenir la traçabilité de la provenance et des licences lors des contributions collectives.
20. Permettre de suivre les projets qui consomment les ressources lorsque ces informations sont disponibles.
21. Faciliter la continuité de maintenance lorsqu'un responsable change.
22. Adapter les mécanismes de collaboration à la taille et aux règles de chaque espace.

---

## 19. Scénarios d'utilisation représentatifs

### Scénario 1 — Une personne travaillant seule

Un utilisateur crée son compte et commence à constituer une bibliothèque personnelle.

Il importe des composants provenant de différentes sources, conserve leurs codes sources et les personnalise. Il crée des variantes et organise ses ressources en collections.

À ce stade, il n'a pas besoin de créer une organisation ou une équipe. Il doit pouvoir bénéficier de toutes les fonctions essentielles de gestion et de personnalisation sans passer par des mécanismes de gouvernance collective.

### Scénario 2 — Une équipe développant une bibliothèque commune

Plusieurs développeurs travaillent au sein d'une équipe chargée de maintenir une bibliothèque de composants.

Certains membres peuvent modifier les ressources, d'autres examiner les contributions et les responsables autoriser les publications.

Un contributeur propose une amélioration. Un réviseur examine le code et la documentation, formule des observations et demande une correction. Le contributeur apporte les modifications nécessaires. La proposition est ensuite approuvée et intégrée à la version de référence.

L'ensemble des opérations reste traçable.

### Scénario 3 — Plusieurs équipes dans une même organisation

Une organisation possède plusieurs équipes qui travaillent sur des projets différents.

Chaque équipe gère certaines ressources, tandis que des bibliothèques communes sont accessibles à plusieurs équipes.

Les permissions sont adaptées aux responsabilités de chacune. Une équipe peut utiliser un composant partagé sans être autorisée à modifier directement sa version de référence.

Lorsqu'une amélioration est nécessaire, elle peut soumettre une contribution aux responsables de la bibliothèque.

### Scénario 4 — Collaboration entre organisations indépendantes

Une première organisation possède une bibliothèque qu'elle souhaite mettre à disposition d'une seconde organisation.

Elle autorise la consultation et la consommation des ressources, mais ne donne pas automatiquement accès à la gestion de son patrimoine.

La seconde organisation peut utiliser les ressources dans ses propres projets et, si cela est autorisé, proposer des améliorations.

Les deux organisations conservent leurs espaces, leurs responsabilités et leurs patrimoines respectifs.

### Scénario 5 — Départ du responsable d'une bibliothèque

Une personne responsable d'une bibliothèque quitte une organisation.

Ses accès sont révoqués, mais les ressources et les contributions qu'elle a produites restent disponibles.

L'organisation désigne un nouveau responsable, qui reprend le suivi de la bibliothèque et peut consulter son historique.

Les versions, publications et dépendances ne sont pas supprimées par le départ de l'ancien responsable.

### Scénario 6 — Modifications concurrentes

Deux contributeurs travaillent sur une même ressource.

Le premier modifie le comportement d'un composant tandis que le second intervient sur sa présentation. Leurs modifications peuvent être compatibles, mais elles doivent être examinées ensemble avant intégration.

Dans une autre situation, les deux contributeurs modifient la même partie du code et créent un conflit.

La plateforme doit rendre ces situations visibles, permettre la comparaison des modifications et préserver les états précédents jusqu'à la résolution.

### Scénario 7 — Publication soumise à validation

Une équipe dispose du droit de modifier une bibliothèque, mais seule une personne responsable peut publier une nouvelle version dans le registre organisationnel.

Un contributeur prépare une évolution, un réviseur l'examine et un approbateur autorisé valide son intégration.

La publication intervient ensuite dans le respect des responsabilités définies.

### Scénario 8 — Mutualisation d'un système de design

Une organisation maintient un système de design utilisé par plusieurs équipes.

Les ressources communes sont gérées dans une bibliothèque de référence. Les équipes peuvent consulter les composants, utiliser les variantes autorisées et proposer des améliorations.

Les modifications du système de design sont examinées en tenant compte des projets qui consomment les ressources concernées.

Cette organisation permet de mutualiser le travail sans imposer que toutes les équipes gèrent individuellement des copies indépendantes de chaque composant.

### Scénario 9 — Contribution externe à une ressource partagée

Une organisation rend une ressource accessible à des contributeurs externes.

Un utilisateur extérieur propose une amélioration, accompagnée d'une explication et des modifications correspondantes.

Les responsables de la ressource peuvent examiner la proposition sans donner à son auteur accès aux autres bibliothèques ou aux informations internes de l'organisation.

### Scénario 10 — Suivi des dépendances entre projets

Plusieurs projets d'une même organisation utilisent une bibliothèque commune.

Un responsable souhaite modifier une ressource importante.

Avant de valider cette évolution, il consulte les projets consommateurs identifiés, les versions utilisées et les éventuelles dépendances concernées.

Il peut ainsi organiser l'évolution de la bibliothèque en tenant compte des conséquences possibles sur les projets.

---

## 20. Résultat attendu

À l'issue de cette session, la plateforme doit être comprise comme un environnement capable de soutenir une collaboration structurée autour d'un patrimoine logiciel, depuis l'utilisation individuelle jusqu'à la gestion collective par plusieurs équipes et organisations.

Elle ne doit pas être limitée à un système de comptes et de permissions. Elle doit permettre d'organiser les responsabilités, de préserver les patrimoines, de coordonner les contributions, de suivre les décisions et de maintenir la continuité des ressources dans le temps.

Les utilisateurs doivent pouvoir collaborer sans perdre la maîtrise des ressources qu'ils possèdent ou administrent. Les organisations doivent pouvoir partager certaines bibliothèques sans exposer l'intégralité de leurs patrimoines. Les équipes doivent pouvoir contribuer à des ressources communes sans rendre leur évolution incontrôlable.

La collaboration doit également rester liée aux réalités techniques du produit : les fichiers sources, les versions, les dépendances, les variantes, les systèmes de design, les licences et les projets consommateurs doivent conserver leur cohérence dans les activités collectives.

**Le résultat recherché est un environnement dans lequel plusieurs personnes peuvent construire, maintenir, enrichir et partager un patrimoine logiciel commun, avec des responsabilités explicites, des droits maîtrisés, une traçabilité complète et une continuité indépendante des changements de membres ou d'organisation.**

---

## 21. Consignes pour l'analyse et la conception ultérieures

Les besoins de cette session doivent être pris en compte avec ceux des sessions précédentes.

Il ne faudra pas réduire la collaboration à une simple gestion des utilisateurs, ni supposer qu'un espace, une équipe ou une organisation doit nécessairement correspondre à une structure technique particulière.

Il faudra examiner les différentes situations d'utilisation et déterminer comment garantir la cohérence entre :

- Les comptes et les appartenances.
- Les espaces de travail et les patrimoines.
- Les rôles et les permissions.
- Les ressources et leurs propriétaires.
- Les contributions et les versions.
- Les révisions et les validations.
- Les bibliothèques partagées et les organisations indépendantes.
- Les publications et les responsabilités.
- Les projets consommateurs et les ressources distribuées.
- Les historiques et la continuité du patrimoine.

Aucune technologie, aucun protocole, aucun fournisseur et aucune architecture technique ne sont imposés par cette session.

Les solutions proposées ultérieurement devront démontrer comment elles répondent à ces besoins, comment elles préservent les distinctions conceptuelles présentées et comment elles permettent une évolution progressive sans rendre le fonctionnement collectif inutilement complexe.

La plateforme devra rester modulaire, extensible et adaptée aussi bien aux utilisateurs individuels qu'aux organisations qui gèrent un patrimoine logiciel important.
