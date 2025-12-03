# Getting Started

Welcome to the Cooperative Systems Spaces wiki! This guide will help you contribute to our documentation.

## Prerequisites

Before you begin, make sure you have:
- Git installed
- A text editor
- Access to the wiki repository
- GitHub account with repository access
- Basic understanding of Markdown

## Setup Steps

### 1. Clone the Repositories

The wiki and pages are in sibling folders:

```bash
# Clone the wiki
cd ~/Development/projects
git clone https://github.com/cooperative-systems/cooperative-systems-spaces-wiki.git

# Clone the pages (if needed)
git clone https://github.com/cooperative-systems/cooperative-systems-spaces-pages.git
```

### 2. Make a new branch

You won't be able to push directly to the main branch. Always work on a feature branch:

```bash
cd cooperative-systems-spaces-wiki
git checkout -b update-tool-documentation
```

Use descriptive branch names like:
- `add-drill-guide`
- `update-safety-rules`
- `fix-typo-hammer-doc`

### 3. Editing

Edit the wiki files using any text editor. All files use Markdown format (`.md`).

**Markdown Quick Reference:**
- `# Heading` - Top level heading
- `## Subheading` - Second level heading
- `**bold text**` - Bold text
- `*italic text*` - Italic text
- `[Link Text](FILE.md)` - Link to another page
- `- Item` - Bullet point
- ` ```code``` ` - Code block (use triple backticks)

**Linking to other pages:**
- Same directory: `[Tools](TOOLS.md)`
- Subdirectory: `[Hammer](TOOLS/HAMMER.md)`
- Parent directory: `[Index](../INDEX.md)`

### 4. Commit Changes

After making your edits, commit them with a clear message:

```bash
# Check what files changed
git status

# Add the files you modified
git add TOOLS/HAMMER.md
git add TOOLS.md

# Or add all changed files
git add .

# Commit with a descriptive message
git commit -m "Add maintenance section to hammer documentation"
```

**Good commit messages:**
- "Add safety guidelines for table saw"
- "Fix broken link in INDEX.md"
- "Update workshop hours in STUFF.md"
- "Create new drill press guide"

**Bad commit messages:**
- "Update"
- "Fixed stuff"
- "asdf"

### 5. Push Your Branch

Push your branch to GitHub:

```bash
git push origin update-tool-documentation
```

If this is your first push of this branch, Git will provide the exact command to use.

### 6. Make a pull request

1. Go to the repository on GitHub
2. You should see a banner suggesting to create a pull request for your branch
3. Click "Compare & pull request"
4. Fill out the PR template:
   - **Title**: Brief description of changes
   - **Description**: What you changed and why
   - **Reviewers**: Tag at least one other member to review
5. Click "Create pull request"

### 7. Address Review Feedback

Other members may suggest changes:
- Read comments carefully
- Make requested changes in your branch
- Commit and push updates
- Respond to comments when done

### 8. Merge and Cleanup

Once approved:
1. Click "Merge pull request" (or a maintainer will do this)
2. Delete your branch on GitHub
3. Update your local repository:

```bash
git checkout main
git pull origin main
git branch -d update-tool-documentation
```

## Wiki Structure

```
cooperative-systems-spaces-wiki/
├── INDEX.md              # Main index page
├── GETTING_STARTED.md    # This file - how to edit the wiki
├── RULES.md              # Workspace rules
├── WEEKLY_CALENDAR.md    # Weekly schedule
├── STUFF.md              # Miscellaneous info
├── TOOLS.md              # Tools overview
└── TOOLS/
    ├── HAMMER.md         # Hammer documentation
    ├── SAW.md            # Saw documentation
    └── [other tools]     # Add new tools here
```

## Best Practices

### Writing Style
- **Be clear and concise** - Workshop members need quick answers
- **Include safety information** - Always emphasize safety first
- **Use examples** - Show, don't just tell
- **Keep it updated** - Remove outdated information

### File Naming
- Use UPPERCASE for top-level pages (INDEX.md, RULES.md)
- Use UPPERCASE for tool names (HAMMER.md, SAW.md)
- Use underscores for multi-word files (WEEKLY_CALENDAR.md)
- Keep names short and descriptive

### Adding New Tools

When documenting a new tool:
1. Create file in `TOOLS/` directory (e.g., `TOOLS/DRILL.md`)
2. Add link to `TOOLS.md`
3. Use existing tool pages as templates
4. Include these sections:
   - Overview
   - Location
   - Basic Usage
   - Safety
   - Maintenance
   - Tips and Tricks

### Adding Images

If you need to add images:
1. Create an `images/` directory
2. Use descriptive names: `hammer-claw-pulling-nail.jpg`
3. Keep file sizes reasonable (< 1MB)
4. Reference in Markdown: `![Description](images/filename.jpg)`

## Getting Help

- **Markdown help**: GitHub has a [Markdown guide](https://guides.github.com/features/mastering-markdown/)
- **Git help**: Ask in the Discord #wiki channel
- **Content questions**: Check with the shop manager or experienced members
- **Technical issues**: Open an issue on the GitHub repository

## Common Tasks

### Fixing a Typo
```bash
git checkout -b fix-typo
# Edit the file
git add filename.md
git commit -m "Fix typo in safety section"
git push origin fix-typo
# Create PR on GitHub
```

### Adding a New Page
```bash
git checkout -b add-lathe-guide
# Create TOOLS/LATHE.md
# Edit TOOLS.md to add link
git add TOOLS/LATHE.md TOOLS.md
git commit -m "Add lathe documentation"
git push origin add-lathe-guide
# Create PR on GitHub
```

### Updating Multiple Files
```bash
git checkout -b update-safety-info
# Edit multiple files
git add .
git commit -m "Update safety information across all power tool guides"
git push origin update-safety-info
# Create PR on GitHub
```

## Questions?

If you have questions about editing the wiki:
- Check with other members who have contributed
- Look at recent pull requests for examples

Happy documenting! 📝

[Back to Index](INDEX.md)
