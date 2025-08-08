# dotfiles

A dotfiles repository designed for linux instances and development containers. This configuration leverages [chezmoi](https://www.chezmoi.io/) for secure, cross-machine/os dotfile management combined with [mise](https://mise.jdx.dev/) for runtime and tool version management.

## Quick Setup

Run the setup script to bootstrap your environment:

```bash
curl -fsSL https://raw.githubusercontent.com/dankaiser1808/dotfiles/main/setup.sh | bash
```

## What the Setup Script Does

The setup script (`setup.sh`) automates the entire configuration process:

1. **Install chezmoi** - Downloads and installs chezmoi if not already present on the system
2. **Clone repository** - Pulls the latest dotfiles from this Git repository
3. **Apply configurations** - Deploys all dotfile configurations to their appropriate locations
4. **Run customizations** - Executes configuration scripts defined in:
   - `.chezmoiexternal` - External file management and downloads
   - `.chezmoiscripts` - Custom setup and configuration scripts
5. **Install Zsh plugins** - Downloads and configures custom Zsh plugins for enhanced shell functionality

## Features

- **Cross-platform compatibility** - Works seamlessly on Arch Linux and in development containers
- **Secure management** - Leverages chezmoi's security features for sensitive configurations
- **Automated setup** - One-command installation and configuration
- **Extensible** - Easy to customize and extend with additional tools and configurations
- **Version controlled** - All configurations are tracked and versioned through Git

## Customization

The repository structure follows chezmoi conventions. To customize follow these steps:

1. Fork this repository
2. Modify configurations in the chezmoi source directory
3. Update scripts in `.chezmoiscripts` for custom setup tasks
4. Define external dependencies in `.chezmoiexternal`
5. Push changes and re-run the setup script

## Tools Managed

- **Shell**: Zsh with custom plugins and configurations
- **Development tools**: Managed via mise for consistent versions across environments
- **Editor configurations**: Settings for various text editors and IDEs

---

For more information about chezmoi, visit the [official documentation](https://www.chezmoi.io/).