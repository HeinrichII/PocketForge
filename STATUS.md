# PocketForge Status

## Hardware
- Samsung Galaxy A23
- 4 GB RAM
- Android with Termux

## Core Stack
- llama.cpp compiled locally
- Qwen2.5-0.5B-Instruct Q4_K_M
- Qwen2.5-1.5B-Instruct Q4_K_M
- Stable context size: 384 tokens

## Local Models
- ~/PocketForge/models/Qwen2.5-0.5B-Instruct-Q4_K_M.gguf
- ~/PocketForge/models/Qwen2.5-1.5B-Instruct-Q4_K_M.gguf

## Current Architecture
- pf-ai is the shared AI engine
- ai delegates to pf-ai fast
- ai-smart delegates to pf-ai smart
- summarize delegates to pf-ai smart
- explain delegates to pf-ai smart
- outline extracts full-file headings and bullet points without AI
- review performs a Bash syntax check, then delegates excerpt analysis to pf-ai smart
- Direct prompts use single-turn mode
- Interactive prompts remain available
- Piped input is supported

## Offline Status
- Model loading uses local GGUF files
- Normal inference requires no network access
- Offline operation has been tested successfully

## Working Commands
- ai
- ai-smart
- pf-ai
- project
- pf
- note
- todo
- review
- summarize
- explain
- outline

## Completed Milestones
- Compiled llama.cpp locally
- Downloaded and tested two GGUF models
- Built fast and smart launchers
- Created project dashboard
- Built note and todo commands
- Created shared pf-ai engine
- Migrated ai and ai-smart to pf-ai
- Migrated summarize to pf-ai
- Migrated explain to pf-ai
- Migrated review to pf-ai
- Added deterministic full-file outline command
- Tested chunked AI summarization and rolled it back due to unreliable paraphrasing
- Added deterministic Bash syntax checking to review
- Added single-turn and piped-input support
- Severed Hugging Face runtime dependency
- Verified fully offline inference

## Current Limitations
- Effective context remains small at 384 tokens
- summarize and explain inspect only short file excerpts
- review analyzes only the first 20 lines after syntax checking
- Small models may ignore requested bullet limits or make minor wording errors
- Chunked AI summaries may alter or invent technical meaning
- outline provides reliable extractive coverage but does not compress content

## Next Refactor
- Add chunked file processing
- Improve project memory
- Improve review coverage beyond the first 20 lines

## Roadmap
- Better project memory
- Chunked file analysis
- Script review improvements
- Log explanation
- One-shot AI commands
- Automatic project loading
- Search across project notes
- Optional voice support

## Safety Rule
Do not delete cached models or project files without explicit review and direction.

## Last Updated
2026-07-12
