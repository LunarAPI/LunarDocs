# LunarAPI

Lunar API is a powerful backend service providing authentication, player statistics, leaderboards, and much more. This guide explains how to set up the environment, authenticate users, and interact with the API effectively.

## 🚀 Getting Started

### 🛠️ Obtaining an API Key

To generate an API key, visit api.Lunarify.app, create an account, and register an API key.

## 📡 API Usage

All API requests require an API key sent in the `X-API-Key` header.

## 📌 Endpoints

### 🎮 Players

- **Get player info:**
  ```bash
  curl https://API.Lunarify.app/api/v1/player/{id} \
    -H "X-API-Key: your_api_key_here"
  ```

### ⚔️ Matches

- **Get ranked match details:**
  ```bash
  curl https://API.Lunarify.app/api/v1/match/ranked/{id} \
    -H "X-API-Key: your_api_key_here"
  ```
- **Get unranked match details:**
  ```bash
  curl https://API.Lunarify.app/api/v1/match/unranked/{id} \
    -H "X-API-Key: your_api_key_here"
  ```

### 🗺️ Maps

- **Get all maps:**
  ```bash
  curl https://API.Lunarify.app/api/v1/maps \
    -H "X-API-Key: your_api_key_here"
  ```
- **Get maps base URL:**
  ```bash
  curl https://API.Lunarify.app/api/v1/maps/base-url \
    -H "X-API-Key: your_api_key_here"
  ```

### 🦸 Heroes

- **List all heroes:**
  ```bash
  curl https://API.Lunarify.app/api/v1/hero \
    -H "X-API-Key: your_api_key_here"
  ```
- **Get a specific hero:**
  ```bash
  curl https://API.Lunarify.app/api/v1/hero/{name} \
    -H "X-API-Key: your_api_key_here"
  ```

### 🎒 Items

- **Get all items:**
  ```bash
  curl https://API.Lunarify.app/api/v1/items \
    -H "X-API-Key: your_api_key_here"
  ```
- **Get items by bundle ID:**
  ```bash
  curl https://API.Lunarify.app/api/v1/items/{bundleId} \
    -H "X-API-Key: your_api_key_here"
  ```
- **Search items:**
  ```bash
  curl https://API.Lunarify.app/api/v1/items/search?query=xyz \
    -H "X-API-Key: your_api_key_here"
  ```

### 🏅 Rankings & Leaderboards

- **Get rank distribution:**
  ```bash
  curl https://API.Lunarify.app/api/v1/rank/distribution \
    -H "X-API-Key: your_api_key_here"
  ```
- **Get the global leaderboard:**
  ```bash
  curl https://API.Lunarify.app/api/v1/leaderboard \
    -H "X-API-Key: your_api_key_here"
  ```
- **Get a hero-specific leaderboard:**
  ```bash
  curl https://API.Lunarify.app/api/v1/leaderboard/hero/{heroId} \
    -H "X-API-Key: your_api_key_here"
  ```

### 🎟️ Battle Pass

- **Get battle pass info:**
  ```bash
  curl https://API.Lunarify.app/api/v1/battlepass \
    -H "X-API-Key: your_api_key_here"
  ```

### 🏆 Achievements

- **List all achievements:**
  ```bash
  curl https://API.Lunarify.app/api/v1/achievements \
    -H "X-API-Key: your_api_key_here"
  ```

### 🎫 Codes

- **List all codes:**
  ```bash
  curl https://API.Lunarify.app/api/v1/codes \
    -H "X-API-Key: your_api_key_here"
  ```

### 🎨 Skins

- **List all skins:**
  ```bash
  curl https://API.Lunarify.app/api/v1/skins \
    -H "X-API-Key: your_api_key_here"
  ```

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

