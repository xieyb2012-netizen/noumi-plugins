<!-- Generated from agent-kit; content 5.1.1. Edit canonical sources, then run node scripts/build-agent-kit.mjs. -->

# Music direction

Make the intended sound executable and coherent. `stylePrompt` describes what the music should sound like; `lyrics` contains what should be sung. Do not place operational instructions, analysis, or a review rubric in the sung text.

## Choose compatible musical decisions

Choose for this owner's current request first, relevant sourced preferences second, and the artist's usual sound third. Do not make every song conform to historical taste: a requested dance experiment, a gift, and an ordinary song for the owner can need different sounds. Leave unknown preferences unknown; no questionnaire is needed to make reasonable initial choices.

Start with the purpose and the words. Choose the musical center, then the few supporting details that matter:

- **Genre and groove:** a primary idiom plus a meaningful influence if useful; straight, swung, half-time, dance pulse, conversational rhythm, or free movement.
- **Pace:** an explicit BPM only when meaningful. Emotional sadness does not automatically mean slow, and joy does not automatically mean fast.
- **Voice:** register, texture, articulation, phrasing, and solo/group delivery suited to the narrator. Avoid assigning the same breathy voice to every tender song. `vocalGender` only supports `m` or `f`; leaving it out avoids an unnecessary binary constraint.
- **Arrangement:** name a few instruments and their roles, not a shopping list. Decide what carries pulse, harmony, motif, and space.
- **Movement:** specify a useful contrast, such as close verses opening into a fuller chorus, an uninterrupted rap groove, or a lullaby that remains restrained. Not every song needs a cinematic build.
- **Production:** choose perspective, room, texture, and density where they help. “Amazing, emotional, professional” gives little sonic information.

Write a compact, internally consistent description. English musical vocabulary is often useful for style description, but the API checks nonempty text rather than an English-only rule. Use the requested language for lyrics. Do not invent a universal prompt limit: runtime guide/schema takes precedence, and the active backend may truncate long style text. Front-load the decisions most important to this song.

In the current generation path, direction may be truncated to its first 1000 characters downstream; this is not an HTTP/MCP input `maxLength` validation rule. The pipeline also appends artist DNA, so very long input can crowd out that signature. Keep essential requests first and describe only useful details; do not invent a guarantee for other generation branches.

Optional `genre`, `mood`, `bpm`, `keyscale`, `timesignature`, `negativeTags`, and `vocalGender` must agree with the main prompt. A musical meter is not the same as an input number: use the field's actual schema rather than putting an unsupported “6/8” string into a numeric field. Leave a field unset when it does not improve control.

Prefer the actual song's `genre` when known. Omission inherits the artist's default label, so a quiet piano song by an electronic artist can otherwise retain an electronic label. Stored genre/mood and submitted direction express intent or defaults; they are not analysis of the resulting audio or evidence of the owner's enjoyment.

## Short examples of decisions, not presets

- A quiet reassurance might use “intimate solo vocal, unhurried fingerpicked guitar, warm bass, spare percussion; keep the refrain close rather than expanding into a stadium chorus.” A different narrator might need piano, a dry spoken delivery, or no repeated refrain.
- A playful running chant might need a steady pulse and sharply articulated short phrases rather than layered metaphors and a long bridge.
- A narrative rap might prioritize conversational cadence, a stable drum pocket, and room for syllables; extra tags cannot repair an overfull line.

These illustrate the relationship between intention and sound. Derive each song from its brief; do not reuse these words as a default output.

## Understand existing artist context

Read the selected artist's profile where available. The current generation pipeline appends an artist DNA signature to the song's explicit style direction. Do not promise that a contradictory instruction will completely override an established artist sound. If a result conflicts with the brief, distinguish the submitted direction, stored artist context, and model execution before changing anything.

Voice locking is optional and persistent. Enable `lockVoice: true` only after the owner has listened, approved the voice direction, and explicitly chosen lasting continuity; ordinary authorization for one song is insufficient. The flag attempts to establish a signature after successful generation, but signature creation can fail independently of a ready song. An established signature automatically affects subsequent songs; `lockVoice: false` does not clear it, and the current tools expose no unlock/reset action. Omission also does not disable an existing signature. Do not claim the signature was saved from generation success alone. If a requested voice conflicts with it, explain the limitation and preserve the request as a direction without guaranteeing an override. Do not promise perfect voice identity or exact tempo, key, instrumentation, duration, or tag compliance before listening.

## After an actual listen

Separate problems the agent can fix in words from problems in performance: crowded syllables, unclear message, incompatible arrangement requests, pronunciation, melodic repetition, unwanted voice, balance, clipping, or timing. If audio is unavailable, do not invent listening observations. Rewriting direction or lyrics can be done without generating again; a paid regeneration needs the user's authorization.

Target the responsible layer: if the owner likes the lyrics and melody idea but dislikes heavy drums, preserve the text and identity and specify lighter/sparser percussion. Treat “this time” as local feedback unless they explicitly make it continuing. Give the owner a way to correct an earlier preference; do not keep applying a withdrawn rule through stored artist assumptions or host memory.
