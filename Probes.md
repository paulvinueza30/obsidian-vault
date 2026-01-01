- Live on every node
- Constantly checking status of a node
- Added at the container level
- Different methods of probing some images might not have http requests

**2 Main Kinds**
1. Readiness
2. Liveness

## Liveness

Checks to see if the pod is dead

## Readiness

Checks to see if pod is ready

- Pod is not added to the LoadBalancer until it passes **this** probe

