<!-- Generated from agent-kit; content 5.1.1. Edit canonical sources, then run node scripts/build-agent-kit.mjs. -->

# Structure and performance tags

Tags are probabilistic musical guidance. They do not form an API with guaranteed execution. Separate common structural conventions from optional performance experiments and from supported tool fields.

Choose cues only after understanding the owner's current purpose and wording requirements. No tags is a valid creative choice. Do not infer that an untagged result is weaker, restore an unverified “intro must swallow lyrics” rule, or use a tag formula to override a requested short chant, continuous rap, or direct emotional statement.

## Common structural conventions

Use a standalone bracketed label before a section when the song needs that section, for example `[Verse]`, `[Verse 2]`, `[Chorus]`, `[Pre-Chorus]`, `[Bridge]`, `[Intro]`, or `[Outro]`. Follow it with the words to be sung. This small original example demonstrates placement only:

```text
[Verse]
The gate clicks shut behind the bus
I keep the seat beside me clear
```

Do not copy these lines into unrelated songs. Do not treat the list as a verified exhaustive tag catalog. It illustrates widely used section names; the current Noumi backend does not validate a canonical tag whitelist. A section may be omitted, repeated, or replaced by a more appropriate form. Numbered verses are organizational cues rather than a promise of exact musical lengths.

`Pre-Chorus` leads into a chorus; `Bridge` creates contrast elsewhere. A refrain can return within verses without a separately marked chorus. A hook can occur anywhere and does not require a literal `[Hook]` tag. Adding `[Chorus x2]` is not a reliable command to duplicate words: when a repeated passage is essential and authorized, write the intended passage explicitly.

## Performance intentions

Tempo, instruments, voice, energy, and production primarily belong in `stylePrompt` or supported optional fields. A short bracketed delivery cue may be tested where it serves a clear purpose, but arbitrary compound cues, invented mood tags, parenthesized text, and all-caps words may be ignored, sung aloud, or interpreted differently. Parentheses are not a guaranteed harmony command. Neither a `Drop` tag nor an `Instrumental Break` tag changes the tool into a supported pure-instrumental mode.

Prefer one clear structural cue at a section boundary over a stack of competing directions. Remove an unnecessary cue before adding another. These are editing heuristics, not enforced tag limits. Keep the sung text free of commentary such as “now make the listener cry.”

## Preserve supplied text

When the user says to keep lyrics verbatim, pass their text without inserting tags, refrains, rhyme fixes, translations, or performance syllables. Express musical structure in `stylePrompt` where possible. If a user explicitly authorizes formatting or section marking, add only those changes. Do not silently “improve” original lyrics by inserting your own sung material.

## Evidence levels

Tool schemas and API validations determine allowed fields. Structural conventions guide form. Model response to a cue is an empirical effect that can vary across versions and runs. Listening to one successful song does not establish universal support. Keep these levels separate in both documentation and user reports.
