# daily-dev

An ongoing record of things I build, learn, and experiment with.

Each dated directory contains:
- a short daily log in `README.md`
- self-contained directories for anything I worked on that day

No fixed challenge length, just continuous practice and building.

add the following to `~/.bashrc` or `~/.zshrc`:

```bash
daily() {
  local root="$HOME/path/to/daily-dev/log"
  local today
  today="$(date +%F)"

  local dir="$root/$today"

  mkdir -p "$dir"

  if [[ ! -f "$dir/README.md" ]]; then
    cat > "$dir/README.md" <<EOF
# $today

## Worked On

## Notes

EOF
  fi

  cd "$dir" || return
}
```

---



