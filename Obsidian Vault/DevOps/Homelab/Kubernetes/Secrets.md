Docs:  [https://kubernetes.io/docs/concepts/configuration/secret/]

we can make a secrets yaml file to store api keys and refrence them in our deployment file
to access env vars within our app

# Flow
#### Make secret.yaml file
```yaml
apiVersion: v1
kind: Secret
metadata:
  name: activepieces-api-keys
  namespace: automation
stringData:
  github-token: "secret_key"  
```
#### Apply it

***Note***: we are using the kb alias defined in [[Kubectl#Alias Definition]]]
```bash
kb apply -f secret.yaml
```

#### Configure the deployment to reference secret

```yaml
- name: AP_GITHUB_TOKEN
  valueFrom:
	  secretKeyRef:
		  name: activepieces-api-keys
		  key: github-token
```

### Rollout

```bash
kb rollout restart deployment activepieces -n namespace
```