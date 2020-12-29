# Demand Development Platform

Kustomize files for deploying the open source Reaction Commerce platform on top of Kubernetes/OpenShift.

## Requirements

- [Kustomize](https://kubernetes-sigs.github.io/kustomize/)

## Usage

Clone repo and run `kustomize build` from the root or a specific directory to generate raw YAMLs for CI pipelines.

## Todo

- [ ] Expose ports for remote inspection in dev/test
- [ ] Disable TLS in dev for cert-free local development
- [ ] Add secrets and configmaps
- [ ] [Get Snapshot Metrics from the Hydra Service](https://www.ory.sh/hydra/docs/reference/api#get-snapshot-metrics-from-the-hydra-service)
