# OpenAI Realtime API Client for Python

This is an experimental OpenAI Realtime API client for Python and LlamaIndex. It integrates with LlamaIndex's tools, allowing you to quickly build custom voice assistants.

Include two examples that run directly in the terminal -- using both manual and Server VAD mode (i.e. allowing you to interrupt the chatbot).

## Installation

Install system deps:

```bash
brew install ffmpeg
```

Install python deps:

```bash
# 方法1：直接安装包，测试ok，但是有一个问题是，用的是gpt-4o-realtime-preview-2024-10-01，比较贵。
pip install openai-realtime-client

# 方法2
# Optional: clone the repo and run the examples locally
git clone https://github.com/run-llama/openai_realtime_client.git
cd openai_realtime_client

# 修改使用model

# 执行本地安装
pip install .


```

Set your openai key:

```bash
export OPENAI_API_KEY="sk-..."
```

## Usage

Assuming you installed and cloned the repo (or copy-pasted the examples), you can immediately run the examples.

Run the interactive CLI with manual VAD (try asking for your phone number to see function calling in action):

```bash
python ./examples/manual_cli.py

# 控制台返回
Starting Realtime API CLI...
This process is not trusted! Input event monitoring will not be possible until it is added to accessibility clients.
Connected to OpenAI Realtime API!
Commands:
- Type your message and press Enter to send text
- Press 'r' to start recording audio
- Press 'space' to stop recording
- Press 'q' to quit

```

Or to use streaming mode (which allows you to interrupt the chatbot):
这个demo跑通
```bash
python ./examples/streaming_cli.py

# 控制台返回
Starting Realtime API CLI with Server VAD...
This process is not trusted! Input event monitoring will not be possible until it is added to accessibility clients.
Connected to OpenAI Realtime API!
Audio streaming will start automatically.
Press 'q' to quit


Streaming audio... Press 'q' to stop.

[Speech detected

[Speech ended]

[Speech detected

[Speech ended]


```

**NOTE:** Streaming mode can be a little janky, best to use headphones in a quiet environment.

Take a look at the examples, add your own tools, and build something amazing!
