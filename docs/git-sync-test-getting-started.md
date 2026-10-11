---
title: "Getting started with Git Sync (test)"
---

# Getting started with Git Sync (test)

This doc was added through a pull request to test that **BetterDocs Git Sync** can create a doc from a markdown file.

## What it checks

1. The file is listed under *Import MD Files* in the editor's Git modal.
2. Importing it creates a new BetterDocs doc with this title.
3. The doc keeps a link to `docs/git-sync-test-getting-started.md`.

## A code sample

```bash
wp post list --post_type=docs --s="Git Sync"
```

> If you can read this inside WordPress, the import worked.
