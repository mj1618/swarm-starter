# Swarm

A CLI tool for orchestrating multiple AI coding agents to work on a project plan in parallel.

## Index

1. [Clone this repo](#1-clone-this-repo)
2. [Edit PLAN.md and CLAUDE.md](#2-edit-planmd-and-claudemd)
3. [Install the Swarm CLI](#3-install-the-swarm-cli)
4. [Run](#4-run)

## Getting Started

### 1. Clone this repo

```bash
git clone <your-repo-url>
cd <your-repo>
```

### 2. Edit PLAN.md and CLAUDE.md

Define your project plan in `swarm/PLAN.md`. This is the blueprint that the swarm of agents will execute against.

Update `CLAUDE.md` with any project-specific instructions, conventions, or context that the agents should follow.

### 3. Install the Swarm CLI

Note that you will need one of the Claude, Cursor or Codex CLI's installed before proceeding.
Install the swarm CLI to have swarm available on the command line:

<details>
<summary><strong>Option A: Download Binary (Recommended)</strong></summary>

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

**Windows (x64):**

```powershell
Invoke-WebRequest -Uri https://github.com/mj1618/swarm-cli/releases/latest/download/swarm-cli_windows_amd64.zip -OutFile swarm-cli.zip
Expand-Archive swarm-cli.zip -DestinationPath "$env:LOCALAPPDATA\swarm-cli"
Rename-Item "$env:LOCALAPPDATA\swarm-cli\swarm-cli.exe" "swarm.exe"
# Add to PATH (run once):
[Environment]::SetEnvironmentVariable("Path", "$env:Path;$env:LOCALAPPDATA\swarm-cli", "User")
```

**Windows (ARM64):**

```powershell
Invoke-WebRequest -Uri https://github.com/mj1618/swarm-cli/releases/latest/download/swarm-cli_windows_arm64.zip -OutFile swarm-cli.zip
Expand-Archive swarm-cli.zip -DestinationPath "$env:LOCALAPPDATA\swarm-cli"
Rename-Item "$env:LOCALAPPDATA\swarm-cli\swarm-cli.exe" "swarm.exe"
# Add to PATH (run once):
[Environment]::SetEnvironmentVariable("Path", "$env:Path;$env:LOCALAPPDATA\swarm-cli", "User")
```

</details>

<details>
<summary><strong>Option B: Install with Go</strong></summary>

```bash
go install github.com/mj1618/swarm-cli@latest
```

</details>

<details>
<summary><strong>Option C: Build from Source</strong></summary>

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
