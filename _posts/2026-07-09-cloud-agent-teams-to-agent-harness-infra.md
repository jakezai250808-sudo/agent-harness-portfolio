---
layout: post
title: "From Cloud Agent Teams to Agent Harness / Infra"
date: 2026-07-09
categories: [agent-harness, agent-infra, portfolio]
---

Today I started turning the Cloud Agent Teams work into a public Agent Harness / Agent Runtime Infra portfolio.

The key realization is simple: making agents useful is not just about prompting a model. A real agent system needs governance, runtime infrastructure, evidence, recovery, and a way to prove that work actually happened.

## The Problem

Most agent demos stop at a happy path:

1. a user gives a task;
2. an agent calls a tool;
3. the demo shows a successful output.

That is not enough for engineering work.

In a real team, agents need to handle long-running tasks, changing context, incomplete handoffs, review gates, secrets, runtime state, failed deployments, and cleanup. They also need to explain what is covered and what is not covered.

This is where Agent Harness and Agent Runtime Infra meet.

## Harness Layer

The Harness layer is about agent behavior and coordination.

In Cloud Agent Teams, the most important mechanisms are:

- task ownership and claim-before-work;
- thread-level execution context;
- memory/history preflight before reporting;
- subagent role split;
- PASS/BLOCK review language;
- fresh readback instead of stale assumptions;
- explicit boundaries for what was not tested;
- owner-facing summaries that can be checked.

This is different from a normal chat wrapper. The hard part is not producing text. The hard part is making agents behave like reliable teammates across long workflows.

## Runtime Infra Layer

The Runtime Infra layer is about making agents actually run.

The useful decomposition is:

- Host / Carrier;
- Key / Route;
- Record / Bind;
- Lifecycle;
- Runtime Ready;
- readback;
- rollback;
- orphan cleanup.

For an agent creation workflow, "created" should not mean a row exists in a database. It should mean the agent is visible, has the correct runtime binding, can use the expected model route, can be stopped and started, can be deleted, and leaves no orphaned resources.

That is why create -> visible -> delete -> orphan=0 is a stronger standard than a green unit test.

## Why This Matters for Interviews

For Agent Harness roles, the story is:

> I work on making agents reliable in multi-step engineering workflows: context preflight, task ownership, subagent coordination, evidence-based reporting, review gates, and failure recovery.

For Agent Infra roles, the story is:

> I work on the control plane and runtime path that lets agents run safely: carrier, route, secret handle, lifecycle, readback, rollback, and cleanup.

The strongest position is the intersection:

> I understand both how agents should behave and what infrastructure they need in order to work reliably.

## What I Will Build Publicly

This portfolio will grow through two public projects.

### mini-multi-agent-harness

A minimal harness that demonstrates:

- planner / executor / reviewer roles;
- memory preflight;
- task ownership;
- tool call logs;
- PASS/BLOCK reports;
- fake-green detection;
- recovery after stale context.

### agent-sandbox-control-plane

A minimal control-plane demo that demonstrates:

- create / readback / stop / start / delete lifecycle;
- host / carrier abstraction;
- key / route binding;
- secret handle pattern;
- runtime-ready check;
- cleanup and orphan detection.

## The Publishing Loop

The portfolio will not wait until everything is perfect.

The weekly loop is:

1. ship one small project update;
2. publish one failure case;
3. update one benchmark or evidence table;
4. write one short public note;
5. turn one interview question into a project-backed answer.

The point is to show iteration, not just a final polished artifact.

## First Failure Cases to Write

The first public failure cases should come from real agent teamwork:

- an agent reports from stale context because it did not reread the thread;
- CI is green but real runtime smoke is not covered;
- a review stamp is not fresh for the current head;
- a secret or route appears configured but runtime readback proves it is missing;
- task ownership is unclear and multiple agents duplicate work.

These cases are valuable because they explain why a Harness exists.

## Next Step

The next concrete step is to turn this repository into a working evidence base:

- add architecture diagrams;
- add the first benchmark table;
- add three failure cases;
- build the smallest runnable harness demo;
- build the smallest runtime control-plane demo.

The goal is not just to learn these words. The goal is to make them explainable through real artifacts.

