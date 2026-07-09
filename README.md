# Agent Harness Portfolio

This repository is a public-facing portfolio for Agent Harness and Agent Runtime Infra work.

It is built around three tracks:

1. **Agent Harness**: multi-agent task ownership, memory/history preflight, subagent role split, evidence-based reporting, PASS/BLOCK gates, and failure recovery.
2. **Agent Runtime Infra**: control plane, Host/Carrier, Key/Route, Record/Bind, Runtime Ready, secret handles, gateway/MCP routing, readback, rollback, and orphan cleanup.
3. **Interview Evidence**: failure cases, benchmarks, architecture notes, and weekly writing that turn real engineering work into clear interview stories.

## Projects

- [mini-multi-agent-harness](projects/mini-multi-agent-harness/README.md)
- [agent-sandbox-control-plane](projects/agent-sandbox-control-plane/README.md)

## Writing

The blog is published with GitHub Pages from this repository.

First article:

- [2026-07-09: From Cloud Agent Teams to Agent Harness / Infra](./_posts/2026-07-09-cloud-agent-teams-to-agent-harness-infra.md)

## Operating Principle

The goal is not to show a chatbot demo. The goal is to show how agents can reliably work in real engineering workflows:

- read the right context before acting;
- claim and own tasks;
- use tools with explicit boundaries;
- report evidence instead of vibes;
- separate CI pass, review pass, contract pass, and real runtime smoke;
- recover from stale context and failed handoffs;
- clean up resources and prove orphan count is zero.

