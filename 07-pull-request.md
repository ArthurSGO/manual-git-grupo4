# GitHub e Pull Requests

## O que é um Pull Request (PR)?

Um Pull Request (PR) é uma solicitação para que suas alterações em uma branch (geralmente no seu fork ou branch de trabalho) sejam revisadas e integradas à branch principal (geralmente a `main`). É uma etapa essencial em projetos colaborativos, pois permite que outros revisem e discutam as mudanças antes de integrá-las.

---

## Etapas para Criar um Pull Request

### 1. Crie uma branch
```bash
git checkout -b minha-branch
```

### 2. Faça alterações no seu módulo
Adicione o conteúdo do seu arquivo.

### 3. Adicione e faça commit
```bash
git add .
git commit -m "feat: adiciona conteúdo x"
```

### 4. Verifique o nome da branch principal do seu fork
```bash
git branch
```

### 5. Volte para a branch principal do seu fork
```bash
git checkout main 
```

### 6. Faça merge da sua branch modificada
```bash
git merge minha-branch
```

### 7. Envie para o GitHub
```bash
git push
```

### 8. Crie o Pull Request
- Acesse o repositório no GitHub
- Clique em “Compare & pull request”
- Escreva um título e descrição claros
- Envie para revisão

---

## Como Fazer uma Revisão de Código

### 1. Acesse o Pull Request de um colega

No GitHub, vá até a aba **Pull Requests** e selecione um PR aberto.

### 2. Leia o conteúdo com atenção
- Verifique se está bem explicado
- Veja se há erros de digitação ou comandos faltando
- Sugira melhorias se necessário

### 3. Comente ou aprove o PR

Você pode:

- Comentar trechos específicos com sugestões
- Clicar em **"Approve"** se estiver tudo certo
- Clicar em **"Request changes"** se precisar de ajustes