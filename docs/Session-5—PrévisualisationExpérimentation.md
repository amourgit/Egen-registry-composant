# **SESSION 5/8 — Prévisualisation, expérimentation, tests, validation et maîtrise de la qualité des ressources logicielles**

Cette session définit les exigences relatives à la capacité de vérifier, observer, expérimenter, tester et valider les ressources logicielles avant leur utilisation, leur publication ou leur distribution.

L’objectif est de faire en sorte que la plateforme ne soit pas simplement un endroit où l’on récupère du code source, où l’on modifie des composants et où l’on crée des variantes. Elle doit également permettre de comprendre précisément ce que produit chaque modification, de vérifier que les ressources fonctionnent correctement, d’identifier les régressions, de mesurer leur qualité et de décider en connaissance de cause si elles sont suffisamment fiables pour être utilisées dans d’autres projets.

Une ressource ne doit pas être considérée comme prête simplement parce que son code existe, qu’elle s’affiche dans un aperçu ou qu’elle ne présente aucune erreur immédiatement visible. Elle doit pouvoir être examinée selon plusieurs dimensions : son apparence, son comportement, sa compatibilité, sa robustesse, son accessibilité, ses dépendances, sa maintenabilité, sa cohérence avec les règles de conception et sa capacité à être réutilisée dans des contextes différents.

La plateforme doit donc proposer une véritable expérience d’expérimentation et de contrôle qualité, capable d'accompagner aussi bien une modification mineure d'un bouton qu'une transformation importante d'un ensemble de composants, d'une bibliothèque complète ou d'un système de design.

Il faut également distinguer plusieurs situations qui ne doivent jamais être confondues :

- Une ressource qui peut être prévisualisée.
- Une ressource qui peut être exécutée.
- Une ressource qui a été testée.
- Une ressource dont certains tests ont réussi.
- Une ressource qui a passé l'ensemble des contrôles obligatoires.
- Une ressource qui a été validée pour un usage précis.
- Une ressource qui est suffisamment stable pour être distribuée.
- Une ressource qui est compatible avec un environnement ou un projet particulier.

Ces distinctions sont essentielles. Une ressource peut être visuellement correcte sans être fonctionnelle, fonctionnelle sans être accessible, valide dans un environnement sans l'être dans un autre, ou parfaitement utilisable dans un projet tout en présentant des défauts qui la rendent inadaptée à une distribution générale.

Le système doit permettre de rendre ces différences visibles et compréhensibles.

## **1. Un environnement complet de prévisualisation des ressources**

La plateforme doit permettre de visualiser les ressources logicielles avant, pendant et après leur personnalisation.

La prévisualisation ne doit pas être considérée comme une simple image statique ou une capture du rendu final. Elle doit constituer un environnement permettant d'observer réellement une ressource, de manipuler ses éléments, de tester ses interactions et de comprendre son comportement dans les conditions prévues.

Pour un composant d'interface utilisateur, par exemple, il doit être possible de voir le rendu réel du composant, de modifier certaines propriétés, de déclencher ses interactions et d'observer immédiatement les conséquences des changements.

La plateforme doit pouvoir présenter plusieurs représentations complémentaires d'une même ressource :

- Son rendu visuel normal.
- Ses différentes variantes.
- Ses différents états.
- Ses comportements interactifs.
- Ses configurations possibles.
- Ses propriétés personnalisables.
- Ses dépendances visibles.
- Ses différentes versions.
- Ses déclinaisons selon les environnements ou les contextes d'utilisation.

La prévisualisation doit être suffisamment fidèle pour permettre de prendre des décisions sérieuses sur la qualité de la ressource.

Il ne faut pas qu'un aperçu simplifié donne une impression trompeuse de fiabilité. Lorsque le rendu est approximatif, incomplet ou simulé, cette situation doit être clairement identifiable.

### **1.1. Prévisualisation individuelle**

Chaque ressource doit pouvoir être prévisualisée indépendamment, sans nécessiter sa publication ou son intégration définitive dans un projet externe.

Un utilisateur doit pouvoir ouvrir un composant provenant d'une bibliothèque, consulter son rendu, manipuler ses propriétés et observer son comportement.

Pour un composant d'interface, cela peut notamment inclure :

- Boutons.
- Champs de saisie.
- Menus déroulants.
- Modales.
- Fenêtres contextuelles.
- Tableaux.
- Cartes.
- Barres de navigation.
- Menus latéraux.
- Onglets.
- Notifications.
- Formulaires.
- Composants de sélection.
- Indicateurs de progression.
- Éléments de pagination.
- Interfaces de recherche.
- Éléments de visualisation de données.

La plateforme doit également pouvoir prendre en charge des ressources qui ne sont pas nécessairement des composants visuels. Certaines ressources peuvent être des fonctions, des utilitaires, des services, des configurations, des modèles de données ou des éléments destinés à être consommés par d'autres logiciels.

Pour ces ressources, la prévisualisation doit être adaptée à leur nature. Il ne faut pas imposer une représentation visuelle à tous les types de ressources.

### **1.2. Prévisualisation des variantes**

Lorsqu'une ressource possède plusieurs variantes, il doit être possible de les consulter facilement et de les comparer.

Prenons l'exemple d'un bouton possédant les variantes suivantes :

- Primary.
- Secondary.
- Outline.
- Ghost.
- Destructive.
- Link.

L'utilisateur doit pouvoir afficher toutes ces variantes, observer leurs différences et vérifier leur cohérence.

Il doit également être possible de comparer des variantes qui ne sont pas nécessairement issues du même composant original.

Par exemple, deux boutons provenant de deux bibliothèques différentes peuvent remplir le même rôle, mais présenter des différences de comportement, de structure, d'accessibilité ou de personnalisation.

La plateforme doit faciliter ce type de comparaison sans obliger l'utilisateur à ouvrir plusieurs ressources séparément.

### **1.3. Prévisualisation des états**

Un composant ne doit pas être évalué uniquement dans son état initial.

Il faut pouvoir examiner les différents états possibles d'une ressource.

Pour un bouton, cela peut être :

- État normal.
- État survolé.
- État actif.
- État désactivé.
- État de chargement.
- État de succès.
- État d'erreur.
- État de focus.

Pour un champ de formulaire :

- Vide.
- En cours de saisie.
- Valide.
- Invalide.
- Désactivé.
- En lecture seule.
- En attente de validation.
- Avec message d'erreur.
- Avec message d'aide.

Pour une modale :

- Fermée.
- Ouverte.
- En cours de chargement.
- Avec contenu long.
- Avec confirmation.
- Avec erreur.
- En attente d'une action utilisateur.

L'objectif est de vérifier qu'un composant reste cohérent dans toutes les situations raisonnablement prévisibles, et pas uniquement lorsqu'il est affiché dans sa configuration la plus simple.

### **1.4. Prévisualisation des interactions**

La plateforme doit permettre d'interagir réellement avec les composants lorsqu'ils sont exécutables.

Il ne suffit pas de montrer un bouton qui semble cliquable. L'utilisateur doit pouvoir cliquer dessus et observer le comportement prévu, lorsque celui-ci est disponible.

Il doit notamment être possible de vérifier :

- Les actions déclenchées.
- Les changements d'état.
- Les interactions entre composants.
- Les ouvertures et fermetures.
- Les validations.
- Les sélections.
- Les transitions.
- Les événements.
- Les comportements conditionnels.
- Les réactions aux données fournies.
- Les réponses aux erreurs.

Pour les composants qui dépendent d'un service externe ou d'une API, la plateforme doit permettre de distinguer un comportement réellement connecté d'un comportement simulé.

Par exemple, un composant de recherche peut être testé avec des données fictives, mais il ne doit pas être présenté comme étant connecté à un véritable service de recherche.

Cette distinction doit être explicite.

## **2. Prévisualisation dans plusieurs environnements et dimensions d'affichage**

Une ressource ne sera pas nécessairement utilisée dans les mêmes conditions partout.

Un composant peut être parfaitement adapté à une application de bureau, mais présenter des problèmes sur mobile. Une interface peut être correcte dans un espace de contenu large, mais devenir inutilisable dans un panneau latéral ou une fenêtre de petite dimension.

La plateforme doit donc permettre de prévisualiser les ressources dans différents contextes d'affichage.

### **2.1. Dimensions d'écran**

Pour les ressources visuelles, il doit être possible de tester différentes dimensions :

- Très petits écrans.
- Smartphones.
- Grands smartphones.
- Tablettes.
- Ordinateurs portables.
- Écrans de bureau.
- Grands écrans.
- Conteneurs de dimensions personnalisées.

L'utilisateur doit pouvoir choisir une dimension prédéfinie ou définir librement la largeur et la hauteur de l'espace de prévisualisation.

Il doit également être possible d'observer les changements de comportement lorsque la largeur disponible évolue progressivement.

L'objectif n'est pas seulement de vérifier si un composant rentre dans un écran. Il faut vérifier qu'il reste utilisable, lisible, compréhensible et cohérent.

### **2.2. Prévisualisation responsive**

La plateforme doit permettre d'examiner le comportement responsive des ressources.

Elle doit notamment faciliter la détection des problèmes suivants :

- Débordement horizontal.
- Contenu coupé.
- Éléments qui se chevauchent.
- Texte illisible.
- Boutons trop petits.
- Espacements incohérents.
- Mauvais alignements.
- Colonnes qui ne s'adaptent pas.
- Images déformées.
- Menus qui dépassent de l'écran.
- Composants qui deviennent inutilisables sur mobile.
- Éléments qui disparaissent sans raison fonctionnelle.
- Transitions responsive incohérentes.

Il doit être possible de comparer plusieurs dimensions d'écran simultanément, afin de comprendre rapidement les différences entre les rendus.

### **2.3. Prévisualisation dans un conteneur réel**

La taille de l'écran ne représente pas toujours le véritable espace disponible pour un composant.

Un composant peut être intégré dans :

