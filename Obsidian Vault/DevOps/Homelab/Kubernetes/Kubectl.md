### Alias Definition

**Note**: Add an alias for sudo kubectl

```zsh
alias kb = sudo kubectl
```



# Pods

Basic

```bash
kb get pods
```

- **-w**: watch
- **--show-labels**






# Describe

detailed description of resources

**Note**: because pods are ephemeral k3s gives random names, instead of using describe resource full name access it via label with option -l
