```markdown
# Atelier : Création d’une Page de Détail Produit avec Tailwind CSS

## Objectif
Apprendre à créer une page de détail produit esthétique et responsive avec **Tailwind CSS**, et personnaliser les composants avec les utilitaires et la configuration Tailwind.

---

## Étape 1 : Installation et Configuration

### Option 1 – Via CDN (rapide pour prototypage)
Ajoutez dans le `<head>` :
```html
<script src="https://cdn.tailwindcss.com"></script>
````

Vous pouvez personnaliser à la volée :

```html
<script>
  tailwind.config = {
    theme: {
      extend: {
        colors: {
          primary: '#2563eb',
        },
      },
    },
  }
</script>
```

### Option 2 – Via npm (projet complet)

```bash
npm install -D tailwindcss
npx tailwindcss init
```

Configurez le fichier `tailwind.config.js` :

```js
content: ["./*.html"],
theme: {
  extend: {
    colors: { primary: '#2563eb' },
  },
},
plugins: [],
```

Puis créez un fichier `input.css` :

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

Compilez Tailwind :

```bash
npx tailwindcss -i ./input.css -o ./output.css --watch
```

---

## Étape 2 : Structure HTML de Base

```html
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Détail Produit - Tailwind</title>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-50 text-gray-900">

  <header class="bg-gray-900 text-white py-4">
    <div class="container mx-auto px-4">
      <h1 class="text-xl font-semibold">Boutique Électronique</h1>
    </div>
  </header>

  <main class="container mx-auto px-4 py-10">
    <div class="grid md:grid-cols-2 gap-8">
      <!-- Image du produit -->
      <div>
        <img src="https://via.placeholder.com/500" alt="Produit" class="rounded-2xl shadow-lg">
      </div>

      <!-- Détails du produit -->
      <div>
        <h2 class="text-3xl font-bold text-primary">Casque Bluetooth XYZ</h2>
        <p class="text-gray-500 mb-4">Ref: XYZ-123</p>
        <p class="text-2xl font-semibold text-green-600 mb-4">79,99 €</p>
        <p class="mb-6">Casque sans fil haute qualité avec réduction de bruit active, autonomie de 20h et design ergonomique.</p>

        <label for="quantity" class="block mb-2 font-medium">Quantité</label>
        <input type="number" id="quantity" value="1" min="1"
               class="w-20 border border-gray-300 rounded-lg p-2 mb-6 focus:ring-2 focus:ring-primary focus:outline-none">

        <button class="bg-primary text-white px-6 py-3 rounded-xl shadow hover:bg-blue-700 transition">
          🛒 Ajouter au panier
        </button>
      </div>
    </div>
  </main>

  <footer class="text-center py-6 border-t text-gray-500">
    © 2025 Ma Boutique
  </footer>

</body>
</html>
```

---

## Étape 3 : Personnalisation et Thèmes

Ajoutez dans la config :

```js
theme: {
  extend: {
    colors: {
      primary: '#1e40af',
      accent: '#f97316',
    },
    fontFamily: {
      sans: ['Inter', 'sans-serif'],
    },
  },
},
```

---

## Étape 4 : Composants Avancés :

* **Tabs** : Utilisez `flex space-x-4 border-b`
* **Grid de produits similaires** : `grid grid-cols-2 md:grid-cols-4 gap-6`
* **Responsive** : utilisez `md:`, `lg:`, `xl:` pour ajuster les tailles et espacements

---

## Étape 5 : Accessibilité et Responsive Design

* Utilisez des `alt` pour toutes les images
* Vérifiez les contrastes (`bg-primary text-white`)
* Utilisez `focus:` et `hover:` pour indiquer les interactions

---

## Conclusion

Tailwind CSS offre un contrôle précis du design grâce à ses classes utilitaires.
La configuration et la personnalisation via le fichier `tailwind.config.js` permettent de créer une identité visuelle unique.

---
