# Demand Development Platform

Kustomize files for deploying the open source Reaction Commerce platform on top of Kubernetes/OpenShift.

## Requirements

- [Kustomize](https://kubernetes-sigs.github.io/kustomize/)
- [Kubectl](https://kubectl.docs.kubernetes.io/installation/)

## Usage

Clone repo and run `kustomize build` from the root or a specific directory to generate raw YAMLs. Apply build output directly to cluster:

```sh
kustomize build | kubectl apply -f -
```

You should see output like:

```term
configmap/demandcluster-dev-admin-env-config-fhfctc8dh4 created
configmap/demandcluster-dev-api-env-config-696hf5k7m7 created
configmap/demandcluster-dev-hydra-env-config-m4b65gk7ff created
configmap/demandcluster-dev-identity-env-config-hhk5mgtmhm created
configmap/demandcluster-dev-storefront-env-config-4dhf2kc5cm created
secret/demandcluster-dev-admin-env-secrets-6fbm5h468m created
secret/demandcluster-dev-api-env-secrets-tgd5d5d285 created
secret/demandcluster-dev-hydra-env-secrets-86k98f27k9 created
secret/demandcluster-dev-identity-env-secrets-6fbm5h468m created
secret/demandcluster-dev-storefront-env-secrets-gm47dfg97f created
service/demandcluster-dev-admin-service created
service/demandcluster-dev-api-service created
service/demandcluster-dev-hydra-service created
service/demandcluster-dev-identity-service created
service/demandcluster-dev-storefront-service created
deployment.apps/demandcluster-dev-admin-deployment created
deployment.apps/demandcluster-dev-api-deployment created
deployment.apps/demandcluster-dev-hydra-deployment created
deployment.apps/demandcluster-dev-identity-deployment created
deployment.apps/demandcluster-dev-storefront-deployment created
ingress.networking.k8s.io/demandcluster-dev-admin-ingress created
ingress.networking.k8s.io/demandcluster-dev-api-ingress created
ingress.networking.k8s.io/demandcluster-dev-demandcluster-hydra-admin created
ingress.networking.k8s.io/demandcluster-dev-hydra-frontend created
ingress.networking.k8s.io/demandcluster-dev-identity-ingress created
ingress.networking.k8s.io/demandcluster-dev-storefront-ingress created
```

## Todo

- [ ] Ingegrate [Postgres Operator](https://github.com/zalando/postgres-operator)
- [ ] Integrate [MongoDB Operator](https://github.com/mongodb/mongodb-kubernetes-operator)
- [ ] Expose ports for remote inspection in dev/test
- [x] Disable TLS in dev for cert-free local development
- [x] Add secrets and configmaps
- [ ] [Get Snapshot Metrics from the Hydra Service][1]
- [ ] Disable hydra admin ingress for live environments
- [ ] Consider [Populate a Volume with data stored in a ConfigMap][2]


[1]: https://www.ory.sh/hydra/docs/reference/api#get-snapshot-metrics-from-the-hydra-service
[2]: https://kubernetes.io/docs/tasks/configure-pod-container/configure-pod-configmap/#populate-a-volume-with-data-stored-in-a-configmap
