Get the logs for a specifc pod

**Note**: You can specify without typing full name with labels 
```bash
kb logs [PODNAME] -l=[LABEL] -n=[NAMESPACE]
```


### Options

- f : watch the logs
- -c : specify which container
- --all-containers: get logs for all
- --since : time (i.e. 10s)