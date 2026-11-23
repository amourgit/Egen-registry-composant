# SESSION 4/8 — PERSONNALISATION AVANCÉE, ÉDITION DES SOURCES ET CRÉATION DE RESSOURCES LOGICIELLES

## 1. Objectif général de cette session

La plateforme doit proposer un environnement complet permettant de transformer les ressources logicielles qu'elle héberge, de les adapter à différents besoins, de créer de nouvelles ressources et de construire des ensembles logiciels cohérents à partir de composants existants ou de créations originales.

La personnalisation ne doit pas être considérée comme une simple modification superficielle de l'apparence d'un composant. Elle doit couvrir l'ensemble des dimensions qui caractérisent une ressource logicielle : son code source, sa structure, ses propriétés, son comportement, son apparence, ses dépendances, ses configurations, ses possibilités d'intégration et ses conditions d'utilisation.

Un utilisateur doit pouvoir partir d'une ressource récupérée depuis un catalogue ou un dépôt externe, examiner son contenu, comprendre son organisation, modifier librement son implémentation, adapter ses caractéristiques, tester les résultats et enregistrer une nouvelle version personnalisée.

Il doit également pouvoir partir d'une idée ou d'un besoin qui ne correspond à aucune ressource existante, puis créer une ressource entièrement nouvelle.

La plateforme doit donc répondre à deux grandes situations :

- **Transformer l'existant :** récupérer une ressource, conserver son état d'origine, la modifier, l'adapter, la décliner et produire une ou plusieurs versions personnalisées.
- **Créer du nouveau :** concevoir une ressource à partir de zéro, définir sa structure, ses caractéristiques, ses comportements, ses dépendances et sa documentation, puis l'intégrer au patrimoine logiciel.

Ces deux situations doivent pouvoir se rejoindre. Une ressource créée à partir de zéro peut réutiliser des composants existants. Une ressource personnalisée peut devenir le point de départ d'une nouvelle famille de composants. Un ensemble de composants peut être transformé en une bibliothèque ou un système de design.

La plateforme doit ainsi offrir un environnement de création suffisamment complet pour accompagner aussi bien les modifications ponctuelles que les travaux de conception plus importants.

**L'objectif fondamental est de donner à l'utilisateur une maîtrise réelle des ressources, et non de limiter sa liberté aux options de personnalisation prévues initialement par leur auteur.**

---

# PARTIE I — PRINCIPES FONDAMENTAUX DE LA PERSONNALISATION

## 2. Personnalisation intégrale des ressources

### 2.1. Liberté de transformation

Toute ressource dont l'utilisateur possède les droits de modification doit pouvoir être personnalisée en fonction de ses besoins.

La plateforme ne doit pas supposer que les caractéristiques définies par l'auteur initial sont nécessairement adaptées à tous les contextes.

Un composant peut être intéressant dans son principe, mais nécessiter des modifications importantes pour répondre aux besoins d'un projet particulier.

L'utilisateur doit donc pouvoir intervenir sur les différentes dimensions de la ressource, dans les limites de sa nature et de ses conditions de licence.

La personnalisation peut notamment concerner :

- Le code source.
- L'organisation des fichiers.
- La structure interne.
- Les propriétés exposées.
- Les paramètres configurables.
- Les comportements fonctionnels.
- Les interactions.
- Les événements.
- Les styles.
- Les couleurs.
- La typographie.
- Les dimensions.
- Les espacements.
- Les états visuels.
- Les variantes.
- Les dépendances.
- Les configurations.
- Les interfaces d'utilisation.
- Les possibilités de composition.
- La documentation.
- Les informations de compatibilité.

La plateforme ne doit pas réduire ces possibilités à un ensemble prédéfini de paramètres graphiques.

### 2.2. Personnalisation partielle ou complète

Tous les utilisateurs n'ont pas nécessairement besoin de modifier l'intégralité d'une ressource.

Certains souhaitent uniquement changer sa couleur principale, sa taille ou son apparence.

D'autres souhaitent modifier son comportement, ajouter des propriétés, remplacer une dépendance ou réorganiser complètement son implémentation.

La plateforme doit donc permettre plusieurs niveaux d'intervention.

Un utilisateur doit pouvoir effectuer une modification simple sans devoir comprendre ou modifier l'ensemble du code source.

À l'inverse, un développeur doit pouvoir accéder aux éléments nécessaires pour effectuer une transformation profonde sans être limité par les possibilités d'un éditeur visuel.

Ces deux niveaux ne doivent pas être considérés comme des environnements concurrents. Ils doivent être complémentaires et permettre de travailler sur une même ressource.

### 2.3. Préservation de la ressource initiale

La personnalisation d'une ressource importée ne doit pas entraîner la disparition ou l'altération incontrôlée de sa version d'origine.

La plateforme doit distinguer clairement :

- La ressource originale récupérée.
- L'état de travail utilisé pour les modifications.
- Les modifications non encore enregistrées comme version.
- Les versions personnalisées.
- Les variantes produites.
- Les versions publiées.
- Les éventuelles déclinaisons indépendantes.

Cette distinction est essentielle.

Un utilisateur doit pouvoir expérimenter, modifier ou même réorganiser profondément une ressource sans perdre la possibilité de retrouver son état initial.

La plateforme doit préserver suffisamment d'informations pour comprendre la relation entre la ressource originale et les transformations réalisées.

### 2.4. Liberté sans rupture de traçabilité

La liberté de modification ne doit pas conduire à perdre les informations relatives à l'origine de la ressource.

Lorsqu'un composant provenant d'une source externe est modifié, la plateforme doit pouvoir conserver les informations disponibles sur cette origine.

Elle doit également permettre de distinguer les éléments repris directement, les éléments modifiés et les éléments ajoutés lors de la personnalisation lorsque ces informations peuvent être établies.

Une ressource peut évoluer considérablement tout en conservant une relation historique avec son origine.

Cette relation doit pouvoir être consultée sans empêcher l'utilisateur de gérer sa propre version.

### 2.5. Personnalisation selon les droits applicables

La possibilité technique de modifier une ressource ne signifie pas automatiquement que toutes les modifications sont autorisées.

La plateforme doit tenir compte des licences et des conditions applicables à chaque ressource.

Elle doit permettre de connaître les restrictions identifiées avant d'engager une personnalisation ou une redistribution.

Lorsqu'une ressource est soumise à des conditions particulières, celles-ci doivent rester visibles dans le contexte de travail.

---

## 3. Nature des éléments personnalisables

La plateforme doit reconnaître que les ressources logicielles ne sont pas toutes de même nature.

Un composant d'interface, une bibliothèque, un thème, une configuration, un ensemble de modèles et une application complète ne nécessitent pas exactement les mêmes possibilités de personnalisation.

Elle doit donc adapter l'environnement de travail au type de ressource concerné.

### 3.1. Ressources unitaires

Une ressource unitaire correspond à un élément logiciel identifiable et pouvant être travaillé indépendamment.

Il peut s'agir, par exemple, d'un composant d'interface, d'un utilitaire, d'un élément graphique ou d'une configuration.

L'utilisateur doit pouvoir modifier cet élément sans être obligé de transformer toute la bibliothèque dont il provient.

### 3.2. Ressources composées

Une ressource composée regroupe plusieurs éléments qui participent ensemble à une fonctionnalité ou à une expérience.

Par exemple, un composant complexe peut être constitué de plusieurs sous-composants, de styles, de fichiers de configuration et de ressources graphiques.

La plateforme doit permettre de comprendre cette composition et d'intervenir sur les éléments concernés.

### 3.3. Bibliothèques

Une bibliothèque regroupe plusieurs ressources destinées à être utilisées ensemble ou selon une logique commune.

L'utilisateur doit pouvoir personnaliser une bibliothèque à plusieurs niveaux :

- Modifier une ressource particulière.
- Modifier plusieurs ressources.
- Ajouter de nouveaux éléments.
- Retirer des éléments.
- Réorganiser la bibliothèque.
- Harmoniser les styles.
- Adapter les dépendances.
- Faire évoluer la documentation.
- Produire une nouvelle version de l'ensemble.

La personnalisation d'une bibliothèque doit tenir compte des relations entre ses composants.

### 3.4. Systèmes de design

Un système de design ne se limite pas à une collection de composants visuels.

Il peut regrouper des règles de présentation, des tokens, des conventions, des composants, des variantes, des modèles et des ressources documentaires.

