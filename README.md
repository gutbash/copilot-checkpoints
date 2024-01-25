# twinny

<br>

Are you fed up of all of those so called "free" Copilot alternatives with paywalls and signups?  Fear not my developer friend!  Twinny is the most no-nonsense locally hosted (or api hosted) AI code completion plugin for vscode designed to work seamlessly with [Ollama](https://github.com/jmorganca/ollama) or [llama.cpp](https://github.com/ggerganov/llama.cpp). Like Github Copilot but 100% free and 100% private.

<br>

<div align="center">
    <p>
      Install the twinny vscode extension
    </p>
    <a href="https://marketplace.visualstudio.com/items?itemName=rjmacarthy.twinny">
      <img src="https://code.visualstudio.com/assets/images/code-stable.png" height="50" />
    </a>
</div>


## 🚀 Getting Started

### Easy Installation

You can install the verified extension at [this link](https://marketplace.visualstudio.com/items?itemName=rjmacarthy.twinny) or find the extension in the extensions section of Visual Studio Code marketplace.

Twinny is configured to use Ollama by deafult. Therefore, when installing the twinny extension in Visual Studio Code, it will automatically prompt and guide you through the installation of Ollama using two default small models `codellama:7b-instruct` for chat and `codellama:7b-code` for "fill in the middle" completions. 

If you already have Ollama installed or you want to use llama.cpp instead, you can cancel the automatic setup of Ollama and proceed to update the values inside twinny extension settings to point to your existing models and server.

You can find the settings inside the extension sidebar by clicking the gear icon inside the twinny sidebar or by searching for `twinny` in the extensions search bar.

The main values which need to be updated to switch between Ollama and llama.cpp are:

- `apiUrl` - The url to your Ollama or llama.cpp server (default: localhost)
- `apiPath` - The API path which defaults to `/api/generate` for Ollama and `/completion` for llama.cpp (See llama.cpp docs or Ollama docs).
- `apiPort` - The port of your Ollama (default 11434) or llama.cpp server (default 8080)

If you are using llama.cpp the settings for fim model name and chat model name will be ignored as this should already be configured when running the llama.cpp server.

When the extension is running and the extension is ready you will see a `🤖` icon at the bottom of your code editor which indicates which models are running.

That's it! Enjoy enhanced code completions and chat with twinny! 🎉

## 🤖 Features

- Free
- Private
- Auto code completion
- Fast and accurate
- Multiple language support
- Easy to install
- Configurable endpoint and port and path for completion API
- Chat feature like Copilot Chat
- View diff for code completions
- Accept solution directly to editor
- Copy generated code solution blocks
- Chat history preserved per conversation

Completion:

![twinny](https://github.com/rjmacarthy/twinny/assets/5537428/95a1d8d5-f2fb-47b3-b246-23ff822464c3)

Chat:

<img src="https://github.com/rjmacarthy/twinny/assets/5537428/679bd283-28e9-47ff-9165-84dfe293c56a" width="760"/>


## Tested ans supported Ollama models

- codellama `instruct` for chat and `code` for FIM. (https://ollama.ai/library/codellama)
- phind-codellama for chat (https://ollama.ai/library/phind-codellama)

For FIM - The model must support the llama or deepseek special tokens for prefix and suffix.
For chat - All llama models should work, although any model will probably work too, results may vary if the special tokens are different from Llama.

## Tested and supported Llama CPP models

- twinny and [llama.cpp](https://github.com/ggerganov/llama.cpp) has been tested and is working with the following model: https://huggingface.co/TheBloke/CodeLlama-7B-GGUF

For FIM - The model must support the llama or deepseek special tokens for prefix and suffix.
For chat - All llama models should work, although any model will probably work too, results may vary if the special tokens are different from Llama.

Contributions are welcome please open an issue describing your changes and open a pull request when ready.

This project is under MIT licence, please read the [LICENSE](https://github.com/rjmacarthy/twinny/blob/master/LICENSE) file for more information.

## Known issues

- If the server settings are incorrectly set chat and fim completion will not work, if this is the case please open an issue with your error message.
- Some modles may not support the special tokens of llama or deepseek which means they would not work correctly for FIM completions.
- Sometimes a restart of vscode is required for new settings to take effect.
  
If you have a suggestion for improvement please open an issue and I will do my best to make it happen!
