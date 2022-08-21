# Kubernetes

## Comandos Básicos

- ` kubectl apply -f volume-manifest.yml` => Cria o volume

- ` kubectl apply -f manifest.yml ` => Cria os serviços do manifest

- ` kubectl --help ` => Exibe ajuda

<br>

## Get
- ` kubectl get all ` => Printa todos os pods, services e statefulset

- ` kubectl get pods ` => Printa todos os pods

- ` kubectl get pods --watch ` => Printa os pods conforme seus estados são alterados

- ` kubectl get svc ` => Printa todos os services

<br>

## Describe
- ` kubectl describe pods ` => Descreve os detalhes dos pods

- ` kubectl describe pv ` => Descreve os detalhes dos persistent volumes

<br>

## Delete
- `kubectl delete pods --all -> Deleta todos os pods

- `kubectl delete pods,service,statefulset,pvc,pv --all ` => Deleta tudo

- `kubectl delete -f manifest.yml ` => Deleta o que subiu com o manifest

<br>

## Terminal

- ` kubectl attach <pod> ` => Abre um terminal no pod

- ` kubectl exec -it  <pod> -- sh ` => Executa, iterativamente, no pod especificado, o comando (shell)

<br>

## Outros
- `kubectl logs <pod> ` => Obtém os logs

- `kubectl port-forward service/<service-name> 30000:10000 ` => Comando pra forçar porta

- `kubectl scale statefulsets <pod> --replicas=5 ` => Escala definindo novo número de replicas

- `kubectl create namespace sfn ` => Cria um novo namespace