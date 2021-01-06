# Demand Development Platform

Kustomize files for deploying the open source Reaction Commerce platform on top of Kubernetes/OpenShift.

## Requirements

- [Kustomize](https://kubernetes-sigs.github.io/kustomize/)

## Usage

Clone repo and run `kustomize build` from the root or a specific directory to generate raw YAMLs for CI pipelines.

## Todo

- [ ] Expose ports for remote inspection in dev/test
- [x] Disable TLS in dev for cert-free local development
- [x] Add secrets and configmaps
- [ ] [Get Snapshot Metrics from the Hydra Service][1]
- [ ] Disable hydra admin ingress for live environments
- [ ] Consider [Populate a Volume with data stored in a ConfigMap][2]


[1]: https://www.ory.sh/hydra/docs/reference/api#get-snapshot-metrics-from-the-hydra-service
[2]: https://kubernetes.io/docs/tasks/configure-pod-container/configure-pod-configmap/#populate-a-volume-with-data-stored-in-a-configmap
