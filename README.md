# Alex's Dotfiles

Personal development environment configuration files managed with a bare Git repository.

## Quick Setup

**One-line installation:**
```bash
curl -fsSL https://raw.githubusercontent.com/alexguanga/dotfiles/main/.local/bin/setup-machine | bash
```

**Manual setup:**
```bash
git clone --bare https://github.com/alexguanga/dotfiles.git $HOME/.dotfiles
alias dotfiles='git --git-dir=$HOME/.dotfiles/ --work-tree=$HOME'
dotfiles config --local status.showUntrackedFiles no
dotfiles checkout
source ~/.zshrc
mise install && brew bundle
```

## What's Included

- **Shell**: Zsh with Zinit plugins, Powerlevel10k theme
- **Tools**: mise, Homebrew, fzf, zoxide, Google Cloud SDK
- **Development**: Modern shell environment with smart completions

## Management

```bash
dotfiles status          # Check status
dotfiles add ~/.vimrc    # Add new file
dotfiles commit -m "..."  # Commit changes
dotfiles push            # Push to remote
```

## Documentation

See [`dotfiles-setup-guide.md`](./dotfiles-setup-guide.md) for complete setup and usage instructions.

---

*Powered by bare Git repository approach for simple, transparent dotfiles management.*