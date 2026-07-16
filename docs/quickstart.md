# Welcome to Myrikko

Myrikko provides a unified API for accessing Chinese frontier AI models, including Kimi, GLM, Qwen, DeepSeek, and more.

With one API key and one endpoint, developers can integrate once, switch between models easily, manage billing in one place, and track usage through a unified dashboard.

Myrikko offers developer-friendly pricing with no platform markup on supported models, while intelligent routing and fallbacks help improve reliability when alternative providers are available.

## Step 1. Create an Account

Create a Myrikko account using your email address.

After signing up, verify your email to activate your account.

## Step 2. Get Your API Key

Every new account includes a default API key that you can use immediately.

You can also create a new API key:

1. Go to **Console → Settings → API Keys**.
2. Click **Create API Key**.
3. Copy and store your API key securely.

## Step 3. Configure the Base URL

Configure the base URL for the SDK you are using.

* OpenAI SDK: `https://myrikko.ai/v1`
* Anthropic SDK: `https://myrikko.ai`
* Google GenAI SDK: `https://myrikko.ai`

In most cases, you only need to update your API key, base URL, and model parameter to start sending requests through Myrikko.

## Step 4. Make Your First Request

Myrikko supports multiple popular SDKs, including OpenAI SDK, Anthropic SDK, and Google GenAI SDK.

You can choose the SDK that best matches your existing integration.

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
* Discord: # Welcome to Myrikko

Myrikko provides a unified API for accessing Chinese frontier AI models, including Kimi, GLM, Qwen, DeepSeek, and more.

With one API key and one endpoint, developers can integrate once, switch between models easily, manage billing in one place, and track usage through a unified dashboard.

Myrikko offers developer-friendly pricing with no platform markup on supported models, while intelligent routing and fallbacks help improve reliability when alternative providers are available.

## Step 1. Create an Account

Create a Myrikko account using your email address.

After signing up, verify your email to activate your account.

## Step 2. Get Your API Key

Every new account includes a default API key that you can use immediately.

You can also create a new API key:

1. Go to **Console → Settings → API Keys**.
2. Click **Create API Key**.
3. Copy and store your API key securely.

## Step 3. Configure the Base URL

Configure the base URL for the SDK you are using.

* OpenAI SDK: `https://myrikko.ai/v1`
* Anthropic SDK: `https://myrikko.ai`
* Google GenAI SDK: `https://myrikko.ai`

In most cases, you only need to update your API key, base URL, and model parameter to start sending requests through Myrikko.

## Step 4. Make Your First Request

Myrikko supports multiple popular SDKs, including OpenAI SDK, Anthropic SDK, and Google GenAI SDK.

You can choose the SDK that best matches your existing integration.

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
* Discord: https://discord.gg/pCcmCs3j3

