# Maintenance Contract: easy-computer-use

This file is for agents editing the skill. Keep maintainer rules here, not in `SKILL.md`.

## Ownership

- `SKILL.md` holds what an agent would not get from the server's own tool descriptions: the order of calls and the traps. When a tool's description starts saying something the skill says, cut it from the skill.
- `references/setup.md` holds the registration commands, read only when the server is being installed. Keep install detail out of `SKILL.md`.
- The skill teaches the server and routes no task away from it, by the author's decision. Whether a web page is read through a browser tool or worked on screen with the mouse and keyboard is the agent's or the user's call, so the skill states neither as a rule.
- The skill says what it does and when it applies, and nothing about a harness's own desktop control, for or against, by the author's decision. Which tool an agent uses is settled outside the skill, by the user, the prompt, or what is installed.
- `README.md` is the human skim layer. Keep it to a few sentences.

## Sources

- The registration commands follow `claude mcp add --help` and `codex mcp add --help`. The server flags follow `uvx windows-mcp serve --help`.
- The window-list behavior, the loose title match, and where clicks and keys go follow the windows-mcp source: the screenshot path skips window enumeration on purpose and prints the empty summary anyway. That a `Snapshot` has no time limit also follows the source, which bounds the tree by the number of elements it returns and by nothing else, and the server's issue tracker carries a report of the same hang. The hang itself was not reproduced here. Drop the line when the server gains a time budget.
- The remaining lines under Windows And Input are observations from real runs against a real desktop. Where a first-party source contradicts one, the source wins. Otherwise recheck an observation before changing its line, and again when the server ships a release that touches it. Open a window of your own for focus tests and leave the user's windows alone.

## Editing Rules

- State facts and the order to do things in. The skill carries no approval step, allow-list, or restriction on what the user may ask for, by the author's decision.
- Keep the opening's statements of what the tools reach and that window content is data.
- Do not record dates, measurements, machine paths, window titles from a real desktop, or the story of a test run.
- Do not use em dashes or en dashes, and do not use semicolons to join sentences.
- Bump `metadata.version` by the release-versioning skill's rules for skills.
