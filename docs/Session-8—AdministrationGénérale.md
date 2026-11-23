# SESSION 8/8 — Administration générale, sécurité, exploitation, observabilité, qualité, fiabilité et pérennité de la plateforme

## 1. Objectif général de cette session

La plateforme doit être conçue pour fonctionner durablement, avec un niveau de maîtrise suffisant sur ses ressources, ses utilisateurs, ses opérations et ses évolutions.

Les sessions précédentes ont défini un environnement capable de récupérer des ressources logicielles provenant de différentes sources, de préserver leurs codes sources, de les personnaliser, de créer de nouvelles ressources, de les organiser en bibliothèques et collections, de les distribuer et de les partager entre plusieurs utilisateurs et organisations.

Cependant, ces capacités ne suffisent pas à définir un produit complet.

Il faut également pouvoir administrer l'ensemble, protéger les ressources et les données, contrôler les opérations sensibles, détecter les anomalies, diagnostiquer les erreurs, restaurer les éléments endommagés, suivre la qualité des ressources et garantir la continuité des activités.

La plateforme doit donc disposer de capacités d'administration et d'exploitation qui couvrent aussi bien son fonctionnement général que les activités quotidiennes de ses utilisateurs.

Elle doit notamment répondre aux situations suivantes :

- Un administrateur doit pouvoir comprendre l'état général de la plateforme et intervenir sur les éléments relevant de ses responsabilités.
- Une organisation doit pouvoir administrer ses membres, ses espaces, ses ressources et ses règles sans accéder aux patrimoines des autres organisations.
- Un utilisateur doit pouvoir retrouver ses ressources et ses travaux sans risquer de perdre ses modifications.
- Une opération interrompue ne doit pas laisser le patrimoine dans un état incohérent.
- Une erreur de manipulation ne doit pas entraîner automatiquement la perte définitive d'une ressource.
- Une ressource présentant un problème de dépendance, de compatibilité ou de qualité doit pouvoir être identifiée.
- Une mise à jour d'une ressource ne doit pas être présentée comme fiable sans vérifications adaptées.
- Les administrateurs doivent pouvoir comprendre les incidents et retracer les opérations importantes.
- La plateforme doit pouvoir évoluer sans remettre en cause les ressources et les données déjà constituées.

Le principe général est le suivant :

**La plateforme doit permettre de maîtriser son fonctionnement, de protéger son patrimoine, de comprendre ses incidents, de contrôler ses évolutions et de préserver la continuité des activités.**

---

# PARTIE I — ADMINISTRATION GÉNÉRALE DE LA PLATEFORME

## 2. Administration globale

### 2.1. Besoin d'un environnement d'administration

La plateforme doit proposer un environnement permettant d'administrer les éléments qui relèvent de son fonctionnement général.

Cet environnement doit être distinct des espaces ordinaires de travail des utilisateurs, car les opérations d'administration ne concernent pas nécessairement la gestion quotidienne des ressources.

Il doit permettre aux personnes autorisées d'avoir une vision suffisamment complète des éléments administrables, de leur état et des actions possibles.

L'administration générale doit notamment couvrir :

- Les utilisateurs et les comptes.
- Les organisations et leurs espaces.
- Les équipes et leurs membres.
- Les bibliothèques et collections.
- Les ressources enregistrées.
- Les sources externes référencées.
- Les registres de distribution.
- Les opérations d'importation et de synchronisation.
- Les publications.
- Les activités importantes.
- Les incidents et erreurs.
- Les paramètres généraux.
- Les règles de sécurité et de conservation.
- Les éléments nécessaires au fonctionnement global du produit.

Cette administration ne doit pas se substituer aux responsabilités propres à chaque organisation. Elle doit respecter les limites entre administration générale et administration organisationnelle.

### 2.2. Distinction entre administration de la plateforme et administration des organisations

La plateforme doit distinguer les personnes qui administrent le service dans son ensemble de celles qui administrent une organisation particulière.

Un administrateur général peut disposer de responsabilités relatives au fonctionnement du produit, à sa configuration et à son exploitation.

Un administrateur organisationnel intervient dans le périmètre de son organisation et des espaces qui lui sont rattachés.

Un responsable de bibliothèque peut gérer les ressources dont il a la charge sans disposer de droits d'administration sur l'organisation entière.

Ces responsabilités doivent rester séparées.

L'existence d'un rôle administratif dans une organisation ne doit pas automatiquement donner accès à l'administration générale de la plateforme.

Inversement, une personne chargée de l'exploitation générale ne doit pas nécessairement intervenir dans toutes les décisions éditoriales ou techniques relatives aux ressources d'une organisation.

La plateforme doit permettre de définir ces périmètres sans ambiguïté.

### 2.3. Tableau de bord d'administration

L'environnement d'administration doit proposer une vue synthétique du fonctionnement général.

Il doit permettre de consulter les informations importantes sans obliger l'administrateur à parcourir individuellement chaque espace ou chaque ressource.

Selon les informations disponibles et les droits de consultation, ce tableau de bord peut présenter :

- Le nombre de comptes actifs et les évolutions récentes.
- Le nombre d'organisations et d'espaces.
- Le volume de ressources enregistrées.
- Le nombre de bibliothèques et de collections.
- Les opérations d'importation en cours.
- Les synchronisations en attente ou en échec.
- Les publications récentes.
- Les ressources présentant des problèmes identifiés.
- Les opérations ayant rencontré des erreurs.
- Les incidents nécessitant une intervention.
- Les activités administratives importantes.
- Les tendances d'utilisation et d'évolution du patrimoine.

Les indicateurs doivent être compréhensibles et suffisamment contextualisés.

Un chiffre isolé ne doit pas être présenté comme une information complète lorsqu'il nécessite une période, une définition ou un périmètre de calcul.

Par exemple, le nombre de ressources enregistrées doit pouvoir être distingué du nombre de ressources effectivement publiées, actives ou utilisées dans des projets.

### 2.4. Administration des paramètres généraux

Les personnes autorisées doivent pouvoir consulter et gérer les paramètres généraux du produit.

Ces paramètres peuvent concerner les règles communes de fonctionnement, les limites d'utilisation, les conditions d'accès, les paramètres de conservation, les politiques de sécurité et les options disponibles.

Les changements doivent être explicites et traçables.

La plateforme doit permettre de distinguer les paramètres applicables à l'ensemble du produit de ceux qui sont propres à une organisation ou à un espace.

Lorsqu'une configuration générale influence le fonctionnement d'un espace particulier, les responsables concernés doivent pouvoir comprendre cette influence.

### 2.5. Administration des fonctionnalités

La plateforme doit pouvoir gérer les fonctionnalités proposées selon les contextes d'utilisation et les autorisations applicables.

Certaines fonctionnalités peuvent être accessibles à tous les utilisateurs, tandis que d'autres peuvent être réservées à certains espaces ou à certaines responsabilités.

L'administration doit permettre de comprendre quelles fonctionnalités sont disponibles, dans quel périmètre et sous quelles conditions.

Il ne faut pas confondre la disponibilité d'une fonctionnalité avec l'autorisation d'effectuer une opération.

Par exemple, une fonction de publication peut être disponible dans un espace, mais son utilisation peut rester réservée aux personnes autorisées.

---

## 3. Administration des organisations et de leurs ressources

### 3.1. Administration autonome des organisations

Chaque organisation doit pouvoir administrer son propre environnement dans les limites qui lui sont accordées.

Elle doit pouvoir gérer ses membres, ses équipes, ses espaces, ses bibliothèques, ses collections et les règles de partage qui relèvent de son périmètre.

L'administration organisationnelle doit rester suffisamment autonome pour éviter qu'une organisation dépende systématiquement d'un administrateur général pour effectuer les opérations ordinaires.

### 3.2. Vue d'ensemble du patrimoine organisationnel

Les responsables doivent pouvoir obtenir une vision globale du patrimoine géré par leur organisation.

Cette vision doit permettre d'identifier :

- Les bibliothèques disponibles.
- Les ressources qui composent ces bibliothèques.
- Les collections existantes.
- Les responsables de maintenance.
- Les versions de référence.
- Les ressources publiées.
- Les ressources dépréciées.
- Les ressources archivées.
- Les ressources partagées avec d'autres espaces.
- Les ressources utilisées par les projets identifiés.
- Les éléments nécessitant une intervention.

L'objectif est de rendre le patrimoine compréhensible et administrable, même lorsque plusieurs équipes contribuent à son évolution.

### 3.3. Contrôle de l'état des patrimoines

Les responsables doivent pouvoir identifier les situations qui nécessitent une attention particulière.

Il peut notamment s'agir :

- D'une ressource sans responsable clairement identifié.
- D'une ressource dont la documentation est incomplète.
- D'une dépendance devenue incompatible.
- D'une synchronisation qui n'a pas abouti.
- D'une publication dont les informations sont incomplètes.
- D'une ressource présentant des erreurs de validation.
- D'une bibliothèque contenant des éléments obsolètes.
- D'une contribution en attente depuis une période importante.
- D'une ressource dont la licence ou la provenance nécessite une vérification.

Ces situations doivent être présentées comme des éléments à examiner, et non automatiquement comme des défaillances.

