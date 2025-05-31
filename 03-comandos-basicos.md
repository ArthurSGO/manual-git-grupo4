# Comandos Básicos do Git

> Dedicado a Heloise Henriques Maciel, cuja paixão pelo aprendizado e compartilhamento de conhecimento inspira todos ao seu redor.

## Introdução

O Git é um sistema de controle de versão distribuído que permite rastrear mudanças em arquivos e coordenar o trabalho entre várias pessoas. Este guia apresenta os comandos básicos essenciais para começar a usar o Git efetivamente.

## Comandos Essenciais

### 1. git init

O comando `git init` é o primeiro passo para começar a usar o Git em um projeto.

```bash
git init
```

Este comando cria um novo repositório Git na pasta atual, inicializando o diretório `.git` que contém todos os arquivos necessários para o controle de versão.

**Exemplo de uso:**
```bash
# Navegue até a pasta do seu projeto
cd meu-projeto

# Inicialize o repositório Git
git init
```

### 2. git add

O comando `git add` adiciona arquivos à área de preparação (staging area).

```bash
git add <arquivo>
git add .  # Adiciona todos os arquivos modificados
```

**Exemplos de uso:**
```bash
# Adicionar um arquivo específico
git add README.md

# Adicionar todos os arquivos modificados
git add .

# Adicionar arquivos com extensão específica
git add *.js
```

### 3. git commit

O comando `git commit` salva as mudanças preparadas no histórico do repositório.

```bash
git commit -m "mensagem descritiva"
```

**Exemplos de uso:**
```bash
# Commit básico
git commit -m "Adiciona funcionalidade de login"

# Commit com descrição detalhada
git commit -m "Corrige bug na validação de formulário" -m "Detalhes adicionais sobre a correção"
```

### 4. git status

O comando `git status` mostra o estado atual do seu diretório de trabalho e da área de preparação.

```bash
git status
```

**Exemplo de saída:**
```
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        novo-arquivo.txt
```

### 5. git log

O comando `git log` exibe o histórico de commits do repositório.

```bash
git log
git log --oneline  # Versão simplificada
git log --graph    # Visualização gráfica
```

**Exemplos de uso:**
```bash
# Ver histórico completo
git log

# Ver histórico simplificado
git log --oneline

# Ver histórico com gráfico de branches
git log --graph --oneline --all
```

### 6. git diff

O comando `git diff` mostra as diferenças entre arquivos no diretório de trabalho e na área de preparação.

```bash
git diff
git diff <arquivo>
```

**Exemplos de uso:**
```bash
# Ver todas as mudanças não preparadas
git diff

# Ver mudanças em um arquivo específico
git diff README.md

# Ver mudanças entre commits
git diff commit1 commit2
```

## Melhores Práticas

1. **Commits Atômicos**
   - Faça commits pequenos e focados
   - Cada commit deve representar uma mudança lógica completa

2. **Mensagens de Commit Claras**
   - Use verbos no imperativo
   - Seja específico e descritivo
   - Exemplo: "Adiciona validação de email" em vez de "Adicionando validação"

3. **Frequência de Commits**
   - Faça commits regularmente
   - Não acumule muitas mudanças em um único commit

## Casos de Uso Comuns

### Iniciando um Novo Projeto
```bash
mkdir novo-projeto
cd novo-projeto
git init
git add .
git commit -m "Commit inicial"
```

### Salvando Mudanças Diárias
```bash
git add .
git commit -m "Atualiza documentação e corrige bugs menores"
```

### Verificando o Estado do Projeto
```bash
git status
git diff
git log --oneline
```

## Recursos Adicionais

- [Documentação oficial do Git](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com/)
- [Pro Git Book](https://git-scm.com/book/en/v2)

## Conclusão

Dominar estes comandos básicos do Git é fundamental para um fluxo de trabalho eficiente em desenvolvimento de software. Lembre-se que a prática leva à perfeição, e estes comandos se tornarão naturais com o uso constante.

> "O conhecimento é a melhor herança que podemos deixar." - Heloise Henriques Maciel 