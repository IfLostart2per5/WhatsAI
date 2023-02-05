# WhatsAI

A ChatGPT and Midjourney-Diffusion WhatsApp Bot.

### Usage

- Text: `$gpt your query`
- Audio: `$gpt-tts your query` (Default to portuguese. Change in the code).
- Image: `$mid-diff your query`
- Singer: `$sing your query` (Default query order is exactly: **artist**/**song**)

### Instalation

- Only [***Python 3.9***](https://www.python.org/downloads/release/python-390/) supports **pytorch's CPU/GPU** for image generation. Install it or [***build from source***](https://github.com/python/cpython/tree/3.9).
- **Microsoft Visual C++ 14.0** or greater is required for image generation. Get it with [***Microsoft C++ Build Tools***](https://visualstudio.microsoft.com/visual-cpp-build-tools/). 
- Install all dependencies with `npm i -y`.
- Check if [***requirements.txt***](https://github.com/wesuRage/WhatsAI/blob/main/requirements.txt) is properly configured for your system. Then run `pip3 install -r ./requirements.txt`.


- Creat a `.env` file and set your [***OpenAI API Key***](https://beta.openai.com/account/api-keys) for chatGPT like this:

```s
OPENAI_API_KEY="YOUR_API_KEY"
```

- Authenticate with your WhatsApp by scanning the QR Code that will show up in the terminal.

# The app

### Building the code
- First run `npm run build`
- Then run the app with `npm start`

### Running for tests
- Run the app with `npm run dev`
- Check the scripts section on `package.json` for single test or help

### Restart

On production, you can and **should** restart the app after a period of time to prevent a bug of Baileys stop detecting new messages. Do it by uncommenting [***line 117***](https://github.com/wesuRage/WhatsAI/blob/6458aa9aab667c154fe29bd9b56e0fc7a7422ca8/src/bot.ts#L117) on the main `bot.ts` file at `src/`.

> ### On mobile connection error
> *You may have to run the app twice, since there is a sort of bug on the Baileys dependency. So follow this steps if this is the case:*

> - Scan the QR Code and wait until the scan screen closes
> - Stop the app on the terminal with `Ctrl + C`
> - Run the app again
