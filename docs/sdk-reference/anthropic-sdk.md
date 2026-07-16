### Anthropic SDK (Python)

```python
import anthropic

client = anthropic.Anthropic(
    api_key="YOUR_API_KEY",
    base_url="https://myrikko.ai"
)

res = client.messages.create(
    model="GLM-5.1",
    max_tokens=128,
    messages=[{"role": "user", "content": "Hello, please introduce yourself briefly."}],
)

print(res.content[0].text)
```
