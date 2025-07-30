# gpt-context-shell

**gpt-context-shell** is a command-line interface (CLI) wrapper around a GPT-based language model. It aims to create a persistent, evolving memory layer between the user and the AI—one that mimics how human memory works: by retaining core ideas while compressing and abstracting older details over time.

## 🔍 Purpose

This project is designed for users who want more than just a sliding window of context. Instead of resending the entire conversation history every time, this shell builds a long-term memory structure that:

- Records all messages and interactions
- Gradually summarizes older content
- Prioritizes important ideas and discards trivia
- Supports semantic search and hierarchical navigation

## 🧠 Core Ideas

- **Semantic memory:** Builds a tree or graph of ideas that are compressed into summaries over time.
- **Selective forgetting:** Lets users pin key information and allow unimportant context to fade.
- **CLI-first:** All commands happen in the shell—no GUI, just a focused interface for thought and memory.
- **Modular and local:** Runs locally, stores data in human-readable formats like JSON or SQLite.

## 🛠️ Example Commands (planned)

- `say "What's the capital of Spain?"` — Ask GPT something and save both prompt and reply
- `remember "My cat’s name is Charlie"` — Save personal facts without sending to GPT
- `summarize [session|branch|range]` — Condense older entries into a summary
- `recall "cat name"` — Search for relevant facts or entries
- `pin [id]` — Mark a memory as essential (immune to forgetting)
- `forget [id]` — Remove or de-prioritize parts of memory

## 🗂️ Planned Data Structure

Each interaction or memory is stored as a node with:

- `raw_text`
- `summary` (optional)
- `timestamp`
- `importance_score`
- `tags`
- `hash`

Nodes are grouped into branches or topics, with summaries at various levels.

## 💡 Vision

Think of it as your AI assistant’s long-term memory. Over time, it doesn’t just get *bigger*—it gets *sharper*. It forgets noise, retains essence, and builds a structured mental model of your needs, thoughts, and patterns.

## 🔐 Privacy

All data is stored locally. No cloud. No logging to third parties. (Unless you configure it yourself.)

## 🧪 Status

Early prototype. Only scaffolding in place. Design still evolving.

---

Want to contribute, ask questions, or share ideas? Open an issue or start a discussion.
