instead of copying a directory to two different places, use a symlink to make a pointer to that directory instead

```bash
ln -s [SOURCE] [DEST]
```

**Note**: Use full path for source and dest for it properly work.

## Verify

**Long Listing Format**

```bash
ls -l path[[Systemd]]
```

**Show Directories**

```bash
ls -d path
```

-> : means theres a link

