# chat-cmd
A simple command line chat application using only `bash`

In order to get the pretty output JQ and [rich-cli](https://github.com/Textualize/rich-cli) are required. You can install them using the following commands
```bash
sudo apt install jq
pip install rich-cli
```

## Usage
You can start chatting by running the following command
```bash
./chat-cmd
```
This creates a default context and continues the chat where you last left off. If you want to start a new chat, you can do so by running the following command
```bash
./chat-cmd [chat-context-name]
```
This creates a new context and starts a new chat. The context files are stored in the `~/.chat-cmd` directory.

To use custom **system** message that aligns the chat to your specific need you can run the following command
```bash
./chat-cmd [chat-context-name] [system-message]
```
This creates a new context and starts a new chat with the specified system message.

## Configuration
There are a few configuration options in the script

| Variable            | Description                                                                                                      | Default                           |
|---------------------|------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| `API_URL`           | The URL of the chat API                                                                                          | -                                 |
| `API_KEY`           | The API key for the chat API                                                                                     | -                                 |
| `YOU_NAME`          | The name of the user                                                                                             | You                               |
| `SYSTEM_NAME`       | The name of the system                                                                                           | GPT                               |
| `YOU_COLOR`         | The color of the user's name                                                                                     | $GREEN_COLOR                      |
| `SYSTEM_COLOR`      | The color of the system's name                                                                                   | $RED_COLOR                        |
| `SYSTEM_CMD`        | The default system message, can be overwritten by the user using second command line argument                    | You are a helpful AI assistant... |
| `FILE_NAME`         | The name of the file to store the chat context. Can be overwritten by the user using first command line argument | chat_context                      |
| `CONTEXT_DIR`       | The directory to store the chat context                                                                          | $HOME/.chat-cmd                   |
| `CONTEXT`           | Full path to the chat context file                                                                               | $CONTEXT_DIR/$FILE_NAME           |
| `MAX_TOKENS`        | The maximum number of tokens to send to the chat API                                                             | 800                               |
| `TEMPERATURE`       | The temperature of the chat API                                                                                  | 0.7                               |
| `TOP_P`             | The top p value of the chat API                                                                                  | 0.95                              |
| `FREQUENCY_PENALTY` | The frequency penalty of the chat API                                                                            | 0                                 |
| `PRESENCE_PENALTY`  | The presence penalty of the chat API                                                                             | 0                                 |
| `STOP`              | The stop token of the chat API                                                                                   | null                              |