La plateforme doit donc permettre de personnaliser ces différents éléments de manière cohérente.

Un utilisateur doit pouvoir faire évoluer un système de design sans devoir modifier manuellement chaque composant de façon indépendante lorsque plusieurs éléments partagent les mêmes règles.

### 3.5. Ressources non visuelles

La personnalisation doit également concerner les ressources qui ne disposent pas nécessairement d'une représentation graphique.

Il peut s'agir de fonctions utilitaires, de bibliothèques techniques, de configurations, de scripts ou d'autres éléments logiciels.

La plateforme ne doit donc pas faire de l'aperçu visuel une condition obligatoire pour accéder à l'environnement de personnalisation.

---

# PARTIE II — ENVIRONNEMENT COMPLET D'ÉDITION DES SOURCES

## 4. Accès aux codes sources

### 4.1. Consultation intégrale du contenu

La plateforme doit permettre d'accéder aux fichiers sources qui composent une ressource.

L'utilisateur doit pouvoir examiner le contenu d'une ressource sans se limiter à sa description ou à son aperçu visuel.

Pour une ressource composée de plusieurs fichiers, il doit pouvoir naviguer dans l'ensemble de sa structure.

Il doit notamment pouvoir identifier les fichiers de code, les styles, les configurations, les ressources graphiques, la documentation et les autres éléments associés.

### 4.2. Exploration de l'arborescence

L'environnement de travail doit permettre de parcourir l'organisation des fichiers et dossiers.

L'utilisateur doit pouvoir comprendre comment les différents éléments sont regroupés et quelles relations existent entre eux.

L'arborescence doit préserver les noms, les chemins et la structure logique de la ressource.

Elle doit également permettre d'identifier les éléments importants, notamment les fichiers d'entrée, les fichiers de configuration, les composants principaux et les ressources complémentaires lorsque ces informations sont disponibles.

### 4.3. Consultation des fichiers individuels

L'utilisateur doit pouvoir ouvrir et consulter chaque fichier pertinent.

Il doit pouvoir passer d'un fichier à un autre sans perdre le contexte de son travail.

La consultation doit permettre de comprendre le contenu, les références et les relations entre les fichiers.

### 4.4. Recherche dans les sources

La plateforme doit permettre de rechercher des éléments dans le code source.

La recherche doit pouvoir porter sur :

- Un nom de fichier.
- Un nom de dossier.
- Une fonction.
- Une classe.
- Un composant.
- Une propriété.
- Une variable.
- Une méthode.
- Une référence.
- Une chaîne de caractères.
- Un élément de configuration.
- Un terme présent dans plusieurs fichiers.

L'objectif est de permettre à l'utilisateur de retrouver rapidement un élément dans une ressource volumineuse.

La recherche doit pouvoir être limitée à un fichier, un dossier, une ressource ou un ensemble de ressources selon le contexte.

### 4.5. Navigation entre les références

Lorsqu'un élément du code fait référence à un autre fichier, composant ou module, l'environnement doit faciliter la compréhension de cette relation.

L'utilisateur doit pouvoir retrouver les éléments associés sans devoir parcourir manuellement toute l'arborescence.

Cette capacité est particulièrement importante pour les ressources composées et les bibliothèques qui contiennent de nombreux fichiers.

---

## 5. Modification directe des codes sources

### 5.1. Édition complète

La plateforme doit proposer un véritable environnement d'édition du code source.

L'utilisateur doit pouvoir modifier directement le contenu des fichiers, ajouter des instructions, supprimer des éléments, réorganiser le code et transformer l'implémentation existante.

L'éditeur ne doit pas être limité à la modification de quelques champs ou paramètres prédéfinis.

Il doit permettre de travailler sur les fichiers sources dans leur ensemble, dans les limites des formats pris en charge.

### 5.2. Gestion de plusieurs fichiers

La modification d'une ressource nécessite souvent d'intervenir sur plusieurs fichiers.

L'utilisateur doit pouvoir travailler sur différents fichiers au cours d'une même session.

Il doit pouvoir comprendre quels fichiers ont été modifiés, lesquels sont encore dans leur état initial et lesquels ont été ajoutés ou supprimés.

La plateforme doit permettre de retrouver rapidement les fichiers concernés par les modifications en cours.

### 5.3. Opérations sur les fichiers

L'environnement de travail doit permettre d'effectuer les opérations nécessaires à la modification d'une ressource :

- Créer un fichier.
- Ajouter un dossier.
- Renommer un fichier.
- Renommer un dossier.
- Déplacer un fichier.
- Déplacer un dossier.
- Supprimer un fichier.
- Supprimer un dossier.
- Dupliquer un élément.
- Réorganiser l'arborescence.
- Modifier le contenu des fichiers.

Ces opérations doivent être prises en compte dans l'historique de travail de la ressource.

### 5.4. Gestion des modifications non enregistrées

L'utilisateur doit pouvoir identifier les modifications qui n'ont pas encore été enregistrées dans une version de référence.

La plateforme doit éviter qu'une navigation, un changement d'espace ou une fermeture involontaire provoque la perte silencieuse d'un travail en cours.

Elle doit permettre de distinguer les modifications enregistrées des modifications encore en attente.

### 5.5. Annulation et rétablissement

L'environnement doit permettre d'annuler certaines opérations et de rétablir des modifications précédemment annulées.

Cette capacité doit couvrir les opérations courantes d'édition et les changements apportés aux fichiers lorsque cela est possible.

L'utilisateur doit pouvoir revenir sur une modification sans devoir recommencer manuellement toutes les opérations suivantes.

### 5.6. Comparaison des fichiers

La plateforme doit permettre de comparer différents états d'un fichier.

L'utilisateur doit pouvoir identifier les lignes ou les parties qui ont été ajoutées, supprimées ou modifiées.

Cette comparaison doit être possible entre l'état de travail et la version précédente, entre deux versions enregistrées ou entre une version originale et une version personnalisée.

### 5.7. Gestion des modifications à grande échelle

La plateforme doit également prendre en compte les situations dans lesquelles une modification affecte plusieurs fichiers.

L'utilisateur doit pouvoir identifier le périmètre de la modification et examiner les conséquences sur l'ensemble de la ressource.

Il doit être possible de distinguer les modifications intentionnelles des changements secondaires provoqués par une opération de transformation.

---

## 6. Fonctionnalités avancées de l'environnement d'édition

### 6.1. Assistance à l'écriture du code

L'éditeur doit faciliter le travail de développement.

Selon les formats et langages pris en charge, cela peut inclure :

- La coloration syntaxique.
- L'indentation.
- La mise en forme du code.
- L'autocomplétion.
- La navigation dans les symboles.
- L'identification des erreurs.
- Les suggestions de correction.
- La recherche de références.
- L'affichage des informations contextuelles.
- L'aide à la compréhension du code.

Ces fonctionnalités doivent améliorer la productivité sans limiter la liberté de modification.

### 6.2. Aide à la compréhension

L'utilisateur peut récupérer une ressource qu'il n'a pas créée et dont il ne maîtrise pas immédiatement l'organisation.

La plateforme doit faciliter la compréhension de son contenu.

Elle peut notamment aider à identifier :

- Le rôle des fichiers.
- Les composants principaux.
- Les points d'entrée.
- Les propriétés disponibles.
- Les dépendances.
- Les relations entre les modules.
- Les configurations importantes.
- Les éléments qui contrôlent l'apparence.
- Les éléments qui contrôlent le comportement.

L'assistance doit s'appuyer sur les informations réellement disponibles.

Elle ne doit pas présenter une interprétation incertaine comme une caractéristique confirmée de la ressource.

### 6.3. Assistance à la modification

L'utilisateur doit pouvoir bénéficier d'une aide pour comprendre les conséquences d'une modification et identifier les éléments à adapter.

Par exemple, lorsqu'il souhaite changer le comportement d'un composant, l'environnement peut l'aider à retrouver les fichiers susceptibles d'être concernés.

Lorsqu'il souhaite ajouter une propriété, il peut être utile d'identifier les endroits où cette propriété doit être déclarée, utilisée et documentée.

L'objectif est de faciliter les transformations sans imposer une manière unique de coder.

### 6.4. Assistance à la correction

La plateforme peut proposer des suggestions lorsqu'elle identifie des erreurs ou des incohérences.

