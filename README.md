# Saúde Open Source

Protocolos para uma saúde descentralizada.

> A saúde centralizada virou caixa-preta. Nós abrimos o código.

Saúde Open Source é uma biblioteca pública, educacional e versionada de fundamentos, screenings, protocolos e módulos de saúde integrativa. A proposta não é substituir acompanhamento clínico. É documentar raciocínio, riscos, contraindicações, referências e limites — de forma aberta, rastreável e revisável.

## Arquitetura do projeto

- Marca: Saúde Open Source
- Tese: saúde descentralizada
- Domínio pretendido: https://saudeopensource.xyz
- Canal canônico: site estático neste repositório
- Distribuição: YouTube e Substack
- Ponte clínica: Tele-Farmácia Integralista — https://farmaciaintegrativa.xyz/

## Por que “open source” em saúde?

Porque protocolos fechados viram autoridade sem auditoria. Este projeto trata conteúdo de saúde como documentação viva:

- fundamentos explícitos;
- hipóteses separadas de evidência consolidada;
- contraindicações visíveis;
- riscos publicados junto com benefícios;
- páginas versionadas;
- `llms.txt`, `sitemap.xml` e Schema.org para rastreabilidade por buscadores e LLMs.

## Estrutura atual

```text
/
├── index.html
├── fundamentos/
├── screening/
├── protocolo-mestre/
│   ├── index.html
│   ├── faq.html
│   ├── shot-matinal.html
│   └── timeline-90-dias.html
├── modulos/
│   ├── index.html
│   └── desparasitacao/
├── css/
├── llms.txt
├── sitemap.xml
└── _headers
```

## Semana 2 — status real

Concluído:

- marcadores antigos de URL da Tele-Farmácia zerados;
- M5 ativado em `modulos/index.html`;
- página `modulos/desparasitacao/index.html` criada e revisada;
- linguagem de die-off corrigida para orientação clínica segura;
- FAQ de ivermectina sem estrutura posológica pública;
- pt-BR padronizado;
- índice/sumário adicionado;
- referências organizadas em camadas: farmacológica, etnomedicina e hipótese integrativa;
- `llms.txt` e `sitemap.xml` atualizados para `saudeopensource.xyz`.

Pendente fora do repositório:

- comprar/apontar `saudeopensource.xyz`;
- ligar o repositório ao Cloudflare Pages;
- validar deploy público, DNS e HTTPS.

## Deploy sugerido

Cloudflare Pages:

- Framework preset: None / Static HTML
- Build command: vazio
- Build output directory: `/`
- Production branch: `main`
- Custom domain: `saudeopensource.xyz`

## Aviso

Conteúdo exclusivamente educacional. Não constitui diagnóstico, prescrição ou protocolo individualizado. Aplicação clínica requer screening e acompanhamento profissional habilitado.
