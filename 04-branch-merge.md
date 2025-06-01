## Vinicius Pedron

### Branches e Merge
### Introdução
Ao trabalhar com projetos em equipe no Git, é comum que várias pessoas desenvolvam funcionalidades diferentes ao mesmo tempo. Para que isso ocorra de forma organizada e sem conflitos, utilizamos branches (ramificações). Elas permitem criar linhas de desenvolvimento paralelas, que depois podem ser unidas (merge) à branch principal.

## 1. O que são Branches
Uma branch é uma cópia da linha principal do seu projeto (geralmente chamada main) que permite trabalhar em alterações separadamente. Isso evita conflitos enquanto outras pessoas também fazem mudanças no mesmo repositório.

Vantagens de usar branches:

Trabalhar em novas funcionalidades sem interferir na versão principal

Testar ideias ou correções de bugs

Facilitar a colaboração entre vários desenvolvedores

## 2. Como criar uma branch
Para criar uma nova branch no Git:

bash
$ git branch nome-da-branch


bash
$ git branch pagina-contato

## 3. Como mudar para uma branch
Depois de criar uma branch, você precisa mudar para ela para começar a trabalhar:

$ git checkout nome-da-branch

Exemplo:
$ git checkout pagina-contato

Você também pode criar e trocar ao mesmo tempo com:
git checkout -b nome-da-branch

## 4. Como deletar uma branch
Quando a branch já foi mesclada (merge) e você não precisa mais dela, pode deletá-la:

$ git branch -d nome-da-branch

Para forçar a exclusão (mesmo sem merge):
$ git branch -D nome-da-branch

## 5. Como fazer Merge de branches
Para unir (mesclar) as alterações de uma branch secundária com a principal:

Passo a passo:
1. Volte para a branch principal (geralmente main):
$ git checkout main

2. Execute o merge da branch desejada:
$ git merge nome-da-branch

Exemplo:
$ git merge pagina-contato
Se não houver conflitos, o Git fará a mesclagem automaticamente.

## 6. Como lidar com conflitos de merge
Conflitos acontecem quando as duas branches alteram o mesmo trecho de um arquivo.

Exemplo de conflito:

 HEAD
>conteúdo da main

 conteúdo da feature
>pagina-contato

Como resolver:

1.Abra o arquivo com conflito.

2.Edite o trecho conflituoso, decidindo o que manter.

3.Salve o arquivo.

4.Marque como resolvido:
$ git add nome-do-arquivo

5. Finalize com:
$ git commit

## 7. Demonstração completa (exemplo prático)

1. Criar uma nova branch
git checkout -b pagina-contato

2. Fazer alterações no código
echo "Página de contato" > contato.html

3. Adicionar e commitar as mudanças
git add contato.html
git commit -m "feat: adiciona página de contato"

4. Voltar para a main
git checkout main

5. Fazer o merge
git merge pagina-contato