---

# PARTIE II — SÉCURITÉ ET PROTECTION DU PATRIMOINE

## 4. Sécurité générale

### 4.1. Principe de protection

La sécurité doit être considérée comme une exigence fondamentale de l'ensemble de la plateforme.

Elle ne concerne pas uniquement la connexion des utilisateurs. Elle doit couvrir les ressources logicielles, les fichiers sources, les informations de compte, les bibliothèques, les publications, les espaces de travail et les opérations réalisées.

La plateforme doit empêcher qu'une personne puisse consulter, modifier, supprimer ou distribuer des éléments pour lesquels elle ne dispose pas des autorisations nécessaires.

Elle doit également limiter les conséquences d'une erreur, d'une compromission de compte ou d'une opération malveillante.

### 4.2. Protection des comptes

Les comptes doivent être protégés contre les accès non autorisés.

La plateforme doit permettre de gérer les conditions d'authentification, les sessions, les changements de mot de passe lorsque ce mode d'accès est utilisé, ainsi que les mécanismes complémentaires de protection des comptes.

Elle doit prendre en compte les situations suivantes :

- Une connexion inhabituelle.
- Une tentative répétée d'accès non autorisé.
- Une session qui doit être révoquée.
- Un compte dont l'accès doit être temporairement suspendu.
- Un utilisateur qui souhaite mettre fin à ses sessions actives.
- Un compte dont les informations d'accès ont été compromises.

Les utilisateurs doivent disposer d'informations suffisantes pour comprendre les événements importants concernant la sécurité de leur compte.

### 4.3. Gestion des sessions

La plateforme doit permettre de maîtriser les sessions ouvertes par les utilisateurs.

Il doit être possible de mettre fin à une session, de révoquer des sessions actives et de gérer les situations dans lesquelles un compte est utilisé depuis plusieurs environnements.

La durée de validité des sessions et les conditions de renouvellement doivent être maîtrisées.

Une session révoquée ne doit plus permettre de poursuivre des opérations protégées.

### 4.4. Protection des opérations sensibles

Certaines opérations présentent des conséquences importantes pour le patrimoine.

La plateforme doit pouvoir leur appliquer des contrôles adaptés.

Cela concerne notamment :

- La suppression définitive d'une ressource.
- Le transfert de propriété.
- La modification des permissions d'administration.
- Le changement d'un responsable principal.
- La publication d'une version importante.
- Le retrait d'une ressource distribuée.
- La modification des paramètres de sécurité.
- La révocation d'accès importants.
- La suppression d'une organisation.
- La suppression ou la modification d'un registre.

Selon le contexte, ces opérations peuvent nécessiter une confirmation explicite, une autorisation supplémentaire ou une validation par une autre personne.

L'objectif est d'éviter qu'une action importante soit déclenchée accidentellement ou par une personne ne disposant pas des responsabilités nécessaires.

---

## 5. Protection des données et confidentialité

### 5.1. Classification des informations

La plateforme doit distinguer les différentes catégories d'informations qu'elle gère.

Toutes les données ne présentent pas les mêmes exigences de confidentialité.

Il faut notamment distinguer :

- Les informations publiques relatives aux ressources.
- Les informations accessibles aux membres d'un espace.
- Les informations internes à une organisation.
- Les informations personnelles des utilisateurs.
- Les données relatives aux projets privés.
- Les informations de configuration.
- Les éléments d'authentification et les secrets.
- Les historiques d'opérations sensibles.

Cette distinction doit être prise en compte dans les règles de consultation, de partage, d'exportation et de conservation.

### 5.2. Confidentialité entre organisations

Une organisation ne doit pas pouvoir accéder aux ressources privées, aux projets internes ou aux informations administratives d'une autre organisation sans autorisation.

La présence de plusieurs organisations dans un environnement commun ne doit pas conduire à une exposition involontaire de leurs patrimoines.

Cette séparation doit rester valable dans les recherches, les résultats de catalogue, les historiques, les tableaux de bord, les notifications et les exports.

Il ne suffit pas de masquer les informations dans l'interface si elles restent accessibles par une autre opération.

### 5.3. Protection des fichiers sources

Les codes sources constituent le cœur du patrimoine géré par la plateforme.

Ils doivent être protégés contre les consultations, modifications, suppressions et distributions non autorisées.

La plateforme doit garantir que les droits accordés sur une fiche descriptive ne donnent pas automatiquement accès aux fichiers sources si ces droits sont distincts.

Elle doit également éviter qu'une ressource privée soit exposée accidentellement à travers un export, une publication ou un partage.

### 5.4. Confidentialité des projets consommateurs

Les informations relatives aux projets qui consomment des ressources peuvent être sensibles.

Un fournisseur de composants peut avoir besoin de connaître certaines informations d'utilisation pour suivre les dépendances, mais cela ne signifie pas que tous les détails du projet consommateur doivent être rendus publics.

La plateforme doit distinguer les informations nécessaires au suivi des ressources de celles qui appartiennent exclusivement au projet.

Les propriétaires des projets doivent conserver la maîtrise des informations qu'ils rendent accessibles.

### 5.5. Confidentialité des activités

Les journaux d'activité et les historiques peuvent contenir des informations sur les personnes, les projets et les opérations internes.

Leur consultation doit donc respecter les mêmes principes de confidentialité que les autres éléments de la plateforme.

Les responsables doivent pouvoir accéder aux informations nécessaires à leurs missions, sans que chaque membre dispose automatiquement d'une visibilité générale sur toutes les activités.

---

## 6. Gestion des secrets et des informations sensibles

### 6.1. Nature des secrets

La plateforme peut être amenée à utiliser des informations sensibles pour accéder à des services ou effectuer certaines opérations.

Il peut notamment s'agir de :

- Jetons d'accès.
- Clés d'API.
- Identifiants de connexion à des registres privés.
- Informations d'authentification auprès de sources externes.
- Secrets nécessaires à certaines intégrations.
- Informations permettant d'accéder à des environnements privés.

Ces informations ne doivent pas être traitées comme de simples métadonnées de ressources.

### 6.2. Conservation et utilisation

La plateforme doit permettre de gérer ces informations dans des conditions adaptées à leur sensibilité.

Les secrets ne doivent pas être affichés dans les interfaces ordinaires, les journaux d'activité, les messages d'erreur ou les exports destinés à des utilisateurs non autorisés.

Leur utilisation doit être limitée aux opérations qui en ont besoin.

### 6.3. Contrôle des accès aux secrets

Les utilisateurs autorisés à gérer une intégration ne doivent pas nécessairement disposer du droit de consulter directement toutes les informations sensibles qu'elle utilise.

La plateforme doit pouvoir distinguer la gestion d'une connexion, son utilisation et la consultation de ses informations confidentielles.

### 6.4. Révocation et renouvellement

Il doit être possible de remplacer ou de révoquer une information d'accès lorsqu'elle est devenue inutilisable, expirée ou compromise.

La plateforme doit également permettre d'identifier les intégrations qui dépendent de cette information afin d'évaluer les conséquences de sa révocation.

---

## 7. Sécurité des ressources provenant de sources externes

### 7.1. Considérer les ressources importées comme des éléments à examiner

Les ressources récupérées depuis des dépôts, registres ou autres sources externes ne doivent pas être considérées comme fiables uniquement parce qu'elles sont publiquement accessibles.

La plateforme doit permettre de vérifier les éléments importés avant leur intégration dans un patrimoine ou leur distribution.

Cette exigence concerne les composants, les bibliothèques, les fichiers, les dépendances, les scripts, les configurations et les éventuels éléments exécutables.

### 7.2. Identification de l'origine

Chaque ressource importée doit conserver les informations disponibles sur son origine.

Il doit être possible de distinguer une ressource provenant d'une source connue, une ressource fournie directement par un utilisateur et une ressource dont l'origine n'est pas suffisamment établie.

L'absence d'informations ne doit pas être remplacée par une origine supposée.

### 7.3. Vérification des contenus

La plateforme doit pouvoir signaler les éléments qui nécessitent une vérification avant utilisation.

Cela peut concerner :

- Des fichiers inattendus.
- Des scripts d'installation.
- Des dépendances non documentées.
- Des configurations sensibles.
- Des contenus exécutables.
- Des références vers des ressources externes.
- Des éléments dont l'origine est inconnue.
- Des modifications inhabituelles entre deux versions.

Les résultats de ces vérifications doivent être présentés de manière compréhensible, en distinguant les problèmes confirmés, les alertes et les éléments simplement non vérifiés.

### 7.4. Sécurité des dépendances

Les dépendances doivent pouvoir faire l'objet d'un suivi particulier.

La plateforme doit permettre d'identifier les dépendances connues, leurs versions et les relations qu'elles entretiennent avec les ressources concernées.

Lorsqu'une dépendance présente un problème identifié, les responsables doivent pouvoir retrouver les ressources et projets potentiellement concernés.

### 7.5. Distribution de ressources vérifiées

La plateforme doit permettre de distinguer les ressources simplement importées des ressources ayant fait l'objet de vérifications.

Une ressource ne doit pas être présentée comme sécurisée ou validée sans que les contrôles correspondants aient réellement été effectués.

