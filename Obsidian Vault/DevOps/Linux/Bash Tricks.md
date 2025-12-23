
## Remove Numbers From Files

**Safe Dry Run**
```bash
for f in *\(*\)*; do echo "Moving: $f  ->  $(echo "$f" | sed -E 's/ ?\([0-9]+\)//')"; done
```

**Actual Rename**

```bash
for f in *\(*\)*; do mv "$f" "$(echo "$f" | sed -E 's/ ?\([0-9]+\)//')"; done
```