Ces suggestions doivent être compréhensibles et permettre à l'utilisateur de décider s'il souhaite les appliquer.

Une correction suggérée ne doit pas modifier automatiquement les fichiers sans que l'utilisateur puisse comprendre le changement réalisé.

### 6.5. Contrôle des changements proposés

Lorsqu'une assistance automatique produit une modification, l'utilisateur doit pouvoir examiner les changements avant leur intégration.

Il doit pouvoir comparer l'état initial et le résultat proposé, accepter ou refuser les modifications et conserver la possibilité de revenir à l'état précédent.

L'assistance doit rester un moyen d'accélérer le travail, et non un mécanisme qui retire à l'utilisateur la maîtrise de ses sources.

---

# PARTIE III — PERSONNALISATION VISUELLE ET INTERFACE DE CONCEPTION

## 7. Édition visuelle des ressources

### 7.1. Environnement de personnalisation visuelle

La plateforme doit proposer un environnement permettant de modifier visuellement les ressources qui possèdent une représentation graphique.

L'utilisateur doit pouvoir observer le rendu d'un composant et ajuster ses caractéristiques visuelles sans devoir nécessairement intervenir directement dans le code pour chaque modification.

Cet environnement doit être relié à la ressource réellement travaillée.

Il ne doit pas s'agir d'une simple maquette indépendante dont le résultat ne pourrait pas être répercuté dans les fichiers sources.

### 7.2. Modification des propriétés visuelles

L'utilisateur doit pouvoir personnaliser les caractéristiques visuelles pertinentes :

- Couleurs.
- Arrière-plans.
- Bordures.
- Rayons.
- Ombres.
- Dimensions.
- Largeurs.
- Hauteurs.
- Espacements.
- Marges.
- Alignements.
- Typographies.
- Tailles de texte.
- Graisses.
- Opacités.
- Icônes.
- Images.
- Transitions.
- Animations.
- États visuels.

Les possibilités doivent être adaptées au type de composant et à sa structure.

### 7.3. Modification de la composition visuelle

Au-delà des propriétés individuelles, l'utilisateur doit pouvoir intervenir sur la disposition des éléments.

Selon les capacités de la ressource, cela peut inclure :

- La disposition des sous-éléments.
- Leur alignement.
- Leur espacement.
- Leur ordre.
- Leur positionnement.
- Leur regroupement.
- Leur visibilité.
- Leur organisation dans différentes zones.

Cette capacité est importante pour les composants complexes qui ne peuvent pas être personnalisés uniquement en changeant quelques couleurs.

### 7.4. Gestion des états visuels

Un composant interactif peut présenter plusieurs états.

L'environnement doit permettre de les examiner et, lorsque cela est pertinent, de les personnaliser.

Par exemple :

- État normal.
- État survolé.
- État actif.
- État sélectionné.
- État désactivé.
- État de chargement.
- État de validation.
- État d'erreur.
- État ouvert.
- État fermé.
- État de focus.

La plateforme doit permettre de comprendre à quel comportement correspond chaque état.

### 7.5. Prévisualisation des modifications

Les modifications visuelles doivent pouvoir être observées rapidement.

Lorsqu'un utilisateur modifie une propriété, il doit pouvoir examiner le résultat sans devoir systématiquement publier la ressource ou l'intégrer dans un projet externe.

L'aperçu doit représenter autant que possible le comportement réel du composant.

Les limitations de prévisualisation doivent être signalées lorsqu'une ressource nécessite un contexte particulier pour fonctionner correctement.

---

## 8. Modification des thèmes et des styles

### 8.1. Personnalisation des thèmes

La plateforme doit permettre de modifier les thèmes associés aux ressources.

Cela concerne notamment les couleurs principales, secondaires et complémentaires, les arrière-plans, les surfaces, les textes, les bordures et les états fonctionnels.

L'utilisateur doit pouvoir adapter une ressource à une identité visuelle particulière.

### 8.2. Gestion des tokens de design

Lorsque la ressource utilise des tokens de design, l'utilisateur doit pouvoir les consulter, les modifier et les organiser.

Ces tokens peuvent concerner :

- Les couleurs.
- Les typographies.
- Les espacements.
- Les dimensions.
- Les rayons.
- Les ombres.
- Les niveaux d'élévation.
- Les opacités.
- Les transitions.
- Les autres valeurs partagées.

La plateforme doit permettre de comprendre quels composants utilisent les tokens concernés.

### 8.3. Modification centralisée

Lorsque plusieurs ressources utilisent des valeurs communes, l'utilisateur doit pouvoir modifier ces valeurs de manière cohérente.

Une modification d'un token partagé peut affecter plusieurs composants.

La plateforme doit donc permettre d'identifier les ressources concernées avant ou après la modification.

### 8.4. Variations de thèmes

Un même ensemble de composants peut nécessiter plusieurs thèmes.

La plateforme doit permettre de créer et de gérer différentes déclinaisons visuelles.

Par exemple, un même système de design peut proposer plusieurs identités visuelles ou plusieurs modes d'affichage.

Ces variations doivent pouvoir être conservées et comparées sans dupliquer inutilement toutes les ressources.

### 8.5. Modes d'affichage

Lorsque les ressources le permettent, l'environnement doit pouvoir prendre en compte plusieurs modes d'affichage, notamment les thèmes clair et sombre.

Il doit être possible d'examiner les composants dans ces différents contextes et de personnaliser les règles associées.

### 8.6. Cohérence entre les composants

La personnalisation d'un système de design doit permettre de maintenir une cohérence entre les composants.

L'utilisateur doit pouvoir identifier les composants qui ne respectent plus les règles communes et ceux qui utilisent encore des valeurs particulières.

Cette capacité est importante lorsqu'une bibliothèque comprend un grand nombre de composants.

---

# PARTIE IV — PERSONNALISATION FONCTIONNELLE ET COMPORTEMENTALE

## 9. Modification des propriétés et des paramètres

### 9.1. Gestion des propriétés exposées

Les composants peuvent proposer des propriétés permettant de modifier leur apparence ou leur comportement.

La plateforme doit permettre de consulter et de modifier ces propriétés.

L'utilisateur doit pouvoir comprendre :

- Leur nom.
- Leur rôle.
- Leur type.
- Leur valeur par défaut.
- Leur caractère obligatoire ou facultatif.
- Les valeurs autorisées lorsque celles-ci sont définies.
- Leur effet sur le composant.

### 9.2. Ajout de nouvelles propriétés

L'utilisateur doit pouvoir ajouter de nouvelles propriétés lorsque la nature de la ressource le permet.

Par exemple, un composant peut initialement proposer un titre et un texte, puis être étendu pour accepter une icône, un état supplémentaire ou un paramètre de présentation.

L'ajout d'une propriété doit pouvoir être répercuté dans les éléments concernés de la ressource.

### 9.3. Modification des propriétés existantes

Il doit être possible de modifier les propriétés déjà présentes.

Cela peut concerner leur nom, leur type, leur valeur par défaut, leurs contraintes ou leur comportement.

La plateforme doit permettre d'identifier les éventuelles conséquences sur les projets qui utilisent déjà la ressource.

### 9.4. Suppression des propriétés

L'utilisateur doit pouvoir supprimer une propriété devenue inutile lorsque les conditions de modification le permettent.

La plateforme doit toutefois signaler les éventuelles références à cette propriété dans d'autres parties du composant ou dans les projets consommateurs connus.

### 9.5. Organisation des propriétés

Lorsque le nombre de propriétés devient important, leur organisation doit rester compréhensible.

L'utilisateur doit pouvoir les regrouper selon leur fonction, leur nature ou leur rôle dans la personnalisation du composant.

Cette organisation doit faciliter aussi bien l'édition que la documentation et l'utilisation future de la ressource.

---

## 10. Modification des comportements

### 10.1. Liberté de modification fonctionnelle

La personnalisation doit permettre de modifier ce que fait un composant, et pas uniquement son apparence.

Un utilisateur doit pouvoir adapter les interactions, les règles de fonctionnement et les réponses du composant aux actions de l'utilisateur final.

Par exemple, un composant initialement prévu pour afficher des informations peut être transformé pour intégrer des actions supplémentaires.

### 10.2. Gestion des événements

La plateforme doit permettre de modifier ou d'étendre les événements pris en charge par une ressource lorsque son implémentation le permet.

