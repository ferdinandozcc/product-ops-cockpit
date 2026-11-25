# Product Ops Cockpit

An interactive prototype of a product-operations "operating system": one place to run a product portfolio end to end, with an AI agent layer on top.

**Live demo:** https://ferdinandozcc.github.io/product-ops-cockpit/
*(the demo UI is in Spanish; sample data only)*

## The idea

Most product-ops tooling is a pile of disconnected trackers. This cockpit takes the opposite approach: **model the domain once, and let every view, metric and agent read from the same source.** Add a project or a line of business and nothing in the code changes.

## What it does

- **Scorecard** that computes itself from project state (scope checkpoints, pre-launch readiness, contrasted results, backlog health, open requests, onboarding).
- **Portfolio radar** that flags stalled work and at-risk dependencies.
- **Stage-gates with guards** a project only advances when scope fits the appetite and its metric has a baseline.
- **Backlog grooming** every candidate held to five fields before it's "ready".
- **Request queue** classify and close the loop so nothing sits unanswered.
- **Board update** drafted automatically from the live state of the portfolio.
- **Data sources** each module mapped to the tool it would read from (Linear, PostHog, Slack, etc.), with mock/connected toggles.
- **Agent layer** agents that propose and flag with evidence while the human approves, each carrying its own eval.

Four scenarios (calm week, crisis, launch, onboarding) and a "simulate the week" button show how the cockpit reacts as state changes.

## How it's built

A single self-contained HTML file. No build step, no dependencies, no external calls. The domain model (projects, owners, requests, backlog candidates, onboardings) and two state machines drive everything the scorecard shows, so the metrics are correct by construction.

## Honest scope

This is a **prototype with sample data**. The agents in the published demo are deterministic; the real ones run locally against an API. It exists to show the operating model and the context-first approach to AI, not as a production tool.

## Run it locally

Open `index.html` in any browser. That's it.
