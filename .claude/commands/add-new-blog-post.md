---
name: add-new-blog-post
description: Workflow command scaffold for add-new-blog-post in 2025-blog-public.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /add-new-blog-post

Use this workflow when working on **add-new-blog-post** in `2025-blog-public`.

## Goal

Adds a new blog post to the site, including metadata, content, and assets.

## Common Files

- `public/blogs/index.json`
- `public/blogs/{slug}/config.json`
- `public/blogs/{slug}/index.md`
- `public/blogs/{slug}/*.webp`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Add new entry to public/blogs/index.json
- Create new folder under public/blogs/{slug}/
- Add config.json for the new post
- Add index.md with the post content
- Add any image assets (e.g., .webp) to the post folder

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.