Cela peut concerner les événements déclenchés par les interactions, les changements d'état ou les actions effectuées sur le composant.

L'utilisateur doit pouvoir comprendre quels événements existent et comment ils sont utilisés.

### 10.3. Gestion des interactions

L'environnement doit permettre d'examiner et de modifier les interactions d'un composant.

Cela peut concerner :

- Les clics.
- Les sélections.
- Les changements de valeur.
- Les ouvertures et fermetures.
- Les validations.
- Les soumissions.
- Les changements d'état.
- Les interactions entre plusieurs sous-composants.

### 10.4. Gestion des états fonctionnels

La plateforme doit permettre de comprendre les états internes ou fonctionnels d'une ressource lorsque ceux-ci sont identifiables.

L'utilisateur doit pouvoir modifier leur gestion et leurs transitions.

Cela peut notamment concerner les composants de formulaire, les menus, les fenêtres modales, les systèmes de navigation et les composants interactifs complexes.

### 10.5. Extension des fonctionnalités

L'utilisateur doit pouvoir ajouter de nouvelles fonctionnalités à une ressource.

Il peut notamment ajouter un nouveau comportement, une action supplémentaire, un état particulier ou une capacité de configuration.

La plateforme doit permettre de distinguer les fonctionnalités initiales de celles ajoutées au cours de la personnalisation lorsque cette distinction est pertinente.

---

## 11. Gestion des variantes

### 11.1. Principe des variantes

Une même ressource peut nécessiter plusieurs déclinaisons sans qu'il soit nécessaire de considérer chacune d'elles comme une ressource totalement indépendante.

La plateforme doit permettre de créer et de gérer ces variantes.

Une variante peut représenter une différence visuelle, fonctionnelle, structurelle ou contextuelle.

### 11.2. Variantes visuelles

Un composant peut avoir plusieurs apparences tout en conservant son rôle principal.

Par exemple, un bouton peut disposer de plusieurs styles, tailles, couleurs ou niveaux d'importance.

La plateforme doit permettre de créer et de maintenir ces variantes.

### 11.3. Variantes fonctionnelles

Une ressource peut proposer plusieurs comportements selon son utilisation.

Un composant peut, par exemple, proposer un mode simple et un mode avancé, ou plusieurs modes d'interaction.

La plateforme doit permettre de distinguer ces comportements et de les documenter.

### 11.4. Variantes contextuelles

Une ressource peut être adaptée à différents contextes d'utilisation.

Par exemple, un composant peut être utilisé dans une interface d'administration, une interface publique ou un environnement mobile.

La plateforme doit permettre de gérer les différences nécessaires à ces contextes.

### 11.5. Variantes technologiques

Il peut être nécessaire de proposer plusieurs implémentations d'une même ressource selon les environnements ciblés.

La plateforme doit permettre de gérer ces implémentations sans perdre l'identité et la relation entre les différentes déclinaisons.

Une même ressource conceptuelle peut ainsi disposer de plusieurs réalisations adaptées à différents environnements.

### 11.6. Gestion des variantes apparentées

Les variantes doivent pouvoir être regroupées et comparées.

L'utilisateur doit pouvoir comprendre ce qui est commun et ce qui diffère entre elles.

Une modification d'un élément partagé doit pouvoir être examinée au regard de ses conséquences sur les différentes variantes.

La plateforme doit éviter de transformer une modification commune en une modification incontrôlée de toutes les déclinaisons.

---

# PARTIE V — CRÉATION DE RESSOURCES À PARTIR DE ZÉRO

## 12. Création d'une nouvelle ressource

### 12.1. Création indépendante

La plateforme doit permettre de créer une ressource qui ne provient pas nécessairement d'un composant déjà enregistré.

L'utilisateur doit pouvoir partir d'un besoin, d'une idée ou d'une spécification et construire progressivement une nouvelle ressource.

La création doit être possible même lorsqu'aucune ressource existante ne correspond au résultat recherché.

### 12.2. Définition initiale

Lorsqu'une nouvelle ressource est créée, l'utilisateur doit pouvoir renseigner les informations nécessaires à son identification et à son organisation.

Cela peut notamment concerner :

- Son nom.
- Sa description.
- Sa catégorie.
- Sa nature.
- Son objectif.
- Son environnement cible.
- Sa technologie lorsqu'elle est pertinente.
- Son état initial.
- Son espace de destination.
- Son propriétaire ou responsable.
- Les informations documentaires disponibles.

Les informations requises doivent être adaptées au type de ressource.

### 12.3. Création d'une structure de fichiers

L'utilisateur doit pouvoir construire l'organisation de la nouvelle ressource.

Il doit pouvoir créer des fichiers et des dossiers, définir leur contenu et organiser les éléments selon les besoins du projet.

La plateforme ne doit pas imposer une structure unique à toutes les catégories de ressources.

Elle doit toutefois pouvoir proposer des structures de départ lorsque cela facilite la création.

### 12.4. Création à partir d'un modèle

La plateforme doit pouvoir permettre de démarrer une nouvelle ressource à partir d'un modèle existant.

Un modèle peut fournir une structure initiale, des fichiers, des configurations ou des conventions.

L'utilisateur doit pouvoir modifier ce modèle pour l'adapter à ses besoins.

Il faut distinguer le modèle de départ de la ressource créée à partir de celui-ci.

La création ne doit pas entraîner la modification du modèle original.

### 12.5. Création à partir d'une ressource existante

L'utilisateur doit également pouvoir utiliser une ressource existante comme point de départ.

Il peut vouloir créer une déclinaison fortement personnalisée, une nouvelle variante ou une ressource dérivée.

La plateforme doit permettre de préserver la relation avec la ressource initiale sans empêcher l'évolution indépendante de la nouvelle création.

---

## 13. Création de composants d'interface

### 13.1. Création de composants individuels

La plateforme doit permettre de créer des composants d'interface destinés à être réutilisés.

L'utilisateur doit pouvoir définir leur structure, leur apparence, leurs propriétés et leurs comportements.

Un composant ne doit pas être considéré comme terminé simplement parce qu'il possède un rendu visuel.

Il doit pouvoir disposer d'une identité, d'une description, d'une organisation de fichiers et des informations nécessaires à son utilisation.

### 13.2. Composition interne

Un composant peut être constitué de plusieurs sous-composants.

La plateforme doit permettre de définir cette organisation.

L'utilisateur doit pouvoir comprendre les éléments qui composent le composant principal et intervenir sur les parties nécessaires.

### 13.3. Propriétés configurables

Le composant doit pouvoir exposer des propriétés adaptées à ses usages.

Ces propriétés doivent permettre de modifier les éléments prévus sans devoir intervenir systématiquement dans le code source.

### 13.4. États et interactions

Le composant doit pouvoir présenter différents états et gérer les interactions nécessaires à son rôle.

L'environnement de création doit permettre de les définir et de les tester.

### 13.5. Documentation du composant

L'utilisateur doit pouvoir documenter le composant, ses propriétés, ses comportements, ses variantes et ses conditions d'utilisation.

Cette documentation doit accompagner la ressource lorsqu'elle est intégrée à une bibliothèque ou distribuée.

---

## 14. Création de ressources plus complexes

### 14.1. Création d'ensembles composites

La plateforme doit permettre de regrouper plusieurs ressources pour former un ensemble cohérent.

Un ensemble composite peut contenir des composants, des sous-composants, des ressources graphiques, des configurations et d'autres éléments associés.

L'utilisateur doit pouvoir définir les relations entre ces éléments.

### 14.2. Création de bibliothèques

L'utilisateur doit pouvoir créer une bibliothèque à partir de ressources existantes ou de nouvelles créations.

Il doit pouvoir définir son contenu, son organisation, ses catégories et ses règles de cohérence.

La bibliothèque doit disposer de sa propre identité et de son propre cycle de vie, sans effacer l'identité individuelle des ressources qui la composent.

### 14.3. Création de familles de composants

La plateforme doit permettre de construire des familles de composants partageant des caractéristiques communes.

Une famille peut regrouper des composants apparentés, des variantes ou des déclinaisons destinées à des usages différents.

L'utilisateur doit pouvoir identifier les éléments communs et les différences entre les membres de cette famille.

### 14.4. Création de systèmes de design

L'environnement doit permettre de construire un système de design à partir de zéro ou de faire évoluer un système existant.