- Une page complète.
- Un panneau latéral.
- Une fenêtre modale.
- Une carte.
- Un tableau.
- Une zone de contenu limitée.
- Un espace de travail.
- Un tableau de bord.
- Un menu.
- Une zone de navigation.

Il faut donc pouvoir tester une ressource dans un conteneur dont les dimensions et les contraintes sont personnalisables.

Cela permet notamment de vérifier qu'un composant reste réutilisable dans des environnements différents, sans dépendre excessivement d'une disposition particulière.

### **2.4. Prévisualisation avec différents thèmes**

Les ressources doivent pouvoir être examinées dans plusieurs contextes visuels.

Il faut notamment pouvoir tester :

- Le thème clair.
- Le thème sombre.
- Les thèmes personnalisés.
- Les palettes de couleurs différentes.
- Les variations de contraste.
- Les configurations typographiques.
- Les différentes échelles d'espacement.
- Les changements de tokens de design.

Un composant qui fonctionne correctement dans un thème peut présenter des problèmes dans un autre.

La plateforme doit donc faciliter la vérification de la compatibilité entre une ressource et les systèmes de design auxquels elle est destinée à appartenir.

### **2.5. Prévisualisation selon les technologies et les environnements cibles**

Toutes les ressources ne seront pas destinées au même environnement.

Il faut pouvoir distinguer les ressources destinées notamment à :

- React.
- Next.js.
- Vue.
- Nuxt.
- Svelte.
- Angular.
- Applications web classiques.
- Applications mobiles.
- Environnements natifs.
- Applications hybrides.
- Bibliothèques partagées.
- Environnements de documentation.

La plateforme doit permettre d'identifier les environnements dans lesquels une ressource peut effectivement être exécutée et prévisualisée.

Une ressource React ne doit pas être considérée automatiquement comme compatible avec Vue ou Svelte simplement parce qu'elle remplit une fonction similaire.

Lorsqu'une représentation est obtenue par adaptation, simulation ou transformation, cela doit être clairement indiqué.

## **3. Environnement d'expérimentation et bac à sable**

La plateforme doit proposer un véritable espace d'expérimentation permettant de manipuler les ressources sans compromettre leurs versions de référence.

L'utilisateur doit pouvoir essayer librement plusieurs configurations, modifier des propriétés, tester des comportements et expérimenter des combinaisons sans que ses essais affectent automatiquement la ressource principale.

Il faut pouvoir travailler sans craindre de dégrader le patrimoine logiciel existant.

### **3.1. Expérimentation sans modification de la ressource de référence**

Lorsqu'un utilisateur ouvre une ressource pour l'expérimenter, les modifications effectuées dans cet espace ne doivent pas être considérées automatiquement comme des modifications définitives.

Il doit être possible de :

- Modifier temporairement le code.
- Changer les propriétés.
- Remplacer certaines données.
- Modifier les styles.
- Ajouter ou retirer des éléments.
- Tester différentes configurations.
- Essayer plusieurs comportements.
- Modifier les dépendances dans un environnement isolé.
- Revenir à l'état initial.
- Conserver une expérimentation.
- Transformer une expérimentation en véritable version de travail.

L'expérimentation doit être réversible.

L'utilisateur doit savoir à tout moment s'il travaille sur la ressource originale, sur une copie de travail ou sur une expérimentation temporaire.

### **3.2. Plusieurs expérimentations simultanées**

Il doit être possible de créer plusieurs expérimentations à partir d'une même ressource.

Prenons un composant de formulaire.

Un utilisateur peut vouloir tester :

- Une version compacte.
- Une version accessible aux personnes utilisant des technologies d'assistance.
- Une version adaptée aux mobiles.
- Une version utilisant un nouveau système de couleurs.
- Une version intégrant de nouvelles interactions.
- Une version destinée à un autre environnement technologique.

Ces expérimentations doivent pouvoir exister simultanément sans se remplacer mutuellement.

Il doit être possible de les nommer, de les décrire, de les comparer, de les conserver et de sélectionner celle qui mérite d'être poursuivie.

### **3.3. Expérimentation avec des données personnalisées**

Une ressource doit pouvoir être testée avec différentes données.

Pour un tableau, par exemple, il doit être possible de tester :

- Un tableau vide.
- Un tableau contenant quelques lignes.
- Un tableau contenant plusieurs centaines de lignes.
- Des données très longues.
- Des valeurs manquantes.
- Des données invalides.
- Des caractères spéciaux.
- Des contenus multilingues.
- Des valeurs extrêmes.

Pour un formulaire, il doit être possible de tester des saisies normales, des saisies invalides, des champs facultatifs, des champs obligatoires et des situations particulières.

L'objectif est d'éviter qu'une ressource soit considérée comme fiable uniquement parce qu'elle fonctionne avec un jeu de données simple.

### **3.4. Simulation des services externes**

Certaines ressources dépendent d'API, de services distants, de bases de données ou de systèmes tiers.

Il faut permettre de tester ces ressources sans nécessairement disposer d'un accès réel à tous ces services.

L'environnement d'expérimentation doit pouvoir prendre en charge des situations simulées telles que :

- Réponse normale d'une API.
- Réponse vide.
- Réponse incorrecte.
- Erreur serveur.
- Erreur réseau.
- Délai de réponse important.
- Interruption de connexion.
- Authentification refusée.
- Données partielles.
- Réponse inattendue.

Il faut pouvoir vérifier comment une ressource réagit lorsque ses dépendances ne se comportent pas comme prévu.

Une ressource de qualité doit pouvoir gérer les situations d'échec de manière compréhensible et maîtrisée.

### **3.5. Conservation des expériences**

Les expérimentations intéressantes ne doivent pas disparaître sans laisser de trace.

L'utilisateur doit pouvoir conserver une expérience, lui donner un nom, documenter son objectif et la reprendre ultérieurement.

Il doit également être possible de comparer plusieurs expériences et de récupérer les éléments pertinents de l'une d'elles pour les intégrer dans une version de travail.

Il faut distinguer clairement :

- Une expérience temporaire.
- Une expérience sauvegardée.
- Une expérience abandonnée.
- Une expérience transformée en version de travail.
- Une expérience validée.
- Une expérience utilisée comme base d'une nouvelle ressource.

## **4. Tests fonctionnels des ressources**

La plateforme doit permettre de vérifier que les ressources réalisent correctement les fonctions pour lesquelles elles ont été conçues.

Le contrôle fonctionnel ne doit pas être limité à la vérification de l'affichage.

Il doit permettre d'examiner les actions, les résultats, les interactions et les différents scénarios d'utilisation.

### **4.1. Vérification des fonctionnalités principales**

Chaque ressource doit pouvoir être évaluée selon les fonctions qu'elle est censée fournir.

Pour un composant de sélection, par exemple, il faut vérifier :

- La possibilité de sélectionner un élément.
- La possibilité de désélectionner un élément.
- La gestion de plusieurs sélections.
- La conservation de la valeur sélectionnée.
- Le comportement lorsque la liste est vide.
- Le comportement lorsque les données changent.
- La gestion des valeurs invalides.
- Le comportement lorsqu'il est désactivé.

Pour un composant de pagination :

- Passage à la page suivante.
- Retour à la page précédente.
- Accès à une page précise.
- Gestion de la première page.
- Gestion de la dernière page.
- Gestion d'une liste vide.
- Gestion d'un nombre important de pages.
- Actualisation lorsque le nombre d'éléments change.

Il doit être possible de définir les comportements attendus et de vérifier que la ressource les respecte.

### **4.2. Tests des interactions entre composants**

Les composants ne fonctionnent pas toujours individuellement.

Ils peuvent être associés pour constituer des interfaces plus complexes.

La plateforme doit permettre de tester les interactions entre plusieurs ressources.

Par exemple :

- Un champ de recherche qui filtre un tableau.
- Un bouton qui ouvre une modale.
- Un formulaire qui affiche des erreurs de validation.
- Un sélecteur qui modifie le contenu d'une autre zone.
- Un menu qui contrôle une navigation.
- Un composant de filtre qui modifie plusieurs résultats.
- Un tableau dont les actions déclenchent des fenêtres de confirmation.

Il faut vérifier que les composants communiquent correctement et que leurs comportements restent cohérents lorsqu'ils sont assemblés.

### **4.3. Tests des scénarios d'utilisation**

Il doit être possible de définir des scénarios complets représentant les actions d'un utilisateur.

Un scénario pourrait, par exemple, consister à :

1. Ouvrir un formulaire.
2. Saisir des informations.
3. Soumettre le formulaire.
4. Détecter une erreur.
5. Corriger les données.
6. Soumettre à nouveau.
7. Afficher un message de confirmation.

La plateforme doit pouvoir vérifier si les étapes attendues se déroulent correctement.

Cette capacité est particulièrement importante pour les ressources composites et les ensembles de composants qui doivent fonctionner ensemble.

### **4.4. Tests des événements et des comportements conditionnels**

Les ressources peuvent déclencher ou recevoir des événements.

Il faut pouvoir vérifier :

- Les événements produits.
- Les événements reçus.
- Les conditions de déclenchement.
- Les changements d'état.
- Les conséquences d'une action.
- Les comportements conditionnels.
- Les événements qui ne doivent pas être déclenchés.
- Les interactions qui doivent être bloquées dans certaines situations.

Il faut également identifier les cas où plusieurs événements sont susceptibles de se produire simultanément ou dans un ordre particulier.

### **4.5. Tests de non-régression fonctionnelle**

Une modification peut corriger un problème tout en introduisant un autre défaut.

La plateforme doit donc permettre de vérifier qu'une évolution ne détruit pas les fonctionnalités qui existaient auparavant.

Lorsqu'une ressource est modifiée, il doit être possible de comparer les comportements avant et après la modification.

Par exemple, lorsqu'un bouton reçoit une nouvelle variante visuelle, il faut vérifier que ses autres propriétés et ses interactions habituelles continuent de fonctionner.

La non-régression doit être considérée comme un élément fondamental de la qualité, particulièrement pour les ressources utilisées dans plusieurs projets.

