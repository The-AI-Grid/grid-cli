# The Grid CLI

Lab onboarding and model management CLI for [The Inference Grid](https://theinferencegrid.com).

## Install

### Homebrew (macOS / Linux)

```bash
brew install The-AI-Grid/tap/grid
```

### Download Binary

Download the latest release for your platform from [Releases](https://github.com/The-AI-Grid/grid-cli/releases).

### Debian / Ubuntu

```bash
curl -LO https://github.com/The-AI-Grid/grid-cli/releases/latest/download/grid-cli_<version>_linux_amd64.deb
sudo dpkg -i grid-cli_*.deb
```

## Quick Start

```bash
# Authenticate
grid auth login --endpoint api.theinferencegrid.com:443 --api-key <YOUR_KEY>

# Push a model
grid model push \
  --name my-model \
  --version 1 \
  --origin "r2://my-bucket/model.safetensors" \
  --sign-key lab-key.pem \
  --security-tier SEC0

# Check status
grid model status my-model --version 1
```

## Provider CLI

The `gridprov` CLI is also available for provider operations:

```bash
brew install The-AI-Grid/tap/gridprov
```

## License

Proprietary. See [LICENSE](LICENSE) for details.
