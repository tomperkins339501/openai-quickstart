# openai-quickstart

OpenAI API quickstart project using Node.js and the OpenAI SDK.

## Prerequisites

- [Node.js](https://nodejs.org/) v18 or higher
- An [OpenAI API key](https://platform.openai.com/api-keys)

## Setup

### 1. Clone the repository

```powershell
git clone https://github.com/tomperkins339501/openai-quickstart.git
cd openai-quickstart
```

### 2. Set your OpenAI API key (Windows PowerShell)

```powershell
setx OPENAI_API_KEY "your_api_key_here"
```

> Restart PowerShell after running this command for the variable to take effect.

### 3. Install dependencies

```powershell
npm install
```

### 4. Run the example

```powershell
node example.mjs
```

Or use the npm script:

```powershell
npm start
```

## What it does

The `example.mjs` file sends a prompt to the OpenAI API and prints the response to the console:

```js
import OpenAI from "openai";

const client = new OpenAI();

const response = await client.responses.create({
  model: "gpt-4o",
  input: "Write a one-sentence bedtime story about a unicorn."
});

console.log(response.output_text);
```

## Resources

- [OpenAI Developer Docs](https://developers.openai.com/api/docs/quickstart)
- [OpenAI Node.js SDK on GitHub](https://github.com/openai/openai-node)
