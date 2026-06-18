```markdown
# 2025-blog-public Development Patterns

> Auto-generated skill from repository analysis

## Overview

This skill covers the core development patterns and workflows of the `2025-blog-public` repository, a TypeScript-based blogging platform. The repository manages blog post content, metadata, and assets in a structured public directory. It documents how to add and update blog posts, as well as the project's coding conventions and testing patterns.

## Coding Conventions

**File Naming**
- Use `camelCase` for file names.
  - Example: `blogPostUtils.ts`, `getPostData.ts`

**Import Style**
- Use relative imports for modules within the project.
  - Example:
    ```typescript
    import { getPostData } from './blogPostUtils';
    ```

**Export Style**
- Prefer named exports.
  - Example:
    ```typescript
    // blogPostUtils.ts
    export function getPostData(slug: string) { ... }
    ```

**Commit Messages**
- Freeform style, often short (average 13 characters).
  - Example: `fix typo`, `add post`, `update meta`

## Workflows

### Add New Blog Post
**Trigger:** When someone wants to publish a new blog post.  
**Command:** `/new-blog-post`

1. Add a new entry to `public/blogs/index.json` with the new post's metadata (title, slug, date, etc.).
2. Create a new folder under `public/blogs/{slug}/`, where `{slug}` is the unique identifier for the post.
3. Add a `config.json` file in the new folder with post-specific configuration.
4. Add an `index.md` file containing the post's Markdown content.
5. Add any image assets (e.g., `.webp` files) needed for the post to the same folder.

**Example Directory Structure:**
```
public/
  blogs/
    index.json
    my-new-post/
      config.json
      index.md
      cover.webp
```

**Example `index.json` Entry:**
```json
{
  "title": "My New Post",
  "slug": "my-new-post",
  "date": "2025-01-01",
  "author": "Jane Doe"
}
```

### Update Existing Blog Post
**Trigger:** When someone wants to edit or update a blog post's content.  
**Command:** `/update-blog-post`

1. Locate the relevant post's folder: `public/blogs/{slug}/`.
2. Edit the `index.md` file to update the post content.

**Example:**
```markdown
// public/blogs/my-new-post/index.md

# Updated Title

New content goes here...
```

## Testing Patterns

- Test files use the `*.test.*` naming pattern (e.g., `blogPostUtils.test.ts`).
- The specific testing framework is unknown, but tests are colocated with source files or in the same directory.

**Example Test File:**
```typescript
// blogPostUtils.test.ts
import { getPostData } from './blogPostUtils';

test('getPostData returns correct data', () => {
  const data = getPostData('my-new-post');
  expect(data.title).toBe('My New Post');
});
```

## Commands

| Command            | Purpose                                      |
|--------------------|----------------------------------------------|
| /new-blog-post     | Add a new blog post with metadata and assets |
| /update-blog-post  | Update the content of an existing blog post  |
```
