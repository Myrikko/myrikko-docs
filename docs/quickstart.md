# Welcome to Myrikko

Myrikko gives you access to multiple frontier AI models through a single API key.  With a single API endpoint, you can integrate once to use different models and switch between them as your needs evolve.
It automatically routes requests based on provider latency and availability, helping you maintain reliable access to the models you use. You can manage billing across models in one place and track usage through a unified dashboard. With no platform markup, Myrikko also offers transparent, developer-friendly pricing.

## Step 1. Create an Account

Sign up for Myrikko using your email, GitHub, or Google account.

## Step 2. Get Your API Key

Every new account includes a default API key that you can use immediately.
You can also create a new API key:
1. Go to Workspace → Settings → API Keys.
2. Create a new API Key.
3. Copy and store your API key securely.

## Step 3. Configure the Base URL

Configure the base URL for the SDK you are using.
- OpenAI SDK: https://myrikko.ai/v1
- Anthropic SDK: https://myrikko.ai
- Google GenAI SDK: https://myrikko.ai
In most cases, you only need to update your API key, base URL, and model parameter to start sending requests through Myrikko's unified API.

## Step 4. Make Your First Request

Myrikko supports popular SDKs, including the OpenAI, Anthropic, and Google GenAI SDKs.
You can choose the SDK that best matches your existing integration.

### OpenAI SDK (Python)

```python
from openai import OpenAI

client = OpenAI(
    api_key="YOUR_API_KEY",
    base_url="https://myrikko.ai/v1"
)

res = client.chat.completions.create(
    model="glm-5.3-flash",
    messages=[{"role": "user", "content": "Hello, please introduce yourself briefly."}],
    temperature=1,
    max_tokens=128,
    top_p=1,
    stop=None
)

print(res.choices[0].message.content)
```

### Anthropic SDK (Python)

```python
import anthropic

client = anthropic.Anthropic(
    api_key="YOUR_API_KEY",
    base_url="https://myrikko.ai"
)

res = client.messages.create(
    model="deepseek-v4.1-flash",
    max_tokens=128,
    messages=[{"role": "user", "content": "Hello, please introduce yourself briefly."}],
)

print(res.content[0].text)
```

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
    model="gpt-6.1-sol",
    contents="Hello, please introduce yourself briefly.",
)

print(res.text)
```

---

## Usage & Billing

You can monitor your usage from the dashboard, including:

* API requests
* Token usage
* Costs
* Model usage

Billing is based on the input and output tokens consumed by each request. Each model has its own input and output token pricing, which is displayed on the Model Marketplace page.

For billing and account management questions, please contact us at [support@myrikko.ai](mailto:support@myrikko.ai).

---

## Need Help?

If you have questions or run into issues, you can reach us through:

* Email: [support@myrikko.ai](mailto:support@myrikko.ai)
* Discord: https://discord.gg/bNRPdsXGDH
