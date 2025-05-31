##Arthur Soares Gardim  -  14526

# Clone, Push e Pull no Git

## Clonando um Repositório

O comando `git clone` permite criar uma cópia local de um repositório remoto. Para clonar um repositório:

1. Acesse o repositório no GitHub que deseja clonar
2. Clique no botão "Code" e copie a URL do repositório

![Clonar repositório](./imagens/Clonar%20Repositório.png)

3. No terminal, navegue até a pasta onde deseja clonar o repositório e execute:

```bash
git clone <URL-do-repositório>
```

## Push: Enviando Alterações para o Repositório Remoto

Após fazer alterações locais e realizar commits, você precisa enviar essas mudanças para o repositório remoto:

```bash
# Enviar alterações do branch atual
git push origin <nome-do-branch>

# Exemplo para o branch main
git push origin main
```

### Boas Práticas para Push

1. Sempre faça pull antes de push para evitar conflitos
2. Verifique se todos os arquivos necessários foram commitados
3. Certifique-se de estar no branch correto
4. Confirme se os testes passaram (se aplicável)

## Pull: Atualizando seu Repositório Local

O comando `git pull` busca e integra alterações do repositório remoto para seu repositório local:

```bash
# Atualizar o branch atual
git pull origin <nome-do-branch>

# Exemplo para o branch main
git pull origin main
```

### Situações Comuns

1. **Quando usar Pull:**
   - Ao começar a trabalhar
   - Antes de criar um novo branch
   - Antes de fazer push
   - Quando outros desenvolvedores avisarem sobre atualizações

2. **Resolvendo Conflitos no Pull:**
   ```bash
   # Se houver conflitos, resolva-os e depois:
   git add .
   git commit -m "Resolve conflitos do merge"
   git push origin <branch>
   ```

## Fluxo de Trabalho Típico

```bash
# 1. Atualize seu repositório local
git pull origin main

# 2. Faça suas alterações e commit
git add .
git commit -m "Descrição das alterações"

# 3. Atualize novamente para garantir
git pull origin main

# 4. Envie suas alterações
git push origin main
```

---

Com estes comandos, você pode sincronizar seu trabalho entre repositórios locais e remotos, mantendo um fluxo de trabalho organizado e eficiente.