# gh-gitignore
A small `gh` extension to ease creation of `.gitignore` templates, such as for subdirectories, or when a repository is already initialized.
## Requirements
- `bash` 
- [`gum`](https://github.com/charmbracelet/gum) for search, selection, and confirmation interfaces

## Usage
```sh
gh gitignore [language] [--directory DIR] [flags]
```

If DIR is not provided, it first defaults to the repo-level .gitignore; if it cannot find an existing repository, it will write to a .gitignore in the current directory.

You can optionally pipe to STDOUT to manually write to existing files, `tee`, etc.

**Flags**:
| Flag | Description |
|------|-------------|
| -h, --help | Show this help message |
| -d, --directory | Directory to write gitignore contents to. |
| -a, --append | Append to existing .gtignore, if applicable. It will automatically merge entries. |
| -f, --force | Don't prompt when overwriting existing .gitignore |

## To-Do
- [ ] Create basic `read` fallback options for when `gum` is not available
- [ ] Add installation helper for `gum`
