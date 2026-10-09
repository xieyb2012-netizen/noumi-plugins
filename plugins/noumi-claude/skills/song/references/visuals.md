<!-- Generated from agent-kit; content 5.1.1. Edit canonical sources, then run node scripts/build-agent-kit.mjs. -->

# Cover and artist visuals

## Song cover

`coverDescription` is optional. Derive a simple, executable visual direction from the song's intent, lyrics, planned sound, and artist context. Missing art preferences are normally a creative choice the agent can make without asking.

The current purpose takes priority over general visual preferences. A child's gift may call for playful art without making that the owner's lasting visual taste. Personal memories and third-party details are not automatically authorized for cover art: use only relevant details the owner is willing to include, and do not invent their real likeness, life history, or achievements.

Choose a subject or abstract idea, its visual relationship or action, a medium, and useful light/color details. A few relevant details are enough. Close-ups, landscapes, people, objects, original graphics, and abstraction can all work; do not default every song to the same genre cliché. Think of alternative directions if useful, then submit one description with the song. This planning does not require generating several images, assigning scores, or designing automatic typography.

Current cover delivery requirements: 方形构图；单幅一张，不要多格拼贴、宫格或分屏；不要文字、字母、数字、水印或 logo. Do not claim to have heard the audio when choosing art before generation. A ready song can be delivered while its cover is still pending. Do not trigger an extra paid image request to solve polling trouble.

## Artist avatar

The avatar describes the long-lived artist, not the current song. `visualIdentity` is optional; omission does not block music creation. The registration/profile path stores the description; usable descriptions contain at least 20 characters. Keep the description within the active schema limits.

Use a figure, mask/object, original graphic symbol, or abstraction as appropriate. Choose a recognizable idea and explain what should be drawn. No type is mandatory. Do not ask for a portrait merely because the artist makes pop music.

The platform appends only these delivery requirements:

1. 方形 (square 1:1).
2. 单幅一张，不要多格拼贴、宫格或分屏，不要边框.
3. 不要文字、字母、数字、水印.
4. 不要第三方品牌标识或商标. Original non-letter graphic symbols are allowed.

除此之外平台不加任何东西. Style, brightness, background, composition, and subject size remain creative choices.

The following are display consequences, not additional rules — 后果，不是规定，自己取舍:

- The avatar undergoes 圆形裁切 and 圆角方裁切; edge details may disappear.
- It can appear at **24px**, where tiny details become indistinct.
- It appears on 深色的网站 and 浅色的 APP; think about recognition on both backgrounds. A dark palette is a legitimate choice, not a forbidden one.

The current **免费首铸** is paid by the **平台**, happens **自动** when an artist has no avatar and has a usable description, and is **每个音乐人只有这一次**. The trigger is 与先后顺序无关: a description supplied during registration or added later can qualify. Do not invent a separate image request or claim that changing a description gives another free image.

Avatar regeneration is **尚未开放** in the current contract; future paid regeneration would consume **积分** under its own authorization. Changing `visualIdentity` **不会换掉** an existing avatar; it remains 原样保留. Confirm live availability before promising a change.

HTTP profile access, when supported by the current authenticated connection: `GET /api/v1/agent/profile` reads avatar state; `PATCH /api/v1/agent/profile` with `visualIdentity` stores the description. Do not invent an MCP profile-edit tool. Check the returned state, including `needs-identity`, `queued`, `generating`, `has-avatar`, `failed`, or `idle`, and report the actual result without claiming every failure refunds or retries.
