# Claude Code Marketplace

A marketplace for Claude Code plugins maintained by severity1.

## What is This?

This marketplace provides a curated collection of Claude Code plugins that extend Claude Code's functionality with custom commands, agents, hooks, and integrations.

## Installation

To add this marketplace to your Claude Code installation:

```bash
claude marketplace add https://github.com/severity1/claude-code-marketplace
```

## Available Plugins

### claude-code-prompt-improver
Enriches vague prompts with research-based clarifying questions before Claude Code executes them.

- **Repository**: [severity1/claude-code-prompt-improver](https://github.com/severity1/claude-code-prompt-improver)

## Contributing Plugins

To add a plugin to this marketplace:

### 1. Prepare Your Plugin

Ensure your plugin is hosted on GitHub with a valid plugin structure. Your plugin should include:

- A `.claude-plugin/plugin.json` manifest file (if using strict mode)
- Plugin components (commands, agents, hooks, or MCP servers)
- A README.md with usage instructions

### 2. Add Plugin Entry

Edit `.claude-plugin/marketplace.json` and add your plugin to the `plugins` array:

```json
{
  "name": "your-plugin-name",
  "source": {
    "source": "github",
    "repo": "your-github-username/your-plugin-repo"
  },
  "description": "Brief description of what your plugin does"
}
```

### Required Fields
- `name`: Plugin identifier (kebab-case, no spaces)
- `source`: GitHub repository location
- `description`: Clear, concise plugin description

### Optional Fields

Add these to improve discoverability and provide more information:

```json
{
  "name": "your-plugin-name",
  "source": {
    "source": "github",
    "repo": "your-github-username/your-plugin-repo"
  },
  "description": "Brief description of what your plugin does",
  "version": "1.0.0",
  "author": "Your Name",
  "homepage": "https://github.com/your-github-username/your-plugin-repo",
  "license": "MIT",
  "keywords": ["productivity", "automation"],
  "category": "tools"
}
```

### 3. Submit a Pull Request

1. Fork this repository
2. Add your plugin entry to `.claude-plugin/marketplace.json`
3. Update this README.md to include your plugin in the Available Plugins section
4. Submit a pull request with:
   - Clear title: "Add [plugin-name] plugin"
   - Description of what your plugin does
   - Link to your plugin repository

### 4. Review Process

Plugin submissions will be reviewed for:
- Valid plugin structure and manifest
- Working functionality
- Clear documentation
- No malicious code
- Adherence to Claude Code plugin standards

## Source Types

Plugins can be sourced from:

**GitHub (recommended):**
```json
"source": {
  "source": "github",
  "repo": "owner/repo-name"
}
```

**Git URL:**
```json
"source": {
  "source": "url",
  "url": "https://gitlab.com/team/plugin.git"
}
```

**Relative path (for local development):**
```json
"source": "./plugins/local-plugin"
```

## Resources

- [Claude Code Documentation](https://docs.claude.com/en/docs/claude-code)
- [Plugin Marketplaces Guide](https://docs.claude.com/en/docs/claude-code/plugin-marketplaces.md)
- [Creating Plugins](https://docs.claude.com/en/docs/claude-code/plugins)

## License

This marketplace configuration is available under the MIT License.

## Contact

For questions or issues, contact:
- Email: johnreilly.pospos@gmail.com
- GitHub: [@severity1](https://github.com/severity1)
