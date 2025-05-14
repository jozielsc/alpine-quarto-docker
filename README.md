# Quarto via Docker no Alpine Linux

Este repositório fornece um script para executar o [Quarto](https://quarto.org) via Docker no Alpine Linux, permitindo usar o comando `quarto` diretamente no terminal.

## 📦 Dependências

- Docker [Wiki Alpine Linux](https://wiki.alpinelinux.org/wiki/Docker)
- Instale as seguintes dependências:

```sh
apk add --no-cache bash git coreutils
```

## 🚀 Instalação

Clone este repositório e crie um link simbólico para o script:
```sh
git clone https://github.com/jozielsc/alpine-quarto-docker.git .
ln -s quarto-docker/quarto /usr/local/bin/quarto
chmod +x quarto-docker/quarto
```

Recarrege o shell
```sh
exec bash
```

## ✅ Teste

Execute:
```sh
quarto --version
```
Você deverá ver a versão do Quarto sendo exibida a partir da imagem Docker utilizada.

## 💡 Exemplos de uso

```sh
quarto render documento.qmd
quarto preview
```

O script cuida automaticamente do uso do Docker para que você possa trabalhar como se tivesse o Quarto instalado localmente.

