# PocketForge Handoff v0.2

## Project Summary

PocketForge is a personal offline AI engineering workspace running on a
Samsung Galaxy A23 using Termux, llama.cpp, and local GGUF models.

The goal is to build a practical AI-assisted terminal environment that
runs locally whenever practical.

## Hardware

-   Samsung Galaxy A23 (SM-A236U)
-   Android
-   \~4 GB RAM
-   Termux

## AI Stack

-   llama.cpp (compiled locally)
-   Qwen2.5-0.5B-Instruct GGUF (fast model)
-   Qwen2.5-1.5B-Instruct GGUF (smart model)
-   Stable launch context: `-c 384`

## Current Commands

-   ai
-   ai-smart
-   project
-   pf
-   note
-   todo
-   review
-   summarize
-   explain

## Workspace

    ~/PocketForge/
        IDENTITY.md (planned)
        STATUS.md
        NOTES.md
        TODO.md
        CHANGELOG.md

## Lessons Learned

-   The 1.5B model is stable on the Galaxy A23 with `-c 384`.
-   Large prompts exceed the effective working context.
-   Loading \~30 lines of a file works reliably for summarize/explain.
-   Large project files should be split into focused documents instead
    of one giant notebook.

## Features Completed

-   Compiled llama.cpp locally.
-   Downloaded and launched two GGUF models.
-   Built custom launchers.
-   Created project dashboard.
-   Built note and todo commands.
-   Built review and explain helpers.
-   Built summarize helper and tuned it to use 30-line chunks.

## Next Refactor

Create a shared AI engine:

    pf-ai

All AI commands should delegate to `pf-ai` so model selection, context
size, and launch parameters exist in one place.

## Future Roadmap

-   pf-ai refactor
-   Better project memory
-   Chunked file processing
-   Script review improvements
-   Log explanation
-   One-shot AI commands
-   Automatic project loading
-   Search across project notes

## Working Style

Preferred workflow:

1.  Build
2.  Test
3.  Fix
4.  Repeat

Keep explanations concise during implementation, but pause periodically
for architecture reviews and progress summaries.

## Personal Note

This project started with a simple question:

> "Can I install Linux on this phone?"

It evolved into building a custom offline AI workstation from scratch.

The collaboration balanced practical engineering with curiosity,
experimentation, and plenty of laughter. Preserve that spirit while
continuing the project.
