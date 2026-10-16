# Setup

Register the server once per machine, at user scope:

```text
claude mcp add --scope user windows-mcp -- uvx windows-mcp serve
codex mcp add windows-mcp -- uvx windows-mcp serve
```

Any other harness takes the same stdio command.
