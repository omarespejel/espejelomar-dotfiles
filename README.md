# Dotfiles Managed with chezmoi

This repository contains personal dotfiles managed with [chezmoi](https://www.chezmoi.io/) for cross-platform configuration management.

## Quick Start

Install chezmoi and apply these dotfiles:

```sh
sh -c "$(curl -fsLS chezmoi.io/get)" -- init --apply espejelomar
```

Replace `espejelomar` with your GitHub username if you fork this repository.

## Contents

This repository includes common configuration files: `.zshrc`, `.tmux.conf`, `.gitconfig`, and other dotfiles. All files are managed through chezmoi for consistent syncing across machines.

**Important**: This repository contains no secrets or sensitive data.

## Security

Never store API keys, tokens, or passwords in public dotfiles repositories. Use `.chezmoiignore` or chezmoi's encryption features to exclude sensitive data. Consult [chezmoi's documentation](https://www.chezmoi.io/user-guide/secrets/) for implementation details.

## Usage

### Initial Setup

Install chezmoi:

```sh
brew install chezmoi
```

Initialize chezmoi with this repository:

```sh
chezmoi init --apply espejelomar
```

For SSH access:

```sh
chezmoi init --apply git@github.com:espejelomar/chezmoi-dotfiles.git
```

Review changes before applying:

```sh
chezmoi diff
chezmoi apply
```

### File Management

Edit a tracked dotfile:

```sh
chezmoi edit ~/.zshrc
```

Add a new dotfile to tracking:

```sh
chezmoi add ~/.vimrc
```

### Updates

Pull and apply the latest changes:

```sh
chezmoi update
```

## Best Practices

- Exclude secrets using `.chezmoiignore` or encryption
- Edit files through `chezmoi edit` for proper tracking
- Use chezmoi templates for cross-platform compatibility
- Public dotfiles repositories are standard practice in the development community

## Resources

- [chezmoi documentation](https://www.chezmoi.io/)
- [Managing Dotfiles with chezmoi](https://jerrynsh.com/how-to-manage-dotfiles-with-chezmoi/)
- [Official Quick Start](https://chezmoi.io/quick-start/)