## **5. Tests visuels et contrôle de cohérence graphique**

La qualité d'une ressource visuelle ne se limite pas à son fonctionnement.

Elle doit également respecter les attentes graphiques, les règles de présentation et les contraintes de conception définies.

La plateforme doit permettre de contrôler les rendus et de détecter les différences inattendues.

### **5.1. Comparaison visuelle entre versions**

Il doit être possible de comparer le rendu de deux versions d'une même ressource.

Cette comparaison doit faciliter l'identification des modifications concernant :

- Les dimensions.
- Les espacements.
- Les couleurs.
- Les typographies.
- Les bordures.
- Les ombres.
- Les alignements.
- Les positions.
- Les icônes.
- Les images.
- Les animations.
- Les comportements responsive.

L'utilisateur doit pouvoir identifier rapidement les différences introduites par une modification.

Il ne doit pas être obligé de se souvenir de l'ancien rendu pour comprendre ce qui a changé.

### **5.2. Détection des régressions visuelles**

La plateforme doit permettre de repérer les changements visuels non souhaités.

Par exemple :

- Un texte qui déborde.
- Un bouton dont la taille change anormalement.
- Une icône qui disparaît.
- Une couleur qui devient illisible.
- Un espacement qui se dégrade.
- Une modale qui sort de l'écran.
- Une disposition qui ne respecte plus les proportions attendues.
- Un élément qui se retrouve masqué.
- Une variante qui ne correspond plus aux autres variantes de la même famille.

Les différences visuelles doivent pouvoir être examinées selon leur importance.

Il faut également tenir compte du fait qu'une différence visuelle n'est pas nécessairement une erreur. Certaines modifications sont volontaires.

La plateforme doit donc permettre de distinguer les changements attendus des régressions potentielles.

### **5.3. Vérification de la cohérence d'un ensemble**

La qualité visuelle doit pouvoir être examinée au niveau d'une ressource individuelle, mais également au niveau d'un groupe de ressources.

Par exemple, dans une bibliothèque de composants, il faut pouvoir vérifier que :

- Les boutons utilisent des dimensions cohérentes.
- Les champs de formulaire respectent les mêmes règles.
- Les cartes suivent une logique commune.
- Les espacements restent harmonisés.
- Les couleurs correspondent au système de design.
- Les états interactifs sont cohérents.
- Les typographies sont utilisées de manière uniforme.
- Les variantes d'une même famille présentent une logique compréhensible.

Une bibliothèque peut contenir des composants individuellement corrects tout en présentant une forte incohérence lorsqu'ils sont utilisés ensemble.

La plateforme doit donc être capable d'évaluer la qualité collective d'un ensemble.

### **5.4. Contrôle des animations et transitions**

Les animations doivent également pouvoir être examinées.

Il faut notamment vérifier :

- La fluidité.
- La durée.
- La cohérence des transitions.
- Les interruptions.
- Les changements d'état.
- Les animations répétitives.
- Les comportements lorsque l'utilisateur interagit rapidement.
- Les préférences de réduction des animations.
- Les éventuels effets perturbants.

Une animation ne doit pas être considérée comme correcte uniquement parce qu'elle se déclenche.

Elle doit rester compréhensible, proportionnée et adaptée au contexte d'utilisation.

## **6. Accessibilité et qualité de l'expérience utilisateur**

La plateforme doit accorder une importance particulière à l'accessibilité.

Une ressource ne doit pas être considérée comme pleinement aboutie simplement parce qu'elle fonctionne avec une souris et qu'elle présente un rendu visuellement satisfaisant.

Elle doit également être examinée selon les besoins des personnes qui utilisent des technologies d'assistance ou des modes d'interaction différents.

### **6.1. Navigation au clavier**

Il doit être possible de vérifier que les composants interactifs peuvent être utilisés au clavier.

Les contrôles doivent notamment porter sur :

- L'accès aux éléments interactifs.
- L'ordre de navigation.
- La visibilité du focus.
- Les raccourcis éventuels.
- La sortie des fenêtres modales.
- La navigation dans les menus.
- La sélection des éléments.
- La cohérence des interactions clavier.

Un composant qui ne peut pas être utilisé correctement sans souris doit être signalé.

### **6.2. Structure sémantique**

La plateforme doit pouvoir examiner la structure sémantique des ressources.

Il faut notamment contrôler :

- L'utilisation appropriée des éléments sémantiques.
- La hiérarchie des titres.
- La structure des formulaires.
- L'identification des champs.
- Les libellés des boutons.
- Les rôles des éléments interactifs.
- Les relations entre les contenus.
- La cohérence des informations accessibles.

Une interface peut être visuellement correcte tout en étant difficile à comprendre pour un lecteur d'écran.

Cette dimension doit donc être examinée indépendamment du rendu graphique.

### **6.3. Contrastes et lisibilité**

Il faut pouvoir détecter les problèmes liés aux contrastes entre les textes et leurs arrière-plans.

La plateforme doit permettre d'examiner :

- Les textes principaux.
- Les textes secondaires.
- Les textes désactivés.
- Les messages d'erreur.
- Les indicateurs d'état.
- Les icônes.
- Les éléments interactifs.
- Les bordures importantes.
- Les éléments qui transmettent une information par la couleur.

Il faut également prendre en compte la lisibilité des contenus selon les tailles de texte et les différents thèmes.

### **6.4. Technologies d'assistance**

Lorsque cela est pertinent, la plateforme doit permettre de vérifier le comportement des ressources avec des technologies d'assistance.

Elle doit notamment faciliter l'identification des problèmes liés :

- Aux libellés absents.
- Aux descriptions insuffisantes.
- Aux changements d'état non annoncés.
- Aux éléments interactifs mal identifiés.
- Aux contenus dynamiques difficiles à comprendre.
- Aux fenêtres modales mal structurées.
- Aux zones de navigation insuffisamment explicites.

### **6.5. Référentiels et niveaux d'accessibilité**

Les contrôles doivent pouvoir s'appuyer sur des référentiels reconnus, notamment les recommandations WCAG.

Il doit être possible de distinguer les contrôles automatisables des vérifications qui nécessitent une appréciation humaine.

La plateforme ne doit pas afficher une conformité absolue lorsque seuls quelques contrôles automatisés ont été effectués.

Elle doit présenter clairement :

- Les critères examinés.
- Les critères validés.
- Les critères non validés.
- Les critères non applicables.
- Les critères qui nécessitent une vérification manuelle.
- Les limites de l'évaluation.

L'objectif est de fournir une évaluation honnête et exploitable, plutôt qu'une simple note d'accessibilité difficile à interpréter.

## **7. Vérification technique et intégrité du code source**

Au-delà de l'apparence et des comportements, la plateforme doit permettre de contrôler la qualité technique des ressources.

Le code source doit pouvoir être examiné afin d'identifier les erreurs, incohérences et problèmes susceptibles d'empêcher son utilisation.

### **7.1. Vérification syntaxique**

Il doit être possible de détecter les erreurs de syntaxe présentes dans les fichiers.

Cela concerne notamment :

- Les fichiers TypeScript.
- Les fichiers JavaScript.
- Les fichiers JSX et TSX.
- Les fichiers Vue.
- Les fichiers Svelte.
- Les fichiers CSS.
- Les fichiers JSON.
- Les fichiers de configuration.
- Les fichiers de définition de types.
- Les fichiers de documentation contenant des exemples exécutables.

La plateforme doit indiquer les fichiers concernés, les emplacements des erreurs et, lorsque cela est possible, les explications associées.

### **7.2. Vérification des types**

Pour les ressources utilisant un système de typage, il faut pouvoir contrôler la cohérence des types.

Les contrôles peuvent notamment porter sur :

- Les propriétés obligatoires.
- Les propriétés facultatives.
- Les types des paramètres.
- Les valeurs retournées.
- Les événements.
- Les interfaces.
- Les types génériques.
- Les incompatibilités.
- Les valeurs nulles ou indéfinies.
- Les types incorrectement déclarés.

L'objectif est de repérer les problèmes susceptibles d'apparaître lors de l'utilisation de la ressource dans un projet consommateur.

### **7.3. Analyse statique du code**

La plateforme doit pouvoir examiner le code sans nécessairement l'exécuter.

Cette analyse doit faciliter la détection de :

- Variables inutilisées.
- Imports inutilisés.
- Déclarations redondantes.
- Code inaccessible.
- Instructions suspectes.
- Mauvaises pratiques.
- Incohérences de style.
- Erreurs potentielles.
- Complexité excessive.
- Fonctions trop longues.
- Dépendances inutiles.
- Patterns problématiques.

Les résultats doivent être présentés avec suffisamment de contexte pour que l'utilisateur puisse comprendre le problème et décider de la correction à apporter.

### **7.4. Vérification des imports et des dépendances**

Il faut contrôler que les dépendances déclarées par une ressource sont cohérentes avec les fichiers et les fonctionnalités qu'elle utilise.

La plateforme doit notamment détecter :

- Les imports manquants.
- Les imports incorrects.
- Les dépendances non déclarées.
- Les dépendances inutilisées.
- Les versions incompatibles.
- Les références à des fichiers inexistants.
- Les dépendances circulaires.
- Les dépendances externes indisponibles.
- Les références vers des ressources supprimées ou déplacées.

Elle doit également permettre de comprendre si une ressource peut être utilisée de manière autonome ou si elle dépend d'un ensemble plus large de ressources.

### **7.5. Vérification de la compilation et de la construction**

Lorsqu'une ressource est destinée à être compilée ou intégrée dans un environnement de construction, il doit être possible de vérifier si elle peut effectivement être construite.

Les contrôles doivent pouvoir identifier :

- Les erreurs de compilation.
- Les erreurs de résolution des modules.
- Les incompatibilités de configuration.
- Les problèmes de génération.
- Les erreurs de construction.
- Les dépendances impossibles à résoudre.
- Les ressources manquantes.
- Les conflits de versions.
- Les problèmes liés aux environnements cibles.

