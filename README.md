Utilizei o k3d pois já o conhecia antes, portanto, para poder rodar o kubernetes localmente basta instalar o k3d e rodar os seguintes comandos:

```sh
$ k3d cluster create cluster-desafio-2-full-cycle -p "3001:30000@loadbalancer"
$ # ir até o diretório k8s, onde está localizado o arquivo deployment.yml
$ kubectl apply -f .
```

por fim, basta aguardar a api subir e acessar a aplicação em localhost:3001

Se houver uma forma de bindar uma porta local para uma nodePort utilizando o Kind, basta bindar na porta `30000`.
