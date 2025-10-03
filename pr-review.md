---
allowed-tools: Bash
description: Get the PR number and check the ones that have the address the thumbs up emoji reactions for unresolved comments
---

## Context

- Using the `gh` CLI tool to address the thumbs up emoji reactions for Unresolve conversations for the PR: $ARGUMENTS

## Your Task
For GitHub links, use the `gh` CLI tool.

-  Ask any questions needed to clarify the requests for the previously Unresolve conversations.
-  Propose a fixes as a list to approach these comments in the PR.
   - Think about this. Wait for feedback.
- Review the changes using zen. Automatically fix any critical issues
- Run linters and formatters
- Run pre-commit run --all-files and only take the files in the PR. the other revert if needed.
- Execute any relevant tests - do not execute the whole suite unless absolutely necessary
- Create a commit for each of the comments in the PR using conventional commit format.
  - ask me about the commit before doing it.