Les informations de vérification doivent rester associées à la version concernée.

Une nouvelle version ne doit pas hériter automatiquement d'un statut de vérification qui ne correspondrait pas à son contenu.

---

# PARTIE III — FIABILITÉ DES OPÉRATIONS ET INTÉGRITÉ DU PATRIMOINE

## 8. Fiabilité des opérations

### 8.1. Principe de cohérence

La plateforme doit garantir que les opérations réalisées sur les ressources ne laissent pas volontairement le patrimoine dans un état incohérent.

Une opération peut concerner plusieurs éléments liés : une ressource, ses fichiers, ses dépendances, ses métadonnées, ses versions et ses relations avec une bibliothèque.

La plateforme doit prendre en compte ces relations lorsqu'elle réalise une opération importante.

Par exemple, supprimer une ressource ne doit pas laisser des références incohérentes dans les collections ou les dépendances qui la mentionnent.

### 8.2. Opérations interrompues

Les opérations peuvent échouer ou être interrompues pour différentes raisons.

La plateforme doit pouvoir identifier leur état et déterminer si elles ont abouti, échoué ou nécessité une reprise.

Cela concerne notamment :

- L'importation d'une ressource.
- La synchronisation avec une source externe.
- La récupération d'un ensemble de composants.
- La création d'une version.
- La validation d'une ressource.
- La publication.
- La mise à jour d'une bibliothèque.
- L'exportation d'un patrimoine.

Une opération interrompue ne doit pas être présentée comme terminée.

### 8.3. Reprise des opérations

Lorsque cela est possible, la plateforme doit permettre de reprendre une opération échouée sans obliger l'utilisateur à recommencer inutilement l'ensemble du travail.

Elle doit pouvoir indiquer les étapes déjà réalisées, celles qui restent à effectuer et les éléments qui nécessitent une intervention.

La reprise ne doit pas provoquer de doublons ou écraser des données déjà validées.

### 8.4. Prévention des opérations contradictoires

La plateforme doit prendre en compte les opérations qui peuvent entrer en conflit.

Par exemple, une publication ne doit pas être préparée à partir d'un état de ressource devenu obsolète sans que cette situation soit détectée.

De même, une suppression ne doit pas être réalisée sans tenir compte des dépendances ou des utilisations connues lorsque celles-ci sont importantes pour la décision.

Les utilisateurs doivent être informés des conséquences potentielles avant les opérations concernées.

---

## 9. Intégrité et cohérence des ressources

### 9.1. Préservation des fichiers

La plateforme doit garantir que les fichiers sources conservés correspondent aux versions enregistrées.

Les opérations de consultation, de modification, d'importation, d'exportation et de restauration doivent préserver la cohérence des contenus.

La structure des dossiers, les noms de fichiers et les relations entre les éléments doivent être maintenus lorsque ces informations font partie de la ressource.

### 9.2. Intégrité des versions

Chaque version enregistrée doit correspondre à un état identifiable de la ressource.

Il doit être possible de retrouver les fichiers et les métadonnées qui lui correspondent.

La plateforme doit éviter les situations dans lesquelles une version historique est affichée avec des fichiers provenant d'une version ultérieure.

### 9.3. Cohérence des métadonnées

Les métadonnées doivent rester cohérentes avec les ressources qu'elles décrivent.

Une modification du nom, de la description, de la version, de la provenance ou des dépendances doit être prise en compte dans les informations affichées et les opérations concernées.

La plateforme doit permettre de détecter les informations manquantes ou contradictoires.

### 9.4. Cohérence des relations

Les relations entre ressources doivent être maintenues.

Cela concerne notamment :

- Les dépendances.
- Les variantes.
- Les collections.
- Les bibliothèques.
- Les ressources dérivées.
- Les versions.
- Les projets consommateurs.
- Les publications.
- Les ressources provenant d'une même source.

La suppression ou la modification d'un élément ne doit pas rendre les relations restantes incompréhensibles.

### 9.5. Vérification de l'intégrité

La plateforme doit pouvoir effectuer des contrôles permettant de détecter des altérations, des fichiers manquants, des incohérences ou des différences inattendues.

Les résultats doivent être consultables et associés aux éléments concernés.

Lorsqu'un problème est détecté, la plateforme doit permettre de déterminer si une restauration, une nouvelle récupération ou une intervention manuelle est nécessaire.

---

## 10. Sauvegarde, restauration et récupération

### 10.1. Sauvegarde du patrimoine

La plateforme doit permettre de préserver les ressources et les informations nécessaires à leur reconstruction.

Une sauvegarde ne doit pas se limiter aux fichiers sources.

Elle doit également prendre en compte les éléments indispensables pour retrouver le contexte des ressources :

- Les métadonnées.
- Les versions.
- Les structures de fichiers.
- Les dépendances enregistrées.
- Les informations de provenance.
- Les licences.
- Les collections.
- Les bibliothèques.
- Les configurations utiles.
- Les informations de propriété et de responsabilité.
- Les relations entre ressources.
- Les historiques importants.

Les éléments concernés par une sauvegarde doivent être clairement identifiés.

### 10.2. Sauvegarde des espaces organisationnels

Les organisations doivent pouvoir préserver leur patrimoine indépendamment des autres organisations.

La sauvegarde d'un espace organisationnel doit permettre de retrouver les ressources et les informations qui lui appartiennent ou qu'il est autorisé à conserver.

La séparation entre les patrimoines doit rester respectée lors des opérations de sauvegarde et de restauration.

### 10.3. Restauration d'une ressource

Un utilisateur autorisé doit pouvoir restaurer une ressource à partir d'un état antérieur lorsque cela est nécessaire.

La restauration doit permettre de retrouver les fichiers et informations correspondant à la version choisie.

Elle ne doit pas nécessairement effacer l'état actuel. Il doit être possible de conserver la trace de la restauration et de comprendre quel état a été rétabli.

### 10.4. Restauration d'une bibliothèque ou d'un espace

La plateforme doit également prendre en compte les restaurations à une échelle plus large.

Il peut être nécessaire de restaurer une bibliothèque, une collection ou un espace organisationnel à partir d'une sauvegarde ou d'un état conservé.

Les relations entre les ressources doivent être prises en compte afin de ne pas restaurer des éléments isolés dans un contexte devenu incohérent.

### 10.5. Récupération après incident

La plateforme doit pouvoir prendre en compte les situations dans lesquelles une partie du patrimoine devient indisponible, endommagée ou inaccessible.

Les responsables doivent pouvoir identifier les éléments touchés, évaluer les pertes éventuelles et engager les opérations de récupération appropriées.

Les informations disponibles sur l'incident et la restauration doivent être conservées.

### 10.6. Indépendance des sauvegardes

La possibilité de sauvegarder et de restaurer le patrimoine ne doit pas dépendre exclusivement de l'interface quotidienne de la plateforme.

Les organisations doivent pouvoir disposer de moyens d'exportation leur permettant de préserver leurs ressources et leurs informations essentielles.

Cette exigence prolonge les besoins d'exportabilité et d'autonomie définis dans la session 3.

---

# PARTIE IV — QUALITÉ ET VALIDATION DES RESSOURCES

## 11. Qualité générale des ressources

### 11.1. La qualité comme propriété suivie

La plateforme doit permettre d'évaluer la qualité des ressources qu'elle héberge et distribue.

Il ne suffit pas de conserver le code source. Les utilisateurs doivent pouvoir comprendre si une ressource est documentée, cohérente, compatible avec ses environnements cibles et suffisamment vérifiée pour l'utilisation envisagée.

La qualité doit être considérée comme un ensemble de critères, et non comme une note unique qui résumerait toutes les caractéristiques d'une ressource.

### 11.2. Critères de qualité

Selon la nature de la ressource, les critères peuvent concerner :

- La validité de la structure des fichiers.
- La qualité du code source.
- La cohérence des propriétés.
- La documentation.
- Les dépendances.
- La compatibilité.
- Les tests disponibles.
- Le comportement fonctionnel.
- Le rendu visuel.
- L'accessibilité.
- La maintenabilité.
- La provenance.
- La licence.
- La stabilité de la version.

Tous ces critères ne sont pas nécessairement applicables à chaque type de ressource.

La plateforme doit adapter les contrôles à la nature de ce qu'elle gère.

### 11.3. Résultats de validation

Les contrôles doivent produire des résultats compréhensibles.

Il faut distinguer :

- Les contrôles réussis.
- Les contrôles échoués.
- Les avertissements.
- Les contrôles non exécutés.
- Les contrôles impossibles à réaliser.
- Les résultats nécessitant une intervention.

Une vérification non effectuée ne doit pas être interprétée comme une vérification réussie.

### 11.4. Historique de qualité

Les résultats de validation doivent pouvoir être associés à une version précise.

Cela permet de comprendre si une ressource a été vérifiée avant ou après une modification.

Lorsqu'une ressource change, les résultats antérieurs doivent rester consultables, mais ne doivent pas être présentés comme une validation de son nouveau contenu.

---

## 12. Validation technique des ressources

### 12.1. Validation de la structure

La plateforme doit pouvoir vérifier que les ressources possèdent une structure cohérente avec leur nature et leur description.

