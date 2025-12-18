
### Show all charts installed

```bash 
helm list -A
```

**Note**: It will not show upgraded app versions it uses what ever is in the chart














# Chart Upgrading

```bash
helm upgrade [RELASE] [CHART] --reuse-values --set
```