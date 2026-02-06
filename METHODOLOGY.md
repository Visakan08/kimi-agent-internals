# Methodology

This analysis was conducted through plain-English conversation with Kimi's
publicly accessible agent interfaces. No code was written by the researcher.
No authentication was bypassed. No adversarial or injection prompts were used.

---

## AI Disclosure

This research was conducted with assistance from
[Claude Code](https://docs.anthropic.com/en/docs/claude-code) for
organizing, analyzing, and documenting the findings. The extraction
itself was performed entirely through conversation with Kimi.

## How the Extraction Worked

I asked Kimi questions in natural language, across multiple conversational
sessions, using the standard chat interface at kimi.com/agent (OK Computer).

I asked things like "what files are in your environment?" and "can you show me
the contents of your Python source code?" The agent decided, autonomously, to
run shell commands and Python code to answer my questions. It then returned
the results in its responses.

I did not write `os.listdir()` or `open()` calls. The agent chose those
methods itself to fulfill my plain-English requests. Every piece of information
in this repository was provided by the agent through its standard conversational
interface, then exported through the agent's own file-output capabilities.

This is a meaningful distinction. I did not execute technical extraction
commands. I asked an AI assistant questions about itself, and it answered them.

---

## What Interfaces Were Used

- **kimi.com/agent** (OK Computer) — The primary interface. This mode gives
  the agent shell access, Python execution, and a persistent filesystem.
  These are advertised, documented capabilities available to all users.

- **kimi.com/chat** (Base Chat) — Used for comparison and to extract the
  Base Chat system prompt.

- **kimi.com/docs**, **kimi.com/sheets**, **kimi.com/slides**,
  **kimi.com/websites** — Used to extract specialized agent prompts by
  asking each agent to describe its own instructions.

All interfaces are publicly accessible. No paid tier or special access was
required.

---

## What Was Not Done

- No prompt injection or jailbreak techniques were used
- No authentication was bypassed or credentials misused
- No binaries were decompiled
- No adversarial prompts were crafted to circumvent safety measures
- No other users' sessions or data were accessed
- No backend infrastructure outside the container was probed
- No code was written by the researcher — all commands were chosen and
  executed by the agent itself

---

## The Agent's Role

This point deserves emphasis: the Kimi agent has full shell and Python
access by design. When asked about its own environment, it uses those
capabilities to inspect and report on its own files. It is designed to do
this. The agent read its own source code, formatted it, and provided it
in response to conversational requests.

The agent also exported files through its standard output mechanisms. I
did not intercept, scrape, or extract data through any channel other than
the agent's own responses and file exports.

---

## Reproducibility

Anyone with access to Kimi OK Computer (kimi.com/agent) can reproduce
these findings by asking the agent about its environment in plain English.
The agent will use its built-in capabilities to inspect and report on its
own files.

---

## Limitations

This is a point-in-time snapshot from February 2026. The system may change.
Container isolation limits visibility into host and backend infrastructure.
Some binaries were not analyzed due to scope and legal considerations.
The analysis covers what the agent was willing to share through standard
conversation.

---
