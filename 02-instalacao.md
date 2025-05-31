##Arthur Soares Gardim  -   14526

# Como Baixar e Instalar o Git

## Windows

1. Acesse o site oficial do Git: [https://git-scm.com/downloads](https://git-scm.com/downloads)

2. Clique em "Download for Windows"
![Página de download 1](./imagens/Página%20de%20download.png)

3. Clique em "Click here to download" para baixar o instalador
![Página de download 2](./imagens/Página%20de%20download%202.png)

4. Execute o arquivo baixado (.exe)

5. Já no instalador, é recomendado clicar em "next" em quase todas as telas, só é necessário mudar uma opção
- Ao chegar na tela "Choosing the default editor used by Git", escolha o "Use Visual Studio Code as Git's default editor"
![Instalador VSCode](./imagens/Instalador%20VS%20Code.png)

6. Depois disso é só continuar clicando em "next" até o fim do instalador

7. Quando a instalação terminar, você pode escolher entre reiniciar o computador agora ou depois
![Fim da instalação](./imagens/Instalador%20Final.png)

## macOS

### Usando Homebrew (Recomendado)
```bash
# Instale o Homebrew primeiro (se não tiver)
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Instale o Git
brew install git
```

### Usando o Instalador
1. Baixe o instalador mais recente do Git para macOS
2. Execute o pacote .dmg baixado
3. Siga as instruções do instalador

## Linux

### Ubuntu/Debian
```bash
# Atualize os pacotes
sudo apt update

# Instale o Git
sudo apt install git
```

### Fedora
```bash
sudo dnf install git
```

### Arch Linux
```bash
sudo pacman -S git
```

## Verificando a Instalação

Após a instalação, abra o terminal (ou Git Bash no Windows) e execute:

```bash
git --version
```

Você deverá ver algo como:
```
git version 2.40.1
```

## Configuração Inicial

Após instalar o Git, configure seu nome de usuário e email:

```bash
git config --global user.name "Seu nome no github"
git config --global user.email "O mesmo email da sua conta no github"
```

---

Com o Git instalado e configurado corretamente, você está pronto para começar a utilizar o controle de versão em seus projetos!