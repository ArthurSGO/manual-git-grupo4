# Branches e Merges no Git

## 1. O que é um Branch?

Um **branch** é como uma ramificação do projeto, onde você pode modificar coisas sem estar realmente mudando o projeto principal. Por padrão, o Git cria um branch chamado `master` (ou `main`) quando você inicializa um repositório.

- Cada branch permite que você trabalhe em paralelo, sem interferir em outras linhas de desenvolvimento.  
- Quando um branch é criado, ele aponta para o mesmo commit que o branch atual.  
- À medida que você faz novos commits, o ponteiro do branch se desloca para o commit mais recente.  

---

## 2. Comandos Básicos de Branch

```bash
# Listar todos os branches locais
git branch

# Criar um novo branch (sem trocar para ele)
git branch <nome-do-branch>

# Criar e trocar para o novo branch
git checkout -b <nome-do-branch>

# Trocar para outro branch existente
git checkout <nome-do-branch>

# Deletar um branch local (quando já foi mesclado)
git branch -d <nome-do-branch>

# Forçar exclusão de um branch local (mesclado ou não)
git branch -D <nome-do-branch>
```

---

## 3. Merge: Integrando Branches

Quando o trabalho em um branch (por exemplo, `feature-x`) está pronto, você normalmente quer mesclá-lo de volta ao branch principal (`main`):

```bash
# 1. Vá para o branch de destino (ex: main)
git checkout main

# 2. Mescle o branch de origem (feature-x)
git merge feature-x
```

---

## 4. Conflitos de Merge

Quando o Git não consegue mesclar automaticamente alterações que afetam as mesmas linhas de um arquivo:

1. Você verá mensagens como:
   ```
   Auto-merging arquivo.txt
   CONFLICT (content): Merge conflict in arquivo.txt
   ```
2. Abra o arquivo conflituoso e resolva as marcas padrão:
   ```diff
   <<<<<<< HEAD
   linha no branch main
   =======
   linha no branch feature-x
   >>>>>>> feature-x
   ```
3. Após resolver, marque como pronto:
   ```bash
   git add arquivo.txt
   git commit -m "mensagem"
   ```

---

## 5. Boas Práticas com Branches e Merges

- **Branch por funcionalidade:** crie um branch para cada nova feature ou correção de bug.  
- **Commits diretos:** faça commits pequenos e temáticos dentro do branch.  
- **Revisão de código:** abra merge requests (Pull Requests) para revisão antes de mesclar.  
- **Limpeza de branches:** delete branches remotos e locais após a mesclagem.  

---

Com estes conceitos e comandos, você estará bem equipado para gerenciar ramificações e mesclagens em seus projetos Git de forma organizada e eficiente!
