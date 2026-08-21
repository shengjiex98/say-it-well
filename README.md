# Code Agent Communication

A portable Agent Skill that helps coding agents communicate in clear, concise,
user-centered language.

Use it for progress updates, questions, explanations, troubleshooting, code
reviews, and final handoffs. It focuses on communication with the user; it does
not impose a source-code style.

## What it changes

The skill teaches an agent to:

- lead with the result, decision, cause, or blocker;
- state evidence, uncertainty, and unrun checks accurately;
- write direct, natural sentences without filler or theatrical narration;
- make technical content easy to scan without over-formatting it; and
- adapt its response to the message type and the task's risk.

The instructions are concise. Longer examples and source notes load only when
the agent needs them.

## Install

Review `SKILL.md` and the supporting files before installing any third-party
skill. Then choose your agent below.

<details>
<summary><strong>OpenAI Codex</strong></summary>

Install from this repository's Codex marketplace:

```bash
codex plugin marketplace add shengjiex98/code-agent-communication
codex plugin add code-agent-communication@code-agent-communication
```

Start a new Codex session after installation. You can open `/plugins` to inspect
or manage the plugin.

Alternatively, install only the standalone skill for your user account:

```bash
git clone https://github.com/shengjiex98/code-agent-communication.git \
  ~/.agents/skills/code-agent-communication
```

Codex discovers user skills in `~/.agents/skills`. To use the skill explicitly,
mention `$code-agent-communication`. Codex can also select it automatically when
the task matches its description.

For one repository, clone or copy the project to
`.agents/skills/code-agent-communication` in that repository instead.

[Codex skill documentation](https://learn.chatgpt.com/docs/build-skills)

</details>

<details>
<summary><strong>Claude Code</strong></summary>

Install from this repository's Claude Code marketplace:

```bash
claude plugin marketplace add shengjiex98/code-agent-communication
claude plugin install code-agent-communication@code-agent-communication
```

The plugin exposes the namespaced skill
`/code-agent-communication:code-agent-communication`. Restart Claude Code after
installing or updating the plugin.

Alternatively, install only the standalone skill for your user account:

```bash
git clone https://github.com/shengjiex98/code-agent-communication.git \
  ~/.claude/skills/code-agent-communication
```

Invoke it with `/code-agent-communication`, or let Claude load it when relevant.
For one repository, use `.claude/skills/code-agent-communication` instead.

[Claude Code skill documentation](https://code.claude.com/docs/en/slash-commands)

</details>

<details>
<summary><strong>GitHub Copilot</strong></summary>

Install the skill for your user account:

```bash
git clone https://github.com/shengjiex98/code-agent-communication.git \
  ~/.agents/skills/code-agent-communication
```

Copilot also supports `~/.copilot/skills` for personal skills. For a project
skill, use `.github/skills/code-agent-communication` or
`.agents/skills/code-agent-communication` in the repository.

[GitHub Copilot skill documentation](https://docs.github.com/en/copilot/concepts/agents/about-agent-skills)

</details>

<details>
<summary><strong>Gemini CLI</strong></summary>

Install directly from GitHub:

```bash
gemini skills install https://github.com/shengjiex98/code-agent-communication
```

The command installs to your user profile by default. Add `--scope workspace`
for the current project only. Gemini CLI also discovers user skills in
`~/.agents/skills` and workspace skills in `.agents/skills`.

[Gemini CLI skill documentation](https://geminicli.com/docs/cli/using-agent-skills/)

</details>

<details>
<summary><strong>Cursor</strong></summary>

Install the skill for your user account:

```bash
git clone https://github.com/shengjiex98/code-agent-communication.git \
  ~/.agents/skills/code-agent-communication
```

Cursor also supports `~/.cursor/skills`. For one repository, use
`.agents/skills/code-agent-communication` or
`.cursor/skills/code-agent-communication` instead. Invoke the skill from the `/`
menu or let Cursor select it automatically.

[Cursor skill documentation](https://cursor.com/docs/skills)

</details>

<details>
<summary><strong>Other Agent Skills-compatible tools</strong></summary>

Clone or copy this repository into the tool's user-level or project-level skills
directory. Keep the directory name `code-agent-communication` and preserve the
repository structure so links from `SKILL.md` continue to work.

The package follows the open [Agent Skills specification](https://agentskills.io/).

</details>

To update a Git-based installation, run `git pull --ff-only` inside the installed
directory.

## Use

Ask the agent to use the skill when you want to force its application. Examples:

```text
Use $code-agent-communication to rewrite this handoff.
```

```text
Use /code-agent-communication and explain the root cause to the user.
```

Invocation syntax varies by agent. Automatic activation depends on the agent and
its settings.

## Package contents

```text
code-agent-communication/
├── .agents/plugins/marketplace.json Codex marketplace catalog
├── .claude-plugin/marketplace.json  Claude Code marketplace catalog
├── plugins/                         Shared Codex and Claude plugin package
├── SKILL.md                         Core instructions and metadata
├── agents/
│   └── openai.yaml                  OpenAI display and invocation metadata
├── references/
│   ├── google-style-basis.md        Source coverage and adaptation decisions
│   └── response-patterns.md         Before-and-after response examples
├── CONTRIBUTING.md                  Contribution and provenance requirements
├── LICENSE                          CC BY 4.0 legal text
├── NOTICE.md                        Attribution and trademark notice
├── PRIVACY.md                       Plugin privacy disclosure
├── SUPPORT.md                       Public support channel
├── TERMS.md                         Plugin terms of use
└── README.md                        Installation and usage
```

The Codex and Claude Code catalogs point to one shared, skills-only plugin under
`plugins/code-agent-communication`. That package contains both
platform manifests and a complete copy of the standalone skill, including its
references, license, and attribution notice.

## Design and provenance

This is an original, chat-specific adaptation informed by the
[Google developer documentation style guide](https://developers.google.com/style).
It selects, summarizes, reorganizes, and extends relevant guidance for interactive
coding agents. It does not reproduce the guide wholesale.

The source map in `references/google-style-basis.md` records the relevant guide
sections and the project-specific decisions derived from them. The examples in
`references/response-patterns.md` are original to this project.

## License and attribution

This project is licensed under the
[Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/)
(`CC-BY-4.0`). See `LICENSE` for the full legal text and `NOTICE.md` for the
required attribution and change notice.

The Google style guide's prose is also available under CC BY 4.0. This repository
does not include Google logos, brand assets, or copied Google code samples. Google
trademarks are not licensed by CC BY 4.0. This project is not affiliated with or
endorsed by Google.

These files provide a conservative licensing and attribution setup, not legal
advice.