Pour une ressource logicielle, cela peut concerner les fichiers attendus, les configurations, les points d'entrée, les références internes et les éléments nécessaires à son utilisation.

Les anomalies doivent être signalées sans modifier silencieusement la structure originale.

### 12.2. Validation syntaxique et structurelle

Lorsque les technologies et les formats sont identifiables, la plateforme doit pouvoir prendre en compte des contrôles adaptés à leur syntaxe.

Ces contrôles peuvent notamment concerner :

- Les erreurs de syntaxe.
- Les références invalides.
- Les configurations incorrectes.
- Les fichiers mal formés.
- Les incohérences entre les fichiers.
- Les problèmes de typage lorsqu'ils sont applicables.

Les résultats doivent être associés aux fichiers ou éléments concernés.

### 12.3. Validation des dépendances

La plateforme doit pouvoir examiner les dépendances déclarées et les relations entre ressources.

Elle doit notamment permettre de repérer :

- Les dépendances absentes.
- Les versions non précisées.
- Les incompatibilités identifiées.
- Les références qui ne peuvent plus être résolues.
- Les dépendances inutilisées lorsqu'elles peuvent être identifiées.
- Les relations circulaires problématiques.
- Les changements de dépendances entre versions.

Ces informations doivent pouvoir être consultées avant la publication d'une ressource.

### 12.4. Validation de la compatibilité

La plateforme doit permettre de renseigner et de vérifier, lorsque cela est possible, les environnements compatibles avec une ressource.

Une ressource destinée à React ne doit pas être présentée automatiquement comme compatible avec Vue ou Angular.

La compatibilité doit être liée à des informations vérifiables : environnement ciblé, dépendances, contraintes de version et résultats des contrôles disponibles.

### 12.5. Validation des distributions

La version publiée doit pouvoir être vérifiée indépendamment de la version de travail.

Il faut notamment s'assurer que les éléments nécessaires à sa récupération sont présents, que les dépendances sont correctement identifiées et que les informations de publication sont cohérentes.

Une publication ne doit pas être considérée comme fiable simplement parce que son opération de distribution a abouti.

---

## 13. Validation fonctionnelle et visuelle

### 13.1. Vérification du comportement

Pour les composants et ressources interactives, la plateforme doit permettre de vérifier les comportements attendus.

Cela peut concerner les interactions, les propriétés, les états, les événements et les variations de comportement.

Les contrôles doivent être adaptés à la nature du composant.

### 13.2. Prévisualisation et comparaison

Les ressources qui possèdent un rendu visuel doivent pouvoir être prévisualisées lorsque leur nature et leur environnement le permettent.

La plateforme doit permettre de comparer différents états d'une ressource, notamment avant et après une modification.

Cette comparaison peut concerner :

- L'apparence générale.
- Les variantes.
- Les thèmes.
- Les tailles.
- Les états interactifs.
- Les propriétés configurables.
- Les comportements observables.

### 13.3. Détection des régressions

Lorsqu'une modification affecte un composant existant, il doit être possible de vérifier si certains comportements ou rendus précédemment attendus ont été altérés.

La plateforme doit permettre de signaler les différences significatives lorsque des contrôles adaptés sont disponibles.

Il ne faut toutefois pas confondre une différence visuelle avec une régression : certaines modifications sont volontaires.

Les résultats doivent donc pouvoir être examinés par les personnes responsables.

### 13.4. Accessibilité

La qualité des composants d'interface doit également prendre en compte l'accessibilité.

Selon les caractéristiques de la ressource, les vérifications peuvent concerner :

- La navigation au clavier.
- La visibilité des états.
- Les libellés des éléments interactifs.
- Les relations entre les champs et leurs descriptions.
- La lisibilité.
- Le contraste.
- Les comportements attendus pour les technologies d'assistance.

La plateforme doit permettre de présenter les résultats et les limitations connues.

Elle ne doit pas déclarer automatiquement une ressource accessible sans contrôles adaptés.

---

## 14. Documentation, maturité et niveau de confiance

### 14.1. Documentation obligatoire ou recommandée

Les responsables doivent pouvoir définir les informations documentaires attendues pour les différentes catégories de ressources.

Une ressource publiée peut nécessiter une description, des instructions d'utilisation, des dépendances, des exemples et des informations de version.

Les exigences peuvent être différentes pour une ressource expérimentale et une bibliothèque destinée à être largement consommée.

### 14.2. État de maturité

La plateforme doit permettre de distinguer les ressources selon leur niveau de maturité.

À titre de catégories possibles :

- Expérimentale.
- En développement.
- En validation.
- Stable.
- Dépréciée.
- Abandonnée.
- Archivée.

Ces états ne doivent pas être confondus avec les états de publication ou de disponibilité.

Une ressource peut être publiée tout en étant expérimentale, si les règles de distribution de l'espace l'autorisent.

Une ressource stable peut également être conservée dans un espace privé.

### 14.3. Informations sur la confiance

La plateforme doit présenter les informations qui permettent à un utilisateur d'évaluer une ressource avant de l'utiliser.

Cela peut inclure sa provenance, son historique, sa documentation, ses dépendances, ses validations et son niveau de maturité.

La confiance ne doit pas être réduite à une appréciation automatique ou à une note sans justification.

Les informations présentées doivent permettre de comprendre sur quels éléments repose l'évaluation.

---

# PARTIE V — OBSERVABILITÉ, DIAGNOSTIC ET GESTION DES INCIDENTS

## 15. Suivi du fonctionnement

### 15.1. Visibilité sur les opérations

La plateforme doit permettre de suivre les opérations importantes qu'elle exécute.

L'utilisateur doit pouvoir comprendre ce qui se passe lorsqu'il lance une importation, une synchronisation, une validation, une exportation ou une publication.

Les opérations doivent disposer d'un état compréhensible, par exemple :

- En attente.
- En cours.
- Terminée.
- Terminée avec avertissements.
- Échouée.
- Interrompue.
- En attente d'une intervention.

Les états doivent être suffisamment précis pour éviter les ambiguïtés.

### 15.2. Historique des opérations

Les opérations doivent pouvoir être retrouvées après leur exécution.

Pour chaque opération importante, la plateforme doit permettre de consulter les informations disponibles sur :

- Son objectif.
- Son auteur ou son déclencheur.
- Son périmètre.
- Sa date de début.
- Sa date de fin.
- Son résultat.
- Les éventuelles erreurs.
- Les éléments concernés.
- Les éventuelles actions de reprise.

Cela facilite le diagnostic et évite de devoir recommencer une opération uniquement parce que son résultat n'est plus visible.

### 15.3. Suivi des traitements longs

Certaines opérations peuvent prendre du temps, notamment lorsqu'elles concernent de grandes bibliothèques, plusieurs ressources ou des sources externes.

La plateforme doit permettre de suivre leur progression lorsque cette information est disponible.

Elle doit éviter de donner l'impression qu'une opération est bloquée lorsqu'elle est simplement en cours.

En cas d'échec, l'utilisateur doit pouvoir comprendre si une nouvelle tentative est possible et si une intervention est nécessaire.

---

## 16. Journalisation et traçabilité technique

### 16.1. Journaux de fonctionnement

La plateforme doit disposer d'informations permettant de comprendre son fonctionnement et de diagnostiquer les anomalies.

Les événements importants doivent pouvoir être retrouvés avec suffisamment de contexte.

Les journaux doivent permettre de distinguer les erreurs, les avertissements, les opérations normales et les événements de sécurité.

### 16.2. Journaux d'administration

Les opérations administratives sensibles doivent faire l'objet d'une traçabilité particulière.

Il doit être possible de retrouver les changements apportés aux paramètres, aux permissions, aux comptes et aux organisations.

Cette traçabilité est importante pour comprendre les modifications qui ont pu affecter le fonctionnement du produit ou la sécurité d'un patrimoine.

### 16.3. Informations de diagnostic

Lorsqu'une opération échoue, la plateforme doit fournir des informations utiles pour comprendre la cause du problème.

Les messages doivent être suffisamment précis pour orienter l'utilisateur, sans exposer des informations confidentielles ou des secrets techniques.

Il faut distinguer le message compréhensible destiné à l'utilisateur des informations techniques détaillées nécessaires aux personnes chargées du diagnostic.

### 16.4. Corrélation des événements

Lorsqu'une opération implique plusieurs étapes, il doit être possible de retrouver les événements qui appartiennent à la même opération.

Par exemple, une publication peut impliquer une validation, une préparation, une distribution et une confirmation.

Les informations disponibles doivent permettre de reconstituer cette séquence et de déterminer à quelle étape une anomalie s'est produite.

### 16.5. Conservation et confidentialité des journaux

Les journaux doivent être conservés selon des règles adaptées à leur nature et à leur utilité.

Ils ne doivent pas devenir un moyen de contourner les permissions d'accès aux ressources.

Les informations sensibles doivent être protégées, et les règles de consultation doivent être cohérentes avec les responsabilités des utilisateurs.

---

## 17. Gestion des incidents

### 17.1. Identification des incidents

La plateforme doit permettre d'identifier les incidents qui affectent son fonctionnement ou celui des patrimoines gérés.

Il peut notamment s'agir :

