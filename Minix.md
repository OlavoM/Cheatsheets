# Minix

## Testar internet
- ` ping -c 3 www.google.com `

<br>

## Atualizar
- ` pkgin up `
- ` pkgin_sets `

<br>

## Clonar código fonte:
- ` cd usr `
- ` git clone git://git.minix3.org/minix src `

<br>

## Alterar o código do SO:
- após alterar em src
- ` cd /usr/src `
- ` make `
- ` cd /usr/src/releasetools `
- ` make hdboot `
- ` reboot `
- escolher a opção 2 (latest minix)

<br>

## Compilar e rodar código C
- ` cc NomeDoArquivo.c `
- ` ./a.out `

<br>

# Cores do cursor (video.h):
- ` 0x0000 --> BLACK `
- ` 0x0100 --> BLUE `
- ` 0x0200 --> GREEN `
- ` 0x0300 --> LIGHT BLUE `
- ` 0x0400 --> RED `
- ` 0x0500 --> MAGENTA `
- ` 0x0600 --> ORANGE/YELLOW/SHIT `
- ` 0x0700 --> LIGHT GRAY `
- ` 0x0800 --> GRAY `
- ` 0x0900 --> BLUE PURPLE `
- ` 0x0A00 --> LIGHT GREEN `
- ` 0x0B00 --> CIAN `
- ` 0x0C00 --> LIGHT RED `
- ` 0x0D00 --> VIOLET `
- ` 0x0E00 --> LIGHT YELLOW `
- ` 0x0F00 --> WHITE `