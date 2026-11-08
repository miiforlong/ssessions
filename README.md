# Server Sessions

Simple terminal UI for managing TMUX sessions and profiles.

## Program dependencies
- Bash
- Tmux
- OpenSSH client (`scp`)

## Install dependencies
```bash
sudo apt update && sudo apt install -y tmux openssh-client
```

## Installation
```bash
mkdir -p ~/.local/bin
nano ~/.local/bin/ssessions
chmod +x ~/.local/bin/ssessions
```

Paste the `ssessions` script into the file, then launch it:

```bash
ssessions
```

## Features
- Create, list, attach to, and kill TMUX sessions
- Create and manage profiles
- Automatically change directories when starting a profile
- Execute commands when starting a profile
- Upload and download files using SCP
- Edit configuration directly from the terminal
- Minimal interactive terminal interface

## Configuration
Configure your SSH connection and transfer directories through the application's configuration menu.

## Usage
```bash
ssessions          # Open the interactive menu
ssessions list     # List TMUX sessions
ssessions create   # Create a session
ssessions profiles # List profiles
ssessions config   # Edit configuration
ssessions help     # Show help
```

**Note:** TMUX sessions run on the machine where `ssessions` is executed. For remote session management, connect to your server over SSH first.

## Common issues 

the most common issue is that local/bin is not in the PATH.

To fix it : 

```shell
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```
