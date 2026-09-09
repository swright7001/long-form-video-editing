# Long-form Video Editing

A reusable Codex skill for any creator editing podcasts, interviews, commentary, tutorials or product videos. Produce polished full episodes, captioned short clips, or both. Originally developed for HMH, SimpMe and Denominated; those channels are optional examples, not setup requirements.

## Get started

1. Obtain the complete repository using GitHub access or an archive supplied by the owner.
2. Put the repository folder, named `long-form-video-editing`, in your Codex skills directory: `$CODEX_HOME/skills` if configured, otherwise `~/.codex/skills`. Keep `SKILL.md`, `references/`, `assets/` and `agents/` together. Do not overwrite a previous installation without inspecting it.
3. Start a new Codex task in your footage project and invoke `$long-form-video-editing`, supplying a local video or accessible link and what you want produced.

Example prompt:

> Use $long-form-video-editing for my channel, Garden Notes. Edit this interview into a clean full episode and three vertical shorts. Use my attached branding and cyan-underlined captions on the shorts. Keep source credit visible and processing local. Footage: [provide path or link].

Codex records your preferences in a project-local channel profile. You can customize the channel name, logos, colors, captions, pacing, durations and formats. Included yellow-highlight and cyan-underline designs are starters; your preferences override them. The SimpMe reference images are AI-generated layout examples, not footage to use in your exports.

## Automatic first-use setup

No separate dependency prompt is needed. On first use, Codex shows setup progress, checks FFmpeg/ffprobe, and sets up Python/local transcription or a video downloader only when your edit needs them. Local speech models download on demand and may take time and disk space. Installing the skill folder alone does not launch a background installer or popup—the check runs inside your Codex task. See [the setup procedure](references/tool-setup.md).

Versions are resolved at installation time and recorded in your project. “Latest” is the latest compatible stable package from the selected distribution; OS repositories can lag upstream. Working tools are not automatically upgraded on every edit.

## What you need

- Codex with access to your media and permission to run the required local tools.
- FFmpeg/ffprobe or an equivalent capable video editor for processing and export.
- Existing transcripts or a configured transcription tool for transcript-led editing. Local ASR software/models may require separate setup and adequate compute/storage.

This is an instructional skill with an automatic setup workflow, not a bundled editor or transcription service. When you invoke it, Codex checks your machine and installs missing required tools using the latest compatible stable versions from trusted sources, then verifies they work. Existing working tools are reused. Administrator passwords, installation approvals and other machine restrictions still apply. It requires no particular API key or original creator account; optional cloud processing requires authorization for that provider and material. Another Remotion skill is optional, not required for normal editing.

Original media and earlier exports remain untouched. Publishing is a separate action. Do not commit footage, private transcripts, credentials or project outputs here.

## Repository access

This repository is public. Anyone can clone it or download the complete folder from GitHub; no collaborator invitation is needed.
