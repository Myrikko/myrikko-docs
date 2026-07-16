
### OpenAI SDK (Python)

```python
from openai import OpenAI

client = OpenAI(
    api_key="YOUR_API_KEY",
    base_url="https://myrikko.ai/v1"
)

res = client.chat.completions.create(
    model="Kimi K2.6",
    messages=[{"role": "user", "content": "Hello, please introduce yourself briefly."}],
    temperature=1,
    max_tokens=128,
    top_p=1,
    stop=None
)

print(res.choices[0].message.content)
```
