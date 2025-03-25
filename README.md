# Lunar API Backend

Lunar API is a powerful backend service providing authentication, player statistics, leaderboards, and much more. This guide explains how to set up the environment, authenticate users, and interact with the API effectively.

## 🌍 Environment Setup

Before running the Lunar API backend, set up the required environment variables.

### 📌 Step 1: Create a `.env` File

Run the following command to copy the example environment file:

```bash
cp .env.example .env
```

### 🔑 Step 2: Configure Environment Variables

Ensure the following variables are set in your `.env` file:

```env
JWT_SECRET=your_dev_secret_key_here  # Generate using: openssl rand -base64 32

GITHUB_CLIENT_ID=your_github_client_id
GITHUB_CLIENT_SECRET=your_github_secret
GITHUB_CALLBACK_URL=https://API.Lunarify.app/auth/github/callback
```

## 🚀 Running the Backend

Follow these steps to start the Lunar API backend:

1. Install dependencies:

   ```bash
   npm install
   ```

2. Start the backend server:

   ```bash
   npm run dev
   ```

## 🔐 Authentication

### 🛠️ Obtaining an API Key

To generate an API key, send the following request:

```bash
curl -X POST https://API.Lunarify.app/auth/api-key \
  -H "Content-Type: application/json" \
  -d '{"name": "My API Key", "plan": "free"}'
```

### 🔗 GitHub OAuth Login

Redirect users to authenticate via GitHub:

```bash
GET https://API.Lunarify.app/auth/github
```

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

## 🤝 Contributing

We welcome contributions! Feel free to submit pull requests or report issues on GitHub.

## 📜 License

This project is licensed under the MIT License.

---

🌙 **Lunar API - Empowering the Future of Gaming**

