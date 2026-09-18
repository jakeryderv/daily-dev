# daily-dev

An ongoing record of things I build, learn, and experiment with.

zero AI work in this repo, goal is to learn, practice, and write all of this myself

---

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

use `tags:` to link topics/concepts, and `projects:` to link the independent projects worked on

daily/one-off projects live in the daily dir, ongoing ones land in `projects/` in root dir, so these daily readme's can link both
