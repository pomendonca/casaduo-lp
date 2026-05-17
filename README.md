# casaduo-lp

Landing page estática do [CasaDuo](https://casaduo.app) — plataforma de gestão financeira compartilhada para casais e pessoas que dividem despesas.

## Estrutura

```
casaduo-lp/
├── index.html        # Página principal (hero, features, como funciona, preços)
├── privacidade.html  # Política de Privacidade
├── termos.html       # Termos de Uso
├── lgpd.html         # LGPD & direitos do titular
├── favicon.svg       # Ícone do site
└── vercel.json       # Configuração de deploy (clean URLs, headers de segurança)
```

## Deploy

Hospedada na Vercel como site estático. O `vercel.json` configura:

- **Clean URLs** — `/privacidade` em vez de `/privacidade.html`
- **Headers de segurança** — CSP, X-Frame-Options, Referrer-Policy, Permissions-Policy

Para fazer deploy, basta fazer push para a branch principal — a Vercel detecta automaticamente.

## Desenvolvimento local

Qualquer servidor HTTP estático funciona:

```bash
# Python
python3 -m http.server 3000

# Node (npx)
npx serve .
```

Acesse `http://localhost:3000`.

## Páginas legais

As páginas de privacidade, termos e LGPD refletem o comportamento real do app ([finduo](../finduo)):

- **Exclusão de conta** → anonimização imediata (nome, e-mail, foto, descrições de despesas). Registros financeiros históricos preservados de forma anonimizada por legítimo interesse do parceiro do grupo.
- **Exportação** → disponível em PDF e CSV dentro do app.
- **Encerramento** → requer dissolução do grupo com o parceiro antes da exclusão.
