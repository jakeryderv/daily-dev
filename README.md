# daily-dev

An ongoing record of things I build, learn, and experiment with.

Each dated directory contains:
- a short daily log in `README.md`
- self-contained directories for anything I worked on that day

No fixed challenge length, just continuous practice and building.

add the following to `~/.bashrc` or `~/.zshrc`:

```bash
daily() {
  local dir="$HOME/daily-dev/log/$(date +%F)"
  mkdir -p "$dir"
  cd "$dir" || return
}
```

---



