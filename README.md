﻿# WhatsAI

Um bot de WhatsApp usando ChatGTP, Dall-E e Stable-Diffusion!

### Uso

- Texto: 
    - chatGPT: `$gpt sua pergunta`
    - GPTroll: `$gptroll sua pergunta` (Manda respostas incorretas e engraçadas)
    - DAN: `$dan sua pergunta` (Quebra a barreira de filtro do ChatGPT)

- Audio: `$gpt-tts sua pergunta` (ChatGPT responde em audio).

- Imagem: 
    - stable-diffusion-2.1: `$stab-diff pedir imagem`
    - Dall-E: `$dall-e pedir imagem` (Adicione "--four" para 4 resultados)
    - Dall-Var: `$dall-var pedir variação de imagem`

- Sticker: `$sticker` (Marque um video/foto ou envie direto no video/foto)

### Instalação

- Somente [***Python 3.9***](https://www.python.org/downloads/release/python-390/) tem suporte para **pytorch CPU/GPU** para geração de imagens localmente. Instale-o ou [***compile o código fonte***](https://github.com/python/cpython/tree/3.9).
- É preciso **Microsoft Visual C++ 14.0** ou mais atualizado para geração de imagens com o stable-diffusion. Para isso, instale o [***Microsoft C++ Build Tools***](https://visualstudio.microsoft.com/visual-cpp-build-tools/). 
- Instale todas as dependencias com `npm i -y`.
- Verifique se o arquivo [***requirements.txt***](https://github.com/wesuRage/WhatsAI/blob/main/requirements.txt) está devidamente configurado para seu sistema. E então execute `pip3 install -r ./requirements.txt`.


- Configure sua [***API Key da OpenAI***](https://beta.openai.com/account/api-keys) para o ChatGPT e o Dall-E no arquivo `.env`:

```s
OPENAI_API_KEY="SUA_API_KEY"
```

- Faça a autenticação com o WhatsApp escaneando o QR Code que aparecerá no terminal.

# Execução

### Compilando o código
- Primeiro rode `npm run build`
- E então execute o código com `npm start`

### Execução para testes
- Execute o código com `npm run dev`
- Dê uma olhada nos scripts do `package.json` para testes isolados ou debugs

### Restart

Em produção, você pode e **deve** resetar o bot após um período de tempo para previnir um bug do Baileys parar de detectar novas mensagens. Para isso, descomente a [***linha 436***](https://github.com/wesuRage/WhatsAI/blob/81a99b9ac12071d90ba93ff973e75aedc3593c22/src/bot.ts#L436) no arquivo `src/bot.ts`.

> ### Em erros de conexão com o WhatsApp
> *Você talvez tenha que rodar o código duas vezes, já que aparentemente tem um bug na dependencia do Baileys. Então para isso siga os passos:*

> - Escaneie o QR Code e espere até a tela de scan fechar.
> - Pare a execução no terminal com `Ctrl + C`
> - Execute o código de novo.
