---
name: update-existing-blog-post
description: Workflow command scaffold for update-existing-blog-post in 2025-blog-public.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /update-existing-blog-post

Use this workflow when working on **update-existing-blog-post** in `2025-blog-public`.

## Goal

Updates the content of an existing blog post.

## Common Files

- `public/blogs/{slug}/index.md`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Modify the index.md file for the relevant blog post in its folder

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.