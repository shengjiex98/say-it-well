# Contributing

Contributions that make coding-agent communication clearer, more concise, or more
accurate are welcome.

## Make a focused change

1. Keep `SKILL.md` focused on operational instructions for coding-agent messages.
2. Put extended examples in `references/response-patterns.md`.
3. Record source coverage and adaptation decisions in
   `references/google-style-basis.md`.
4. Preserve the user's instructions and project-specific terminology as higher
   authorities than this skill.
5. Validate the skill structure before submitting the change.

## Preserve provenance

Write contributions in your own words. Do not copy large passages, code samples,
images, logos, or other media from the Google guide or another source.

When a change is materially informed by a new source section:

- add the source link to `references/google-style-basis.md`;
- describe the decision incorporated into the skill;
- mark any adapted third-party material and preserve its license; and
- update `NOTICE.md` if the attribution scope changes.

By contributing, you agree to license your contribution under CC BY 4.0, the
project's license.

## Check the result

Confirm that:

- the YAML frontmatter contains the name `code-agent-communication` and a concise
  trigger description;
- every relative link resolves;
- examples state observed checks and uncertainty accurately;
- the first sentence of each example contains the outcome or current state; and
- the change doesn't add unsupported agent-specific behavior to the README.