Ce système peut réunir :

- Des tokens.
- Des règles visuelles.
- Des couleurs.
- Des typographies.
- Des espacements.
- Des composants.
- Des variantes.
- Des modèles.
- Des règles d'utilisation.
- Des ressources documentaires.

La plateforme doit permettre de travailler sur ces éléments comme sur un ensemble cohérent.

### 14.5. Création de modèles réutilisables

L'utilisateur doit pouvoir transformer une structure ou un ensemble de ressources en modèle réutilisable.

Un modèle doit pouvoir servir de point de départ à de nouvelles créations.

Il doit conserver les informations utiles à sa réutilisation sans imposer que toutes les créations dérivées restent identiques.

---

# PARTIE VI — COMPOSITION ET RÉUTILISATION DES RESSOURCES

## 15. Assemblage de ressources existantes

### 15.1. Réutilisation de composants

La plateforme doit faciliter la création de nouvelles ressources à partir de composants déjà disponibles dans le patrimoine.

L'utilisateur doit pouvoir sélectionner des ressources existantes et les intégrer à une nouvelle composition lorsque leur nature le permet.

Cette capacité doit éviter de recréer systématiquement des éléments qui existent déjà.

### 15.2. Assemblage de composants hétérogènes

Un ensemble peut contenir des ressources provenant de différentes sources ou ayant été créées dans des contextes différents.

La plateforme doit permettre de les réunir tout en conservant leurs identités, leurs origines et leurs informations propres.

Le fait de les réunir ne doit pas faire disparaître les distinctions entre leurs implémentations.

### 15.3. Gestion des relations entre éléments

L'utilisateur doit pouvoir comprendre comment les composants d'un ensemble sont liés.

Il doit notamment pouvoir identifier les composants utilisés par d'autres composants, les éléments partagés et les dépendances internes.

### 15.4. Substitution d'un composant

Lorsqu'un ensemble utilise un composant particulier, l'utilisateur doit pouvoir envisager de le remplacer par une autre ressource compatible.

La plateforme doit permettre d'examiner les conséquences de cette substitution.

Cela concerne notamment les propriétés attendues, les comportements, les dépendances et les éventuelles différences d'interface.

### 15.5. Modification d'un ensemble sans altération des sources

Lorsqu'une ressource est intégrée à un nouvel ensemble, les modifications apportées à cet ensemble ne doivent pas nécessairement modifier la ressource originale.

La plateforme doit permettre de distinguer l'utilisation d'une ressource, sa référence et sa transformation.

Cette distinction est fondamentale pour permettre la réutilisation d'un même composant dans plusieurs projets.

---

## 16. Gestion des dépendances pendant la création

### 16.1. Identification des dépendances

Lorsqu'une nouvelle ressource utilise d'autres éléments, la plateforme doit permettre d'identifier les dépendances correspondantes.

Cela peut concerner des composants internes, des bibliothèques externes, des ressources graphiques, des utilitaires ou des éléments de configuration.

### 16.2. Déclaration des dépendances

L'utilisateur doit pouvoir comprendre quelles dépendances sont nécessaires à la ressource et quelles dépendances sont facultatives.

Les informations disponibles doivent permettre d'identifier les versions ou contraintes applicables.

### 16.3. Gestion des changements de dépendances

Lorsqu'une dépendance est ajoutée, remplacée ou supprimée, la plateforme doit permettre d'enregistrer ce changement.

Elle doit également permettre d'identifier les conséquences possibles sur la ressource.

### 16.4. Détection des dépendances manquantes

La plateforme doit pouvoir signaler les dépendances qui ne sont pas disponibles ou dont la résolution n'est pas possible.

L'utilisateur doit pouvoir examiner ces problèmes avant de considérer la ressource comme prête à être utilisée.

### 16.5. Cohérence des ensembles composites

Un ensemble composite doit pouvoir être examiné dans sa globalité.

Il faut éviter qu'un ensemble soit présenté comme complet alors que des éléments nécessaires à son fonctionnement sont absents ou incompatibles.

---

# PARTIE VII — ENVIRONNEMENT DE PRÉVISUALISATION ET D'EXPÉRIMENTATION

## 17. Prévisualisation des ressources

### 17.1. Prévisualisation intégrée

La plateforme doit permettre de visualiser les ressources dont la nature autorise un aperçu.

Cette prévisualisation doit être directement liée à la ressource en cours de création ou de personnalisation.

Elle doit permettre de vérifier rapidement le résultat des modifications.

### 17.2. Prévisualisation des composants

Pour les composants d'interface, l'utilisateur doit pouvoir examiner leur rendu dans différents contextes.

Cela peut notamment inclure :

- Différentes tailles.
- Différentes valeurs de propriétés.
- Différents états.
- Différentes variantes.
- Différents thèmes.
- Différentes dispositions.
- Différentes configurations.

### 17.3. Prévisualisation des ensembles

Les ensembles composites doivent également pouvoir être prévisualisés lorsque cela est possible.

L'objectif est de vérifier le comportement des ressources lorsqu'elles sont utilisées ensemble, plutôt que de ne tester que les composants séparément.

### 17.4. Prévisualisation des systèmes de design

Un système de design doit pouvoir être examiné à travers ses composants et ses règles visuelles.

L'utilisateur doit pouvoir comprendre la cohérence de l'ensemble et identifier les éléments qui nécessitent une adaptation.

### 17.5. Limites de prévisualisation

Certaines ressources ne peuvent pas être prévisualisées sans dépendances, données ou conditions particulières.

La plateforme doit permettre de signaler ces limitations.

Elle ne doit pas afficher un aperçu trompeur qui laisserait penser que la ressource a été entièrement exécutée ou validée alors que ce n'est pas le cas.

---

## 18. Expérimentation et essais

### 18.1. Espace d'expérimentation

L'utilisateur doit pouvoir expérimenter des modifications sans devoir immédiatement les intégrer à une version stable.

Il doit pouvoir tester plusieurs pistes, comparer différents résultats et abandonner une proposition sans altérer le patrimoine de référence.

### 18.2. Plusieurs pistes de travail

Une même ressource peut nécessiter plusieurs propositions de personnalisation.

La plateforme doit permettre de conserver des états de travail distincts lorsque cela est utile.

Par exemple, un utilisateur peut tester une refonte visuelle tout en conservant une autre piste consacrée à l'évolution fonctionnelle du composant.

### 18.3. Comparaison des expérimentations

Les différentes pistes doivent pouvoir être comparées.

L'utilisateur doit pouvoir examiner leurs différences et déterminer laquelle doit être conservée ou intégrée.

### 18.4. Abandon d'une expérimentation

Une expérimentation qui n'est pas retenue doit pouvoir être abandonnée sans affecter la version de référence.

La plateforme doit permettre de distinguer une expérimentation temporaire d'une version effectivement intégrée au patrimoine.

### 18.5. Promotion d'une expérimentation

Lorsqu'une expérimentation est retenue, l'utilisateur doit pouvoir l'intégrer dans le cycle de vie de la ressource.

Cette intégration doit préserver les informations nécessaires pour comprendre d'où vient la nouvelle version et quelles modifications ont été retenues.

---

# PARTIE VIII — VERSIONNEMENT ET ÉVOLUTION DES TRAVAUX

## 19. Gestion des états de travail

### 19.1. Distinction entre travail et version enregistrée

Toutes les modifications réalisées ne doivent pas nécessairement devenir immédiatement une nouvelle version officielle.

La plateforme doit permettre de travailler progressivement et de conserver des modifications en cours.

Une version enregistrée doit correspondre à un état identifiable et récupérable.

### 19.2. Enregistrement des modifications

L'utilisateur doit pouvoir enregistrer son travail à des moments choisis.

L'enregistrement doit permettre de retrouver l'état correspondant des fichiers et des informations associées.

### 19.3. Description des modifications

L'utilisateur doit pouvoir documenter les changements réalisés.

Il doit pouvoir indiquer ce qui a été modifié, pourquoi la modification a été effectuée et quelles conséquences sont attendues.

### 19.4. Historique des transformations

La plateforme doit conserver un historique suffisamment détaillé pour comprendre l'évolution d'une ressource.

Cet historique doit pouvoir faire apparaître les modifications importantes, les versions enregistrées, les variantes créées et les transformations réalisées.

### 19.5. Retour à un état précédent

