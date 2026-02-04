# Easy Guide: MkDocs + Mike

This guide helps you understand how to manage **different versions** of your documentation (like v1.0, v2.0) using **MkDocs** and **Mike**.

---

## What is this?

- **MkDocs**: The tool that builds your documentation website from simple text files.
- **Mike**: A helper that organizes your documentation into versions (e.g., "Old Version", "New Version").

Think of **Mike** as a librarian who organizes your books by edition.

---

## Simple Commands

Here are the only commands you really need to know:

| Command | What it does | Use when... |
|---------|--------------|-------------|
| `mkdocs serve` | **Preview** your site (only current version) | You are writing and want to see changes instantly. |
| `mike serve` | **Preview** with version selector | You want to test switching between versions. |
| `mike deploy` | **Publish** a version online | You are ready to share your work. |

---

## How to Publish a Version

### 1. First Time Setup

If this is your first time publishing version 1.0:

```bash
# Publish version 1.0 and call it "latest"
mike deploy --push 1.0 latest

# Tell the site to show "latest" by default
mike set-default --push latest
```

### 2. Updating Documentation

If you made changes and want to update the online site:

```bash
# Update the current version
mike deploy --push 1.0 latest
```

### 3. Releasing a New Version

When you are ready to release version 2.0:

```bash
# Publish version 2.0 and move "latest" to it
mike deploy --push --update-aliases 2.0 latest
```

*Now users will see v2.0 as the main documentation, but v1.0 is still there if they need it!*

---

## FAQ and Troubleshooting

**Q: I see a "404 Error" when I open the site.**
**A:** You probably haven't set the default version. Run this:
```bash
mike set-default --push latest
```

**Q: I don't see the version dropdown.**
**A:** Check your `mkdocs.yml` file. It needs this section:
```yaml
extra:
  version:
    provider: mike
```

**Q: How do I delete a mistake?**
**A:** You can delete a version like this:
```bash
mike delete --push 1.0
```

---

!!! success "You're all set!"
    Managing versions might sound complex, but it's just about publishing your changes to the right "bucket" (version).