Il faut pouvoir distinguer une ressource dont le code est syntaxiquement valide d'une ressource qui a réellement réussi une opération de construction.

### **7.6. Contrôle de la structure des ressources**

La plateforme doit également vérifier la cohérence de la structure des fichiers.

Par exemple :

- Présence des fichiers indispensables.
- Cohérence des chemins.
- Correspondance entre les déclarations et les fichiers.
- Présence des ressources référencées.
- Cohérence des noms.
- Organisation des fichiers.
- Présence des éléments documentaires attendus.
- Absence de références cassées.

Ces contrôles doivent pouvoir être adaptés au type de ressource et aux exigences de son environnement cible.

## **8. Tests de compatibilité et de portabilité**

La plateforme doit permettre de comprendre dans quelles conditions une ressource peut être utilisée.

Une ressource peut fonctionner dans un environnement donné et échouer dans un autre à cause de différences de versions, de dépendances, de configurations ou de fonctionnalités disponibles.

Il est donc nécessaire de proposer une évaluation de compatibilité.

### **8.1. Compatibilité avec les environnements technologiques**

Il doit être possible de déterminer les environnements dans lesquels une ressource peut être utilisée.

Les contrôles peuvent notamment porter sur :

- Les frameworks.
- Les bibliothèques.
- Les versions des langages.
- Les versions des dépendances.
- Les environnements d'exécution.
- Les outils de construction.
- Les systèmes de modules.
- Les exigences de configuration.

La plateforme doit distinguer les compatibilités vérifiées des compatibilités simplement déclarées.

### **8.2. Compatibilité entre versions**

Il faut pouvoir vérifier si une ressource reste utilisable avec différentes versions de ses dépendances.

Par exemple, un composant peut fonctionner avec une version donnée d'une bibliothèque, mais échouer après une mise à jour majeure.

La plateforme doit faciliter l'identification de ces situations.

Elle doit notamment permettre de comprendre :

- Les versions compatibles.
- Les versions non compatibles.
- Les versions non testées.
- Les changements susceptibles de provoquer une rupture.
- Les dépendances dont la mise à jour nécessite une adaptation.

### **8.3. Portabilité des ressources**

La plateforme doit également examiner la capacité d'une ressource à être réutilisée dans différents projets.

Une ressource trop dépendante d'un projet particulier peut être difficile à distribuer.

Il faut donc pouvoir identifier :

- Les références spécifiques à un projet.
- Les chemins locaux codés en dur.
- Les configurations implicites.
- Les dépendances non documentées.
- Les variables d'environnement nécessaires.
- Les services externes obligatoires.
- Les hypothèses non explicites.
- Les éléments qui empêchent une utilisation autonome.

L'objectif est de favoriser des ressources dont les conditions d'utilisation sont suffisamment claires pour permettre leur réutilisation.

### **8.4. Évaluation de la facilité d'intégration**

Une ressource peut être techniquement compatible tout en étant difficile à intégrer.

La plateforme doit donc permettre d'examiner la complexité de son intégration.

Il faut notamment prendre en compte :

- Le nombre de dépendances.
- La complexité de configuration.
- Les adaptations nécessaires.
- Les prérequis techniques.
- Les éventuelles modifications à apporter au projet consommateur.
- La présence d'exemples d'intégration.
- La clarté de la documentation.
- Les risques de conflits avec les ressources existantes.

Cette évaluation doit aider l'utilisateur à anticiper le travail nécessaire avant d'adopter une ressource.

## **9. Performance et maîtrise de la consommation des ressources**

La qualité d'une ressource doit également être évaluée selon son efficacité.

Un composant peut fonctionner correctement tout en étant trop lourd, trop lent ou excessivement consommateur de ressources.

La plateforme doit donc permettre de contrôler les aspects liés aux performances lorsque cela est pertinent.

### **9.1. Performance du rendu**

Pour les ressources visuelles, il doit être possible d'observer :

- Le temps nécessaire au rendu.
- Les ralentissements éventuels.
- Les mises à jour inutiles.
- Les changements d'état coûteux.
- Les problèmes de fluidité.
- Les comportements lors de manipulations répétées.

L'objectif est de détecter les composants qui dégradent l'expérience utilisateur dans des conditions normales ou intensives.

### **9.2. Poids des ressources**

Il doit être possible de mesurer le poids des ressources et de leurs dépendances.

Cela peut notamment concerner :

- Les fichiers sources.
- Les fichiers générés.
- Les assets.
- Les polices.
- Les images.
- Les bibliothèques externes.
- Les dépendances ajoutées.
- Les éléments inutilisés.

La plateforme doit permettre de comprendre ce qui contribue au poids global d'une ressource.

### **9.3. Consommation mémoire et comportement dans la durée**

Lorsque cela est pertinent, les ressources doivent pouvoir être examinées sur des périodes d'utilisation prolongées.

Il faut pouvoir identifier :

- Les consommations mémoire anormales.
- Les fuites de mémoire potentielles.
- Les événements qui ne sont pas correctement libérés.
- Les traitements répétés inutilement.
- Les accumulations de données.
- Les comportements qui se dégradent avec le temps.

### **9.4. Performance selon les volumes de données**

Certaines ressources peuvent fonctionner parfaitement avec quelques éléments et devenir très lentes lorsque le volume augmente.

Il doit donc être possible de tester différentes charges.

Par exemple :

- Un tableau avec 10 lignes.
- Un tableau avec 100 lignes.
- Un tableau avec 1 000 lignes.
- Un tableau avec plusieurs dizaines de milliers de lignes, lorsque le cas d'usage le justifie.

Il faut pouvoir observer l'évolution du comportement et identifier les limites de la ressource.

### **9.5. Présentation des résultats de performance**

Les mesures doivent être accompagnées de leur contexte.

Une mesure isolée n'a pas nécessairement de valeur si l'on ignore :

- L'environnement de test.
- Les conditions d'exécution.
- Le volume de données.
- La configuration utilisée.
- Les versions des dépendances.
- La méthode de mesure.

La plateforme doit donc conserver les informations nécessaires pour interpréter correctement les résultats.

Elle ne doit pas présenter une mesure obtenue dans un environnement particulier comme une garantie universelle de performance.

## **10. Sécurité et détection des risques techniques**

Les ressources provenant de sources externes, les codes personnalisés et les dépendances tierces peuvent introduire des risques.

La plateforme doit permettre d'identifier les problèmes de sécurité susceptibles d'affecter les ressources avant leur utilisation ou leur distribution.

### **10.1. Analyse du code source**

Il doit être possible de rechercher des éléments potentiellement dangereux dans le code.

Les contrôles peuvent notamment concerner :

- Les secrets exposés.
- Les clés d'API intégrées directement dans le code.
- Les mots de passe codés en dur.
- Les configurations sensibles.
- Les usages dangereux de certaines fonctions.
- Les opérations non sécurisées.
- Les accès excessifs.
- Les comportements suspects.
- Les dépendances présentant des vulnérabilités connues.

La plateforme doit permettre de signaler les problèmes avec leur emplacement et leur niveau de gravité.

### **10.2. Vérification des dépendances**

Les dépendances doivent pouvoir être examinées selon leur état de sécurité.

Il faut notamment identifier :

- Les dépendances présentant des vulnérabilités connues.
- Les versions obsolètes.
- Les versions abandonnées.
- Les dépendances dont la maintenance est incertaine.
- Les dépendances présentant des risques connus.
- Les dépendances transitives qui introduisent des vulnérabilités.

Il faut également pouvoir distinguer une vulnérabilité confirmée d'un risque potentiel ou d'une information qui nécessite une investigation.

### **10.3. Exécution dans un environnement maîtrisé**

Les ressources provenant de sources externes ne doivent pas être exécutées sans précaution.

La plateforme doit prévoir des conditions d'expérimentation adaptées aux risques présentés par les ressources.

Il faut notamment prendre en compte :

- Les scripts inconnus.
- Les opérations sur le système de fichiers.
- Les accès réseau.
- Les appels à des services externes.
- Les installations de dépendances.
- Les commandes exécutables.
- Les comportements nécessitant des permissions particulières.

L'utilisateur doit pouvoir comprendre les conditions dans lesquelles une ressource est exécutée et les limites imposées à cet environnement.

### **10.4. Qualification des résultats de sécurité**

Les résultats doivent être classés de manière compréhensible.

Il faut distinguer :

- Les vulnérabilités critiques.
- Les vulnérabilités importantes.
- Les vulnérabilités modérées.
- Les avertissements.
- Les bonnes pratiques non respectées.
- Les éléments nécessitant une vérification manuelle.

La plateforme ne doit pas laisser croire qu'une ressource est totalement sécurisée simplement parce qu'aucune vulnérabilité n'a été détectée par les contrôles effectués.

Une absence de détection n'est pas une preuve absolue d'absence de risque.

## **11. Système de campagnes de tests et de validation**

La plateforme doit permettre de regrouper plusieurs contrôles dans des campagnes cohérentes.

L'objectif est d'éviter de traiter chaque test comme une opération isolée sans relation avec les autres.

Une campagne doit pouvoir représenter une vérification complète effectuée sur une ressource, une variante, une collection ou une bibliothèque.

### **11.1. Campagnes adaptées aux types de ressources**

Toutes les ressources ne nécessitent pas les mêmes contrôles.

Un composant visuel, une fonction utilitaire, un ensemble d'icônes et une bibliothèque de composants n'ont pas les mêmes exigences.

Il doit donc être possible de définir des campagnes adaptées à chaque catégorie de ressources.

Une campagne destinée à un composant d'interface pourrait inclure :

- Vérification syntaxique.
- Vérification des types.
- Prévisualisation.
- Tests fonctionnels.
- Tests responsive.
- Contrôle d'accessibilité.
- Analyse des dépendances.
- Analyse de performance.
- Vérification de la documentation.

Une campagne destinée à une collection d'icônes pourrait plutôt inclure :

- Vérification des fichiers.
- Vérification des formats.
- Contrôle des dimensions.
- Contrôle des noms.
- Détection des doublons.
- Vérification des licences.
- Prévisualisation.
- Contrôle de la cohérence graphique.