L'utilisateur doit pouvoir retrouver un état antérieur lorsque cela est nécessaire.

Le retour à un état précédent ne doit pas effacer automatiquement les informations sur les versions plus récentes.

---

## 20. Gestion de plusieurs versions et branches de travail

### 20.1. Évolutions parallèles

Une ressource peut nécessiter plusieurs évolutions en parallèle.

Par exemple, une équipe peut travailler sur une refonte visuelle pendant qu'une autre prépare une amélioration fonctionnelle.

La plateforme doit permettre de gérer ces travaux sans imposer leur fusion immédiate.

### 20.2. Comparaison des évolutions

Les différentes évolutions doivent pouvoir être comparées.

L'utilisateur doit pouvoir identifier les changements apportés à chaque version et les éléments communs.

### 20.3. Fusion des modifications

Lorsque plusieurs évolutions doivent être réunies, la plateforme doit permettre d'examiner les modifications et de maîtriser leur intégration.

Elle doit pouvoir identifier les situations dans lesquelles deux modifications affectent les mêmes fichiers ou éléments.

### 20.4. Gestion des conflits

Lorsque des modifications sont incompatibles, l'utilisateur doit pouvoir comprendre le conflit et choisir la manière de le résoudre.

La plateforme ne doit pas écraser silencieusement des changements importants.

### 20.5. Conservation des versions indépendantes

Toutes les évolutions parallèles ne doivent pas nécessairement être fusionnées.

Certaines peuvent devenir des variantes permanentes ou des déclinaisons indépendantes.

La plateforme doit permettre de conserver ces situations sans imposer une seule version unique pour tous les usages.

---

# PARTIE IX — COORDINATION ENTRE ÉDITION VISUELLE ET ÉDITION DU CODE

## 21. Cohérence entre les différentes formes d'édition

### 21.1. Un même patrimoine, plusieurs modes d'intervention

La plateforme doit permettre de travailler sur une même ressource à travers plusieurs modes d'édition.

Un utilisateur peut modifier directement le code, tandis qu'un autre intervient sur les propriétés visuelles.

Ces opérations doivent concerner la même ressource et ne pas créer des versions sans relation entre elles.

### 21.2. Répercussion des modifications

Lorsqu'une modification effectuée dans l'environnement visuel correspond à un changement dans les sources, ce changement doit pouvoir être intégré dans les fichiers concernés.

De la même manière, une modification du code qui affecte les caractéristiques visuelles doit pouvoir être prise en compte dans l'aperçu lorsque les conditions le permettent.

### 21.3. Prévention des incohérences

La plateforme doit éviter que les différentes représentations d'une ressource deviennent contradictoires.

Par exemple, un éditeur de propriétés ne doit pas continuer à présenter une propriété comme disponible alors qu'elle a été supprimée du code source et que cette suppression a été reconnue.

### 21.4. Identification des modifications non répercutées

Lorsqu'une modification ne peut pas être automatiquement représentée dans un autre mode d'édition, la plateforme doit le signaler.

L'utilisateur doit comprendre quelles parties sont synchronisées et lesquelles nécessitent une intervention supplémentaire.

### 21.5. Liberté de revenir au code

L'édition visuelle ne doit pas enfermer l'utilisateur dans une interface de configuration.

Il doit pouvoir accéder au code source à tout moment lorsqu'il souhaite effectuer une transformation qui dépasse les possibilités de l'éditeur visuel.

---

# PARTIE X — GESTION DES ASSETS ET DES RESSOURCES ASSOCIÉES

## 22. Gestion des éléments graphiques

### 22.1. Assets graphiques

La plateforme doit permettre de gérer les éléments graphiques associés aux ressources.

Cela peut inclure :

- Images.
- Illustrations.
- Icônes.
- Logos.
- Illustrations vectorielles.
- Fonds.
- Textures.
- Éléments décoratifs.
- Ressources graphiques complémentaires.

L'utilisateur doit pouvoir les consulter, les remplacer, les ajouter et les organiser.

### 22.2. Modification des assets

Lorsque la nature du fichier le permet, l'utilisateur doit pouvoir modifier ou remplacer un asset.

La plateforme doit permettre d'identifier les ressources qui utilisent cet asset afin d'évaluer les conséquences de son remplacement.

### 22.3. Préservation des fichiers originaux

La modification d'un asset ne doit pas nécessairement détruire le fichier original.

La plateforme doit pouvoir conserver les versions antérieures et permettre de retrouver l'état précédent.

### 22.4. Organisation des assets

Les assets doivent pouvoir être organisés de manière cohérente avec les composants qui les utilisent.

Un utilisateur doit pouvoir retrouver rapidement les éléments associés à une ressource ou à une bibliothèque.

### 22.5. Licences des assets

Les conditions de réutilisation des éléments graphiques doivent être prises en compte.

Un composant peut posséder une licence particulière alors que certains assets intégrés possèdent des conditions distinctes.

La plateforme doit permettre de conserver ces informations afin d'éviter de supposer qu'une licence unique couvre automatiquement tous les éléments.

---

## 23. Gestion des polices et ressources typographiques

La plateforme doit permettre de gérer les ressources typographiques utilisées dans les composants et les systèmes de design.

L'utilisateur doit pouvoir identifier les polices utilisées, leurs variantes, leurs poids et les conditions de leur utilisation lorsque ces informations sont disponibles.

Il doit pouvoir adapter les choix typographiques et comprendre quelles ressources utilisent les polices concernées.

Les changements doivent pouvoir être examinés au niveau des composants et des ensembles qui en dépendent.

---

## 24. Gestion des animations et transitions

Lorsque les ressources utilisent des animations ou des transitions, la plateforme doit permettre de les examiner et de les personnaliser.

Cela peut concerner :

- La durée.
- Le délai.
- La vitesse.
- Les transitions.
- Les effets.
- Les états animés.
- Les interactions déclenchant les animations.

L'utilisateur doit pouvoir comprendre les effets des modifications et vérifier leur résultat dans la prévisualisation lorsque cela est possible.

La personnalisation doit également permettre de prendre en compte les préférences de réduction des animations lorsque la ressource le permet.

---

# PARTIE XI — ORGANISATION DES RESSOURCES CRÉÉES

## 25. Identification des créations

### 25.1. Identité propre

Toute nouvelle ressource doit pouvoir disposer de sa propre identité.

Une création issue d'une personnalisation ne doit pas être confondue avec la ressource originale.

La plateforme doit permettre de distinguer la ressource initiale, sa déclinaison et les éventuelles ressources qui en sont dérivées.

### 25.2. Description

L'utilisateur doit pouvoir documenter l'objectif de la ressource, son fonctionnement, ses caractéristiques et ses conditions d'utilisation.

La description doit permettre à une autre personne de comprendre ce que la ressource apporte.

### 25.3. Classification

Les nouvelles créations doivent pouvoir être classées dans les catégories et espaces appropriés.

L'utilisateur doit pouvoir les intégrer à une bibliothèque existante ou constituer une nouvelle collection.

### 25.4. Attribution des responsabilités

La plateforme doit permettre d'identifier les personnes responsables de la création et de la maintenance d'une ressource.

Cette information est importante lorsque la ressource est partagée et évolue collectivement.

### 25.5. Informations de provenance

Lorsqu'une création réutilise des ressources existantes, la plateforme doit pouvoir conserver les informations relatives à ces origines.

Une création originale et une création dérivée ne doivent pas être confondues.

---

## 26. Documentation des ressources créées et personnalisées

### 26.1. Documentation fonctionnelle

L'utilisateur doit pouvoir expliquer le rôle de la ressource et les problèmes qu'elle permet de résoudre.

### 26.2. Documentation technique

La documentation doit pouvoir décrire les éléments nécessaires à la compréhension et à la maintenance de la ressource.

Cela peut notamment inclure sa structure, ses dépendances, ses configurations et ses contraintes.

### 26.3. Documentation des propriétés

Pour les composants, les propriétés exposées doivent pouvoir être documentées avec leur rôle, leur type, leurs valeurs possibles et leurs effets.

### 26.4. Documentation des variantes

Les différentes variantes doivent pouvoir être expliquées afin que les futurs utilisateurs comprennent dans quelles situations les utiliser.

### 26.5. Documentation des modifications

Lorsqu'une ressource est fortement personnalisée, il doit être possible de documenter les différences importantes par rapport à son état initial.

