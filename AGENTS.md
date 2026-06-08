> For Mintlify product knowledge (components, configuration, writing standards),
> install the Mintlify skill: `npx skills add https://mintlify.com/docs`

# Termique documentation — agent instructions

## About this project

- This is the Termique documentation site built on [Mintlify](https://mintlify.com)
- Pages are MDX files with YAML frontmatter
- Configuration lives in `docs.json`
- Related surfaces: desktop app, API backend, mobile companion app, landing page

## Terminology

| Term | Usage |
|------|-------|
| host | A server managed through Termique. Not "server" or "node" unless the context requires it. |
| group | A named collection of hosts for organization. |
| snippet | A saved command or script. Not "command template" or "macro". |
| SSH key | An authentication key pair. Plural "SSH keys". |
| credential | A password or private key used for SSH authentication. |
| session | A live SSH terminal connection. |
| master password | The user's chosen password that protects all stored credentials. |
| DEK | Data Encryption Key — wrapped by the master password, used to encrypt individual credentials. |
| workspace | Not used. Termique is a personal tool with optional team sharing. |
| user | The person using Termique. Not "member" or "customer". |
| sync | The process of mirroring data between local SQLite and the API backend. |

## Voice and style

- Use active voice and second person ("you").
- Keep sentences concise — one idea per sentence.
- Use sentence case for all headings.
- **Bold** for UI elements: Click **Add host**.
- `Code` for file names, commands, paths, ports, hostnames, and any value that could be copy-pasted into a terminal.
- No exclamation marks, no emoji, no hype language.
- Be terse and technical. Termique is a tool for engineers.
- Numbers use numerals without "approximately" or "about": `22`, `2.3 KB/s`, `00:14:32`.

## Content boundaries

- Document only user-facing features. Internal architecture (Rust mutex patterns, db schema internals) belongs in the main repo's `CLAUDE.md` and `docs/`, not here.
- Do not document internal admin-only API endpoints.
- Do not include screenshots of the API backend or database schema unless they are relevant to self-hosting users.
- Security documentation should explain what Termique does (E2EE, master password, DEK wrapping) without detailing the cryptographic primitives or key sizes unless necessary.

## Writing examples

| ✅ Termique voice | ❌ Avoid |
|---|---|
| Add host | Let's add your first server! |
| connection refused — port 22 | Oops! Something went wrong 😔 |
| 4 hosts · 1 connected | You have 4 hosts (1 is currently connected) |
| Tap to connect | Click here to start your session |
