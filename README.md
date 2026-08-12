# Legatus AI
*AI-powered risk auditor for legacy Java modernization.*

---
## What it is:
An AI agent with read-only access to Java/Spring codebases that automatically scans a repository and produces a risk-scored modernization report — surfacing deprecated dependencies, architectural smells, security vulnerabilities, and migration complexity, without a human having to manually read every file.

## The problem it solves:
Enterprises sit on large, aging Java/Spring codebases where nobody has full visibility into modernization risk. Figuring out "what's safe to touch, what's dangerous, what needs updating first" today means a senior engineer manually reading through thousands of files — slow, inconsistent, and rarely done proactively. This agent automates that first-pass audit, turning weeks of manual review into a structured, explainable report a team can act on.

## How it works (grows phase by phase across this roadmap):
Understands the codebase — indexes the repo using retrieval (RAG), so it can pull relevant code context instead of trying to stuff an entire repo into one prompt.
Plans and acts autonomously — an agent decides which files/modules matter, retrieves relevant context, calls tools (dependency/vulnerability checks), and synthesizes findings across multiple steps rather than a single LLM call.
Remembers across the run — carries findings from earlier modules forward (e.g., a deprecated library flagged in one class propagates as a known issue to downstream classes using it).
Produces a structured, risk-scored report — deprecated dependencies, architectural smells, security risks, migration complexity — each with a confidence/severity rating and reasoning, not just a raw dump.
Runs safely on someone else's code — read-only access, guardrails against prompt injection via malicious code comments, least-privilege tool access, audit logging.
Is evaluated, not just demoed — a golden set of known-risk code samples with automated scoring, so the report's reliability is measurable, not anecdotal.

## Why this project specifically:
Leverages 11 years of real Java/Spring depth — this isn't a toy domain learned from scratch, it's applying deep existing expertise to a new engineering discipline.
Genuinely useful and potentially sellable, not just a resume artifact.
Naturally forces every core AI engineering skill in sequence: RAG, agentic orchestration, memory, evaluation, and production-grade deployment — each phase of the roadmap adds a real, working slice to this one system.
