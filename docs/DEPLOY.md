# Deploy — Cloudflare Pages

## Objetivo

Publicar o repositório `jvmasc/saude.opensource` em:

https://saudeopensource.xyz

## Configuração recomendada

No Cloudflare Pages:

- Connect to Git: GitHub
- Repository: `jvmasc/saude.opensource`
- Production branch: `main`
- Framework preset: None
- Build command: deixar vazio
- Build output directory: `/`

## Domínio

Depois de comprar `saudeopensource.xyz`:

1. Adicionar o domínio no Cloudflare.
2. Trocar os nameservers no registrador para os nameservers da Cloudflare.
3. Em Pages, adicionar custom domain:
   - `saudeopensource.xyz`
   - opcional: `www.saudeopensource.xyz`
4. Aguardar emissão automática de HTTPS.

## Checklist pós-deploy

Validar:

- `https://saudeopensource.xyz/`
- `https://saudeopensource.xyz/fundamentos/`
- `https://saudeopensource.xyz/screening/`
- `https://saudeopensource.xyz/protocolo-mestre/`
- `https://saudeopensource.xyz/modulos/`
- `https://saudeopensource.xyz/modulos/desparasitacao/`
- `https://saudeopensource.xyz/llms.txt`
- `https://saudeopensource.xyz/sitemap.xml`

Verificar também:

- ausência de marcadores antigos de URL da Tele-Farmácia;
- canonical URLs apontando para `.xyz`;
- JSON-LD válido;
- headers de segurança aplicados pelo `_headers`;
- link para Tele-Farmácia: `https://farmaciaintegrativa.xyz/`.
