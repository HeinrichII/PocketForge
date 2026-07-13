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

## Completed Milestones
- Compiled llama.cpp locally
- Downloaded and tested two GGUF models
- Built fast and smart launchers
- Created project dashboard
- Built note and todo commands
- Built review, summarize, and explain helpers
- Created shared pf-ai engine
- Migrated ai and ai-smart to pf-ai
- Migrated summarize to pf-ai
- Severed Hugging Face runtime dependency
- Verified fully offline inference

## Current Refactor
- Migrate explain to pf-ai
- Improve review for limited context
- Add safer chunked file processing

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
