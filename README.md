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

### Languages & Runtimes (mise)
- **Node.js** (latest), **Python** (3.11.12), **Go** (latest)
- **Package managers**: poetry, uv

### Cloud & Infrastructure (mise)
- **Kubernetes**: kubectl, helm
- **Infrastructure**: terraform
- **GitHub**: gh CLI

### Development Tools (Homebrew)
- **Editors**: vim, neovim
- **Terminal**: tmux, k9s, kubie
- **Git**: hub, tig, diff-so-fancy
- **Search**: fzf, the_silver_searcher
- **File tools**: exa, bat, dust, duf
- **Databases**: pgcli, pspg
- **System**: readline, gnu-getopt, zsh
- **Monitoring**: bpytop, vivid
- **Other**: chezmoi, hasura-cli, antibody

### Applications (Homebrew Casks)
- **Docker** (containerization)
- **StrongDM** (secure access)

### Shell Environment
- **Zsh** with Powerlevel10k theme
- **Modern CLI tools** and smart completions
- **Automated development tasks** via mise

## Management

```bash
dotfiles status          # Check status
dotfiles add ~/.vimrc    # Add new file
dotfiles commit -m "..."  # Commit changes
dotfiles push            # Push to remote
```

---

*Powered by bare Git repository approach for simple, transparent dotfiles management.*