La plateforme doit donc permettre d'adapter les exigences de validation à la nature réelle des ressources.

### **11.2. Campagnes personnalisables**

L'utilisateur doit pouvoir définir ses propres campagnes de validation.

Il doit pouvoir choisir :

- Les contrôles à effectuer.
- Les contrôles obligatoires.
- Les contrôles facultatifs.
- Les conditions de réussite.
- Les niveaux de gravité acceptables.
- Les environnements de test.
- Les configurations à examiner.
- Les ressources concernées.

Il doit également être possible de conserver ces campagnes afin de les réutiliser sur plusieurs ressources.

### **11.3. Campagnes récurrentes**

Certaines ressources doivent être régulièrement contrôlées.

Une ressource peut être correcte aujourd'hui, mais devenir problématique après une mise à jour de ses dépendances ou une modification de son environnement.

La plateforme doit donc permettre de relancer des campagnes :

- Après une modification du code.
- Après une mise à jour des dépendances.
- Après une nouvelle version.
- Avant une publication.
- Avant une distribution.
- Après une modification importante du système de design.
- À intervalles réguliers, selon les besoins.

### **11.4. Historique des campagnes**

Chaque campagne doit produire un résultat conservable.

L'utilisateur doit pouvoir consulter :

- La date du contrôle.
- La ressource concernée.
- La version examinée.
- La configuration utilisée.
- Les contrôles effectués.
- Les résultats.
- Les erreurs détectées.
- Les avertissements.
- Les éléments non vérifiés.
- Les corrections apportées.
- Le statut final.

Cet historique doit permettre de suivre l'évolution de la qualité d'une ressource dans le temps.

### **11.5. Comparaison entre campagnes**

Il doit être possible de comparer deux campagnes effectuées sur une même ressource.

Par exemple, après une correction, l'utilisateur doit pouvoir identifier :

- Les problèmes qui ont disparu.
- Les problèmes qui persistent.
- Les nouveaux problèmes apparus.
- Les contrôles qui ont été améliorés.
- Les résultats qui se sont dégradés.
- Les éléments qui restent à examiner.

L'objectif est de pouvoir démontrer qu'une modification a effectivement amélioré la qualité de la ressource.

## **12. Système de résultats, rapports et indicateurs de qualité**

Les contrôles doivent produire des résultats suffisamment détaillés pour permettre une compréhension réelle de l'état d'une ressource.

La plateforme ne doit pas se limiter à afficher une simple mention « Succès » ou « Échec ».

Elle doit présenter une synthèse compréhensible, mais également permettre d'accéder aux détails nécessaires à l'analyse.

### **12.1. Statut global de qualité**

Chaque ressource doit pouvoir disposer d'un état de qualité synthétique.

Cet état doit tenir compte des contrôles effectués et des exigences applicables.

Les états pourraient notamment distinguer :

- Non évaluée.
- Évaluation en cours.
- Évaluation partielle.
- Conforme aux contrôles effectués.
- Conforme avec réserves.
- Non conforme.
- Bloquée par des erreurs.
- Validation expirée.
- Validation à renouveler.

Ces états doivent être clairement distingués du cycle de vie général de la ressource.

Une ressource publiée peut, par exemple, recevoir ultérieurement une alerte de qualité à la suite d'une vulnérabilité découverte dans l'une de ses dépendances.

### **12.2. Résultats détaillés**

Pour chaque problème détecté, il doit être possible de consulter :

- Sa description.
- Son emplacement.
- Sa catégorie.
- Son niveau de gravité.
- Son origine.
- Son impact potentiel.
- Les conditions dans lesquelles il apparaît.
- Les conséquences possibles.
- Les recommandations de correction.
- Son statut de traitement.

L'utilisateur doit pouvoir passer du résultat à la ressource concernée.

Lorsqu'un problème est lié à un fichier source, il doit être possible d'accéder directement au fichier et à la zone concernée.

### **12.3. Indicateurs par dimension**

Il doit être possible de consulter les résultats selon plusieurs dimensions :

- Qualité du code.
- Qualité fonctionnelle.
- Qualité visuelle.
- Accessibilité.
- Compatibilité.
- Performance.
- Sécurité.
- Documentation.
- Maintenabilité.
- Portabilité.
- Intégrité des dépendances.

Il faut éviter de fusionner toutes ces dimensions dans une note unique qui masquerait les faiblesses d'une ressource.

Une ressource peut obtenir de bons résultats sur le plan visuel et présenter de graves problèmes de sécurité.

Ces informations doivent rester distinctes.

### **12.4. Rapports exportables**

Les résultats doivent pouvoir être conservés et exportés.

Les rapports peuvent être utiles pour :

- Les équipes de développement.
- Les responsables de bibliothèques.
- Les équipes de validation.
- Les responsables de publication.
- Les personnes qui consomment les ressources.
- Les équipes chargées de la maintenance.

Il doit être possible de produire des rapports détaillés et des synthèses adaptées à différents publics.

Un rapport destiné à un développeur doit présenter les informations techniques nécessaires à la correction.

Un rapport destiné à un responsable de validation doit plutôt mettre en évidence les risques, les exigences non satisfaites et les décisions à prendre.

### **12.5. Traçabilité des validations**

Une validation doit toujours être associée à une version précise de la ressource et aux conditions dans lesquelles elle a été obtenue.

Il faut pouvoir retrouver :

- La version validée.
- Les contrôles effectués.
- Les résultats.
- La date.
- L'auteur ou le responsable de la validation.
- Les éventuelles réserves.
- Le périmètre de la validation.

Il ne faut pas qu'une ressource modifiée conserve automatiquement le statut de validation d'une version antérieure.

Lorsqu'une modification importante intervient, la plateforme doit permettre d'identifier les validations qui doivent être renouvelées.

## **13. Gestion des erreurs, anomalies et corrections**

La détection d'un problème n'est utile que si elle permet de comprendre ce qui doit être corrigé et de suivre la résolution.

La plateforme doit donc proposer une gestion structurée des anomalies.

### **13.1. Centralisation des anomalies**

Les anomalies détectées doivent pouvoir être regroupées et consultées dans un espace dédié.

Il faut pouvoir distinguer :

- Les erreurs bloquantes.
- Les erreurs fonctionnelles.
- Les régressions visuelles.
- Les problèmes d'accessibilité.
- Les incompatibilités.
- Les problèmes de dépendances.
- Les vulnérabilités.
- Les problèmes de performance.
- Les défauts documentaires.
- Les avertissements.

L'utilisateur doit pouvoir filtrer les anomalies par ressource, version, catégorie, gravité et état de traitement.

### **13.2. Qualification et priorisation**

Toutes les anomalies ne présentent pas le même niveau d'urgence.

La plateforme doit permettre de qualifier leur importance en tenant compte de leur impact réel.

Une erreur qui empêche la construction d'une ressource ne doit pas être traitée de la même manière qu'un défaut esthétique mineur.

Il faut pouvoir identifier les problèmes qui :

- Empêchent toute utilisation.
- Empêchent une distribution.
- Affectent certaines fonctionnalités.
- Affectent certains environnements.
- Dégradent l'expérience utilisateur.
- Présentent un risque de sécurité.
- Réduisent la qualité sans bloquer l'utilisation.

### **13.3. Suivi des corrections**

Une anomalie doit pouvoir suivre un cycle de traitement.

Par exemple :

- Détectée.
- À examiner.
- Confirmée.
- En cours de correction.
- Corrigée.
- En attente de vérification.
- Résolue.
- Non corrigée volontairement.
- Classée sans suite.

Il doit être possible de documenter la décision prise et les raisons qui la justifient.

### **13.4. Vérification après correction**

Une correction ne doit pas être considérée comme définitive uniquement parce que le code a été modifié.

Il faut pouvoir relancer les contrôles concernés et vérifier que le problème a effectivement disparu.

Il faut également examiner si la correction a introduit d'autres problèmes.

La plateforme doit donc conserver le lien entre :

- L'anomalie initiale.
- La modification effectuée.
- La version corrigée.
- La campagne de vérification.
- Le résultat final.

### **13.5. Gestion des anomalies acceptées**

Certaines anomalies peuvent être connues et acceptées temporairement.

Par exemple, une ressource peut présenter un défaut mineur qui ne justifie pas de bloquer son utilisation dans un contexte expérimental.

La plateforme doit permettre de documenter ces exceptions.

Toutefois, une anomalie acceptée ne doit pas disparaître de l'historique.

Il faut conserver :

- La raison de l'acceptation.
- Le responsable de la décision.
- Le périmètre concerné.
- La durée éventuelle de l'acceptation.
- Les risques connus.
- Les conditions dans lesquelles l'exception peut être maintenue.

## **14. Qualité des dépendances et fiabilité de l'écosystème logiciel**

Une ressource ne peut pas être évaluée indépendamment de tout ce dont elle dépend.

Un composant peut être correctement développé et néanmoins devenir inutilisable à cause d'une dépendance externe défaillante, abandonnée ou incompatible.

La plateforme doit donc permettre d'évaluer la qualité de l'environnement logiciel associé à chaque ressource.

### **14.1. Évaluation des dépendances directes et transitives**

Il doit être possible de connaître les dépendances directes d'une ressource, mais également les dépendances introduites indirectement.

L'utilisateur doit pouvoir comprendre :

- Quelles dépendances sont nécessaires.
- Pourquoi elles sont utilisées.
- Quelles versions sont concernées.
- Quelles autres dépendances elles introduisent.
- Quels problèmes sont connus.
- Quelles dépendances sont facultatives.
- Quelles dépendances peuvent être remplacées.

### **14.2. Détection des dépendances fragiles**

Il faut pouvoir signaler les dépendances qui présentent des signes de fragilité :

- Absence de maintenance connue.
- Versions très anciennes.
- Dépendances abandonnées.
- Compatibilité incertaine.
- Vulnérabilités connues.
- Documentation insuffisante.
- Difficultés d'installation.
- Dépendances fortement liées à un environnement particulier.

