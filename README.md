# Agent Sandbox

Agent Sandbox is a way to run AI Agents inside a MicroVM.

## Features:

* Uses podman and krun
* Uses squid in a container to control what the container can access
* Supports opencode with Anthropic and Claude Code right now
  * Uses [meridian](https://github.com/rynfar/meridian) and 
  [opencode-with-claude](https://github.com/ianjwhite99/opencode-with-claude)
* Configurable sandbox home directory (~/.local/share/agent-sandbox/homes/$sandbox_name), -H overrides the default
* Configurable proxy (~/.config/agent-sandbox/squid.conf)

## Usage:

* `agent -s` : open a shell in the sandbox. opencode and claude can be run from there
* `agent -o` : run opencode in the sandbox
* `agent -c` : run claude code in the 
* `agent -n foo -c`: run claude code in a sandbox named foo
* `agent -H ~/foo -n foo`: run claude code in sandbox named foo with its home directory as ~/foo

## Roadmap

* Support more agents
* Support more endpoints with opencode
* Make container somewhat configurable
