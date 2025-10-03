---
allowed-tools: Bash
description: Task to help local code review on what is okay or needs to be changed.
---

## Context

- Based on the github PR $ARGUMENTS you, in conjunction with zen mcp should do a local code review.

## Your Task
Should to a local code review in conjunction with zen mcp. based on the PR $ARGUMENTS

- give a list on the title of the possible PR's comments. So I can accept or not the comment.
- If the comment is accepted please expand on that one. And create a comment using gh cli to the PR
- Repeat this until the comments in the initial list are over.
