# Curso de kubernetes básico utilizando o minikube
Arquivos criados durante as aulas e disponibilizados para os alunos

## Comandos utilizados com frequência no curso

## Criar namespace:
~~~bash
kubectl create namespace <nome-do-namespace>
~~~

## Aplicar um arquivo no formato yaml no cluster
~~~bash
kubectl apply -f <nome-do-arquivo>
~~~

## Listar os pods de um namespace
~~~bash
kubectl get pods -n <nome-do-namespace>
~~~

## Deletar um pod
~~~bash
kubectl delete -f <nome-do-arquivo>
~~~
ou
~~~bash
kubectl delete pod <nome-do-pod> -n <nome-do-namespace>
~~~

## Descrever um pod ou qualquer outro objeto do kubernetes
~~~bash
kubectl describe pod <nome-do-pod> -n <nome-do-namespace>
~~~

## Logar dentro de um container com um só container
~~~bash
kubectl exec -ti <nome-do-pod> -n <nome-do-namespace> sh
~~~

## Logar dentro de um container com mais de um container
~~~bash
kubectl exec -ti <nome-do-pod> -c <nome-do-container> -n <nome-do-namespace> sh
~~~
## Verificar os logs de um pod com um só container
~~~bash
kubectl logs -f <nome-do-pod> -n <nome-do-namespace> 
~~~

## Verificar os logs de um pod com um só container
~~~bash
kubectl logs -f <nome-do-pod> -c <nome-do-container> -n <nome-do-namespace> 
~~~
