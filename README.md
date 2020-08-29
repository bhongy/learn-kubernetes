# Kubernetes Commands

```sh
k apply -f .
k get all
# see history, debug what's wrong with the pod
k describe po <name>
k describe svc <name>
k get po --show-labels -l release=0.5
k get po -o wide

k delete po --all
k delete po -l app=webapp
k delete -f <filename>
k delete -f .

k logs <pod_name>
k logs -f <pod_name>

k rollout status deploy <name>
k rollout history deploy <name>
k rollout undo deploy <name>
k rollout undo deploy <name> --to-revision=<revision>
```

## Kops

- we use gossip-based cluster so we can skip "Configure DNS" and most of "Cluster State Storage" (just need to create S3 bucket)
