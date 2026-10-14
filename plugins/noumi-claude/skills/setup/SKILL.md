---
name: setup
description: Check or help connect the installed Noumi plugin in Claude Code. Verify the actual plugin source, current identity and live guide without registering an artist or generating a song.
user-invocable: true
---

<!-- Generated from agent-kit; content 5.1.2. Edit canonical sources, then run node scripts/build-agent-kit.mjs. -->

# Connect Noumi in Claude Code

Inspect the current host version and available plugin tools. Use the installed plugin's actual `noumi-plugin` service; the tool prefix is host-supplied. If another working Noumi source (for example a claude.ai account connector) already exists, say so and reuse one source rather than stacking them. If authentication is required, have the human open the interactive `/mcp` interface and select that service, then complete the browser authorization themselves. "Connected" in the list only means the server is reachable; an identity tool refused as unauthorized means authorization has not happened, not that no artist exists. On the Windows desktop app, if authorization stops at an "Open Claude" prompt, ask the human to run `claude` in a normal terminal, authorize the service in `/mcp` there, then start a new desktop session; both share the authorization. Do not infer support in Claude's ordinary chat interface from support in Code. Do not read or copy credentials, authorization codes or full authorization links, and never ask for a musician key in chat.

Call `noumi_whoami` and then `noumi_get_guide` when available. Report the actual tool source, the account, the artist to use (name and ID) and its existing works. A network or authentication error does not mean there is no artist. A verified empty artist list during connection testing does not authorize registration. Do not change competing service configurations, register, create music, or spend credits as a connection test. Recovery steps by host: https://noumi.cc/api-docs#troubleshooting.

Use [song](../song/SKILL.md) only when the user requests actual creation. Installation and authorization are separate from paid creation. Content version 5.1.2; packaged plugin 5.1.2.
