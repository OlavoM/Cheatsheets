# Linux

## Significado do terminal
- `username@machinename:(current working directory)$`
- `~` => Diretório home
- `/` => Diretório root

<br>

## Comandos Linux
- `cd directoryname` => (change directory) muda para o diretório especificado
- `cd -` => Volta para o diretório anterior
- `cd /` => Vai para o diretório root
- `cd ~` => Vai para o diretório home
- `cd ..` => Vai para o diretório acima

<br>

- `mkdir directoryname` => (make directory) cria um diretório
- `rmdir directoryname` => (remove directory) deleta o diretório

<br>

- `cp arquivo_origem local_destino` => (copy) copia arquivos
- `cp -r arquivo_origem local_destino` => (copy recursive) copia recursivamente,com diretórios e conteúdos
- `rm filename` => (remove) deleta arquivos
- `mv arquivo_origem local_destino` => (move) move arquivos

<br>

- `sudo comando` => Diz ao SO que o comando deve ser executado com o superusuário root

<br>

- `ls` => (list) exibe os arquivos do diretório
- `ls -l` => Exibe em formato de lista, com informações 
- `pwd`  => (print working directory) exibe o diretório atual

<br>

- crtl+alt+t => Abre o terminal
- crtl+l => (comando clear) limpa a tela
- crtl+shift+c => Copia no terminal
- crtl+shift+v => Cola no terminal
- setas do teclado => Caminham pelos comandos anteriores
- TAB => Auto-completa
- `exit` => Fecha o terminal

<br>

- `apt` => (Advanced Package Tool) gerenciador de pacotes do Debian
- `apt-cache search packagename` => Procura no cache do apt o pacote especificado
- `apt-get` => Modo para instalar (também é possivel utilizar somente apt)
- Usar somente `apt` ao invés de `apt-get` é uma alternativa mais recente
- `sudo apt-get` => As alterações afetarão todos os usuários, é necessário que o root faça isso
- `sudo apt-get install packagename` => Instala o pacote e suas dependências, se já instalado, atualiza
- `sudo apt-get remove packagename` => Remove o pacote de forma limpa, junto com dependências não necessárias
- `sudo apt-get purge packagename` => Remove junto com os arquivos de configuração
- `sudo apt-get update` => Atualiza o cache do apt-get
- `sudo apt-get upgrade` => Atualiza todos os pacotes
- `sudo apt-get clean` => Limpa o cache do apt-get
- `sudo apt dist-upgrade` => Atualiza a distro

<br>

- `... | less` => Canaliza a saída do comando, usa-se teclas para navegar na lista e "q" para sair, passa a informação do primeiro processo para o less através do pipe "|"

<br>

- `sudo nano filename` => Inicia o editor de texto nano com permissões de root e abre o arquivo especificado

<br>

- `comando &` => Executa o serviço no bg (background)
- `fg` -> Traz o serviço do bg para o fg (foreground)

<br>

- `sudo passwd username` => Alterar senha no Linux

<br>

- `tar -xzvf arquivo.tar.gz` => Descompacta tar.gz
- `tar -czvf arquivo.tar.gz diretorio_para_compatar` => Compacta como tar.gz

<br>

- `whoami` => Printa o usuário atual

<br>

- `id -g -n` => Printa o grupo atual

<br>

- `lsb_release -a`=> Checka a versão do Ubuntu

<br>

## Remote Desktop xdrp (adaptação de protocolo windows)
- `sudo apt-get install xrdp`
- `hostname -I` (e anota o IP)
- Abre o "Conexão de Área de Trabalho Remota" no Windows e conecta

<br>

## GCC
- `gcc filename.c -o newFilename -o0` => -o0 -o1 -o2 -o3 são graus de otimização
- `.\newFilename` => Roda o executável
- `time .\newFilename` => Tempo de execução do programa

<br>

## Bug do Raspberry Configuration no BerryBoot
```
sudo blkid
Copy the UUID for /dev/mmcblk0p1 (sem aspas)
sudo nano /etc/fstab
Add this line: UUID=paste_from_above /boot vfat defaults 0 2
Save the file
Now it will stick after reboot
```

<br>

## Fixar IP do Raspberry
- `ifconfig`
- Localize as informações do IP do wlan0 (inet addr, etc)
- `sudo nano /etc/dhcpcd.conf`
- Escreva:
```
interface wlan0
static ip_address=192.168.1.101(<-ip) /24
static routers=192.168.1.1
static domain_name_servers = 192.168.1.1 8.8.8.8
```
- Depois salva e reinicia