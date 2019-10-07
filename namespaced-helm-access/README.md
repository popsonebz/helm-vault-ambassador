kubectl apply -f role.yaml

helm init --service-account stratus-tiller --tiller-namespace stratus-dev


helm install --name stratus-be-dev --namespace stratus-dev --tiller-namespace stratus-dev -f Desktop/bug_out/gitlab/values.yml gitlab/gitlab-omnibus


helm install stable/vault-operator --namespace stratus-dev --tiller-namespace stratus-dev

helm list --tiller-namespace stratus-dev

helm delete --purge --tiller-namespace stratus-dev
