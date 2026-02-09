# Vitalis - Loja Shopify

Tema desenvolvido aqui e conectado à Shopify via **GitHub**.

## Fluxo

1. **Editar** o tema aqui na raiz do projeto (`layout/`, `sections/`, `templates/`, etc.).
2. **Enviar** as mudanças para o GitHub (`git add`, `commit`, `push`).
3. **Publicar** na Shopify a partir do tema conectado ao GitHub.

## Guia completo: GitHub + Shopify

Siga o passo a passo em:

**📖 [GITHUB-SHOPIFY.md](GITHUB-SHOPIFY.md)**

Lá está:
- Criar repositório no GitHub
- Subir o tema (comandos `git`)
- Conectar na Shopify (Conectar com GitHub)
- Como atualizar o tema depois

## Estrutura

O **tema está na raiz** do repositório (assim a Shopify reconhece ao conectar com GitHub):

```
Cash/
  layout/             ← Tema Shopify (edite aqui)
  sections/
  templates/
  assets/
  config/
  GITHUB-SHOPIFY.md   ← Guia GitHub + Shopify
  README.md
```

## Comandos rápidos (depois de configurado)

```bash
cd C:\Users\User\Desktop\Gustavo2\Cash
git add .
git commit -m "Sua mensagem"
git push
```

Depois, na Shopify: Temas → tema conectado → publicar atualização.