Cette documentation facilite la maintenance et les éventuelles mises à jour ultérieures.

---

# PARTIE XII — COLLABORATION PENDANT LA PERSONNALISATION

## 27. Travail à plusieurs sur une même ressource

La personnalisation et la création peuvent impliquer plusieurs personnes.

La plateforme doit donc prendre en compte les situations dans lesquelles plusieurs utilisateurs interviennent sur une même ressource ou sur des ressources liées.

### 27.1. Identification des travaux en cours

Les utilisateurs autorisés doivent pouvoir comprendre qu'une ressource fait actuellement l'objet de modifications.

Ils doivent pouvoir identifier les travaux en cours lorsque les règles de visibilité de l'espace le permettent.

### 27.2. Modifications parallèles

Plusieurs personnes peuvent travailler sur des parties différentes d'une même ressource.

La plateforme doit permettre de gérer ces modifications sans provoquer de perte de travail.

### 27.3. Conflits de modification

Lorsque plusieurs personnes modifient les mêmes éléments, la plateforme doit permettre de détecter les situations de conflit.

Elle doit faciliter leur comparaison et leur résolution.

### 27.4. Revue des changements

Les modifications importantes doivent pouvoir être examinées avant leur intégration dans une version de référence.

Les personnes autorisées doivent pouvoir consulter les changements, formuler des observations et demander des corrections.

### 27.5. Commentaires et annotations

Les utilisateurs doivent pouvoir associer des commentaires aux ressources et, lorsque cela est possible, aux fichiers ou parties précises du travail.

Ces échanges doivent permettre de discuter d'une modification sans perdre le contexte auquel elle se rapporte.

### 27.6. Responsabilités

La plateforme doit permettre d'identifier les personnes ayant réalisé, examiné et validé les changements importants.

Ces informations doivent pouvoir être retrouvées dans l'historique de la ressource.

---

# PARTIE XIII — CONTRÔLES ET VALIDATION DES CRÉATIONS

## 28. Vérification des ressources pendant le travail

### 28.1. Contrôle de cohérence

La plateforme doit permettre de vérifier que les modifications réalisées ne rendent pas la ressource incohérente.

Les contrôles peuvent porter sur les fichiers, les références, les propriétés, les dépendances et les configurations.

### 28.2. Détection des erreurs

Lorsque des erreurs peuvent être identifiées, elles doivent être signalées à l'utilisateur.

Les messages doivent indiquer les éléments concernés et fournir suffisamment de contexte pour permettre une correction.

### 28.3. Vérification de la compatibilité

La plateforme doit permettre d'examiner si la ressource reste compatible avec les environnements qu'elle annonce prendre en charge.

Lorsqu'une modification affecte cette compatibilité, l'information doit être visible.

### 28.4. Vérification du comportement

Les ressources interactives doivent pouvoir être testées dans les conditions adaptées.

L'utilisateur doit pouvoir examiner les comportements essentiels et identifier les anomalies.

### 28.5. Vérification visuelle

Pour les composants graphiques, la plateforme doit permettre de contrôler le rendu après modification.

Les différences visuelles doivent pouvoir être examinées et comparées.

---

## 29. Préparation d'une ressource à son intégration dans le patrimoine

Une ressource créée ou personnalisée doit pouvoir passer d'un état de travail à un état suffisamment structuré pour être intégrée au patrimoine.

Cette étape doit permettre de vérifier que les informations essentielles sont présentes.

Selon la nature de la ressource, cela peut concerner :

- Son identité.
- Sa description.
- Ses fichiers.
- Sa structure.
- Ses dépendances.
- Ses propriétés.
- Ses variantes.
- Sa documentation.
- Ses licences.
- Sa provenance.
- Ses environnements compatibles.
- Ses résultats de validation.

La plateforme doit pouvoir signaler les éléments manquants ou incohérents.

L'intégration au patrimoine ne doit pas être confondue avec la publication publique.

Une ressource peut être intégrée et conservée dans une bibliothèque privée sans être distribuée à l'extérieur.

---

# PARTIE XIV — SCÉNARIOS D'UTILISATION COMPLETS

## 30. Scénario 1 — Personnalisation complète d'un composant provenant de shadcn/ui

Un utilisateur découvre un composant dans une bibliothèque externe et souhaite l'adapter à son propre système de design.

Il récupère les fichiers sources, examine leur organisation et identifie les composants, styles et dépendances concernés.

Il conserve la version initiale, puis crée un état de travail personnalisé.

Il modifie les couleurs, la typographie, les propriétés exposées et certains comportements.

Il ajoute ensuite une variante adaptée à un autre contexte d'utilisation.

Il prévisualise les différentes versions, vérifie les comportements et enregistre son résultat.

La plateforme doit lui permettre de conserver la relation avec le composant d'origine tout en lui donnant une identité propre pour sa version personnalisée.

## 31. Scénario 2 — Transformation profonde d'un composant

Un utilisateur récupère un composant dont l'apparence lui convient, mais dont le fonctionnement ne correspond pas à son besoin.

Il souhaite modifier sa logique interne, ajouter des propriétés, introduire de nouveaux événements et changer certaines interactions.

Il accède aux fichiers sources et effectue les modifications nécessaires.

La plateforme doit lui permettre de travailler sur plusieurs fichiers, de comparer les changements, d'examiner les erreurs et de tester le comportement obtenu.

Le résultat doit pouvoir être conservé comme une nouvelle version de la ressource.

## 32. Scénario 3 — Création d'un composant à partir de zéro

Un utilisateur souhaite créer un composant qui n'existe pas dans son patrimoine.

Il définit son nom, sa description et son objectif.

Il construit sa structure, crée les fichiers nécessaires et définit les propriétés et comportements.

Il ajoute ses styles, ses états et les ressources complémentaires.

Il prévisualise le composant, effectue des essais, corrige les erreurs et documente son fonctionnement.

La ressource peut ensuite être intégrée à une bibliothèque.

## 33. Scénario 4 — Création d'une bibliothèque complète

Une équipe souhaite constituer sa propre bibliothèque de composants.

Elle commence par récupérer certains composants existants et crée ceux qui manquent.

Elle harmonise les styles, les propriétés, les comportements et les conventions.

Elle définit les composants communs, les variantes et les tokens partagés.

Elle organise l'ensemble en catégories et documente les composants.

La plateforme doit permettre de gérer chaque composant individuellement tout en conservant une vision cohérente de la bibliothèque.

## 34. Scénario 5 — Création d'un système de design

Une organisation souhaite disposer de son propre système de design.

Elle définit ses règles visuelles, ses couleurs, ses typographies, ses espacements et ses tokens.

Elle construit ensuite une bibliothèque de composants correspondant à ces règles.

Elle crée différentes variantes et vérifie la cohérence de l'ensemble.

La plateforme doit permettre de faire évoluer les règles communes et d'identifier les composants concernés par chaque changement.

## 35. Scénario 6 — Création de plusieurs variantes d'un composant

Un utilisateur souhaite proposer plusieurs versions d'un même composant.

Il conserve une version principale et crée différentes variantes adaptées à des contextes particuliers.

Chaque variante peut avoir des propriétés, des styles ou des comportements spécifiques.

La plateforme doit permettre de les regrouper, de les comparer et de suivre leur évolution.

## 36. Scénario 7 — Réutilisation de composants dans une nouvelle composition

Un utilisateur souhaite construire un composant complexe à partir de plusieurs composants déjà disponibles.

Il sélectionne les éléments nécessaires, les assemble et définit leurs relations.

Il adapte certaines propriétés et ajoute les comportements propres à l'ensemble.

La plateforme doit préserver l'identité des composants réutilisés et permettre de comprendre les dépendances de la nouvelle composition.

## 37. Scénario 8 — Modification visuelle et modification du code

Un concepteur modifie l'apparence d'un composant dans l'environnement visuel.

Un développeur intervient ensuite directement dans le code pour modifier son comportement.

La plateforme doit permettre de retrouver les deux catégories de modifications et de maintenir une représentation cohérente de la ressource.

Les éventuelles incompatibilités entre les changements doivent être signalées.

## 38. Scénario 9 — Deux pistes de personnalisation indépendantes

Une équipe souhaite tester deux orientations différentes pour un même composant.

Une première piste propose une refonte visuelle.

Une seconde piste modifie le comportement fonctionnel.