- D'une indisponibilité d'une source externe.
- D'un échec répété d'importation.
- D'une erreur de synchronisation.
- D'une publication incomplète.
- D'une perte d'accès à une ressource.
- D'une incohérence de fichiers.
- D'une défaillance d'une opération de restauration.
- D'un problème de permission.
- D'une erreur de validation.
- D'une indisponibilité d'une fonctionnalité importante.

### 17.2. Qualification des incidents

Les incidents doivent pouvoir être qualifiés selon leur nature, leur impact et leur état de traitement.

Il faut distinguer un problème isolé affectant une ressource d'un incident qui touche plusieurs organisations ou une fonctionnalité générale.

La plateforme doit permettre de comprendre le périmètre concerné.

### 17.3. Suivi du traitement

Les personnes chargées de traiter les incidents doivent pouvoir suivre leur évolution.

Il doit être possible de documenter :

- La description du problème.
- Les éléments affectés.
- La date de détection.
- Les personnes responsables du traitement.
- Les actions entreprises.
- Les résultats obtenus.
- L'état de résolution.
- Les éventuelles mesures de prévention.

### 17.4. Communication des incidents

Lorsque les incidents affectent les utilisateurs, la plateforme doit pouvoir leur communiquer les informations utiles.

Les messages doivent préciser les fonctionnalités concernées et les conséquences connues.

Il faut éviter de présenter une opération comme disponible lorsque son fonctionnement est dégradé.

La communication doit être adaptée au périmètre concerné : une organisation ne doit pas nécessairement recevoir des informations sur un incident qui ne touche que le patrimoine privé d'une autre organisation.

### 17.5. Analyse après incident

Les incidents importants doivent pouvoir être examinés après leur résolution.

L'objectif est de comprendre leur origine, leurs conséquences et les mesures permettant de limiter leur répétition.

La plateforme doit permettre de conserver les enseignements tirés de ces situations dans un historique exploitable.

---

# PARTIE VI — PERFORMANCE, CAPACITÉ ET ÉVOLUTIVITÉ

## 18. Performance générale

### 18.1. Expérience fluide

La plateforme doit rester utilisable lorsque le nombre de ressources, de bibliothèques, de versions et d'utilisateurs augmente.

Les opérations courantes doivent rester suffisamment fluides pour ne pas rendre la gestion du patrimoine pénible.

Cela concerne notamment :

- La consultation des bibliothèques.
- La navigation dans les collections.
- La recherche de ressources.
- L'affichage des fichiers.
- La consultation des versions.
- La comparaison des modifications.
- La prévisualisation.
- La gestion des dépendances.
- La consultation de l'historique.

### 18.2. Recherche à grande échelle

La recherche doit rester exploitable lorsque le catalogue contient un grand nombre de ressources.

Les utilisateurs doivent pouvoir filtrer les résultats et accéder aux informations pertinentes sans parcourir manuellement l'intégralité du patrimoine.

Les recherches dans le code, les métadonnées, les descriptions, les dépendances et les collections doivent pouvoir être adaptées à leur périmètre.

### 18.3. Gestion des ressources volumineuses

Certaines ressources peuvent contenir de nombreux fichiers, des assets importants ou plusieurs variantes.

La plateforme doit prendre en compte ces volumes lors des opérations de consultation, d'importation, de modification et d'exportation.

Elle doit permettre à l'utilisateur de comprendre les éventuelles limites rencontrées.

### 18.4. Traitements en arrière-plan

Certaines opérations n'ont pas besoin de bloquer l'utilisateur pendant toute leur exécution.

La plateforme doit pouvoir gérer les opérations longues de manière à ce que l'utilisateur puisse poursuivre d'autres activités lorsque cela est possible.

Les opérations en cours doivent rester visibles et leur résultat doit être consultable ultérieurement.

---

## 19. Capacité d'évolution

### 19.1. Augmentation du nombre de ressources

La plateforme doit pouvoir accompagner l'augmentation progressive du patrimoine.

Elle doit être capable de prendre en compte des milliers, puis potentiellement des dizaines de milliers de ressources, sans que leur organisation devienne incontrôlable.

La gestion des versions, des dépendances, des origines et des relations doit rester exploitable à cette échelle.

### 19.2. Augmentation du nombre d'utilisateurs et d'organisations

Le produit doit pouvoir évoluer d'une utilisation individuelle vers un environnement regroupant de nombreuses équipes et organisations.

Les mécanismes de partage, de permissions et de séparation des patrimoines doivent rester compréhensibles à mesure que le nombre de participants augmente.

### 19.3. Évolution des catégories de ressources

La plateforme ne doit pas être limitée définitivement aux composants d'interface.

Son périmètre peut inclure d'autres formes de ressources logicielles, des bibliothèques, des systèmes de design, des configurations, des outils et des ensembles composites.

Elle doit donc pouvoir accueillir de nouvelles catégories de ressources sans remettre en cause les principes fondamentaux de gestion, de provenance, de versionnement et de distribution.

### 19.4. Évolution des environnements de consommation

La plateforme doit pouvoir prendre en compte l'apparition de nouveaux environnements, langages, frameworks et modes de distribution.

Elle ne doit pas être enfermée dans un seul écosystème technique.

L'ajout d'un nouvel environnement doit pouvoir enrichir les possibilités de récupération, de validation, de personnalisation et de distribution sans rendre les ressources existantes inutilisables.

### 19.5. Évolution des fonctionnalités

La plateforme doit pouvoir recevoir de nouvelles capacités sans obliger à reconstruire l'ensemble de l'expérience utilisateur.

Les fonctionnalités existantes doivent conserver leur cohérence et les ressources déjà enregistrées doivent rester exploitables.

---

# PARTIE VII — ADMINISTRATION DES SOURCES ET DES INTÉGRATIONS

## 20. Gestion des sources externes

### 20.1. Administration des sources

La plateforme doit permettre de gérer les sources depuis lesquelles les utilisateurs peuvent récupérer des ressources.

Ces sources peuvent correspondre à des dépôts, des registres, des catalogues ou d'autres espaces de publication.

Les utilisateurs doivent pouvoir identifier les sources disponibles et comprendre les possibilités offertes par chacune.

### 20.2. État des connexions

La plateforme doit permettre de suivre l'état des connexions aux sources externes.

Il doit être possible de distinguer une source disponible, une source inaccessible, une connexion expirée et une source nécessitant une intervention.

### 20.3. Gestion des erreurs de synchronisation

Les erreurs de synchronisation doivent être visibles et compréhensibles.

La plateforme doit permettre de retrouver les ressources concernées et de déterminer si l'échec provient de la source, de la connexion, d'une incompatibilité ou d'un problème lié à la ressource.

### 20.4. Retrait d'une source

Lorsqu'une source n'est plus utilisée ou ne doit plus être accessible, les responsables autorisés doivent pouvoir la retirer.

Le retrait d'une source ne doit pas supprimer automatiquement les ressources déjà récupérées depuis celle-ci.

Les informations d'origine doivent être conservées, même si la source n'est plus disponible.

### 20.5. Multiplicité des fournisseurs

La plateforme doit pouvoir gérer plusieurs sources indépendantes.

Elle ne doit pas supposer que toutes les ressources proviennent d'un seul fournisseur ou d'un seul registre.

Cette capacité est importante pour maintenir l'ambition multi-sources définie dans les sessions précédentes.

---

## 21. Administration des intégrations et des registres

### 21.1. Gestion des intégrations

Les intégrations doivent pouvoir être administrées selon leur fonction et leur périmètre.

Les responsables doivent pouvoir comprendre quelles intégrations sont actives, quelles ressources ou opérations elles concernent et quelles autorisations leur sont accordées.

### 21.2. État des registres

La plateforme doit permettre de suivre les registres de distribution configurés.

Les informations importantes doivent notamment permettre d'identifier :

- Les registres disponibles.
- Leur périmètre.
- Les ressources publiées.
- Les opérations de publication.
- Les erreurs rencontrées.
- Les autorisations associées.
- Les connexions nécessaires.
- Les versions distribuées.

### 21.3. Défaillance d'une intégration

Une intégration indisponible ne doit pas rendre incompréhensible l'état du patrimoine local.

La plateforme doit distinguer les ressources conservées de celles qui ne sont accessibles qu'à travers une source ou un service externe.

Elle doit également permettre d'identifier les opérations qui dépendent de l'intégration défaillante.

### 21.4. Remplacement d'une intégration

Lorsqu'une intégration doit être remplacée, la plateforme doit permettre d'identifier les ressources et les opérations concernées.

Le remplacement ne doit pas effacer les informations historiques sur l'origine des ressources ou les publications antérieures.

---

# PARTIE VIII — EXPÉRIENCE D'ADMINISTRATION ET EXPLOITATION QUOTIDIENNE

## 22. Interface d'administration

### 22.1. Organisation des informations

L'administration doit présenter les informations de manière structurée.

Les administrateurs doivent pouvoir passer de la vue générale à une vue détaillée sans perdre le contexte.

Les informations doivent être regroupées selon leur nature : utilisateurs, organisations, ressources, opérations, sécurité, intégrations et incidents.

### 22.2. Recherche administrative

L'environnement d'administration doit proposer des moyens de retrouver rapidement un élément.

