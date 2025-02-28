# Kata 4

# Objectifs pédagogiques

- Comprendre et appliquer un design “mobile first” à des applications web
- Utiliser les media queries pour adapter le style en fonction de la taille de l'écran
- Créer des mises en page fluides et flexibles avec CSS Flexbox et Grid
- Utiliser les pseudo-classes (**:hover**, **:focus**, etc) et pseudo-éléments (**::before**, **::after**, etc) pour styliser des états spécifiques
- Comprendre et appliquer les différentes unités de mesure (rem, em, px, %, etc) pour adapter la taille des éléments

---

- Respecter les normes d’accessibilité dès la phase de conception d’un projet numérique
- Implémenter des solutions pour améliorer l’accessibilité numérique dans des projets web

---

- Déployer des applications web par l’intermédiaire des plateformes de déploiement et d’hébergement (type Vercel).

---

- Effectuer des opérations CRUD (Create, Read, Update, Delete) dans les bases de données relationnelles en utilisant le langage SQL

# Cas pratique 1 : Création de deux pages responsive et accessibles (1h30)

## **Contexte**

Tu travailles en tant que développeur·se fullstack pour Yoogy, une plateforme accompagnant au rééquilibrage alimentaire. Ton projet du moment est le nouveau design de leur page “Recettes”.

Bob, le designer de l’équipe, a transmis ces deux maquettes: 

- Maquette de la vue “Liste des recettes”, accessible depuis la page `index.html`
    - Figma: https://www.figma.com/design/yZf9DnAms8iJ4YVsiHQpgJ/Yoogy---Maquettes?node-id=0-1&p=f&t=XkHWyJ8PBO4BFBgC-0
    - Framer: https://framer.com/projects/Yoogy-MVP-Niveau-1--WYAMwNoNCWxH5l6fp3ZR-dOi18?node=X4DAMfbIC
    - 🔍 Voir les effets d’animation sur le prototype généré par Framer: https://renewed-feature-267779.framer.app/
- Maquette de la vue “Détail d’une recette” `detail.html`
    - Figma: https://www.figma.com/design/yZf9DnAms8iJ4YVsiHQpgJ/Yoogy---Maquettes?node-id=4-1278&p=f&t=XkHWyJ8PBO4BFBgC-0
    - Framer : https://framer.com/projects/Yoogy-MVP-Niveau-1--WYAMwNoNCWxH5l6fp3ZR-dOi18?node=sOLbSo4Ak
    - 🔎 Voir les effets d’animation sur le prototype généré par Framer: https://renewed-feature-267779.framer.app/recipes/energizing-bowl
    - ⚠️ L’image principale de la recette doit rester *sticky* et attachée en haut de la page au scroll !
    
    [demo-detail-page-recette.mov](attachment:8c501ec0-593a-4d24-a32d-acc42d9f9477:demo-detail-page-recette.mov)
    

