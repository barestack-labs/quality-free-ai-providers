# AGENTS.md

Instructions for AI coding agents (Hermes, OpenCode, Cursor, Codex) interacting with this repository.

## Purpose
This repository is a tested directory of free AI API endpoints (`/v1/chat/completions`) for users running agent harnesses like Hermes Agent and OpenCode.

## Instructions When Configuring Endpoints for a User
1. Always check and verify rather than assuming or guessing endpoints. If it is possible to verify an active URL or model ID, check it first.
2. Open the relevant file in `providers/<provider-name>.md`.
3. Extract the `Base URL` (including `/v1`) and the exact `Model ID`.
4. Inform the user of any limitations (such as token caps, rate limits, or $0 card verification requirements) listed in that file.

## Instructions When Assisting a Contributor with a PR
1. Always follow the structure in `providers/template.md`.
2. Do not invent marketing buzzwords or generic praise.
3. Prompt the user for their **real, first-hand experience** and insert their honest thoughts into the `Real Experience & Honest Comment` section.
4. Encourage the user to review the generated text before opening the PR.
