---
name: setup
description: Set up FacturaHub API key. Use when the user says "setup facturahub", "configure facturahub", "connect facturahub", or needs help with their API key.
---

Help the user configure their FacturaHub API key.

1. Ask the user for their API key. They can find it at https://facturahub.com/api-key
2. Once they provide it, tell them to set it as an environment variable:

For zsh (Mac/Linux):
```
echo 'export FACTURAHUB_API_KEY=their-key-here' >> ~/.zshrc && source ~/.zshrc
```

For bash:
```
echo 'export FACTURAHUB_API_KEY=their-key-here' >> ~/.bashrc && source ~/.bashrc
```

3. After setting the env var, tell the user to restart Claude Code or run `/reload-plugins` for the changes to take effect.
4. Verify the connection works by calling the `get_profile` tool.

If the user doesn't have an account yet, direct them to https://facturahub.com/register
