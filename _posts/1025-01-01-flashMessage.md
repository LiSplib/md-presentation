---
layout: post
---

Gestion des messages Flash

<small>J'utilise les messages Flash pour avertir l'utillisateur de la réussite ou de l'echec de sa requête.
Les messages flash sont gérés par la `$_SESSION['flash']`.
Il faut lui donner en paramètres la couleur Bootstrap ('danger', 'success' etc) puis le message a afficher.
La session est est détruite directement après son appel donc le message disparaît au rechargement de la page ou changement de page.</small>
<small style="font-size: 10px!important;">
```
<?php if(!empty($_SESSION['flash'])) : ?>
<div class="container text-center mt-4">
<?php if(isset($_SESSION['flash'])): ?>
    <?php foreach($_SESSION['flash'] as $type => $message): ?>
        <div class="alert alert-<?= $type; ?>">
            <?= $message; ?>
        </div>
    <?php endforeach; ?>
    <?php unset($_SESSION['flash']); ?>
<?php endif; ?>
</div>
<?php endif; ?>
```
