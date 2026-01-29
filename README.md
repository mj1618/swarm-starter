# Swarm Demo

This shows you how to setup your own zero-shot project using swarm-cli.

## Index

- [Prereqs](#prereqs)
- [Instructions](#instructions)
  - [Create the plan](#create-the-plan)
  - [Optionally update AGENTS.md](#optionally-update-agentsmd)
  - [Kick off the planner and coder](#kick-off-the-planner-and-coder)

## Prereqs

1. Install either [Cursor Agent CLI](https://cursor.com/docs/cli/overview) or [Claude Code CLI](https://code.claude.com/docs/en/setup) (and buy some tokens)
2. Install [swarm-cli](https://github.com/mj1618/swarm-cli)
3. Create your own [convex.dev](https://www.convex.dev/login) account (if you use the tech-stack defaults)
4. Set the swarm-cli to your particular agent (default is claude code). E.g. `swarm config set-backend cursor -g`

## Instructions

### Create the plan

First start by editing `swarm/PLAN.md` with your own project plan. 
Optionally change the tech stack to your desired stack here also.

### Optionally update AGENTS.md

AGENTS.md provides instructions to every agent that runs in your project.
This can include some code guidelines, or how to use common tools.
Leave this as-is if you choose to use the default tech-stack, write your own or you can leave this completely blank if you like.

### Kick off the planner and coder

Run `swarm up -d` and it will use `swarm/swarm.yaml` to kick off the desired ralph loops.
By default there is a planner loop (uses `swarm/prompts/planner.md` for each loop) and a coder loop (uses `swarm/prompts/coder.md` for each loop).

Keep an eye on the loops using the following commands:
```bash
swarm ls
swarm inspect planner
swarm tail -f planner
swarm down
```

A complete list of commands is found at [swarm-cli](https://github.com/mj1618/swarm-cli)