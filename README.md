# Say It Well

**Ship the work. Say it well.**

Say It Well is a portable Agent Skill that helps coding agents turn working notes
into clear, useful messages. It replaces noisy work logs, vague caveats, and
buried conclusions with communication that leads with the outcome and gives the
user what they need to act.

Use it for progress updates, questions, troubleshooting, code reviews,
explanations, and final handoffs. It improves the conversation around the code;
it doesn't impose a source-code style.

## What it teaches

Say It Well helps an agent:

- lead with the result, decision, cause, or blocker;
- separate observed evidence from inference and unrun checks;
- replace routine narration with useful changes of state;
- write direct, natural sentences without filler;
- format technical details for fast scanning; and
- match the depth of a message to the task and its risk.

The core instructions stay compact. Extended examples and source notes load only
when a task needs them.

## Install

Review `SKILL.md` and the supporting files before installing any third-party
skill. Then choose your agent.

<details>
<summary><strong>OpenAI Codex</strong></summary>

Install from this repository's Codex marketplace:

```bash
codex plugin marketplace add shengjiex98/say-it-well
codex plugin add say-it-well@say-it-well
```

Start a new Codex task after installation. Open `/plugins` to inspect or manage
the plugin.

Alternatively, install only the standalone skill for your user account:

```bash
git clone https://github.com/shengjiex98/say-it-well.git \
  ~/.agents/skills/say-it-well
```

Codex discovers user skills in `~/.agents/skills`. Mention `$say-it-well` to
apply it explicitly, or let Codex select it when the request matches. For one
repository, install it under `.agents/skills/say-it-well` instead.

[Codex skill documentation](https://learn.chatgpt.com/docs/build-skills)

</details>

<details>
<summary><strong>Claude Code</strong></summary>

Install from this repository's Claude Code marketplace:

```bash
claude plugin marketplace add shengjiex98/say-it-well
claude plugin install say-it-well@say-it-well
```

The plugin exposes `/say-it-well:say-it-well`. Restart Claude Code after
installing or updating the plugin.

Alternatively, install only the standalone skill:

```bash
git clone https://github.com/shengjiex98/say-it-well.git \
  ~/.claude/skills/say-it-well
```

Invoke it with `/say-it-well`. For one repository, install it under
`.claude/skills/say-it-well` instead.

[Claude Code skill documentation](https://code.claude.com/docs/en/slash-commands)

</details>

<details>
<summary><strong>GitHub Copilot</strong></summary>

Install the skill for your user account:

```bash
git clone https://github.com/shengjiex98/say-it-well.git \
  ~/.agents/skills/say-it-well
```

Copilot also supports `~/.copilot/skills`. For a project skill, use
`.github/skills/say-it-well` or `.agents/skills/say-it-well`.

[GitHub Copilot skill documentation](https://docs.github.com/en/copilot/concepts/agents/about-agent-skills)

</details>

<details>
<summary><strong>Gemini CLI</strong></summary>

Install directly from GitHub:

```bash
gemini skills install https://github.com/shengjiex98/say-it-well
```

The command installs to your user profile by default. Add `--scope workspace`
for the current project only.

[Gemini CLI skill documentation](https://geminicli.com/docs/cli/using-agent-skills/)

</details>

<details>
<summary><strong>Cursor</strong></summary>

Install the skill for your user account:

```bash
git clone https://github.com/shengjiex98/say-it-well.git \
  ~/.agents/skills/say-it-well
```

Cursor also supports `~/.cursor/skills`. For one repository, use
`.agents/skills/say-it-well` or `.cursor/skills/say-it-well`. Invoke the skill
from the `/` menu or let Cursor select it automatically.

[Cursor skill documentation](https://cursor.com/docs/skills)

</details>

<details>
<summary><strong>Other Agent Skills-compatible tools</strong></summary>

Clone or copy this repository into the tool's user-level or project-level skills
directory. Keep the directory name `say-it-well` and preserve the repository
structure so links from `SKILL.md` continue to work.

The package follows the open [Agent Skills specification](https://agentskills.io/).

</details>

To update a Git-based installation, run `git pull --ff-only` inside the installed
directory.

## Use

Ask the agent to apply Say It Well when the quality of the explanation matters:

```text
Use $say-it-well to turn these notes into a concise handoff.
```

```text
Use /say-it-well and explain the root cause to the user.
```

Invocation syntax varies by agent. Automatic activation depends on the agent and
its settings.

## Package contents

```text
say-it-well/
├── .agents/plugins/marketplace.json Codex marketplace catalog
├── .claude-plugin/marketplace.json  Claude Code marketplace catalog
├── plugins/say-it-well/          Shared Codex and Claude plugin package
├── SKILL.md                         Core instructions and metadata
├── agents/openai.yaml               OpenAI display and invocation metadata
├── references/
│   ├── google-style-basis.md        Source coverage and adaptation decisions
│   └── response-patterns.md         Before-and-after response examples
├── CONTRIBUTING.md                  Contribution and provenance requirements
├── LICENSE                          CC BY 4.0 legal text
├── NOTICE.md                        Attribution and trademark notice
├── PRIVACY.md                       Plugin privacy disclosure
├── SUPPORT.md                       Public support channel
└── TERMS.md                         Plugin terms of use
```

The marketplace catalogs point to one shared, skills-only plugin under
`plugins/say-it-well`. That package contains a complete copy of the standalone
skill, its references, license, and attribution notice.

## Design and provenance

Say It Well is an original, chat-specific adaptation informed by the
[Google developer documentation style guide](https://developers.google.com/style).
It selects, summarizes, reorganizes, and extends relevant guidance for interactive
coding agents; it doesn't reproduce the guide wholesale.

The source map in `references/google-style-basis.md` records the relevant guide
sections and project-specific decisions. The examples in
`references/response-patterns.md` are original to this project.

## License and attribution

This project is licensed under the
[Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/)
(`CC-BY-4.0`). See `LICENSE` for the full legal text and `NOTICE.md` for the
required attribution and change notice.

The Google style guide's prose is also available under CC BY 4.0. This repository
doesn't include Google logos, brand assets, or copied Google code samples. Google
trademarks are not licensed by CC BY 4.0. This project is not affiliated with or
endorsed by Google.

These files provide a conservative licensing and attribution setup, not legal
advice.
