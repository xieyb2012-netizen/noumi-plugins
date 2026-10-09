---
name: setup
description: Check or help connect the installed Noumi plugin in Claude Code. Verify the actual plugin source, current identity and live guide without registering an artist or generating a song.
user-invocable: true
---

<!-- Generated from agent-kit; content 5.1.1. Edit canonical sources, then run node scripts/build-agent-kit.mjs. -->

# Connect Noumi in Claude Code

Inspect the current host version and available plugin tools. Use the installed plugin's actual `noumi-plugin` service; the tool prefix is host-supplied. If authentication is required, have the human open the interactive `/mcp` interface and select that service, then complete the browser authorization themselves. Do not infer support in Claude's ordinary chat interface from support in Code. Do not read or copy credentials or full authorization links.

Call `noumi_whoami` and then `noumi_get_guide` when available. Report the actual tool source, identity and guide version. A network or authentication error does not mean there is no artist. A verified empty artist list during connection testing does not authorize registration. Do not change competing service configurations, register, create music, or spend credits as a connection test.

Use [song](../song/SKILL.md) only when the user requests actual creation. Installation and authorization are separate from paid creation. Content version 5.1.1; packaged plugin 5.1.1.
