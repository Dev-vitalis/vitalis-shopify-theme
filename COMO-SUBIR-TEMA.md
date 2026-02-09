# Como subir o tema para a Shopify

O tema está **na raiz** do projeto (`layout/`, `sections/`, `templates/`, `assets/`, `config/`). Você edita aí e depois envia para a Shopify de um destes jeitos.

---

## Opção 1: Enviar ZIP (a mais fácil)

1. **Criar o ZIP**
   - Abra a pasta do projeto (Cash) no explorador de arquivos.
   - Selecione **só as pastas do tema**: `assets`, `config`, `layout`, `sections`, `templates` (e os arquivos dentro delas). Não inclua README, .git, etc.
   - Clique com o botão direito → **Enviar para** → **Pasta compactada (ZIP)**.
   - Dê um nome, por exemplo: `tema-vitalis.zip`.

2. **Enviar na Shopify**
   - Admin da loja → **Loja online** → **Temas**.
   - **Adicionar tema** → **Enviar arquivo ZIP**.
   - Escolha o `tema-vitalis.zip` e aguarde o envio.
   - Depois: **Personalizar** (se quiser) e **Publicar**.

Sempre que mudar algo no tema, zip de novo e envie de novo (ou use a opção 2).

---

## Opção 2: Conectar com GitHub

1. **Criar repositório no GitHub**
   - github.com → New repository (ex: `vitalis-tema`).
   - Não marque “Add README” se for subir o tema (a raiz do repo será o tema).

2. **Subir o tema para o GitHub**
   - No seu PC, na pasta do projeto (Cash), onde o tema já está na raiz (`layout/`, `sections/`, etc.):
   - Inicialize git (se ainda não tiver):  
     `git init`
   - Adicione o remoto:  
     `git remote add origin https://github.com/SEU-USUARIO/vitalis-tema.git`
   - Commit e push:  
     `git add .`  
     `git commit -m "Tema Vitalis"`  
     `git push -u origin main`
   - A raiz do repo já é o tema (assets, config, layout, sections, templates).

3. **Conectar na Shopify**
   - Admin → **Loja online** → **Temas**.
   - **Adicionar tema** → **Conectar com GitHub**.
   - Autorize e escolha o repositório e o branch (ex: `main`).
   - O tema passa a ser esse repositório; alterações no GitHub você publica pela própria Shopify quando quiser.

---

## Opção 3: Shopify CLI (terminal)

1. Instale:  
   `npm install -g @shopify/cli @shopify/theme`

2. Na pasta do projeto (raiz, onde estão layout/, sections/, etc.):  
   `shopify theme push`

3. Faça login na Shopify quando pedir; o tema sobe para a loja.

---

## Resumo

| Método   | Quando usar                          |
|----------|--------------------------------------|
| **ZIP**  | Quer algo rápido, sem GitHub/CLI.   |
| **GitHub** | Quer versionar e sincronizar com a loja. |
| **CLI**  | Quem já usa terminal e Node.         |

Recomendação: comece com **ZIP**; se quiser manter tudo no GitHub e sincronizar, use **GitHub**.
