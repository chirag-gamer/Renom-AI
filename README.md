# Renom-AI API

Yo, check it out—**Renom-AI** is a dope conversational AI API you can use to chat with smart models like **Claude-3.7-Sonnet**. It’s not open-source, but it’s public and ready for you to mess with. Nothing crazy big, just solid and easy to use for your projects.

---

## How to Use It

### Quick Start

Hit up the `/chat` endpoint with a GET request and your prompt. Like this:

```bash
http://66.206.0.186:50249/chat?prompt=sup
```

You’ll get a clean JSON response:

```json
{
  "prompt": "sup",
  "model": "claude-3.7-sonnet",
  "answer": "What’s good? How can I help you?"
}
```

### Pick a Model

You can add `&model=` to switch it up, but right now it’s just "claude-3.7-sonnet":

```bash
http://66.206.0.186:50249/chat?prompt=sup&model=claude-3.7-sonnet
```

No model picked? It sticks with the default.

### Code Vibes

Here’s how to roll with it in Python or JavaScript:

#### Python

```python
import requests

url = "http://66.206.0.186:50249/chat"
params = {"prompt": "What’s up with AI?"}
response = requests.get(url, params=params)
print(response.json()["answer"])
```

#### JavaScript (Node.js)

```javascript
const axios = require('axios');

const url = 'http://66.206.0.186:50249/chat';
const params = { prompt: 'What’s up with AI?' };

axios.get(url, { params })
  .then(response => console.log(response.data.answer))
  .catch(error => console.error('Error:', error));
```

---

## What You Can Hit

- **/chat**: Send a prompt, get a reply. Simple.
- **/stats**: Check some basic stats like word count or requests.
- **/models**: See what models are live (just "claude-3.7-sonnet" for now).

---

## What’s Next

We’re keeping it chill but adding some cool stuff later:
- More models to play with.
- Image generation from prompts.
- API keys for security.
- Better stats to track usage.

---

## Got Issues?

Hit us up if you’re stuck:
- **Email**: support@renom-ai.com

---

It’s free to use, personal or commercial, no stress. Just a good tool to have fun with. Let me know if you need more!
