
### Google GenAI SDK (Python)

```python
from google import genai

client = genai.Client(
     api_key="YOUR_API_KEY",
     http_options={
        "base_url": "https://myrikko.ai"
    },
)

res = client.models.generate_content(
    model="GLM-5.2",
    contents="Hello, please introduce yourself briefly.",
)

print(res.text)
```