La plateforme doit permettre de conserver les deux travaux séparément, de les comparer et de décider si leurs changements peuvent être réunis ou s'ils doivent rester des variantes indépendantes.

## 39. Scénario 10 — Réutilisation d'une ressource sous licence particulière

Un utilisateur souhaite personnaliser une ressource dont la licence prévoit certaines conditions.

La plateforme doit lui permettre de consulter les informations disponibles sur cette licence et de comprendre les contraintes applicables à la modification et à la redistribution.

La personnalisation doit conserver les informations de provenance nécessaires à la traçabilité.

## 40. Scénario 11 — Modification d'un token partagé

Une équipe modifie une valeur de design utilisée par plusieurs composants.

La plateforme doit permettre d'identifier les composants concernés et de visualiser les conséquences de la modification.

L'équipe peut examiner les résultats, corriger les éventuelles incohérences et enregistrer une nouvelle version de son système de design.

## 41. Scénario 12 — Création d'une ressource à partir d'un modèle

Un utilisateur sélectionne un modèle existant pour créer une nouvelle ressource.

Il récupère la structure initiale, modifie les fichiers, ajoute ses propres éléments et adapte les configurations.

La plateforme doit conserver le modèle original et enregistrer la nouvelle ressource comme une création distincte.

---

# PARTIE XV — EXIGENCES FONDAMENTALES DE CETTE SESSION

## 42. Exigences fonctionnelles

La plateforme devra permettre :

1. De personnaliser intégralement les ressources dont la modification est autorisée.
2. De distinguer les ressources originales, les états de travail, les variantes et les versions personnalisées.
3. De préserver les codes sources originaux.
4. De consulter l'ensemble des fichiers d'une ressource.
5. D'explorer son arborescence.
6. De rechercher dans les fichiers et le code.
7. De naviguer entre les références et dépendances.
8. De modifier directement le code source.
9. De créer, déplacer, renommer, dupliquer et supprimer des fichiers et dossiers.
10. De suivre les modifications non enregistrées.
11. D'annuler et de rétablir les opérations d'édition.
12. De comparer différents états des fichiers.
13. De bénéficier d'une assistance à l'écriture et à la compréhension du code.
14. De contrôler les modifications proposées par les outils d'assistance.
15. De personnaliser les caractéristiques visuelles.
16. De modifier les thèmes et les tokens de design.
17. De gérer les états visuels et les interactions.
18. De modifier les propriétés exposées.
19. D'ajouter, modifier et supprimer des propriétés.
20. De transformer les comportements fonctionnels.
21. De créer des variantes visuelles, fonctionnelles et contextuelles.
22. De gérer plusieurs implémentations lorsque cela est nécessaire.
23. De créer des ressources à partir de zéro.
24. De créer des ressources à partir de modèles.
25. De créer des ressources dérivées d'éléments existants.
26. De construire des composants individuels.
27. De créer des ensembles composites.
28. De construire des bibliothèques.
29. De créer et faire évoluer des systèmes de design.
30. D'assembler et de réutiliser des ressources existantes.
31. De préserver les identités et les origines des éléments réutilisés.
32. De gérer les dépendances pendant la création.
33. De prévisualiser les ressources lorsque leur nature le permet.
34. D'expérimenter plusieurs pistes de travail.
35. De comparer et promouvoir les expérimentations retenues.
36. De gérer plusieurs états et versions de travail.
37. De gérer les modifications parallèles et les conflits.
38. De coordonner l'édition visuelle et l'édition du code.
39. De gérer les assets et les ressources associées.
40. De documenter les ressources créées et personnalisées.
41. De permettre la collaboration pendant la personnalisation.
42. De vérifier les ressources au cours de leur création.
43. De préparer leur intégration dans le patrimoine.
44. De conserver les informations de provenance et de licence.

---

# PARTIE XVI — RÉSULTAT ATTENDU

## 43. Un véritable environnement de personnalisation et de création

Le résultat attendu est un environnement de travail complet permettant de passer librement de la consultation d'une ressource à sa modification, puis à sa transformation ou à sa création.

L'utilisateur ne doit pas être limité à une interface de personnalisation proposant uniquement quelques options définies par le créateur initial.

Il doit pouvoir accéder au code source, modifier les fichiers, adapter la structure, changer les comportements, créer des propriétés, produire des variantes et construire des compositions plus complexes.

En parallèle, il doit disposer d'outils permettant de travailler visuellement sur les ressources qui s'y prêtent, de prévisualiser les résultats et de personnaliser les thèmes et systèmes de design.

Les deux approches doivent fonctionner ensemble.

Un utilisateur doit pouvoir commencer par une modification visuelle, poursuivre dans le code, revenir à l'aperçu, comparer les versions et enregistrer le résultat dans son patrimoine.

La plateforme doit également permettre de créer de nouvelles ressources sans dépendre d'un catalogue existant.

Elle doit accompagner la création d'un composant simple comme la constitution d'une bibliothèque complète ou d'un système de design.

## 44. Ce que cette session ne doit pas réduire

La personnalisation ne doit pas être réduite à un éditeur de propriétés.

L'édition du code ne doit pas être réduite à un simple visualiseur de fichiers.

La prévisualisation ne doit pas être réduite à une image statique indépendante de la ressource.

La création ne doit pas être réduite à la duplication de composants existants.

La gestion des variantes ne doit pas être réduite à la création de copies sans relation.

La composition ne doit pas être réduite à l'assemblage visuel de blocs sans gestion de leurs dépendances.

La gestion d'un système de design ne doit pas être réduite à un simple éditeur de couleurs.

La plateforme doit réunir toutes ces dimensions dans un environnement cohérent.

## 45. Principes directeurs

La conception ultérieure devra respecter les principes suivants :

- **Liberté de modification :** l'utilisateur doit pouvoir intervenir sur les sources et les caractéristiques des ressources dans les limites des droits applicables.
- **Préservation de l'original :** les transformations ne doivent pas détruire l'état initial.
- **Traçabilité :** les relations entre les ressources originales et leurs déclinaisons doivent rester compréhensibles.
- **Réversibilité :** les expérimentations et modifications doivent pouvoir être examinées, annulées ou restaurées lorsque cela est possible.
- **Cohérence :** les différentes formes d'édition doivent travailler sur une représentation cohérente de la ressource.
- **Réutilisabilité :** les ressources créées doivent pouvoir être réutilisées dans d'autres ensembles et projets.
- **Composition :** plusieurs ressources doivent pouvoir former des ensembles plus complexes sans perdre leurs identités.
- **Indépendance :** une création personnalisée doit pouvoir évoluer sans dépendre systématiquement de la ressource initiale.
- **Compatibilité :** les environnements et contraintes d'utilisation doivent être identifiables.
- **Documentation :** les ressources doivent pouvoir être comprises et maintenues par d'autres personnes.
- **Maîtrise :** les modifications doivent rester compréhensibles et contrôlables par l'utilisateur.
- **Modularité :** les ressources et leurs capacités doivent pouvoir être organisées et réutilisées indépendamment lorsque cela est pertinent.

## CONCLUSION DE LA SESSION 4

Cette session définit l'un des domaines les plus importants de la plateforme : sa capacité à transformer un patrimoine de ressources logicielles en un véritable environnement de création.

La plateforme doit permettre à ses utilisateurs de ne pas être de simples consommateurs de composants préfabriqués. Ils doivent pouvoir comprendre ces composants, récupérer leurs sources, les adapter à leurs besoins, les transformer profondément, créer leurs propres variantes et construire de nouvelles ressources.

Elle doit également permettre de passer d'une ressource isolée à des ensembles plus importants : composants composés, familles de composants, bibliothèques et systèmes de design.

L'édition directe des sources, la personnalisation visuelle, la modification des comportements, la gestion des variantes, la création de ressources et la prévisualisation doivent donc être considérées comme des capacités complémentaires d'un même environnement.

**L'ambition est de fournir un véritable atelier logiciel : un espace dans lequel toute ressource autorisée peut être comprise, explorée, modifiée, personnalisée, recomposée, créée et préparée pour devenir un élément durable du patrimoine logiciel de l'utilisateur ou de son organisation.**

Cette session ne définit volontairement aucune architecture technique, aucun framework, aucun éditeur particulier et aucun outil imposé. Ces choix devront être étudiés ultérieurement à partir des besoins exprimés.
