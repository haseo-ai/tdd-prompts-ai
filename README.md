# TDD Prompts for AI Agents

[English](README.md) | [한국어](README.ko.md)

> Prompts That Dramatically Reduce AI Rework: Test-Driven Development for AI coding agents.

![TDD Prompts for AI](assets/1000576710.jpg)

---

## What Is This?

A collection of battle-tested prompts for applying **Test-Driven Development (TDD)** with AI coding agents (Claude, GPT, Gemini, Codex, etc.).

**The core idea:** TDD embeds long-term memory directly into your source code — so when your AI agent loses context, the tests remember what the code is supposed to do.

> *Long-term memory for planning → Markdown files*
> *Long-term memory for development → TDD*

---

## Why TDD for AI?

Humans struggle with TDD because MVP deadlines feel urgent. AI agents have the same time pressure — but unlike humans, they **can actually handle the workload**.

TDD doesn't shine during MVP development. It shines:

- **During real service operation** — catching bugs before your users do
- **During agent handoff** — when you switch from one AI agent to another, tests serve as the specification
- **When context windows reset** — tests persist where session memory doesn't

---

## TDD vs. Harness Pattern

| | Harness | TDD |
|---|---|---|
| Purpose | Build MVP fast | Ensure long-term code quality |
| QA | Included | Separate, after tests pass |
| When to apply | First (MVP phase) | After MVP is stable |
| Scope | New features | Entire codebase refactor |

They can be used together, but it's wise to apply them **separately** — build with Harness first, then harden with TDD.

---

## Prompts

### 1. Start TDD

```
"Are we actually doing Test-Driven Development (TDD) right now?"
```

> **Note:** TDD assumes a terminal/CLI environment. If you apply TDD to UI/Frontend work, it can reduce design creativity — choose whether to include it.
>
> Example: *(continuing the same prompt)* "But exclude the frontend from TDD."

### 2. Full-Scope TDD

```
"Refactor the entire project using Test-Driven Development (TDD)."
```

> The main agent tends to minimize its workload to reduce token usage. Unless you say "entire project," it will only apply TDD to new tasks.
>
> **Note:** If this is a team project or open-source contribution, specify which folders must not be touched.
>
> Example: *(continuing the same prompt)* "But never touch OOO, and limit changes to OOO. This rule applies only to this project, so don't store it in the global workspace memory — keep it only in the project's internal memory."

### 3. Uninterrupted Multi-Agent

```
"Proceed through Phase 1 to Phase 10 without interruption.
If a sub-agent times out, retry up to three times.
If it still fails, the main agent should handle only that sprint and then move on."
```

> "Phase 1–10" is just an example — adjust according to what the main agent defines.

### 4. Progress Check (Careful!)

```
"Is everything going smoothly?"
```

> ⚠️ **Do NOT say "Check the progress."** The keyword "check" makes the agent interpret it as a **new task**, causing it to abandon the original work entirely.

### 5. Verify Tests

```
"Run the tests yourself and verify the results."
```

> Even after finishing TDD, the main agent often won't run the test suite and will just hand it back to you.

### 6. QA & Code Review

```
"Do QA and code review."
```

> Say this **only after the entire test suite passes safely**. During TDD, the agent may have broken the original spec or discovered hidden issues.
>
> ⚠️ **Warning:** If the tests are not stable yet, do NOT say this. Fix the tests manually first. Otherwise, the agent will repeatedly try to fix things that were never working and may end up damaging the entire codebase.

---

## TDD in the AI Era

TDD is a development methodology where AI catches errors at **build time** (source code level) — before **runtime** (when users encounter them). The formal definition of TDD is different, but in the AI era, this interpretation works.

If you've been relying on markdown files for long-term memory because session memory disappears, TDD becomes a way to embed long-term memory directly into the source code.

---

## Summary

> **Planning memory → Markdown files**
> **Development memory → TDD**
