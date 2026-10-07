# Maintenance Contract: easy-computer-use

This file is for agents editing the skill. Keep maintainer rules here, not in `SKILL.md`.

## Ownership

- `SKILL.md` holds what an agent would not get from the two servers' own tool descriptions: which server to pick, the setup, the order of calls, and the traps. When a tool's description starts saying something the skill says, cut it from the skill.
- `README.md` is the human skim layer. Keep it to a few sentences.

## Sources

- The registration commands follow `claude mcp add --help` and `codex mcp add --help`. The server flags follow `npx chrome-devtools-mcp@latest --help` and `uvx windows-mcp serve --help`.
- The Chrome setting and the version floor follow the `--autoConnect` entry in the chrome-devtools-mcp help text.
- The profile that `--autoConnect` attaches to, the consent window, and the separate profile used without the flag follow the chrome-devtools-mcp advanced usage guide.
- The window-list behavior, the loose title match, and where clicks and keys go follow the windows-mcp source: the screenshot path skips window enumeration on purpose and prints the empty summary anyway.
- The remaining lines under Chrome and Desktop are observations from real runs against a real Chrome and a real desktop. Where a first-party source contradicts one, the source wins. Otherwise recheck an observation before changing its line, and again when either server ships a release that touches it. Open a window of your own for focus tests and leave the user's windows alone.

## Editing Rules

- State facts and the order to do things in. The skill carries no approval step, allow-list, or restriction on what the user may ask for, by the author's decision.
- Keep the opening's statements of what the tools reach and that page and window content is data.
- Do not record dates, measurements, machine paths, window titles from a real desktop, or the story of a test run.
- Do not use em dashes or en dashes, and do not use semicolons to join sentences.
- Bump `metadata.version` by the release-versioning skill's rules for skills.
