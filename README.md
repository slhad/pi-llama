# pi-llama

llama.cpp Pi extension. Auto-discovers models from a running `llama-server` and
registers them as the `llama-cpp` provider in pi.

## Install

**From the shell:**

```bash
pi install https://github.com/huggingface/pi-llama
```

This clones to `~/.pi/agent/packages/pi-llama/` and adds an entry to your pi
settings. Every future `pi` invocation auto-loads it.

**From inside an interactive pi session:**

```
!pi install https://github.com/huggingface/pi-llama
```

Then run `/reload` (or restart pi) to load the extension.

**Dev mode:**

```bash
git clone https://github.com/huggingface/pi-llama ~/code/pi-llama
pi -e ~/code/pi-llama/index.ts
```

`-e` loads the extension only for the current session, useful while
developing.

## Usage

```bash
# 1. Install llama-server
curl -LsSf https://llama.app/install.sh | bash

# 2. Start it
llama-server

# 3. Launch pi
pi

# 4. Inside pi
/model              # pick llama-cpp/<id>
```
