# daily-dev

An ongoing record of things I build, learn, and experiment with.

## Structure

```text
daily-dev/
├── README.md
├── projects/
└── log/
    ├── 2026-09-18/
    │   ├── entry.yaml
    │   ├── README.md
    │   └── experiment/
    └── 2026-09-19/
        ├── entry.yaml
        └── README.md
```

* `projects/` contains ongoing projects and experiments that span multiple days.
* `log/` contains one directory per day using the `YYYY-MM-DD` format.
* `entry.yaml` contains structured metadata that can be queried or analyzed later.
* `README.md` contains freeform notes about what I worked on, learned, or want to revisit.
* Small, one-off experiments can live directly inside the relevant daily directory.

## Daily Entry

A minimal `entry.yaml`:

```yaml
date: 2026-09-18
projects: []
tags: []
```

The daily `README.md` can stay lightweight:

```markdown
# 2026-09-18

## Worked On

- ...

## Notes

- ...
```

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

