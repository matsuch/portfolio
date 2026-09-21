# Portfólio — Matheus Rosa Such

Site estático de página única: produto, IA, dados e CRM, com cases profissionais,
projetos pessoais e um case estratégico interativo em 10 etapas.

## Conteúdo

| Arquivo | Descrição |
| --- | --- |
| `index.html` | A página inteira — HTML, CSS e JS em um único arquivo, sem build e sem dependências. |
| `vercel.json` | Configuração de deploy: `cleanUrls`, cabeçalhos de segurança e cache do HTML. |

A única dependência externa é a fonte servida pelo Google Fonts
(Bricolage Grotesque, Geist e Geist Mono). Tudo o mais é inline.

Recursos da página: tema claro/escuro (segue o sistema, com alternância manual),
idioma PT/EN, navegação por teclado no case interativo e `prefers-reduced-motion`
respeitado em todas as animações.

## Rodando localmente

Abrir `index.html` no navegador já basta. Para servir por HTTP:

```bash
python3 -m http.server 8000
# http://localhost:8000
```

## Deploy na Vercel

Não há etapa de build — a Vercel serve a raiz do repositório como estático.

O projeto `matheus-such` já está conectado a este repositório: cada push na
branch de produção gera um deploy de produção, e as demais branches geram
deploys de preview. Framework Preset fica em **Other**, com Build e Output
vazios.

Deploy manual pela CLI, se precisar:

```bash
npx vercel        # preview
npx vercel --prod # produção
```
