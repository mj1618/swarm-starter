# Swarm

A CLI tool for orchestrating multiple AI coding agents to work on a project plan in parallel.

## Index

1. [Clone this repo](#1-clone-this-repo)
2. [Edit PLAN.md](#2-edit-planmd)
3. [Install the Swarm CLI](#3-install-the-swarm-cli)
4. [Run](#4-run)

## Getting Started

### 1. Clone this repo

```bash
git clone <your-repo-url>
cd <your-repo>
```

### 2. Edit PLAN.md

Define your project plan in `swarm/PLAN.md`. This is the blueprint that the swarm of agents will execute against.

### 3. Install the Swarm CLI

You need one of the supported agent backends installed:

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) CLI (preferred)
- [Cursor](https://cursor.sh) with the `agent` CLI
- [Codex CLI](https://github.com/openai/codex) (OpenAI's coding agent)

<details>
<summary><strong>Download Binary (Recommended)</strong></summary>

Download the latest binary for your platform from the [releases page](https://github.com/mj1618/swarm-cli/releases/latest).

**macOS (Apple Silicon):**

```bash
curl -L https://github.com/mj1618/swarm-cli/releases/latest/download/swarm-cli_darwin_arm64.tar.gz | tar xz -C /tmp
sudo mv /tmp/swarm /usr/local/bin/
```

**macOS (Intel):**

```bash
curl -L https://github.com/mj1618/swarm-cli/releases/latest/download/swarm-cli_darwin_amd64.tar.gz | tar xz -C /tmp
sudo mv /tmp/swarm /usr/local/bin/
```

**Linux (x64):**

```bash
curl -L https://github.com/mj1618/swarm-cli/releases/latest/download/swarm-cli_linux_amd64.tar.gz | tar xz -C /tmp
sudo mv /tmp/swarm /usr/local/bin/
```

**Linux (ARM64):**

```bash
curl -L https://github.com/mj1618/swarm-cli/releases/latest/download/swarm-cli_linux_arm64.tar.gz | tar xz -C /tmp
sudo mv /tmp/swarm /usr/local/bin/
```

</details>

<details>
<summary><strong>Install with Go</strong></summary>

```bash
go install github.com/mj1618/swarm-cli@latest
```

</details>

<details>
<summary><strong>Build from Source</strong></summary>

```bash
git clone https://github.com/mj1618/swarm-cli.git
cd swarm-cli
go build -o swarm .
sudo mv swarm /usr/local/bin/
```

</details>

### 4. Run

```bash
swarm up -d     # kick things off
swarm top       # monitor progress
swarm down      # stop the current pipeline
```
