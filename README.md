# ChatGPTCommand

ChatGPT Command是一个基于ChatGPT-3.5-API实现的命令行工具。

它可以用来与一个已训练好的语言模型进行人类类似的对话，并且支持多个对话场景的管理。

## 安装

首先你需要安装 Python 3.11.2 或者更高的版本。

如使用V2Ray进行代理的用户请务必升至最新版本以避免requests库的异常

## 使用

### 1. 登录 ChatGPT

在使用 ChatGPT CLI 之前，你需要先在OpenAI的官网上注册并[获取ChatGPT API 的密钥](https://platform.openai.com/account/api-keys) 。

此后，在env/openai_key.json中输入你的密钥

```json
{"api": "Your API Key"}
```

### 1.5. 设置代理（无需代理的可以跳过）

在Source.py中设置自己的代理服务器

```python
os.environ["HTTP_PROXY"] = "代理服务器IP:端口"
os.environ["HTTPS_PROXY"] = "代理服务器IP:端口"
```

### 2. 运行程序

```sh
python Source.py
```

### 3. 创建新实例

项目具有记录对话记录的功能，一个实例代表了聊天的一个主题，你可以根据需要创建多个实例。要创建新的实例，可以在进入程序后输入：

```sh
【实例】new
```

### 3. 进入一个实例

要进行聊天，首先要进入一个实例，可以通过下面的命令进入：

```sh
【实例】<实例的序号>
```

### 4. 对话

进入场景后，你可以开始与 ChatGPT 进行对话，使用下面的命令：

```sh
【<用户名>】<对话内容>
```

对话的效果取决于训练模型的质量和场景的主题，有些场景可能表现更好，而有些场景可能不那么理想。你可以尝试不同的场景并使用不同的问答输入来测试 ChatGPT。

### 5. 退出实例

要退出当前的实例，可以使用下面的命令：

```sh
【<用户名>】quit
```

## 演示
![image](https://github.com/Ancaeus-whisper/ChatGPTCommand/blob/master/%E6%BC%94%E7%A4%BA.gif)

## 贡献

如果你发现了任何问题或者想要为 ChatGPT Command 做出贡献，请前往 Github 上的 [ChatGPTCommand](https://github.com/Ancaeus-whisper/ChatGPTCommand) 项目。