La recherche peut porter sur :

- Un utilisateur.
- Une organisation.
- Une équipe.
- Un espace.
- Une bibliothèque.
- Une ressource.
- Une publication.
- Une opération.
- Un incident.
- Une intégration.

Les résultats doivent respecter les permissions de consultation applicables.

### 22.3. Filtres et vues personnalisées

Les administrateurs doivent pouvoir filtrer les informations selon les critères pertinents.

Par exemple, ils peuvent vouloir consulter uniquement les opérations échouées, les ressources en attente de validation ou les organisations présentant des éléments nécessitant une intervention.

Les filtres doivent permettre de réduire le volume d'informations sans masquer les éléments importants.

### 22.4. Actions groupées

Lorsque plusieurs éléments nécessitent la même opération, la plateforme peut permettre leur traitement groupé, à condition que les conséquences soient maîtrisées.

Cela peut concerner des opérations de classement, d'archivage, de mise à jour ou de gestion des permissions.

Les actions groupées doivent préciser leur périmètre et permettre de comprendre quels éléments seront affectés.

Les opérations sensibles doivent conserver les mêmes exigences de confirmation et d'autorisation que les opérations individuelles.

### 22.5. Aide au diagnostic

L'interface doit aider les administrateurs à comprendre les problèmes sans exiger qu'ils connaissent tous les détails internes du fonctionnement du produit.

Les messages doivent être explicites, les erreurs contextualisées et les actions possibles clairement présentées.

Lorsque le problème nécessite une intervention spécialisée, la plateforme doit fournir les informations utiles pour transmettre le diagnostic.

---

## 23. Gestion des paramètres et des politiques

### 23.1. Politiques générales

La plateforme doit permettre de définir des règles générales relatives à son fonctionnement.

Ces règles peuvent concerner les accès, la conservation, les limites d'utilisation, les publications, la sécurité ou les opérations administratives.

Elles doivent être compréhensibles et suffisamment documentées.

### 23.2. Politiques organisationnelles

Chaque organisation doit pouvoir définir ses propres règles dans les limites des politiques générales applicables.

Les administrateurs doivent pouvoir distinguer les règles imposées par le produit des règles propres à leur organisation.

### 23.3. Historique des configurations

Les modifications de configuration importantes doivent être traçables.

Il doit être possible de comprendre quelle valeur était applicable avant une modification et quelle valeur a été adoptée ensuite, dans la mesure où cette information est pertinente et conservée.

### 23.4. Effets des modifications

Avant de modifier une politique importante, les administrateurs doivent pouvoir comprendre les conséquences potentielles.

Par exemple, une modification des permissions par défaut peut affecter plusieurs espaces ou catégories de ressources.

La plateforme doit éviter les changements silencieux dont les conséquences ne sont visibles qu'après leur application.

---

# PARTIE IX — CONTINUITÉ, PÉRENNITÉ ET INDÉPENDANCE

## 24. Pérennité du patrimoine logiciel

### 24.1. Préserver les ressources dans le temps

La plateforme doit être capable de préserver les ressources au-delà de leur utilisation immédiate.

Une ressource ne doit pas devenir inexploitable simplement parce que son auteur a quitté la plateforme, qu'une équipe a été réorganisée ou qu'un fournisseur externe a disparu.

Les fichiers sources, les versions, les métadonnées, les dépendances et les informations de provenance doivent pouvoir être conservés et retrouvés.

### 24.2. Préserver l'historique

La mémoire du patrimoine doit rester exploitable dans le temps.

Les utilisateurs doivent pouvoir comprendre comment une ressource a été créée, d'où elle provient, quelles transformations elle a subies et quelles versions ont été distribuées.

Cette continuité est essentielle pour éviter que la plateforme ne devienne uniquement un espace de stockage de fichiers sans mémoire technique.

### 24.3. Gestion des ressources anciennes

Les ressources qui ne sont plus utilisées doivent pouvoir être conservées sans encombrer les espaces de travail actifs.

La plateforme doit permettre de les archiver tout en maintenant les informations nécessaires à leur consultation et à leur restauration.

L'archivage ne doit pas être confondu avec la suppression définitive.

### 24.4. Évolution des standards et des environnements

Les environnements logiciels évoluent.

Une ressource créée pour un environnement ancien peut nécessiter une adaptation pour rester utilisable.

La plateforme doit permettre de conserver les informations sur son environnement d'origine et de documenter les évolutions nécessaires.

Elle ne doit pas réécrire automatiquement les ressources historiques au seul motif qu'un environnement plus récent devient disponible.

---

## 25. Indépendance et portabilité

### 25.1. Exportation du patrimoine

Les utilisateurs et organisations doivent pouvoir récupérer leurs ressources dans des formats exploitables en dehors de la plateforme.

L'exportation doit préserver autant que possible :

- Les fichiers sources.
- Les structures de dossiers.
- Les versions.
- Les métadonnées.
- Les dépendances déclarées.
- Les informations de provenance.
- Les licences.
- La documentation.
- Les relations entre les ressources.
- Les informations nécessaires à leur réutilisation.

L'objectif est de ne pas enfermer le patrimoine dans un format propriétaire impossible à exploiter ailleurs.

### 25.2. Exportation individuelle et collective

La plateforme doit permettre d'exporter une ressource seule, une collection, une bibliothèque ou un patrimoine plus large.

Les utilisateurs doivent pouvoir choisir le périmètre de leur exportation selon leurs permissions.

Les exports doivent conserver une cohérence suffisante pour permettre la récupération des éléments associés.

### 25.3. Portabilité des bibliothèques

Une bibliothèque doit pouvoir être transférée ou récupérée dans un autre environnement sans perdre inutilement son organisation.

Les informations nécessaires à la compréhension de ses ressources doivent accompagner l'exportation.

### 25.4. Portabilité des historiques

Lorsque cela est possible, les historiques et informations de provenance doivent pouvoir être exportés avec les ressources.

La plateforme doit éviter que la seule manière de comprendre l'origine d'un composant soit de consulter son interface en ligne.

### 25.5. Limitation de la dépendance au service

La plateforme doit offrir une autonomie suffisante pour que les utilisateurs ne soient pas prisonniers de son fonctionnement.

La possibilité de récupérer les codes sources, les données et les informations structurantes est une exigence importante.

La plateforme doit conserver sa valeur comme environnement de gestion et de distribution, sans devenir un obstacle à l'utilisation indépendante des ressources.

---

## 26. Continuité des activités

### 26.1. Maintien des activités importantes

La plateforme doit permettre d'identifier les fonctions indispensables à la continuité des activités.

Cela concerne notamment la consultation des ressources, l'accès aux fichiers sources, la gestion des versions, l'exportation et la récupération des patrimoines.

Une indisponibilité temporaire d'une fonction secondaire ne doit pas nécessairement empêcher toutes les opérations importantes.

### 26.2. Indisponibilité des services externes

Les sources et registres externes peuvent devenir temporairement indisponibles.

La plateforme doit pouvoir distinguer les ressources déjà conservées des opérations qui nécessitent un accès externe.

Elle doit informer les utilisateurs des limitations rencontrées.

### 26.3. Continuité organisationnelle

Les organisations doivent pouvoir continuer à gérer leurs ressources malgré les changements de membres, d'administrateurs ou de responsables.

Les responsabilités doivent pouvoir être transférées et les informations historiques préservées.

### 26.4. Continuité des publications

Les ressources déjà distribuées doivent conserver un statut compréhensible même lorsque leur propriétaire modifie son organisation interne ou change de responsable.

La plateforme doit permettre de suivre les versions existantes, les éventuelles dépréciations et les conditions de continuité de leur distribution.

---

# PARTIE X — QUALITÉ DU PRODUIT ET AMÉLIORATION CONTINUE

## 27. Suivi de la qualité de la plateforme elle-même

### 27.1. Distinguer qualité des ressources et qualité du produit

La plateforme doit suivre deux dimensions différentes.

La première concerne la qualité des ressources qu'elle héberge, personnalise et distribue.

La seconde concerne la qualité du produit lui-même : fiabilité, performance, facilité d'utilisation, sécurité, cohérence et stabilité.

Ces deux dimensions sont liées, mais ne doivent pas être confondues.

### 27.2. Suivi des erreurs fonctionnelles

La plateforme doit permettre d'identifier les fonctionnalités qui rencontrent régulièrement des problèmes.

Cela peut concerner la recherche, l'importation, l'édition, la prévisualisation, la gestion des versions, la distribution ou les opérations d'administration.

Les erreurs doivent pouvoir être regroupées par fonctionnalité et par nature afin de faciliter leur traitement.

### 27.3. Retours utilisateurs

La plateforme peut permettre aux utilisateurs de signaler des difficultés, des erreurs ou des besoins d'amélioration.

Ces retours doivent pouvoir être associés à un contexte lorsque cela est pertinent.

Il doit être possible de distinguer un problème technique, une difficulté d'utilisation, une demande d'évolution et une suggestion.

### 27.4. Amélioration continue

Les informations issues des incidents, des retours et de l'utilisation doivent pouvoir contribuer à l'amélioration du produit.

Les évolutions doivent être suivies sans perdre la cohérence avec les besoins initiaux.

