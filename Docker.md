# Docker

## Comandos Gerais
- ` sudo docker ps ` => Lista os container em execução
- `docker --version` => Exibe a versão do docker instalado
- `docker exec -it <container-name> /bin/bash` => executa (iterativamente) um terminal bash dentro do container especificado

<br>

## Instalar e Desinstalar (Linux - Ubuntu)
- Instalar (Usar este script é o método mais simples):
```
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh ./get-docker.sh
```
- Desintalar : `sudo apt-get purge docker-ce docker-ce-cli containerd.io`