La plateforme doit éviter de présenter automatiquement ces dépendances comme dangereuses. Elle doit plutôt fournir des éléments permettant d'évaluer leur niveau de risque.

### **14.3. Évaluation de l'impact des dépendances**

Il doit être possible de comprendre ce qui se passe lorsqu'une dépendance évolue.

Par exemple, une mise à jour d'une bibliothèque peut affecter plusieurs composants qui l'utilisent.

La plateforme doit permettre d'identifier les ressources concernées et de comprendre l'étendue des vérifications nécessaires.

Cette capacité doit s'étendre aux bibliothèques et collections complètes, pas uniquement aux composants individuels.

### **14.4. Contrôle des ressources composites**

Une ressource composite peut être constituée de plusieurs composants, utilitaires, styles et dépendances.

La plateforme doit pouvoir évaluer la qualité de l'ensemble.

Elle doit notamment identifier :

- Les éléments non vérifiés.
- Les dépendances incompatibles.
- Les composants présentant des anomalies.
- Les ressources dupliquées.
- Les références cassées.
- Les conflits de versions.
- Les incohérences entre les différents éléments.

Un ensemble ne doit pas être considéré comme fiable simplement parce que chacun de ses éléments semble correct individuellement.

Il faut également examiner leur compatibilité et leur comportement lorsqu'ils sont réunis.

## **15. Comparaison et évaluation de plusieurs ressources candidates**

La plateforme doit permettre de comparer plusieurs ressources qui répondent à un besoin similaire.

Cette fonctionnalité est importante lorsqu'un utilisateur hésite entre plusieurs composants provenant de différentes bibliothèques ou sources.

Prenons l'exemple de plusieurs composants de tableau.

Ils peuvent tous afficher des données, mais présenter des différences importantes concernant :

- Les fonctionnalités.
- Les possibilités de personnalisation.
- Les performances.
- L'accessibilité.
- Les dépendances.
- La complexité du code.
- La documentation.
- La compatibilité.
- La facilité d'intégration.
- La stabilité.

La plateforme doit faciliter cette comparaison.

### **15.1. Comparaison fonctionnelle**

Il doit être possible de comparer les fonctionnalités disponibles dans chaque ressource.

Par exemple, un composant peut proposer le tri, la pagination, le filtrage et la sélection multiple, tandis qu'un autre propose uniquement l'affichage des données.

Ces différences doivent être clairement visibles.

### **15.2. Comparaison technique**

Il doit être possible de comparer les caractéristiques techniques :

- Technologies utilisées.
- Dépendances.
- Poids.
- Complexité.
- Versions compatibles.
- Organisation du code.
- Conditions d'utilisation.
- Résultats des contrôles.
- Historique de maintenance disponible.

### **15.3. Comparaison visuelle et ergonomique**

Les ressources candidates doivent pouvoir être examinées dans des conditions comparables.

Elles doivent être présentées avec des données, des dimensions et des scénarios similaires lorsque cela est possible.

L'objectif est d'éviter les comparaisons trompeuses dues à des conditions de prévisualisation différentes.

### **15.4. Comparaison selon un contexte d'utilisation**

La meilleure ressource n'est pas nécessairement celle qui possède le plus de fonctionnalités.

Une ressource peut être excellente pour un projet complexe et inadaptée à un projet qui exige une solution légère.

Il faut donc pouvoir examiner les candidates selon des exigences précises.

Par exemple :

- Ressource adaptée à un projet léger.
- Ressource adaptée à une application complexe.
- Ressource adaptée à un système de design institutionnel.
- Ressource adaptée à une application mobile.
- Ressource adaptée à une bibliothèque réutilisable.
- Ressource adaptée à un environnement technologique particulier.

La plateforme doit aider à comprendre les avantages, les limites et les compromis de chaque choix, sans imposer artificiellement un classement universel.

## **16. Validation à plusieurs niveaux**

La validation doit pouvoir être réalisée à différents niveaux selon l'importance de la ressource et son usage prévu.

Une ressource expérimentale n'a pas nécessairement les mêmes exigences qu'une bibliothèque destinée à être distribuée à de nombreux projets.

La plateforme doit donc permettre de distinguer plusieurs niveaux de validation.

### **16.1. Validation individuelle**

Une ressource peut être validée indépendamment.

Par exemple, un composant peut être contrôlé, testé et accepté avant d'être intégré dans une bibliothèque.

### **16.2. Validation d'une variante**

Une variante doit pouvoir être validée indépendamment de sa ressource d'origine.

Une modification importante peut introduire des problèmes spécifiques qui ne concernent pas les autres variantes.

Il faut donc pouvoir identifier précisément la variante examinée.

### **16.3. Validation d'une collection**

Une collection doit pouvoir être évaluée comme un ensemble.

Il faut notamment examiner :

- La cohérence entre les ressources.
- La complétude.
- Les dépendances internes.
- Les doublons.
- Les conflits.
- La qualité documentaire.
- La compatibilité générale.

### **16.4. Validation d'une bibliothèque**

Une bibliothèque complète doit pouvoir faire l'objet d'une évaluation globale.

Cette validation peut tenir compte de la qualité des composants, mais aussi de la cohérence de l'ensemble, de sa documentation, de ses dépendances et de sa capacité à être utilisée dans plusieurs projets.

### **16.5. Validation selon une destination**

Une ressource peut être validée pour un usage précis sans être considérée comme universellement compatible.

Par exemple :

- Validée pour React.
- Validée pour une version précise de Next.js.
- Validée pour un thème particulier.
- Validée pour un environnement de production déterminé.
- Validée pour une application interne.
- Validée pour une distribution publique.

La plateforme doit permettre d'indiquer clairement le périmètre de chaque validation.

### **16.6. Validation humaine et technique**

Il faut distinguer les contrôles effectués automatiquement des validations qui nécessitent une décision humaine.

Certains critères peuvent être vérifiés automatiquement, tandis que d'autres demandent une appréciation du rendu, de l'expérience utilisateur, de la documentation ou de la pertinence fonctionnelle.

La plateforme doit permettre de combiner ces deux dimensions.

Une validation humaine ne doit pas effacer les résultats techniques, et des résultats techniques positifs ne doivent pas remplacer les décisions humaines lorsqu'elles sont nécessaires.

## **17. Gestion des exigences de qualité selon les usages**

Toutes les ressources ne doivent pas être soumises aux mêmes exigences.

La plateforme doit permettre de définir des niveaux d'exigence adaptés à leur destination.

Une ressource destinée à une expérimentation personnelle peut tolérer certains avertissements.

Une ressource destinée à être intégrée dans plusieurs applications institutionnelles doit répondre à des exigences plus strictes.

### **17.1. Profils de qualité**

Il doit être possible de définir plusieurs profils d'exigence.

À titre d'exemple :

**Profil expérimental**

- Vérifications fondamentales.
- Prévisualisation.
- Détection des erreurs bloquantes.
- Contrôle minimal des dépendances.
- Absence d'exigence de publication.

**Profil de développement**

- Vérification syntaxique.
- Vérification des types.
- Tests fonctionnels.
- Analyse des dépendances.
- Contrôle de compatibilité.
- Vérification des régressions principales.

**Profil de distribution**

- Contrôles techniques renforcés.
- Documentation suffisante.
- Vérification des licences.
- Contrôle de sécurité.
- Contrôle d'accessibilité selon le périmètre.
- Vérification de la portabilité.
- Validation de la version distribuée.

**Profil de production**

- Contrôles obligatoires adaptés à la destination.
- Absence de défauts bloquants.
- Compatibilité vérifiée.
- Dépendances maîtrisées.
- Tests fonctionnels suffisants.
- Validation documentée.
- Traçabilité des résultats.

Ces profils doivent rester personnalisables.

Il ne faut pas enfermer la plateforme dans une liste rigide de niveaux de qualité.

### **17.2. Critères bloquants et non bloquants**

Il doit être possible de définir quels problèmes empêchent une validation.

Par exemple :

- Une erreur de compilation peut être bloquante.
- Une vulnérabilité critique peut être bloquante.
- Une documentation incomplète peut être bloquante pour une distribution publique.
- Un défaut visuel mineur peut être non bloquant dans un environnement expérimental.

Les règles doivent être explicites.

L'utilisateur doit comprendre pourquoi une ressource est bloquée et ce qu'il doit faire pour satisfaire les exigences.

### **17.3. Validation conditionnelle**

Il doit être possible de valider une ressource avec des réserves.

Cette situation peut être nécessaire lorsque certains contrôles ne sont pas applicables, lorsque certaines dépendances ne peuvent pas être testées ou lorsqu'une limitation connue est acceptée.

La validation conditionnelle doit toujours être accompagnée d'une explication.

Elle ne doit pas être confondue avec une validation complète.

## **18. Documentation des tests et reproductibilité des résultats**

Un résultat de test n'a de valeur durable que si l'on peut comprendre comment il a été obtenu.

La plateforme doit donc permettre de conserver les informations nécessaires à la reproduction des contrôles.

Pour chaque campagne importante, il doit être possible de retrouver :

- La version exacte de la ressource.
- Les versions des dépendances.
- La configuration de test.
- Les données utilisées.
- Les environnements concernés.
- Les contrôles effectués.
- Les éventuelles simulations.
- Les résultats obtenus.
- Les anomalies détectées.

Il doit également être possible de documenter les tests manuels.

Un utilisateur doit pouvoir décrire une procédure, préciser les actions effectuées et enregistrer le résultat de son observation.

Cette documentation est particulièrement importante pour les ressources complexes, les comportements difficiles à automatiser et les validations nécessitant une appréciation humaine.

La plateforme doit permettre de reproduire autant que possible les conditions d'une validation antérieure.

Elle doit également signaler lorsque les conditions ont changé au point de rendre une comparaison directe peu fiable.

## **19. Contrôle qualité des ressources provenant de sources externes**

