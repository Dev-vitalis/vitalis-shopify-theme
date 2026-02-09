# Conectar tema Vitalis ao Shopify via GitHub

Siga estes passos para subir o tema para o GitHub e conectar na Shopify.

---

## Parte 1: Criar o repositório no GitHub

1. Acesse **https://github.com** e faça login.
2. Clique em **+** (canto superior direito) → **New repository**.
3. Preencha:
   - **Repository name:** `vitalis-shopify-theme` (ou outro nome).
   - **Description:** (opcional) Tema Vitalis para Shopify.
   - Deixe **Public**.
   - **Não** marque "Add a README file".
4. Clique em **Create repository**.

---

## Parte 2: Subir o tema para o GitHub

Abra o **terminal** (ou CMD) na pasta do projeto:

```bash
cd C:\Users\User\Desktop\Gustavo2\Cash
```

Se ainda não tiver Git instalado, baixe em: https://git-scm.com/download/win

### Primeira vez (inicializar e enviar)

```bash
git init
git add .
git commit -m "Tema Vitalis - inicial"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/vitalis-shopify-theme.git
git push -u origin main
```

**Troque** `SEU-USUARIO` pelo seu usuário do GitHub e `vitalis-shopify-theme` pelo nome do repositório que você criou.

Exemplo: se seu usuário é `joao` e o repo é `vitalis-tema`:
```bash
git remote add origin https://github.com/joao/vitalis-tema.git
```

### Se o Git pedir usuário e senha

- **Usuário:** seu usuário do GitHub.
- **Senha:** use um **Personal Access Token** (o GitHub não aceita mais senha normal).
  - GitHub → Settings → Developer settings → Personal access tokens → Generate new token.
  - Marque pelo menos `repo`.
  - Use o token no lugar da senha.

---

## Parte 3: Conectar o repositório na Shopify

1. No **Admin da sua loja Shopify**, vá em **Loja online** → **Temas**.
2. Clique em **Adicionar tema**.
3. Escolha **Conectar com GitHub** (ou "Connect from GitHub").
4. Se aparecer, clique em **Instalar** o app GitHub da Shopify e autorize.
5. Selecione sua **conta** e o **repositório** (ex: `vitalis-shopify-theme`).
6. Escolha o **branch** (geralmente `main`).
7. Confirme. O tema será criado e ligado ao GitHub.

A partir daí, o tema na Shopify fica vinculado a esse repositório.

---

## Parte 4: Atualizar o tema depois

Quando você mudar arquivos do tema (layout/, sections/, templates/, etc.) aqui no projeto:

```bash
cd C:\Users\User\Desktop\Gustavo2\Cash
git add .
git commit -m "Descrição da alteração"
git push
```

Na Shopify:

- Em **Temas**, o tema conectado ao GitHub mostrará que há atualizações (ou você pode abrir o tema e publicar a versão mais recente, conforme a interface).
- Use **Publicar** quando quiser que essa versão vire a tema ativo da loja.

---

## Resumo

| Passo | Onde | Ação |
|-------|------|------|
| 1 | GitHub | Criar repositório novo (vazio) |
| 2 | Terminal (pasta Cash) | `git init`, `add`, `commit`, `remote add`, `push` |
| 3 | Shopify Admin | Temas → Adicionar tema → Conectar com GitHub → escolher repo e branch |
| 4 | Daqui em diante | Editar tema na raiz → `git add`, `commit`, `push` → publicar na Shopify quando quiser |

---

## Problemas comuns

**"Git não é reconhecido"**  
Instale o Git: https://git-scm.com/download/win e reinicie o terminal.

**"Support for password authentication was removed"**  
Use um Personal Access Token do GitHub no lugar da senha.

**"Conectar com GitHub" não aparece**  
Confirme que está em Loja online → Temas → Adicionar tema; a opção pode estar como "Connect from GitHub" ou dentro de "More themes".

**Tema não atualiza na Shopify**  
Dê `git push` no repositório e, na Shopify, abra o tema conectado e use a opção para publicar/atualizar a partir do GitHub.
