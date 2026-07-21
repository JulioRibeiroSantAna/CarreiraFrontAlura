# Guia Completo de Git: Branches e Fluxo de Trabalho

## Padrões de Nomenclatura
- **Novas funcionalidades e modificações:** `feat/descricao-da-modificacao` ou `feature/descricao-da-modificacao`
- **Correções de problemas ou bugs:** `fix/descricao-do-problema` ou `bugfix/descricao-do-problema`
- **Correções urgentes direto na branch principal:** `hotfix/descricao-do-problema`

---

## Comandos Essenciais

### Listagem e Navegação
- **Ver branch atual e listar as locais:** `git branch`
- **Acessar e navegar entre branches:** `git switch nome-da-branch`

### Criação e Edição
- **Criar uma nova branch:** `git branch nome-da-branch`
- **Criar e já acessar a branch no mesmo comando (Atalho):** `git switch -c nome-da-branch`
- **Renomear a branch atual:** `git branch -m "novo-nome"`

---

## Gerenciamento de Alterações Temporárias (Stash)
*Útil quando você precisa mudar de branch mas não quer fazer commit de arquivos inacabados.*

- **Guardar alterações temporariamente:** `git stash`
- **Recuperar as alterações guardadas:** `git stash pop`
- **Listar todos os stashes salvos:** `git stash list`
- **Descartar/apagar o stash mais recente:** `git stash drop`

---

## Comandos Mais Usados no Dia a Dia

- **Ver o status dos arquivos (modificados, staged ou não rastreados):** `git status`
- **Ver o histórico de commits de forma resumida e limpa:** `git log --oneline`
- **Ver o que mudou nos arquivos (diferenças) antes de dar o `add`:** `git diff`
- **Atualizar a branch atual baixando as novidades do repositório remoto:** `git pull`

---

## Fluxo de Trabalho Completo (Da Criação ao GitHub)

1. **Atualizar a branch principal:** `git checkout main` e `git pull`
2. **Criar e mudar para a nova branch:** `git switch -c feat/nome-da-sua-feature`
3. **Modificar os arquivos:** Faça as alterações necessárias no seu editor de código e salve-as.
4. **Adicionar os arquivos modificados (Staging):** `git add .`
5. **Criar o Commit:** `git commit -m "feat: descrição curta da alteração"`
6. **Enviar para o GitHub pela primeira vez (Upstream):** `git push -u origin feat/nome-da-sua-feature`
7. **Envios seguintes:** `git push`