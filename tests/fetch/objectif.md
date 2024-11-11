# Objectif du Test : Création d'une Mini-Application Pokémon

## Description

Créer une page web simple qui utilise l'API Pokémon pour afficher des informations sur un Pokémon. L'utilisateur pourra entrer le nom d'un Pokémon et voir ses informations de base.

## Fonctionnalités à Réaliser

### 1. Interface Simple

- Un champ de texte pour entrer le nom du Pokémon
- Un bouton "Rechercher"
- Une zone pour afficher les résultats

### 2. Recherche de Pokémon

- Utiliser fetch() pour obtenir les données depuis l'API
- URL de l'API : `https://pokeapi.co/api/v2/pokemon/[nom]`
- Afficher :
  - Nom du Pokémon
  - Image
  - Type(s)
  - Taille
  - Poids

## Code de Base Fourni

```javascript
// HTML de base
<div>
  <input type="text" id="pokemonName" placeholder="Entrez un nom de Pokémon">
  <button onclick="searchPokemon()">Rechercher</button>
  <div id="result"></div>
</div>

// JavaScript à compléter
function searchPokemon() {
  // 1. Récupérer la valeur de l'input

  // 2. Faire la requête fetch()

  // 3. Afficher les résultats
}
```

## Exemple de Requête fetch()

```javascript
fetch("https://pokeapi.co/api/v2/pokemon/pikachu")
  .then((response) => response.json())
  .then((data) => {
    console.log(data);
  })
  .catch((error) => {
    console.log("Erreur:", error);
  });
```

## Critères de Réussite

1. **Le Programme Doit :**

   - Récupérer correctement les données de l'API
   - Afficher les informations demandées
   - Gérer les erreurs basiques (Pokémon non trouvé)

2. **Points Bonus :**
   - Ajouter un message de chargement
   - Mettre en forme les résultats avec du CSS simple
   - Gérer la casse du nom (pikachu/Pikachu/PIKACHU)

## Temps Alloué

- 1 heure

## Aide et Conseils

### Structure de la Réponse API

```javascript
{
  name: "pikachu",
  types: [{ type: { name: "electric" }}],
  height: 4,
  weight: 60,
  sprites: {
    front_default: "URL_DE_L_IMAGE"
  }
}
```

### Étapes Suggérées

1. Commencer par faire une requête simple avec un nom fixe
2. Ajouter l'input utilisateur
3. Afficher les données une par une
4. Ajouter du style basique
5. Gérer les erreurs

### Exemple de Gestion d'Erreur Simple

```javascript
.catch(error => {
  document.getElementById('result').innerHTML =
    "Désolé, ce Pokémon n'a pas été trouvé !";
});
```

## Conclusion

Ce test simple permet de pratiquer :

- L'utilisation de fetch()
- La manipulation du DOM
- La gestion basique des erreurs
- L'interaction utilisateur
