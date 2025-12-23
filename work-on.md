---
allowed-tools: Bash
description: Get a ticket from Linear and start work
---

## Context

- Using the Linear MCP, get the details for ticket $ARGUMENTS

## Your Task

- Create a branch that includes the ticket ID as part of the name and whether this is
a bug fix, new feature (bug/ticket or feat/ticket)
- Review the information and any related content in the ticket (like GitHub links, Sentry issues).
For GitHub links, use the `gh` CLI tool.
For Sentry, use the Sentry MCP server.
- Ask any questions needed to clarify the request in the ticket.
- Propose a fix. Think about this. Wait for feedback.
- Work on the fix. Consider how we can test this. Manual QA is OK, but unit tests are
preferred. Make sure to call out at the end the steps to manually QA if unit tests are
not possible
- Review the changes using pal. Automatically fix any critical issues
- Run linters and formatters
- Execute any relevant tests - do not execute the whole suite unless absolutely necessary
- Create a commit using conventional commit format
- Create a PR
