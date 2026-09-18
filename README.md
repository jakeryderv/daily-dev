# daily-dev

An ongoing record of things I build, learn, and experiment with.

## Structure

```text
daily-dev/
├── README.md
├── projects/
└── log/
    ├── 2026-09-18/
    │   ├── README.md
    │   └── experiment/
    └── 2026-09-19/
        └── README.md
```

* `projects/` contains ongoing projects or experiments that span multiple days.
* `log/` contains one directory per day using the `YYYY-MM-DD` format.
* Each daily `README.md` contains YAML front matter for structured metadata and Markdown for freeform notes.
* Small, one-off experiments can live directly inside the relevant daily directory.

## Daily Entry

A minimal daily `README.md`:

```markdown
---
date: 2026-09-18
projects: []
tags: []
---

# 2026-09-18

## Worked On

- ...

## Notes

- ...
```

The front matter keeps basic metadata easy to parse or query later, while the rest of the file stays flexible and human-readable.

## Shell Helper

Add the following to `~/.bashrc` or `~/.zshrc`:

```bash
daily() {
  local dir
  dir="$HOME/daily-dev/log/$(date +%F)"

  mkdir -p "$dir"
  cd "$dir" || return
}
```

Then run:

```bash
daily
```

to create today's log directory if needed and move into it.
