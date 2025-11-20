+++
date = '2025-11-20T00:00:00Z'
title = 'SEPs Are Moving to Pull Requests'
author = 'David Soria Parra (Lead Maintainer)'
tags = ['announcement', 'governance', 'community', 'sep']
+++

We're updating how Specification Enhancement Proposals (SEPs) are submitted and managed. Starting today, SEPs will be created as pull requests to the [`seps/` directory](https://github.com/modelcontextprotocol/specification/tree/main/seps) instead of GitHub issues.

## Why the Change?

When we introduced SEPs back in July, we chose GitHub issues as our starting point. Issues are familiar, low-friction, and got us up and running quickly. But as more proposals have come through the process, we've identified a few pain points:

**Scattered discussions.** With issues, the proposal text lives in the issue body while implementation details often end up in a separate PR. This splits the conversation and makes it harder to follow the full history of a proposal.

**No version history.** Issues don't have the same revision tracking that files in a repository do. When a SEP evolves through review, it's difficult to see what changed and when.

The new PR-based approach, inspired by [Python's PEP process](https://peps.python.org/), addresses all three.

## How It Works

The new workflow is straightforward:

1. **Draft your SEP** as a markdown file named `0000-your-feature.md` using the [SEP template](https://github.com/modelcontextprotocol/specification/blob/main/seps/README.md#sep-file-structure)

2. **Create a pull request** adding your SEP to the `seps/` directory

3. **Update the SEP number** by amending your commit to rename the file using the PR number (e.g., PR #1850 becomes `1850-your-feature.md`)

4. **Find a sponsor** from our [maintainer list](https://github.com/modelcontextprotocol/modelcontextprotocol/blob/main/MAINTAINERS.md) to shepherd your proposal

5. **Iterate** on feedback directly in the PR

That's it. The PR number becomes the SEP number, discussion happens in one place, and git tracks every revision.

## What About Status?

One notable change: **sponsors are now responsible for updating SEP status**. In addition to applying labels to the pull request, the sponsor updates the `Status` field directly in the SEP markdown file. This keeps the canonical state of the proposal in the file itself, versioned alongside the content, while PR labels make it easy to filter and find SEPs by status.

Status transitions work the same as before: `Draft` to `In-Review` to `Accepted` to `Final`, with the sponsor managing each transition as the proposal progresses.

## Existing SEPs

If you have an open SEP as a GitHub issue, don't worry. Existing proposals can continue through their current workflow. However, we encourage new proposals to use the PR-based process going forward. We are moving all implemented SEPs
into this new structure.

## Getting Started

Ready to propose a change to MCP? Here's what you need:

- Read the updated [SEP Guidelines](https://modelcontextprotocol.io/community/sep-guidelines)
- Check out the [SEP template](https://github.com/modelcontextprotocol/specification/blob/main/seps/README.md#sep-file-structure)
- Browse existing SEPs in the [`seps/` directory](https://github.com/modelcontextprotocol/specification/tree/main/seps) for examples

As always, if you're unsure whether your idea warrants a SEP, start a conversation on [Discord](https://discord.gg/6CSzBmMkjX) or [GitHub Discussions](https://github.com/modelcontextprotocol/modelcontextprotocol/discussions). We're happy to help you figure out the right path forward.

## Thank You

This change is a direct result of feedback from contributors who've been through the SEP process. Your input helps us continuously improve how we build MCP together. Keep it coming.
