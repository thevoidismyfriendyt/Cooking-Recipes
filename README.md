# 🍽️ Recipe Finder

A static web app for finding recipes based on ingredients you already have. Browse 105+ recipes from 20+ cuisines around the world, filter by ingredient or cuisine, and get full step-by-step instructions for every dish.

## Features

- **Ingredient picker** — select ingredients from a scrollable list; recipes are ranked by how many you have
- **Cuisine filter** — filter by country with flag emoji chips (🇯🇵 🇲🇽 🇫🇷 🇮🇳 and more)
- **Match bar** — each card shows how many recipe ingredients you have vs. total needed
- **Recipe detail modal** — click any recipe to see:
  - Prep / cook / total time
  - Servings and difficulty
  - Equipment needed (oven, stove, blender, etc.)
  - Oven temperature in both °F and °C where applicable
  - Full ingredient list (green = you have it, orange = missing)
  - Numbered step-by-step instructions
- **No install, no backend** — open `index.html` in any browser or serve with any static file server

## Cuisines

🇺🇸 American · 🇪🇸 Spanish · 🇮🇹 Italian · 🇫🇷 French · 🇬🇷 Greek · 🇬🇧 British · 🇩🇪 German · 🇹🇷 Turkish · 🇷🇺 Russian · 🇱🇧 Lebanese · 🇲🇦 Moroccan · 🇳🇬 Nigerian · 🇯🇲 Jamaican · 🇮🇳 Indian · 🇯🇵 Japanese · 🇨🇳 Chinese · 🇰🇷 Korean · 🇹🇭 Thai · 🇻🇳 Vietnamese · 🇲🇽 Mexican · 🇧🇷 Brazilian · 🇵🇪 Peruvian · 🇦🇷 Argentine

## Running Locally

```bash
git clone https://github.com/thevoidismyfriendyt/Cooking-Recipes.git
cd Cooking-Recipes
python3 -m http.server 8000
```

Then open `http://localhost:8000` in your browser.

## File Structure

```
index.html    # App shell, styles, and all JavaScript
recipes.js    # Recipes 1–30  (General, Spanish)
recipes2.js   # Recipes 31–68 (Japanese, Chinese, Thai, Vietnamese, Korean, Indian, Moroccan, Lebanese, French)
recipes3.js   # Recipes 69–105 (French cont., Italian, Greek, British, German, Brazilian, Turkish, Russian, Jamaican, Nigerian, Peruvian, Argentine, Mexican)
```

## Adding Recipes

Add a new entry to the `RECIPES`, `RECIPES2`, or `RECIPES3` array following this structure:

```js
{
  id: 106,
  name: "Recipe Name",
  image: "🍳",                          // single emoji
  time: { prep: 10, cook: 20, total: 30 },
  servings: 2,
  difficulty: "Easy",                   // Easy / Medium / Hard
  temperature: { f: 375, c: 190 },      // optional — oven recipes only
  equipment: ["Oven", "Baking Sheet"],
  tags: ["Italian", "Dinner", "Vegetarian"],
  ingredients: [
    { name: "pasta", amount: "200", unit: "g" },
  ],
  steps: [
    "Step one.",
    "Step two.",
  ],
}
```