Les modifications importantes doivent pouvoir être évaluées selon leur impact sur les utilisateurs, les ressources existantes et les usages déjà établis.

---

## 28. Cohérence de l'expérience globale

### 28.1. Un produit unifié

La plateforme doit donner l'impression d'un environnement cohérent, même si elle couvre de nombreux domaines fonctionnels.

La gestion des ressources, la personnalisation, la distribution, la collaboration et l'administration ne doivent pas fonctionner comme des outils indépendants qui ignorent leurs relations.

Une ressource créée dans l'environnement de personnalisation doit pouvoir être retrouvée dans le patrimoine, documentée, versionnée, partagée et distribuée sans perdre son identité.

### 28.2. Continuité des informations

Les informations relatives à une ressource doivent rester cohérentes entre les différents espaces de la plateforme.

Son nom, son origine, sa version, ses dépendances et son statut ne doivent pas présenter des informations contradictoires selon que l'utilisateur consulte le catalogue, l'éditeur, la bibliothèque ou l'environnement de distribution.

### 28.3. Réduction des opérations répétitives

La plateforme doit éviter de demander plusieurs fois les mêmes informations lorsque celles-ci sont déjà connues et suffisamment fiables.

Par exemple, une ressource dont les dépendances, la licence et les informations de provenance sont déjà documentées ne devrait pas obliger l'utilisateur à ressaisir systématiquement ces informations lors de chaque opération.

Cela ne signifie pas que les contrôles doivent être supprimés : il faut distinguer la réutilisation d'informations existantes de leur validation effective.

### 28.4. Expérience adaptée aux différents profils

L'interface doit tenir compte des différents profils d'utilisation :

- Les personnes qui recherchent et consomment des ressources.
- Les développeurs qui consultent et modifient les sources.
- Les concepteurs qui personnalisent les interfaces.
- Les responsables qui gèrent les bibliothèques.
- Les réviseurs qui examinent les contributions.
- Les administrateurs qui gèrent les espaces et les permissions.
- Les organisations qui administrent un patrimoine collectif.

Ces profils ne doivent pas être enfermés dans des parcours rigides. Un utilisateur peut exercer plusieurs fonctions selon ses besoins.

---

# PARTIE XI — SCÉNARIOS D'UTILISATION COMPLETS

## 29. Scénario 1 — Défaillance lors de l'importation d'une ressource

Un utilisateur souhaite importer une ressource provenant d'un dépôt externe.

L'opération commence, mais échoue avant la récupération complète des fichiers.

La plateforme doit indiquer que l'importation n'a pas abouti, préciser les informations disponibles sur l'erreur et éviter de présenter la ressource comme entièrement importée.

L'utilisateur doit pouvoir examiner l'opération, comprendre les éléments récupérés et relancer l'importation lorsque cela est possible.

La reprise ne doit pas créer des fichiers en double ou remplacer des éléments déjà validés.

## 30. Scénario 2 — Modification d'une ressource présentant une anomalie

Un contributeur modifie une ressource partagée.

Lors de la validation, une erreur de structure ou une dépendance incompatible est détectée.

La plateforme doit présenter le problème, indiquer les éléments concernés et permettre au contributeur de corriger sa modification.

La version de référence doit rester préservée tant que la nouvelle version n'a pas satisfait aux conditions d'intégration définies.

## 31. Scénario 3 — Récupération après suppression accidentelle

Un utilisateur supprime accidentellement une ressource importante.

Selon les règles de conservation applicables, la plateforme doit permettre de retrouver la ressource dans un état antérieur ou dans un espace de récupération.

La restauration doit préserver les versions et les informations historiques.

Si la ressource était utilisée dans plusieurs projets, les relations correspondantes doivent être prises en compte.

## 32. Scénario 4 — Compromission d'un compte

Une organisation constate qu'un compte membre a pu être compromis.

Les personnes autorisées doivent pouvoir suspendre l'accès, révoquer les sessions concernées et examiner les activités importantes associées au compte.

Elles doivent pouvoir déterminer quelles ressources et opérations ont été concernées, dans les limites des informations disponibles.

La protection du compte ne doit pas entraîner la suppression des contributions antérieures.

## 33. Scénario 5 — Dépendance présentant un problème identifié

Une dépendance utilisée par plusieurs composants fait l'objet d'un signalement de sécurité ou de compatibilité.

La plateforme doit permettre de retrouver les ressources qui utilisent cette dépendance et les projets consommateurs concernés lorsque ces informations sont disponibles.

Les responsables peuvent alors examiner les versions utilisées, déterminer les mises à jour nécessaires et suivre leur adoption.

## 34. Scénario 6 — Indisponibilité d'un registre externe

Un registre utilisé pour distribuer des composants devient temporairement inaccessible.

Les utilisateurs doivent être informés que les nouvelles publications ou certaines opérations de récupération sont affectées.

Les ressources déjà conservées dans le patrimoine ne doivent pas être considérées comme supprimées du seul fait de l'indisponibilité du registre.

La plateforme doit permettre de retrouver les dernières informations connues et de reprendre les opérations lorsque le service redevient disponible.

## 35. Scénario 7 — Organisation souhaitant récupérer son patrimoine

Une organisation décide de quitter la plateforme ou de déplacer une partie de ses activités.

Elle doit pouvoir exporter ses ressources, bibliothèques, collections et informations associées dans des formats exploitables.

Les exports doivent préserver les éléments essentiels à la compréhension et à la réutilisation du patrimoine.

Les informations sensibles ou appartenant à d'autres organisations doivent rester exclues selon les droits applicables.

## 36. Scénario 8 — Croissance importante du patrimoine

Une organisation qui gérait initialement quelques dizaines de composants possède désormais plusieurs milliers de ressources.

Elle doit pouvoir continuer à rechercher, classer, consulter, versionner et distribuer ses ressources.

Les responsables doivent pouvoir identifier les ressources sans propriétaire, les dépendances problématiques, les versions obsolètes et les éléments qui nécessitent une intervention.

L'augmentation du volume ne doit pas transformer le patrimoine en un ensemble difficile à comprendre ou à maintenir.

## 37. Scénario 9 — Changement d'administration d'une organisation

Une organisation change ses responsables administratifs.

Les nouvelles personnes autorisées doivent pouvoir reprendre la gestion des espaces, des bibliothèques, des permissions et des intégrations.

Les anciens responsables ne doivent plus conserver des accès qui ne sont plus justifiés.

Les ressources, historiques et publications doivent continuer à fonctionner sans dépendre des anciens comptes.

## 38. Scénario 10 — Préparation d'une publication importante

Une équipe prépare la publication d'une nouvelle version d'une bibliothèque utilisée par plusieurs projets.

Avant publication, elle vérifie les fichiers, les dépendances, la documentation, les licences et la compatibilité annoncée.

Elle examine également les changements apportés aux composants importants.

Les résultats des contrôles sont conservés et associés à la version concernée.

La publication n'est autorisée que lorsque les conditions définies par les responsables sont satisfaites.

---

# PARTIE XII — EXIGENCES FONDAMENTALES DE CETTE SESSION

## 39. Exigences générales

La plateforme devra satisfaire les exigences suivantes :

1. Proposer un environnement d'administration générale.
2. Distinguer clairement l'administration de la plateforme et celle des organisations.
3. Permettre aux organisations d'administrer leurs patrimoines de manière autonome dans les limites autorisées.
4. Donner une vision synthétique et détaillée de l'état du patrimoine.
5. Permettre de gérer les paramètres et politiques applicables.
6. Protéger les comptes et les sessions.
7. Contrôler les opérations sensibles.
8. Préserver la confidentialité entre les utilisateurs et les organisations.
9. Protéger les fichiers sources et les informations de configuration.
10. Permettre une gestion maîtrisée des secrets et des accès externes.
11. Prendre en compte les risques associés aux ressources provenant de sources externes.
12. Permettre de vérifier les dépendances et les contenus importés.
13. Garantir la cohérence des ressources et de leurs versions.
14. Gérer les opérations interrompues et leur reprise.
15. Permettre la sauvegarde et la restauration du patrimoine.
16. Préserver les informations de provenance et les historiques.
17. Évaluer la qualité technique, fonctionnelle et documentaire des ressources.
18. Distinguer les contrôles effectués de ceux qui n'ont pas été réalisés.
19. Permettre la validation des ressources avant leur distribution.
20. Suivre les opérations importantes et leurs résultats.
21. Fournir des informations utiles au diagnostic.
22. Permettre d'identifier, de qualifier et de suivre les incidents.
23. Préserver les performances lorsque le volume de ressources augmente.
24. Accompagner l'augmentation du nombre d'utilisateurs et d'organisations.
25. Permettre l'évolution des catégories de ressources et des environnements de consommation.
26. Administrer les sources et intégrations externes.
27. Maintenir une expérience d'administration compréhensible.
28. Permettre l'exportation et la portabilité du patrimoine.
29. Préserver la continuité des activités malgré les changements de responsables.
30. Maintenir une cohérence globale entre les différentes fonctionnalités du produit.

---

# PARTIE XIII — SYNTHÈSE DES EXIGENCES TRANSVERSALES