La plateforme doit être capable d'évaluer les ressources récupérées depuis des sources externes avant qu'elles soient considérées comme exploitables.

Une ressource provenant d'une source réputée ne doit pas être automatiquement considérée comme adaptée à tous les usages.

Elle peut être ancienne, incomplète, incompatible avec l'environnement cible ou dépendante de configurations particulières.

### **19.1. Évaluation à l'acquisition**

Lorsqu'une ressource est récupérée, il doit être possible de déclencher une première évaluation.

Cette évaluation doit notamment examiner :

- La complétude des fichiers.
- La cohérence de la structure.
- Les informations de provenance.
- Les licences déclarées.
- Les dépendances.
- Les erreurs techniques.
- Les éventuelles vulnérabilités.
- La documentation.
- Les possibilités de prévisualisation.
- La compatibilité déclarée.

### **19.2. Comparaison entre l'état d'origine et l'état importé**

Il faut pouvoir vérifier que la ressource importée correspond bien à ce qui était annoncé par sa source.

Lorsque des transformations ont été effectuées lors de l'acquisition, elles doivent être identifiables.

La plateforme doit permettre de distinguer les problèmes qui existaient déjà dans la ressource originale de ceux qui ont été introduits lors de l'importation ou de l'adaptation.

### **19.3. Évaluation après personnalisation**

Une ressource qui était correcte à son acquisition peut devenir défectueuse après modification.

Il faut donc pouvoir relancer les contrôles après chaque transformation significative.

La plateforme doit éviter de réutiliser sans discernement les résultats obtenus sur la version originale pour qualifier une version personnalisée.

### **19.4. Évaluation avant redistribution**

Avant de distribuer une ressource, il doit être possible d'effectuer une évaluation adaptée à son mode de distribution.

Il faut notamment vérifier :

- La cohérence des fichiers.
- La présence des dépendances nécessaires.
- La qualité du code.
- La documentation.
- La compatibilité annoncée.
- Les licences.
- Les éventuels éléments sensibles.
- La stabilité.
- La qualité de la version finale.

L'objectif est d'éviter de distribuer une ressource qui fonctionne uniquement dans l'environnement de travail de son créateur.

## **20. Qualité et validation des systèmes de design complets**

La plateforme ne doit pas limiter l'évaluation de la qualité aux composants individuels.

Elle doit également pouvoir examiner les systèmes de design complets.

Un système de design peut comporter des tokens, des couleurs, des typographies, des règles d'espacement, des composants, des variantes, des modèles d'interface et des règles d'utilisation.

La cohérence doit pouvoir être évaluée à l'échelle de cet ensemble.

### **20.1. Vérification des tokens**

Il doit être possible de contrôler :

- Les tokens définis.
- Les valeurs utilisées.
- Les références entre tokens.
- Les doublons.
- Les valeurs non utilisées.
- Les incohérences.
- Les références manquantes.
- Les variantes de thème.

Il faut notamment pouvoir identifier les composants qui ne respectent pas les tokens attendus.

### **20.2. Cohérence des composants**

La plateforme doit pouvoir vérifier si les composants respectent les conventions du système de design.

Par exemple :

- Les boutons utilisent-ils les bonnes couleurs ?
- Les champs respectent-ils les règles de dimensions ?
- Les cartes utilisent-elles les espacements prévus ?
- Les états d'erreur sont-ils cohérents ?
- Les variantes sont-elles correctement définies ?
- Les composants respectent-ils les conventions typographiques ?

### **20.3. Cohérence des thèmes**

Il doit être possible de vérifier que les différents thèmes d'un système de design sont suffisamment complets et cohérents.

Un thème sombre ne doit pas simplement inverser les couleurs du thème clair si cette transformation produit des problèmes de contraste ou de lisibilité.

La plateforme doit permettre d'examiner les résultats et de détecter les valeurs manquantes ou incohérentes.

### **20.4. Évaluation globale du système**

Il doit être possible de consulter une évaluation globale du système de design, tout en conservant la possibilité d'identifier les ressources responsables des problèmes.

L'utilisateur doit pouvoir passer d'un indicateur général à un composant, un token ou une règle précise.

## **21. Suivi de la qualité dans le temps**

La qualité d'une ressource n'est pas un état définitivement acquis.

Elle peut évoluer en fonction des modifications, des mises à jour des dépendances, des changements technologiques et des exigences des projets consommateurs.

La plateforme doit donc permettre un suivi dans le temps.

### **21.1. Historique de qualité**

Il doit être possible de consulter l'évolution des résultats d'une ressource.

Par exemple :

- Qualité lors de l'acquisition.
- Qualité après personnalisation.
- Qualité avant publication.
- Qualité après une mise à jour.
- Qualité après une correction.
- Qualité après une modification des dépendances.

L'utilisateur doit pouvoir comprendre si la ressource s'améliore, se dégrade ou reste stable.

### **21.2. Alertes de qualité**

La plateforme doit pouvoir signaler les situations qui nécessitent une nouvelle vérification.

Par exemple :

- Une dépendance devient vulnérable.
- Une version compatible devient obsolète.
- Une modification introduit une régression.
- Un contrôle précédemment réussi échoue.
- Une documentation devient incomplète.
- Une ressource utilisée dans plusieurs projets présente un problème.
- Une validation doit être renouvelée.

Les alertes doivent être associées aux ressources et aux versions concernées.

### **21.3. Détection des ressources dégradées**

Il faut pouvoir identifier les ressources dont la qualité se détériore progressivement.

Une ressource peut accumuler des avertissements, des dépendances obsolètes et des problèmes de maintenance sans présenter immédiatement une erreur bloquante.

La plateforme doit permettre de repérer ces situations avant qu'elles ne deviennent critiques.

### **21.4. Comparaison de la qualité entre versions**

Il doit être possible de comparer les résultats de qualité de plusieurs versions d'une même ressource.

Cette comparaison doit permettre d'identifier les améliorations, les régressions et les changements qui ont affecté sa fiabilité.

## **22. Expérience utilisateur de l'espace de validation**

L'ensemble des capacités de contrôle doit rester compréhensible et accessible.

Il ne faut pas transformer la plateforme en un outil d'audit technique difficile à utiliser pour les personnes qui ne sont pas spécialisées dans les tests.

L'expérience doit permettre à différents profils de travailler efficacement.

### **22.1. Vue synthétique**

Lorsqu'un utilisateur ouvre une ressource, il doit pouvoir comprendre rapidement son état.

Il doit notamment voir :

- Si la ressource a été évaluée.
- Si elle présente des erreurs.
- Si des tests ont été effectués.
- Si elle possède des validations.
- Si certaines vérifications sont manquantes.
- Si elle présente des risques connus.
- Si elle peut être utilisée dans le contexte envisagé.

### **22.2. Vue technique détaillée**

Les utilisateurs techniques doivent pouvoir accéder à des informations plus approfondies.

Ils doivent notamment pouvoir examiner :

- Les journaux de tests.
- Les erreurs de compilation.
- Les rapports d'analyse.
- Les résultats détaillés.
- Les différences entre versions.
- Les dépendances concernées.
- Les fichiers sources associés.
- Les informations d'environnement.

### **22.3. Vue orientée décision**

Les responsables de bibliothèque ou de validation doivent pouvoir comprendre rapidement si une ressource peut être acceptée pour un usage donné.

Ils doivent pouvoir identifier les risques, les réserves, les contrôles non effectués et les exigences qui ne sont pas satisfaites.

L'objectif est de faciliter les décisions sans imposer à ces utilisateurs de lire tous les détails techniques.

### **22.4. Navigation entre les résultats et les ressources**

La navigation doit être directe.

Lorsqu'une anomalie est détectée, l'utilisateur doit pouvoir accéder à la ressource, à sa version et, si possible, au fichier concerné.

Lorsqu'une campagne échoue, il doit être possible de retrouver les contrôles responsables de l'échec.

Lorsqu'une validation est accordée, il doit être possible de consulter les éléments qui justifient cette décision.

## **23. Collaboration autour des tests et de la qualité**

La validation des ressources peut impliquer plusieurs personnes.

Un développeur peut effectuer les corrections, un designer examiner le rendu, un responsable vérifier les exigences et un autre membre de l'équipe décider de l'acceptation.

La plateforme doit permettre cette collaboration.

### **23.1. Commentaires sur les résultats**

Il doit être possible de commenter :

- Une anomalie.
- Un résultat de test.
- Une différence visuelle.
- Une campagne.
- Une validation.
- Une réserve.
- Une décision de correction.

Les commentaires doivent rester associés aux éléments concernés.

### **23.2. Attribution des responsabilités**

Il doit être possible d'assigner les anomalies et les actions de correction à des personnes ou à des équipes.

L'objectif est de clarifier qui doit examiner un problème, qui doit le corriger et qui doit vérifier sa résolution.

### **23.3. Décisions de validation**

Certaines validations doivent pouvoir faire l'objet d'une décision formelle.

Il doit être possible de documenter :

- La personne ayant validé.
- La version concernée.
- Le périmètre de validation.
- Les éventuelles réserves.
- La date de décision.
- Les éléments examinés.

### **23.4. Historique des décisions**

Les décisions ne doivent pas être perdues dans des échanges informels.

La plateforme doit conserver l'historique des validations, des refus, des exceptions et des modifications de statut.

Cela permet de comprendre pourquoi une ressource a été acceptée ou refusée à un moment donné.

## **24. Scénarios d'utilisation représentatifs**

Les capacités définies dans cette session doivent permettre de couvrir plusieurs situations concrètes.

### **Scénario 1 — Vérification d'un composant récupéré depuis shadcn/ui**

Un utilisateur récupère un composant depuis une collection shadcn/ui.

Il souhaite vérifier qu'il peut l'utiliser dans son environnement.

La plateforme doit lui permettre de :

1. Consulter le code source.
2. Examiner les dépendances.
3. Prévisualiser le composant.
4. Tester ses propriétés.
5. Examiner ses variantes.
6. Tester ses interactions.
7. Vérifier son comportement responsive.
8. Contrôler son accessibilité.
9. Vérifier sa compatibilité avec son environnement.
10. Identifier les éventuelles anomalies.
11. Conserver les résultats.
12. Décider s'il peut être utilisé comme base de personnalisation.

