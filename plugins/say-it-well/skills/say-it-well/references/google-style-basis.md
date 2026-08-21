# Google style basis

Say It Well adapts the Google developer documentation style guide to interactive
coding-agent communication. This source map records decisions that change an
agent's messages; it doesn't reproduce the guide.

Reviewed on August 20, 2026. Under the
[Google Developers Site Policies](https://developers.google.com/terms/site-policies),
Google publishes the guide's prose under the
[Creative Commons Attribution 4.0 License](https://creativecommons.org/licenses/by/4.0/)
and its code samples under the Apache 2.0 License. This project adapts prose
guidance and does not copy Google code samples.

## Authority and scope

Google's [About this guide](https://developers.google.com/style) establishes a
reference hierarchy: project-specific guidance precedes the Google guide, and
clarity for the actual reader can justify a consistent departure. This skill adds
the user's explicit instructions above that hierarchy.

The guide targets durable developer documentation. This skill targets shorter,
interactive messages from coding agents. The same clarity principles apply, but
the output types differ. The skill therefore covers progress updates, questions,
review findings, troubleshooting, and final handoffs in addition to instructions
and explanations.

## Source coverage

The following sections materially informed the skill:

| Google section | Decision incorporated here |
| --- | --- |
| [Highlights](https://developers.google.com/style/highlights) | Use active voice, second person, descriptive links, sentence case, appropriate lists, code formatting, and conditions before instructions. |
| [Voice and tone](https://developers.google.com/style/tone) | Sound like a knowledgeable friend; stay direct, respectful, human, and free of frivolous language, forced politeness, and difficulty judgments. |
| [Active voice](https://developers.google.com/style/voice) | Name the actor unless the actor is irrelevant or the object deserves emphasis. |
| [Second person and first person](https://developers.google.com/style/person) | Address the reader as *you*, use imperatives for actions, distinguish the reader from the software's end user, and avoid ambiguous first-person plural language. |
| [Present tense](https://developers.google.com/style/tense) and [Contractions](https://developers.google.com/style/contractions) | Describe current behavior in present tense and use common contractions, especially for clear negation. |
| [Sentence structure](https://developers.google.com/style/sentence-structure) and [Paragraph structure](https://developers.google.com/style/paragraph-structure) | Put conditions before dependent actions, keep one idea per paragraph, and put critical information first. |
| [Write for a global audience](https://developers.google.com/style/translation) | Prefer short, unambiguous sentences; simple words; consistent terms; explicit antecedents; standard word order; and literal, culturally neutral language. |
| [Write accessible documentation](https://developers.google.com/style/accessibility) | Make content scannable, keep headings hierarchical, use descriptive links, avoid visual-only cues and directional language, and don't rely on punctuation for meaning. |
| [Write inclusive documentation](https://developers.google.com/style/inclusive-documentation) | Avoid unnecessarily gendered, ableist, violent, divisive, and metaphorical language; preserve exact legacy code terms only when necessary. |
| [Jargon](https://developers.google.com/style/jargon) | Prefer precise plain language; retain audience-relevant terms and define or link unfamiliar ones. |
| [Prescriptive documentation](https://developers.google.com/style/prescriptive-documentation) | Recommend a useful path and distinguish required, optional, expected, possible, and recommended states with precise modal verbs. |
| [Abbreviations](https://developers.google.com/style/abbreviations) and [Articles](https://developers.google.com/style/articles) | Expand unfamiliar abbreviations when useful, avoid internet shorthand, and don't remove grammar merely to shorten text. |
| [Headings and titles](https://developers.google.com/style/headings), [Lists](https://developers.google.com/style/lists), and [Text-formatting summary](https://developers.google.com/style/text-formatting) | Use sentence-case headings, logical hierarchy, numbered sequences, parallel bullets, serial commas, and restrained emphasis. |
| [Procedures](https://developers.google.com/style/procedures) | Put context and goals before actions, use imperative verbs, keep one decision per step, minimize alternate paths, and state results after actions. |
| [Code in text](https://developers.google.com/style/code-in-text), [Code samples](https://developers.google.com/style/code-samples), and [Command-line syntax](https://developers.google.com/style/code-syntax) | Format literal technical elements as code, use grammatical nouns around identifiers, introduce samples by purpose, prefer runnable commands, and show output only when it adds value. |
| [Cross-references and linking](https://developers.google.com/style/cross-references) | Link selectively, use short descriptive text, provide local context, and avoid vague or duplicate links. |
| [UI elements and interaction](https://developers.google.com/style/ui-elements) | Focus on the goal, use exact visible labels when controls matter, and avoid visual-position instructions. |
| [Notes, cautions, warnings, and other notices](https://developers.google.com/style/notices) | Keep essential information in the main flow; reserve warnings for material risk and avoid stacks of asides. |
| [Avoid excessive claims](https://developers.google.com/style/excessive-claims) | Prefer objective, verifiable statements over guarantees, superlatives, and unsupported claims. |
| [Word list](https://developers.google.com/style/word-list) | Applied relevant entries for words such as *can*, *might*, *must*, *should*, *easy*, *simple*, *just*, *please*, *leverage*, *utilize*, *user*, *desire*, *wish*, and *will*. |

## Chat-specific adaptations

- **First-person singular:** The documentation guide focuses on second person and
  careful first-person plural usage. A coding agent may use **I** to report its own
  actions or limitations because that makes responsibility explicit.
- **Outcome-first handoffs:** The paragraph guidance to put critical information
  first becomes a stronger chat rule: lead final responses with the result rather
  than a work log.
- **Evidence labels:** Coding agents can run tools. This skill therefore requires a
  clear distinction between observed output, expected output, inference, and checks
  that weren't run.
- **Markdown code fences:** Google documents four-space Markdown code blocks in its
  publishing environment. Coding chat interfaces generally support fenced blocks
  with language tags, which are easier to copy and distinguish from surrounding
  prose. Project or platform requirements still take precedence.
- **Flexible length:** The accessibility guide suggests fewer than 26 words per
  sentence. This skill treats that number as an editing signal, not a mechanical
  limit. Accuracy and natural syntax come first.
- **Minimal formatting:** Durable documentation often benefits from a formal
  hierarchy. Short chat answers usually don't. This skill adds headings only when
  they materially improve navigation.

## Maintenance guidance

When updating this skill, check the source pages that correspond to the affected
rule and the Google guide's [What's new](https://developers.google.com/style/whats-new)
page. Keep operational instructions in `SKILL.md`; keep examples and provenance in
references. Don't expand the skill into a general grammar manual or a code-style
guide.