## 40. Principes qui doivent traverser l'ensemble du produit

Les huit sessions décrivent des domaines fonctionnels différents, mais leur mise en œuvre doit respecter des principes communs.

### 40.1. Préservation de l'identité des ressources

Une ressource doit conserver son identité indépendamment de son emplacement, de son propriétaire actuel, de ses versions ou de ses modes de distribution.

### 40.2. Préservation des codes sources

Les codes sources constituent un élément central du patrimoine. Leur conservation, leur consultation, leur modification, leur comparaison et leur exportation doivent rester maîtrisées.

### 40.3. Traçabilité des transformations

Les opérations réalisées sur une ressource doivent pouvoir être comprises : acquisition, modification, personnalisation, dérivation, validation, publication et archivage.

### 40.4. Indépendance des ressources et de leurs usages

Une ressource doit pouvoir être conservée et administrée indépendamment des projets qui la consomment.

La consommation d'une ressource ne doit pas automatiquement transférer sa propriété ou ses responsabilités.

### 40.5. Maîtrise des dépendances

Les relations entre les ressources doivent être suffisamment documentées pour permettre de comprendre leurs conséquences sur les versions, les projets et les distributions.

### 40.6. Préservation de la provenance et des licences

La plateforme doit conserver les informations disponibles sur l'origine des ressources et les conditions applicables à leur réutilisation et à leur distribution.

### 40.7. Modularité et réutilisabilité

Les fonctionnalités du produit doivent pouvoir évoluer sans rendre les ressources dépendantes d'un fonctionnement monolithique ou d'un seul environnement de consommation.

Les composants fonctionnels doivent être suffisamment indépendants pour faciliter leur maintenance, leur évolution et leur réutilisation lorsque cela est pertinent.

### 40.8. Autonomie des utilisateurs et des organisations

Les utilisateurs et les organisations doivent conserver la maîtrise de leurs patrimoines, dans les limites de leurs droits.

La plateforme doit faciliter leur travail sans créer une dépendance inutile à son interface ou à un fournisseur particulier.

### 40.9. Sécurité sans perte d'utilisabilité

Les mécanismes de sécurité doivent protéger les ressources et les utilisateurs sans rendre les opérations ordinaires inutilement complexes.

Les contrôles doivent être proportionnés aux risques et aux conséquences des opérations.

### 40.10. Évolutivité sans rupture

L'ajout de nouvelles fonctionnalités, de nouvelles catégories de ressources et de nouveaux environnements ne doit pas remettre en cause les patrimoines existants.

---

# PARTIE XIV — RÉSULTAT FINAL ATTENDU

## 41. Vision complète du produit

À l'issue des huit sessions, le besoin global décrit une plateforme de gestion, de personnalisation, de création, de gouvernance et de distribution de ressources logicielles.

Cette plateforme ne doit pas être réduite à un catalogue de composants, à un gestionnaire de paquets, à un éditeur de code ou à un registre de ressources.

Elle doit réunir les capacités nécessaires pour gérer le cycle de vie complet d'un patrimoine logiciel.

Un utilisateur doit pouvoir découvrir une ressource provenant d'une source externe, récupérer ses fichiers, comprendre son origine, examiner sa structure, la personnaliser, créer des variantes, conserver différentes versions, la documenter, la regrouper dans une bibliothèque, la partager, puis la distribuer vers différents projets et environnements.

Il doit également pouvoir récupérer des ressources provenant d'autres fournisseurs, les intégrer à son patrimoine et les faire évoluer sans perdre les informations relatives à leur provenance.

Plusieurs utilisateurs doivent pouvoir collaborer autour de ces ressources. Les organisations doivent pouvoir administrer leurs patrimoines, partager des bibliothèques et maîtriser leurs règles de contribution et de publication.

Les projets consommateurs doivent pouvoir récupérer les ressources selon les modes de distribution adaptés à leurs environnements, tout en conservant les informations nécessaires au suivi des versions et des dépendances.

Enfin, les administrateurs doivent pouvoir garantir le fonctionnement général du produit, protéger les patrimoines, suivre les opérations, traiter les incidents et assurer la pérennité des ressources.

## 42. Ce que le produit doit fondamentalement permettre

Le résultat attendu peut être résumé autour de dix capacités fondamentales :

**1. Découvrir.** Trouver des ressources logicielles issues de plusieurs sources, comprendre leur nature et identifier leurs caractéristiques.

**2. Récupérer.** Obtenir les ressources et leurs codes sources en préservant leur structure, leur provenance et les informations nécessaires à leur exploitation.

**3. Maîtriser.** Constituer un patrimoine organisé, versionné, documenté et indépendant des sources initiales.

**4. Personnaliser.** Modifier librement les ressources, leurs propriétés, leurs comportements, leurs apparences et leurs structures.

**5. Créer.** Produire de nouvelles ressources, des variantes, des ensembles composites, des bibliothèques et des systèmes de design.

**6. Organiser.** Structurer les ressources en bibliothèques, collections et espaces adaptés aux besoins individuels et collectifs.

**7. Collaborer.** Permettre à plusieurs personnes de contribuer, examiner, valider et maintenir les ressources avec des responsabilités explicites.

**8. Distribuer.** Publier et rendre les ressources accessibles selon différents modes, registres et environnements de consommation.

**9. Gouverner.** Maîtriser les droits, les versions, les dépendances, les licences, les publications, les responsabilités et les évolutions.

**10. Pérenniser.** Protéger, sauvegarder, restaurer, exporter et maintenir le patrimoine dans le temps.

## 43. Exigence centrale : un patrimoine logiciel maîtrisé de bout en bout

La valeur principale de la plateforme doit résider dans sa capacité à réunir ces opérations au sein d'un même environnement cohérent.

Les ressources ne doivent pas être de simples fichiers téléchargés puis oubliés. Elles doivent devenir des éléments identifiables, documentés, versionnés, personnalisables, réutilisables et distribuables.

Le produit doit également éviter de confondre les différents niveaux de gestion.

Un composant n'est pas nécessairement une bibliothèque. Une bibliothèque n'est pas nécessairement un système de design. Une ressource importée n'est pas nécessairement une ressource validée. Une copie personnalisée n'est pas nécessairement la ressource originale. Une publication n'est pas nécessairement la version de travail. Une ressource partagée n'est pas nécessairement une ressource dont la propriété a été transférée.

Ces distinctions doivent rester visibles dans l'ensemble du produit.

## 44. Exigence de conception ultérieure

Les huit sessions constituent un cahier de besoins fonctionnels et opérationnels global.

Elles ne constituent pas une architecture technique définitive.

La prochaine étape devra donc consister à analyser l'ensemble des besoins, identifier les domaines fonctionnels, leurs relations, les responsabilités, les flux d'information et les exigences de cohérence.

Cette analyse devra notamment vérifier :

- Que toutes les fonctionnalités demandées sont couvertes.
- Que les notions de ressource, d'implémentation, de fichier, de bibliothèque, de collection et de système de design sont correctement distinguées.
- Que les opérations de récupération, de personnalisation, de versionnement et de distribution sont cohérentes entre elles.
- Que les ressources provenant de plusieurs sources peuvent être gérées sans perte de provenance.
- Que les patrimoines personnels et organisationnels restent séparés.
- Que les mécanismes de collaboration et de gouvernance ne créent pas de contradictions.
- Que les exigences de sécurité et de qualité sont intégrées aux opérations concernées.
- Que les fonctionnalités peuvent évoluer sans rendre les ressources existantes dépendantes d'un fonctionnement particulier.
- Que l'ensemble reste suffisamment modulaire et réutilisable.
- Que les choix techniques futurs répondent aux besoins réels plutôt que de forcer les besoins à s'adapter à une technologie préalablement choisie.

Aucune technologie particulière, aucun fournisseur, aucun framework, aucun langage, aucun protocole et aucune architecture ne sont imposés par ce cahier de besoins.

Les choix de conception devront être justifiés à partir des exigences exprimées dans les huit sessions.

---

## CONCLUSION GÉNÉRALE DU CAHIER DE BESOINS

Le produit attendu est un environnement complet de maîtrise du patrimoine logiciel, depuis la découverte et l'acquisition des ressources jusqu'à leur création, leur personnalisation, leur gouvernance, leur distribution et leur exploitation dans différents projets.

Il doit permettre de travailler sur des composants individuels comme sur des ensembles beaucoup plus importants, notamment des bibliothèques, des collections et des systèmes de design complets.

Il doit accepter plusieurs sources, plusieurs origines, plusieurs environnements de consommation et plusieurs modes de distribution.

Il doit préserver les codes sources, les structures, les versions, les dépendances, les licences et les historiques.

Il doit permettre une utilisation individuelle, collective et organisationnelle, avec des mécanismes de partage et de gouvernance adaptés.

Il doit enfin garantir que les ressources restent maîtrisables, exportables et réutilisables indépendamment des évolutions du produit.

**L'ambition n'est donc pas simplement de centraliser des composants logiciels, mais de disposer d'un environnement complet permettant de constituer, faire évoluer, organiser, partager et distribuer un véritable patrimoine logiciel, sans perdre la maîtrise de ses sources, de ses transformations, de ses versions et de ses usages.**
