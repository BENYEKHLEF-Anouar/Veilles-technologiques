````markdown
# Atelier : Création d’une Page de Détail Produit avec Bootstrap

## Objectif
Apprendre à créer une page de détail produit moderne et responsive en utilisant **Bootstrap 5**, tout en personnalisant les composants de base.

---

## Étape 1 : Préparer l’Environnement

### Option 1 – Via CDN (recommandé pour les tests rapides)
Ajoutez les liens Bootstrap dans le `<head>` et avant la fin du `<body>` :

```html
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
````

### Option 2 – Via npm (projets structurés)

```bash
npm install bootstrap
```

Puis importez-le dans votre fichier principal :

```js
import 'bootstrap/dist/css/bootstrap.min.css';
import 'bootstrap/dist/js/bootstrap.bundle.min.js';
```

---

## Étape 2 : Structure de Base HTML

Créez un fichier `product.html` :

```html
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Détail Produit - Bootstrap</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

  <header class="bg-dark text-white py-3">
    <div class="container">
      <h1 class="h3">Boutique Électronique</h1>
    </div>
  </header>

  <main class="container my-5">
    <div class="row g-4">
      <!-- Image du produit -->
      <div class="col-md-6">
        <img src="https://via.placeholder.com/500" class="img-fluid rounded shadow" alt="Produit">
      </div>

      <!-- Détails du produit -->
      <div class="col-md-6">
        <h2>Casque Bluetooth XYZ</h2>
        <p class="text-muted">Ref: XYZ-123</p>
        <h3 class="text-primary mb-3">79,99 €</h3>
        <p>Casque sans fil haute qualité avec réduction de bruit active, autonomie de 20h et design ergonomique.</p>

        <div class="mb-3">
          <label for="quantity" class="form-label">Quantité</label>
          <input type="number" id="quantity" class="form-control w-25" value="1" min="1">
        </div>

        <button class="btn btn-primary btn-lg">
          <i class="bi bi-cart-plus"></i> Ajouter au Panier
        </button>
      </div>
    </div>
  </main>

  <footer class="bg-light text-center py-4 mt-5 border-top">
    <small>© 2025 Ma Boutique</small>
  </footer>

  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

---

## Étape 3 : Personnalisation avec les Classes Utilitaires

* Changer la palette :
  `btn-primary` → `btn-success` ou `btn-outline-primary`
* Ajouter de l’ombre :
  `.shadow`, `.shadow-lg`
* Ajuster les espacements :
  `.my-5`, `.p-3`, `.g-4`

---

## Étape 4 : Personnalisation CSS Supplémentaire

Créez `custom.css` :

```css
h2 {
  font-weight: 700;
  color: #0d6efd;
}
.btn-primary {
  background-color: #6610f2;
  border-color: #6610f2;
}
```

Ajoutez-le **après** le lien Bootstrap :

```html
<link rel="stylesheet" href="custom.css">
```

---

## Étape 5 : Composants Avancés

* Ajoutez un **carousel d’images** (`.carousel`)
* Ajoutez des **onglets d’information** (`.nav-tabs`)
* Ajoutez des **cartes de produits similaires** avec `.card`

---

## Étape 6 : Responsive & Accessibilité

* Utilisez les grilles Bootstrap (`col-md-6`, `col-lg-4`, etc.)
* Vérifiez la lisibilité avec le contraste (`bg-light` + `text-dark`)
* Testez sur mobile via les outils de dev

---

## Conclusion

Bootstrap permet de créer rapidement une page de détail produit claire et responsive. La personnalisation passe par les classes utilitaires et un CSS additionnel.

---