Bob a utilisé comme typographies pour ces maquettes la Google Font, [Inter Tight](https://fonts.google.com/specimen/Inter+Tight). 

Ta mission? 🎯  **Intégrer le nouveau design du carnet de recettes !**

Chez Yoogy, la qualité est le mot d’ordre ! Ton code devra : 

1. Suivre les principes du **mobile first**
2. Utiliser **CSS Flexbox et/ou Grid**
3. Exploiter les **media queries**, les **pseudo-classes et pseudo-éléments**
4. Respecter les normes d’accessibilité 

## Instructions

### **1. Mise en place du projet**

- Crée un dossier de projet avec les fichiers
    - `index.html`
    - `detail.html`
    - un fichier `styles.css`

### **2. Structure HTML de la page**

Ta page doit contenir à minima la liste de recettes et le menu, et la page “Détail de recette”

![Le MVP souhaité par Yoogy, issu de la maquette disponible [ici](https://www.figma.com/design/yZf9DnAms8iJ4YVsiHQpgJ/Yoogy---Maquettes?node-id=0-1&p=f&t=XkHWyJ8PBO4BFBgC-0)](attachment:32d5b4b1-eea9-4bae-8e87-602a9a0f089b:Capture_decran_2025-02-26_a_10.01.07.png)

Le MVP souhaité par Yoogy, issu de la maquette disponible [ici](https://www.figma.com/design/yZf9DnAms8iJ4YVsiHQpgJ/Yoogy---Maquettes?node-id=0-1&p=f&t=XkHWyJ8PBO4BFBgC-0)

**Exigences :**

- Utiliser des **balises sémantiques HTML5** (header, section, footer, etc.).
- Ajouter des **attributs d’accessibilité** (`alt`, `aria-label`, `aria-hidden`, etc.).

### **3. Stylisation et design responsive**

Bob est exigeant quant au respect de la maquette. Tu dois intégrer par ordre d'importance : 

- La liste de recettes en respectant les espacements
- Le détail d'une page recette

Par ordre d’importance 👇🏼

**Appliquer un design “mobile first”**

- La page doit être conçue en **mobile first** ! Commence par les règles mobiles par défaut puis ajoute des medias query pour les spécificités sur tablette et desktop.

**Ajouter des animations au scroll sur la page**

- Les textes des recettes doivent apparaître au survol de la page ([effet souhaité ici](https://renewed-feature-267779.framer.app/))

**Ajouter des animations au survol de la souris sur certains blocs**

- Ajouter une bordure verte **au survol des cartes** recettes avec `:hover`.
- L’effet doit aussi être visible à la navigation clavier sur les recettes.
- Mettre un **focus visible sur les boutons** pour améliorer l’accessibilité.

**Techniques à utiliser**

- **CSS Grid et/ou Flexbox** pour organiser la mise en page.
- **Media queries** (`@media screen and (min-width: 768px)`) pour adapter l'affichage sur tablette et desktop.
- **Unités de mesure adaptées** (`rem`, `em`, `%`, `vh`, `vw` selon les besoins).
- **Pseudo-classes et pseudo-éléments** (`:hover`, `:focus`, `::before`, `::after`) pour les effets au survol de la souris sur les liens et les images.
- Les icônes utilisées par Bob se trouvent ici
    - SVG pour la flèche sur la page listant les recettes
    
    ```sql
    <svg width="100%" height="100%" viewBox="-1 -1 12 12" fill="none" id="svg833880176_222" preserveAspectRatio="none">
    <path d="M0 10L10 0M10 0H0M10 0V10" stroke="black" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"></path>
    </svg>
    ```
    
    - [SVG pour le symbole €](https://framerusercontent.com/images/MkPMeK6tNCkKhOwARw8i4kZ0dU.svg)
    - [SVG pour le temps de cuisson](https://framerusercontent.com/images/W7MuhhBrS8cJXCEj4wRGXqr6EY.svg)
    - [SVG pour le niveau de difficulté](https://framerusercontent.com/images/c5dR6jRGW6CChn5u5RBJBSpR8ZU.svg)

<aside>
💡

Teste ta page sur plusieurs tailles d’écran (mobile, tablette, desktop) grâce aux DevTools !

</aside>

### **4. Déploiement**

L’équipe produit veut pouvoir tester la page que tu as réalisé et la transférer à d’autres clients beta-testeurs. 

- **Déployer** la page réalisée sur Github Pages ou Vercel et fournir l’URL du déploiement.

**Bonus**

<aside>
💡

Tu vas utiliser [Framer](http://framer.com/) pour ce bonus ! 
La création de compte est **nécessaire.** Une fois connecté·e, tu pourras observer la maquette comme avec Figma. 

</aside>

Si le temps te le permet et que le MVP est rapidement complété, voici ce qui a été priorisé pour le deuxième MVP. Tu peux voir la maquette du MVP 2 ici: https://framer.com/projects/Yoogy-MVP-2--96cwzIqWzV98w3yhSDpe-276oP?node=X4DAMfbIC 

- Ajouter le composant “Cheminer vers le bien-être” pour inciter à l’abonnement à la plateforme.
- Ajouter des effets d’animation sur les boutons au hover ainsi que sur les icônes de la page.
- Ajouter un effet de changement de couleur sur le vecteur vert au scroll sur la page

---

### **Critères de réussite :**

✅ La page s’affiche correctement et est **responsive** sur mobile, tablette et desktop.

✅ Utilisation correcte de **Flexbox ou Grid** pour la mise en page.

✅ Styles adaptatifs grâce aux **media queries**.

✅ Présence et bon usage des **pseudo-classes et pseudo-éléments**.

✅ Respect des **normes d’accessibilité** (balises sémantiques, attributs ARIA, focus visible).

✅ Bonne compatibilité sur **plusieurs navigateurs**.

✅ La page est **déployée**.

# Cas pratique 2 : Analyse de données (30 minutes)

L’équipe de Yoogiz veut faire une analyse de données pour comprendre quelle catégorie est la plus populaire parmi les utilisateur·ices. 

🎯 Leur objectif est de prévoir de la création de contenu en conséquence : si les utilisateur·ices sont friand·e·s de recettes végétariennes, autant leur en proposer plus !

Voici le dump de la base de données que tu peux charger directement dans PHPMyAdmin 👇🏼

[dump-yoogy.sql](attachment:a656d87b-ee3d-4baf-ac38-261ff543565e:dump-yoogy.sql)

**Maintenance**

Gaston, le rédacteur en chef de Yoggy, te demande d’ajouter une nouvelle recette dans la base de données.

- 🧑🏼‍🍳 **La recette de Gaston**
    
    Salade de pommes de terre - Durée: 5mn - Difficulté: 1 
    Faites cuire des pommes de terre coupées en dès. Mélangez des pommes de terre, des cornichons, du thon émietté, des échalottes, de la mayo et de l’huile ! 
    Elle devra être catégorisée dans les “Entrées”, elle est sans gluten / sans noix / sans arachides et sans sucres !
    
1. Écris une requête pour ajouter cette nouvelle recette dans la base de données et l’associer à la bonne catégorie et aux bonnes restrictions alimentaires.

Mince, Gaston s’est trompé dans la durée ! Il a renseigné 5 mn en temps de préparation alors que ça prend plutôt 35 mn ! 

1. Ecris une requête pour mettre à jour la durée de cette recette 

Décidément, Gaston est un gaffeur! Il se rend compte qu’il avait ajouté dans la base de données une recette en brouillon par erreur!

1. Supprime la recette erronée de Gaston qui a pour titre “Salades de pdt”

**Analyse de données**

1. Écrire une requête pour récupérer toutes les recettes marquées en favori par ChefLeo
2. Fais une requête pour récupérer les recettes qui n'ont jamais été marquées en favori
3. Fais une requête permettant de récupérer le nombre de recette sans gluten et végétariennes sur le site. 
4. Fais une requêtes permettant de lister les catégories les plus mises en favori sur le site par ordre croissant
5. Affiche une liste de tou·te·s les utilisateur·ices du site et le nombre de recettes qu’iels ont marqué en favori (ordonné par ordre décroissant)
6. Supprime les recettes contenant du gluten