# Saude Open Source — Estrutura do Projeto

**Versao:** `v4.0` | **Ultima Atualizacao:** 24-01-2026

---

## ESTRUTURA DE PASTAS

```
Saude Open Source/
│
├── 🔬 HUMAN OS v4.0.md          ← HOMEPAGE (ponto de entrada)
├── README.md                     ← Este arquivo (estrutura do projeto)
├── changelog.md                  ← Historico de atualizacoes
│
├── /protocolo-mestre/            ← PROTOCOLO MESTRE (NUCLEO - comecar aqui)
│   ├── index.md                  ← Visao geral, como comecar
│   ├── shot-matinal.md           ← Receita completa do Shot dos Campeoes
│   ├── timeline-90-dias.md       ← 3 fases com checklist
│   ├── versoes.md                ← Minimalista → Avancada
│   ├── casos-clinicos.md         ← 5 casos documentados
│   ├── faq.md                    ← Perguntas frequentes
│   └── monitoramento.md          ← Sinais de progresso
│
├── /modulos/                     ← MODULOS (Deep Dives)
│   ├── index.md                  ← Indice dos 8 modulos
│   ├── iodo.md                   ← M1: Protocolo de Iodo
│   ├── remineralizacao.md        ← M2: Remineralizacao Essencial
│   ├── detox-halogenios.md       ← M3: Detox de Halogenios
│   ├── intestino.md              ← M4: Integridade Intestinal
│   ├── desparasitacao.md         ← M5: Desparasitacao (NOVO v4.0)
│   ├── dieta-carnivora.md        ← M6: Dieta Carnivora (NOVO v4.0)
│   ├── agua-oxigenada.md         ← M7: Agua Oxigenada (NOVO v4.0)
│   └── bicarbonato-extra.md      ← M8: Bicarbonato Extra (NOVO v4.0)
│
├── /Playbooks/                   ← PLAYBOOKS (sintomas especificos)
│   ├── fadiga.md
│   ├── ansiedade.md
│   ├── insonia.md
│   ├── refluxo.md
│   ├── imunidade-baixa.md
│   └── dor-lombar.md
│
├── /sistemas/                    ← DOCUMENTACAO TECNICA
│   ├── index.md
│   └── ...
│
├── /docs/                        ← DOCUMENTACAO DE SUPORTE
│   ├── SCREENING-v2.md           ← Checklist pre-protocolo (atualizado v4.0)
│   ├── GLOSSARIO.md              ← Termos tecnicos (NOVO v4.0)
│   └── PLAYBOOK-TEMPLATE.md
│
├── /core/                        ← ARQUITETURA E DESIGN
│   └── ARQUITETURA SAUDE OPEN SOURCE_v3.md
│
├── /estrategia/                  ← ESTRATEGIA DE NEGOCIO
│
├── /fundacionais/                ← DEPRECATED (redirects para /modulos/)
│   └── index.md → "Movido para /modulos/"
│
└── /_archive/                    ← ARQUIVOS ANTIGOS/ORIGINAIS
    └── PROTOCOLO BIOQUIMICO... (original arquivado)
```

---

## FLUXO DE USO v4.0

```
USUARIO NOVO:
│
├─ 1. Le HOMEPAGE (🔬 HUMAN OS v4.0.md)
│
├─ 2. Faz SCREENING (/docs/SCREENING-v2.md)
│     └─ Exames, contraindicacoes, red flags
│
├─ 3. PROTOCOLO MESTRE (/protocolo-mestre/) ← COMECAR AQUI
│     └─ Shot dos Campeoes, Timeline 90 dias
│
├─ 4. MODULOS para aprofundamento (/modulos/)
│     └─ Iodo, Remineralizacao, Desparasitacao, etc.
│
└─ 5. PLAYBOOKS se sintoma especifico (/Playbooks/)
      └─ Fadiga, Ansiedade, Refluxo, etc.
```

---

## HIERARQUIA DE PROTOCOLOS

```
NIVEL 0: SCREENING (obrigatorio)
    ↓
NIVEL 1: PROTOCOLO MESTRE (Shot dos Campeoes) ← NUCLEO
    ↓
NIVEL 2: MODULOS (Deep Dives - 8 modulos)
    ↓
NIVEL 3: PLAYBOOKS (sintomas especificos)
```

---

## PARA DESENVOLVEDORES/CONTRIBUIDORES

### Criar Novo Playbook:
1. Copiar `/docs/PLAYBOOK-TEMPLATE.md`
2. Preencher secoes especificas
3. Adicionar secao "Integracao com Protocolo Mestre"
4. Salvar em `/Playbooks/[nome].md`

### Criar Novo Modulo:
1. Criar arquivo em `/modulos/[nome].md`
2. Adicionar banner "Modulo do Protocolo Mestre"
3. Atualizar `/modulos/index.md`

### Arquivos Centralizados (nao duplicar):
- **Screening:** `/docs/SCREENING-v2.md`
- **Glossario:** `/docs/GLOSSARIO.md`
- **Arquitetura 4D:** `/core/` - referenciar, nao copiar

---

## STATUS DO PROJETO v4.0

| Componente | Status | Arquivos |
|------------|--------|----------|
| **Homepage** | ✅ v4.0 | 1 |
| **Protocolo Mestre** | ✅ NOVO | 7 |
| **Modulos** | ✅ v4.0 | 8 (4 novos) |
| **Playbooks** | ✅ Atualizado | 6 |
| **Docs** | ✅ v4.0 | 3 |
| **Core** | ✅ Stable | 2 |

---

## LINKS RAPIDOS

- **Homepage:** `🔬 HUMAN OS v4.0.md`
- **Protocolo Mestre:** `/protocolo-mestre/index.md`
- **Screening:** `/docs/SCREENING-v2.md`
- **Modulos:** `/modulos/index.md`
- **Glossario:** `/docs/GLOSSARIO.md`

---

**Pharmacopeia.info** — The Open Source Health Repository

`v4.0` | `CC BY 4.0` | Mantido por Farm. Joao
