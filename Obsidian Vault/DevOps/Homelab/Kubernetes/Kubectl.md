### Alias Definition

**Note**: Add an alias for sudo kubectl

```zsh
alias kb = sudo kubectl
```

# Create Namespace

```bash
kb create namespace [NAME]

# SHORTHAND
kb create ns [NAME]
```

# Apply / Delete
```bash
# creating a resource
kb apply -f [filename.yaml]

# DELETING

# By file
kb delete -f [filename.yaml]

# By resource - with label or type in full pod name
kb delete [RESOURCE] -l [LABEL] 

```
# Pods

Basic

```bash
kb get pods
```

- **-w**: watch
- **--show-labels**

# Top

```bash
# detailed resource usage
kb top [RESOURCE]
```
# Describe

detailed description of resources based on namespace
j
```bash
kb describe [RESOURCE] -n [NAMESPACE]
```
**Note**: because pods are ephemeral k3s gives random names, instead of using describe resource full name access it via label with option -l
