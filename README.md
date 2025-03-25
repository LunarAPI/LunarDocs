# Lunar API Backend

Lunar API is a powerful backend service providing authentication, player statistics, leaderboards, and much more. This guide explains how to set up the environment, authenticate users, and interact with the API effectively.



### 🛠️ Obtaining an API Key

To generate an API key, go to LunarAPI.org and create an account and register an API-Key.


## 📡 API Usage

All API requests require an API key sent in the `X-API-Key` header.

### 🎮 Players

- **Get player stats:**

  ```bash
  curl https://API.Lunarify.app/api/v1/player/123456 \
    -H "X-API-Key: your_api_key_here"
  ```

- **Update player data:**

  ```bash
  curl -X POST https://API.Lunarify.app/api/v1/player/update-player/123456 \
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
  curl https://API.Lunarify.app/api/v1/hero/iron-man \
    -H "X-API-Key: your_api_key_here"
  ```

### 🏆 Leaderboards

- **Get the global leaderboard:**

  ```bash
  curl https://API.Lunarify.app/api/v1/leaderboard \
    -H "X-API-Key: your_api_key_here"
  ```

- **Get a hero-specific leaderboard:**

  ```bash
  curl https://API.Lunarify.app/api/v1/leaderboard/hero/123 \
    -H "X-API-Key: your_api_key_here"
  ```

### 🗺️ Maps

- **Get maps base URL:**

  ```bash
  curl https://API.Lunarify.app/api/v1/maps/base-url \
    -H "X-API-Key: your_api_key_here"
  ```

- **Get all maps:**

  ```bash
  curl https://API.Lunarify.app/api/v1/maps \
    -H "X-API-Key: your_api_key_here"
  ```

### ⚔️ Matches

- **Get match details:**

  ```bash
  curl https://API.Lunarify.app/api/v1/match/123456 \
    -H "X-API-Key: your_api_key_here"
  ```

### 🎟️ Battle Pass

- **Get battle pass info for a specific season:**

  ```bash
  curl "https://API.Lunarify.app/api/v1/battlepass?season=0" \
    -H "X-API-Key: your_api_key_here"
  ```

### 🏅 Achievements

- **List all achievements:**

  ```bash
  curl https://API.Lunarify.app/api/v1/achievements \
    -H "X-API-Key: your_api_key_here"
  ```

- **Filter achievements:**

  ```bash
  curl "https://API.Lunarify.app/api/v1/achievements?filter=daily" \
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

- **Search for skins:**

  ```bash
  curl "https://API.Lunarify.app/api/v1/skins?search=iron" \
    -H "X-API-Key: your_api_key_here"
  ```

### 🔍 System Status

- **Check system and endpoint status:**

  ```bash
  curl https://API.Lunarify.app/api/v1/system/status
  ```

## 📊 Response Formats

All API responses follow a structured JSON format:

### ✅ Success Response:

```json
{
  "status": "success",
  "data": { ... }
}
```

### ❌ Error Response:

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

