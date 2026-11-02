# AGY YouTube

A portable [Agent Skill](https://agentskills.io/) for using the Antigravity CLI (`agy`) to help review YouTube videos, answer questions, and find available captions. It also triggers on a YouTube link alone.

## Install

After this skill is merged into the repository's default branch, install it with an Agent Skills-compatible installer:

```sh
npx skills add mdiloreto/agy-youtube-review
```

This installs into the current project by default. To make the skill available to OpenCode across projects, use `npx skills add mdiloreto/agy-youtube-review -g -a opencode`.

Alternatively, copy the `agy-youtube` directory into your agent's skills directory. OpenCode discovers global skills under `~/.config/opencode/skills/` and `~/.agents/skills/`.

## Requirements and use

- An installed, authenticated `agy` CLI and network access. Run `agy --help` and `agy models` to check your installation.
- Optionally, `yt-dlp` to list and retrieve captions. Availability varies by video, language, and platform restrictions.
- Provide a public YouTube link, or ask for a summary, transcript, or specific analysis. Ask before sharing private or sensitive content with an external service.

AGY's ability to access a given video depends on its installation, model, permissions, and source access; a model-generated response is not proof that a video was watched and is not a verified transcript. Headless AGY may return search results without accessing the video or may deny a tool that needs interactive approval. Use available captions or an interactive, user-approved run in those cases; do not bypass permissions. The skill calls for evidence and honest limitations instead of invented timestamps or quotes. Full media downloads are not automatic.

## License

MIT; see [LICENSE](LICENSE).
