# LunarAPI

Lunar API is a powerful backend service providing authentication, player statistics, leaderboards, and much more. This guide explains how to set up the environment, authenticate users, and interact with the API effectively.

## 🚀 Getting Started

### 🛠️ Obtaining an API Key

To generate an API key, visit [api.Lunarify.app](https://api.lunarify.app), create an account, and register an API key.

## 📡 API Key Header

All API requests require an API key sent in the `X-API-Key` header.
```json
{
  "X-API-Key": "MY_API_KEY",
}
```

Not providing an API key will result in the following message.

```json
{
  "error": "API key is required"
}
```

Please refer to your language of choice documentation to learn more about HTTP headers.

## 📌 Endpoints

### 🎮 Players

- **Get Player Info:**
  ```plaintext
  https://API.Lunarify.app/api/v1/player/{playerId}
  ```

  **Params:**
    - playerId: The player id to search for.

### ⚔️ Matches

- **Get Ranked Matches:**
  ```plaintext
  https://API.Lunarify.app/api/v1/match/ranked/{playerId}
  ```
  **Params:**
    - playerId: The player id to search for.

- **Get Unranked Matches:**
  ```plaintext
  https://API.Lunarify.app/api/v1/match/unranked/{playerId}
  ```
  **Params:**
    - playerId: The player id to search for.

- **Get Match Details**
  ```plaintext
    https://API.Lunarify.app/api/v1/match/{matchId}
  ```
  **Params:**
  - matchId: The match id to search for.

### 🗺️ Maps

- **Get all maps:**
  ```plaintext
  https://API.Lunarify.app/api/v1/maps
  ```
- **Get maps base URL:**
  ```plaintext
  https://API.Lunarify.app/api/v1/maps/base-url
  ```

### 🦸 Heroes

- **List all heroes:**
  ```plaintext
  https://API.Lunarify.app/api/v1/hero
  ```

- **Get all Teamups:**
  ```plaintext
  https://API.Lunarify.app/api/v1/teamups
  ```

  - **Teamup by ID:**
  ```plaintext
  https://API.Lunarify.app/api/v1/teamups/:id
  ```
  **Params:**
    - Id: The teamup ID under /api/v1/teamups
  
  - **Teamup by Hero:**
  ```plaintext
  https://API.Lunarify.app/api/v1/teamups/hero/:heroId
  ```
  **Params:**
    - heroId: The hero Id under /api/v1/teamups

- **Get a specific hero:**
  ```plaintext
  https://API.Lunarify.app/api/v1/hero/{name}
  ```
  **Params:**
    - Name: The name of the hero to return.

### 🎒 Items

- **Get all items:**
  ```plaintext
  https://API.Lunarify.app/api/v1/items
  ```

- **Get items by bundle ID:**
  ```plaintext
  https://API.Lunarify.app/api/v1/items/{bundleId}
  ```
  **Params:**
    - Bundle Id: The player id to search for.

- **Search items:**
  ```plaintext
  https://API.Lunarify.app/api/v1/items/search?query=xyz
  ```

### 🏅 Rankings & Leaderboards

- **Get rank distribution:**
  ```plaintext
  https://API.Lunarify.app/api/v1/rank/distribution
  ```

- **Get the global leaderboard:**
  ```plaintext
  https://API.Lunarify.app/api/v1/leaderboard
  ```

- **Get a hero-specific leaderboard:**
  ```plaintext
  https://API.Lunarify.app/api/v1/leaderboard/hero/{heroId}
  ```
  **Params:**
    - Hero Id: The hero Id to search for 


### 🎟️ Battle Pass

- **Get battle pass info:**
  ```plaintext
  https://API.Lunarify.app/api/v1/battlepass
  ```

### 🏆 Achievements

- **List all achievements:**
  ```plaintext
  https://API.Lunarify.app/api/v1/achievements
  ```

### 🎫 Codes

- **List all codes:**
  ```plaintext
  https://API.Lunarify.app/api/v1/codes
  ```

### 🎨 Skins

- **List all skins:**
  ```plaintext
  https://API.Lunarify.app/api/v1/skins
  ```
### 🌐 Updates & More

- **List all Dev Diaries:**
  ```plaintext
  https://API.Lunarify.app/api/v1/devdiary
  ```

- **Get Latest Dev Diaries:**
  ```plaintext
  https://API.Lunarify.app/api/v1/devdiary/latest
  ```

- **Get Dev Diary by ID:**
  ```plaintext
  https://API.Lunarify.app/api/v1/devdiary/:id
  ```
  **Params:**
    - Id: The ID from the /api/v1/devdiary
## 📊 Response Formats

### ✅ Success Response

```json
{
  "status": "success",
  "data": { ... }
}
```

### ❌ Error Response

```json
{
  "error": true,
  "message": "Error description"
}
```

## 📉 Rate Limiting

Free-tier API keys have the following limits:

- **100 requests per minute**
- **5000 requests per day**

For higher limits, contact us for premium plans.

---

**Lunar API - Empowering the Future of Gaming**

