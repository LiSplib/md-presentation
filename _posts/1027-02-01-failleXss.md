---
layout: post
---

##### Faille XSS
<small>La faille XSS où "Cross Site Scripting" est l'une des failles les plus répandues dans les sites web.
Cette faille consiste à injecter du code (HTML, JS, etc) dans des formulaires ou directement dans l'url. Ce code peut être interprété directement par le navigateur Web qui ne fera pas de différence entre le code du site et celui injecté par un utilisateur malveillant. L'exploitation de cette faille permet notamment d'exécuter des scripts douteux, de récupérer les informations récoltées sur un serveur distant (cookie, contenu de la page, etc), de rediriger la victime, de casser la structure de la page.
La solution la plus adaptée contre cette faille est d'utiliser en PHP la fonction `htmlspecialchars()`. Cette fonction permet de filtrer les balises et symboles utilisés par le code HTML afin de ne pas les interpréter mais de les afficher comme du texte à la place.
J'ai choisi comme solution de créer une fonction dans mon modèle ModelAdmin</small>