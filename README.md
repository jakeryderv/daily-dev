# daily-dev

An ongoing record of things I build, learn, and experiment with.

Each dated directory contains:
- a short daily log in `README.md`
- self-contained directories for anything I worked on that day

add the following to `~/.bashrc` or `~/.zshrc`:

```bash
daily() {
  local dir="$HOME/daily-dev/log/$(date +%F)"
  mkdir -p "$dir"
  cd "$dir" || return
}
```

use minimal template & metadata for scripting later:

```markdown
---
date: 2026-09-18
tags:
  - python
  - agents
  - rust
projects:
  - agent-test
  - rust-cli
---

# 2026-09-18

## Worked On

- `agent-test/` — experimented with tool calling
- `rust-cli/` — practiced argument parsing

## Learned

- ...
- ...

## Notes

- ...
```
