# 📰 Orvix Games News API

The **Orvix Games News API** is the official REST API for accessing the latest news, announcements, and updates published by Orvix Games.

## Features

- 🚀 Fast JSON responses
- 📰 Latest news articles
- 📱 Easy integration
- 🌍 REST API
- 🔒 HTTPS support

---

## Base URL

```http
https://orvixgames.com/news/
```

---

## Get Latest News

### Request

```http
GET /news/?api=1&limit=6
```

### Full URL

```http
https://orvixgames.com/news/?api=1&limit=6
```

---

## Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| api | Integer | ✅ | Enable JSON output. Use `1`. |
| limit | Integer | ❌ | Maximum number of news articles returned. |

---

## Example Request (JavaScript)

```javascript
fetch("https://orvixgames.com/news/?api=1&limit=6")
  .then(res => res.json())
  .then(data => console.log(data));
```

---

## Example Request (PHP)

```php
<?php

$json = file_get_contents(
    "https://orvixgames.com/news/?api=1&limit=6"
);

$data = json_decode($json, true);

print_r($data);

?>
```

---

## Example Request (Python)

```python
import requests

response = requests.get(
    "https://orvixgames.com/news/?api=1&limit=6"
)

print(response.json())
```

---

## Example Response

```json
{
  "status": "success",
  "news": [
    {
      "id": 1,
      "title": "Viona AI 3.0 Released",
      "description": "The next generation of Viona AI is now available.",
      "url": "https://orvixgames.com/news/viona-ai-3",
      "image": "https://orvixgames.com/uploads/news/image.jpg",
      "date": "2026-07-18"
    }
  ]
}
```

---

## HTTP Status Codes

| Code | Description |
|------|-------------|
| 200 | Request successful |
| 400 | Invalid request |
| 404 | Resource not found |
| 500 | Internal server error |

---

## Rate Limits

Currently there are no public rate limits.

If rate limiting is introduced in the future, this documentation will be updated.

---

## License

This repository contains documentation and usage examples for the Orvix Games News API.

API content and news remain the property of **Orvix Games**.

---

## Official Website

https://orvixgames.com

## Documentation

This repository serves as the official documentation for the Orvix Games News API.

---

Made with ❤️ by Orvix Games