Le composant ne doit pas être considéré comme validé simplement parce qu'il provient d'une bibliothèque connue.

### **Scénario 2 — Contrôle d'un composant profondément personnalisé**

Un utilisateur modifie intégralement un composant existant.

Il change son apparence, ses propriétés, ses comportements et certaines dépendances.

La plateforme doit lui permettre de :

1. Prévisualiser le résultat.
2. Comparer le rendu avec la version précédente.
3. Vérifier les comportements.
4. Tester plusieurs configurations.
5. Identifier les régressions.
6. Contrôler les types.
7. Vérifier les dépendances.
8. Effectuer les tests nécessaires.
9. Documenter les corrections.
10. Évaluer la nouvelle version.

La validation de la version originale ne doit pas être automatiquement transférée à la version personnalisée.

### **Scénario 3 — Comparaison de composants issus de plusieurs sources**

Un utilisateur recherche un composant de tableau et trouve plusieurs implémentations.

Il souhaite choisir celle qui correspond le mieux à son projet.

La plateforme doit lui permettre de :

1. Prévisualiser les différentes ressources.
2. Les tester avec les mêmes données.
3. Comparer leurs fonctionnalités.
4. Examiner leurs dépendances.
5. Vérifier leurs performances.
6. Comparer leurs résultats d'accessibilité.
7. Examiner leurs licences.
8. Comprendre leurs limites.
9. Identifier les adaptations nécessaires.
10. Retenir la ressource la plus appropriée.

### **Scénario 4 — Validation d'une bibliothèque complète**

Une équipe prépare une bibliothèque de composants destinée à être distribuée.

Elle souhaite vérifier sa cohérence et sa fiabilité.

La plateforme doit lui permettre de :

1. Examiner l'ensemble des composants.
2. Vérifier leurs dépendances.
3. Contrôler leurs variantes.
4. Comparer les composants appartenant aux mêmes familles.
5. Vérifier les thèmes.
6. Examiner les tokens.
7. Effectuer des tests fonctionnels.
8. Contrôler l'accessibilité.
9. Vérifier les compatibilités.
10. Examiner la documentation.
11. Identifier les anomalies.
12. Effectuer les corrections.
13. Relancer les campagnes.
14. Produire un rapport global.
15. Valider la bibliothèque pour sa destination.

### **Scénario 5 — Détection d'une régression après une mise à jour**

Une ressource fonctionne correctement et possède une validation antérieure.

Une dépendance est mise à jour.

Après cette modification, certains comportements ne fonctionnent plus.

La plateforme doit pouvoir :

1. Identifier les ressources concernées.
2. Signaler la nécessité d'une nouvelle vérification.
3. Relancer les contrôles pertinents.
4. Identifier les tests qui échouent.
5. Comparer les résultats avec la campagne précédente.
6. Déterminer les conséquences de la mise à jour.
7. Conserver les informations de diagnostic.
8. Permettre la correction.
9. Vérifier à nouveau la ressource.

### **Scénario 6 — Préparation d'une ressource à la distribution publique**

Un utilisateur souhaite distribuer un composant qu'il a créé et personnalisé.

Avant sa distribution, il doit pouvoir vérifier :

- Que le code est complet.
- Que les dépendances sont déclarées.
- Que la ressource peut être installée ou intégrée.
- Que les fonctionnalités principales sont testées.
- Que les comportements attendus sont respectés.
- Que la documentation est suffisante.
- Que les licences sont correctement identifiées.
- Que les éventuels secrets sont absents.
- Que les compatibilités annoncées sont vérifiées.
- Que les défauts bloquants sont résolus.

Il doit ensuite pouvoir conserver un rapport correspondant précisément à la version distribuée.

### **Scénario 7 — Évaluation d'un système de design**

Une équipe crée un système de design complet comprenant des tokens, des thèmes, des composants et plusieurs variantes.

Elle souhaite s'assurer que les éléments sont cohérents.

La plateforme doit permettre de :

1. Examiner les tokens.
2. Vérifier les valeurs.
3. Contrôler les références.
4. Prévisualiser les thèmes.
5. Tester les composants.
6. Comparer les variantes.
7. Détecter les incohérences.
8. Examiner l'accessibilité.
9. Vérifier les comportements responsive.
10. Produire une évaluation globale.

### **Scénario 8 — Utilisation d'une ressource dans plusieurs projets**

Une ressource est utilisée dans plusieurs projets.

Une modification est proposée.

Avant de l'adopter, l'utilisateur souhaite connaître ses conséquences.

La plateforme doit permettre de :

1. Identifier les projets consommateurs.
2. Examiner les versions utilisées.
3. Déterminer les changements introduits.
4. Identifier les incompatibilités potentielles.
5. Effectuer les contrôles nécessaires.
6. Comparer les résultats.
7. Déterminer si la modification peut être adoptée.
8. Conserver les décisions prises.

## **25. Exigences fondamentales à respecter**

Les capacités de cette session doivent respecter plusieurs principes non négociables.

**1. La prévisualisation ne doit pas être confondue avec la validation.**

Un rendu correct ne prouve pas que le code est fiable, que les interactions fonctionnent ou que la ressource est compatible.

**2. Les résultats doivent être rattachés à une version précise.**

Une validation doit toujours correspondre à un état identifiable de la ressource.

**3. Les expérimentations ne doivent pas compromettre les ressources de référence.**

Les essais doivent être réversibles et clairement séparés des modifications définitives.

**4. Les tests doivent être adaptés à la nature des ressources.**

Il ne faut pas imposer les mêmes contrôles à un composant visuel, une fonction, une collection d'icônes et un système de design complet.

**5. Les résultats doivent être compréhensibles.**

Un utilisateur doit pouvoir comprendre ce qui a été testé, ce qui a échoué, ce qui reste incertain et ce qui a été validé.

**6. La qualité doit être multidimensionnelle.**

Une note unique ne doit pas masquer les défauts d'une ressource.

**7. Les contrôles doivent être reproductibles autant que possible.**

Les conditions et les résultats doivent pouvoir être conservés et examinés ultérieurement.

**8. Les validations doivent avoir un périmètre explicite.**

Une ressource validée pour un environnement ne doit pas être automatiquement considérée comme validée pour tous les autres.

**9. Les ressources externes doivent être évaluées indépendamment de leur réputation.**

La provenance est une information importante, mais elle ne constitue pas une preuve de qualité.

**10. Les résultats doivent accompagner le cycle de vie des ressources.**

Une ressource doit pouvoir être réévaluée après une modification, une mise à jour ou un changement des exigences.

**11. La plateforme doit permettre plusieurs niveaux d'exigence.**

Une expérimentation, une bibliothèque interne et une ressource destinée à une distribution publique ne nécessitent pas nécessairement les mêmes garanties.

**12. La validation doit pouvoir associer des contrôles automatisés et des décisions humaines.**

La qualité ne peut pas être entièrement réduite à des vérifications automatiques.

## **26. Résultat attendu de cette session**

À travers cette session, l'objectif est de définir une plateforme capable de fournir un environnement complet de prévisualisation, d'expérimentation, de tests et de validation des ressources logicielles.

L'utilisateur doit pouvoir récupérer une ressource, l'examiner, la personnaliser, l'expérimenter, la tester, détecter ses défauts, corriger ses problèmes, comparer ses versions et déterminer précisément son niveau de fiabilité.

Il doit également pouvoir évaluer plusieurs ressources candidates, contrôler des collections entières, vérifier la cohérence de systèmes de design et suivre l'évolution de la qualité de son patrimoine logiciel.

La plateforme doit ainsi dépasser largement le rôle d'un simple catalogue de composants accompagné d'un aperçu graphique.

Elle doit devenir un environnement dans lequel la qualité des ressources est observable, mesurable, documentée, comparable et maîtrisable.

L'ambition est que chaque ressource puisse disposer d'un véritable dossier de qualité, contenant ses résultats de tests, ses compatibilités vérifiées, ses anomalies connues, ses validations, ses limites et son historique d'évolution.

Ce dossier doit permettre à une personne qui découvre la ressource de comprendre rapidement ce qu'elle peut en attendre, dans quelles conditions elle peut l'utiliser et quelles précautions elle doit prendre.

La qualité ne doit donc pas être une étape facultative située à la fin du processus. Elle doit accompagner toute la vie de la ressource : depuis son acquisition jusqu'à sa distribution, en passant par ses expérimentations, ses personnalisations, ses évolutions et sa maintenance.

## **27. Consigne pour l'analyse et la conception ultérieures**

Les exigences de cette session devront être prises en compte dans l'analyse globale du produit.

Il ne faudra pas réduire cette dimension à l'intégration d'un outil de test ou à l'ajout d'une fenêtre de prévisualisation.

Il faudra étudier l'ensemble des besoins exprimés :

- Prévisualisation fidèle.
- Expérimentation isolée.
- Tests fonctionnels.
- Tests visuels.
- Tests de non-régression.
- Accessibilité.
- Analyse statique.
- Vérification des types.
- Compilation.
- Compatibilité.
- Portabilité.
- Performance.
- Sécurité.
- Contrôle des dépendances.
- Campagnes de tests.
- Rapports.
- Gestion des anomalies.
- Validation humaine.
- Validation technique.
- Suivi de la qualité.
- Comparaison des ressources.
- Évaluation des systèmes de design.

Il faudra également veiller à ne pas supposer que toutes ces capacités doivent être disponibles pour toutes les catégories de ressources. Le périmètre de contrôle doit rester adapté à la nature de chaque ressource, à son environnement et à sa destination.

Enfin, il ne faudra pas anticiper les choix d'architecture, les technologies, les outils ou les modalités d'implémentation dans la définition du besoin. Ces décisions devront intervenir après l'expression complète des exigences fonctionnelles et opérationnelles.


