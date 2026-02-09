pre# SESSION NOTES — Integração Recursos → Projeto Saúde Open Source

**Data Início:** 05-02-2026 | **Última Atualização:** 08-02-2026
**Sessão:** Plano de Integração COMPLETO (Fase 1 + 2 + 3) + Cross-Check + Correções + v4.3 EXPANDIDA
**Status Projeto:** v4.1 → v4.2 (Completo) → **v4.3 EXPANDIDA (Planejado)**

---

## 1. CONTEXTO DO PROJETO

### Descrição
**Saúde Open Source (Pharmacopeia.info)** — Repositório protocolos saúde integrativa baseados evidência + experiência clínica (Farm. João Alves). Estrutura modular: Protocolo Mestre (Shot dos Campeões) + 11 Módulos + Playbooks + Ferramentas.

### Estrutura de Diretórios
```
02. Projetos/3. Saúde Open Source/
├── 00-meta/
│   ├── SAUDE-OPEN-SOURCE-CLAUDE.md (doc mestre)
│   └── changelog.md (histórico versões)
├── 01-conteudo-fonte/ (FONTE DA VERDADE)
│   ├── modulos/ (M1-M11)
│   ├── ferramentas/ (GLOSSARIO, MATRIZ_INTERACOES, protocolos, frameworks)
│   ├── playbooks/ (sintomas específicos)
│   └── protocolo-mestre/
├── 02-recursos/ (processados → integrados)
└── 03-site-hugo/ (espelhamento após aprovação)
```

### Stack Técnico
- **Markdown** (fonte verdade `01-conteudo-fonte/`)
- **Hugo** (site estático `03-site-hugo/`)
- **Git** (versionamento)
- **CC BY 4.0** (licença)

---

## 2. OBJETIVO DA SESSÃO

**Processar 19 arquivos** em `02-recursos/analises-livros/` via **Plano de Integração 3 Fases** (14 gaps identificados).

**Prioridade:** M10 Higienista Moderno

**Meta:** Integrar TODO conteúdo útil ao projeto principal mantendo conformidade rigorosa com padrões.

---

## 3. DECISÕES TÉCNICAS CRÍTICAS

### 3.1 Hierarquia de Conteúdo

**M10 e M11 = Módulos (Nível 2)**, não Playbooks.
- **Razão:** Playbooks = sintoma-específicos; M10/M11 = estilo de vida/estrutura corporal
- **Precedente:** M6 (Dieta Carnívora) também é estilo de vida dentro dos módulos

### 3.2 Padrão de Módulo COMPLETO

**10 seções obrigatórias** (padrão iodo.md):
1. 📌 **TL;DR** (2-3 parágrafos)
2. ⚠️ **Pré-requisitos** (Screening + Shot ≥X dias)
3. 💡 **Princípio Fundamental** (base científica explícita com refs)
4. 📋 **Para Quem é Este Módulo?** (Indicações/Contraindicações)
5. 🚀 **Quick Start** (2 min — 3 ações checkbox)
6. 🔬 **Deep Dive** (15 min — contexto teórico)
7. 🔧 **Protocolo 4D Completo** (30 min — detalhes execução)
8. 🚨 **Red Flags** (quando pausar/investigar)
9. 📊 **Monitoramento** (métricas 0-10 + checkpoints 30/60/90 dias)
10. 📖 **Referências** + 🔗 **Navegação**

### 3.3 Front Matter Duplo

**Markdown status line:**
```markdown
**Status:** `v1.0` | **Última Atualização:** DD-MM-2026
```

**YAML Hugo:**
```yaml
---
title: "Título Completo"
date: 2026-MM-DD
description: "Resumo uma linha"
draft: false
weight: N
categories: [Módulo|Ferramenta|Playbook]
tags: [tag1, tag2, tag3]
---
```

### 3.4 Consistência de Dosagens (CRÍTICO)

**Iodo:** Dose inicial = **1 gota Lugol 5% (6,25mg)**, NÃO 2 gotas.
- GUIA_BASICO_IODO alinha com M1 (iodo.md)
- Nota explícita: guia é resumo, não substitui módulo

### 3.5 Conteúdo Investigativo (Flags Claras)

**ORIGEM_PARASITARIA_CANCER.md** tem aviso destacado:
```
🚨 AVISO CRÍTICO — LEIA ANTES DE CONTINUAR

ESTE NÃO É PROTOCOLO DE TRATAMENTO DE CÂNCER.

Este documento é:
✅ Exploração histórica hipótese minoritária
✅ Contexto filosofia desparasitação preventiva
❌ Recomendação terapêutica câncer
❌ Substituição oncologia convencional
```

**Honestidade sobre evidência** = prioridade máxima.

---

## 4. TRABALHO REALIZADO

### 4.1 FASE 1: FUNDAÇÃO (05-02-2026)

**Entregas: 4 novos documentos + 6 atualizações**

#### Novos Documentos (4):
1. **`modulos/higienista-moderno.md`** (~1050 linhas) — **M10**
   - 6 pilares: Sol, Água, Terra, Alimento Real, Movimento, Ritmo
   - Integra higienismo clássico (J.P. Müller *My System* 1904) + biofísica moderna (Pollack/EZ Water, Becker/bioeletricidade, Hamblin/fotobiomodulação)
   - Corpo = máquina biofísica converte ambiente → vitalidade
   - Sistema 90 dias (implementação gradual)
   - Rotina diária integrada (tabela horários)
   - Protocolo 4D por pilar (BIOQUÍMICA/ESTRUTURA/PSICOLOGIA/ELETROMAGNETISMO)

2. **`ferramentas/MONOGRAFIA_XAROPE_CRAVO_ALHO.md`** (~380 linhas)
   - Bioquímica: alicina (ativação alinase — aquecimento >60°C inativa), eugenol 70-90%, beta-cariofileno agonista CB2
   - 4 mecanismos: expectorante, antitussígeno, antimicrobiano, imunomodulação
   - Posologia: adultos 15ml 3-4x/dia jejum; crianças >2 anos 5ml 3x/dia
   - Preparo maceração frio: mel 40-50°C → cravo 20min → esfriar 25-30°C → alho triturado (descansar 10min) → macerar 24-48h
   - Interações CRÍTICAS: anticoagulantes (potencia INR), hipoglicemiantes (risco hipoglicemia), inibidores protease HIV (CONTRAINDICADO — induz CYP3A4)

3. **`ferramentas/PROTOCOLO_AZUL_METILENO.md`** (~340 linhas)
   - Bypass mitocondrial: aceita elétrons NADH → citocromo C oxidase (complexo IV)
   - Dosagem: 0,5-4 mg/kg/dia (prática: 2-16 gotas sol 1% pessoa 60kg)
   - Ciclo: 5 dias on / 2 off
   - Contraindicações ABSOLUTAS: ISRS (síndrome serotoninérgica), deficiência G6PD
   - Benefícios: ATP neuronal +70%, neuroproteção, cognição, antimicrobiano

4. **`ferramentas/PROTOCOLO_REINTRODUCAO.md`** (~360 linhas)
   - Pós-carnívora (M6): como reintroduzir sem perder progresso
   - Regra: 1 alimento/3 dias
   - Ordem: folhas verdes → crucíferas → oleaginosas → frutas baixo IG → grãos
   - Template monitoramento (sintomas digestivos/inflamatórios/energéticos)
   - Red flags: inchaço >24h, fadiga retorna, dor articular piora

#### Atualizações (6):
- `modulos/index.md` — M10 adicionado, bloco "QUANDO USAR M10", diagrama interconexão, ordem "Para Estilo de Vida Completo"
- `ferramentas/GLOSSARIO.md` — 6 verbetes: Citocromo C oxidase, EZ Water expandido, Fotobiomodulação, Grounding expandido, Higienismo Contemporâneo, Piezoeletricidade
- `ferramentas/MATRIZ_INTERACOES.md` — Azul Metileno + ISRS = CONTRAINDICADO; Xarope + Anticoagulantes = RISCO
- `playbooks/reset-circadiano.md` — Link M10 Pilar RITMO
- `playbooks/mobilidade-fascia.md` — Link M10 Pilar MOVIMENTO + M11 ref futura
- `00-meta/changelog.md` — Entrada v4.2 Fase 1

**Gaps resolvidos:** G1, G2, G11, G13 + M10 consolidado

**Estatísticas Fase 1:** 9→10 módulos, 12→15 ferramentas, ~30→~36 termos GLOSSARIO, ~2800 linhas novas

---

### 4.2 FASE 2: EXPANSÃO (05-02-2026)

**Entregas: 6 novos documentos + 4 atualizações**

#### Novos Documentos (6):
1. **`modulos/fascia.md`** (~1050 linhas) — **M11**
   - UMA rede 3D contínua (não camadas separadas)
   - Órgão sensorial: 6x mais receptores que músculos
   - 80% dor crônica = fascial
   - Sistema tensegral: ossos ilhas flutuantes, fáscia cabos tensão
   - Comunicação 3 níveis: mecânica (mecanotransdução), elétrica (piezoeletricidade 700 m/s vs nervos 100 m/s), química (interleucinas, ácido hialurônico, TGF-β)
   - 12 Anatomy Trains (Thomas Myers) + implicações clínicas
   - Hidratação 70% água
   - Trauma somático → miofibroblastos → armadura fascial
   - Rigidez bloqueia absorção fármacos (-70% MEC desidratada)
   - Protocolo: 10 min alongamento >90 seg/posição, 10 min foam roller 30-90 seg/ponto, colágeno hidrolisado 10g/dia + vit C

2. **`ferramentas/PROTOCOLO_ESTROGENICOS.md`** (~540 linhas)
   - IRS 10 (Top 10 disruptores endócrinos): fitoestrogênios/soja, zearalenona, atrazina, triclosan/APEs, benzofenona/4-MBC, Red 3/40, parabenos, ftalatos, BPA/BPS, EE2
   - Matriz exposição: fonte × meio (água, ar, pele, alimento, cosméticos)
   - Plano níveis: Bronze (BPA, ftalatos, água EE2), Prata (+top 6, cosméticos), Ouro (todos 10 + suplementação)
   - Epigenética: janelas críticas gestação/infância
   - Conexão M3: disruptores competem receptores tireoidianos

3. **`ferramentas/GUIA_BASICO_IODO.md`** (~480 linhas)
   - Entry point rápido (M1 denso/técnico)
   - Exames obrigatórios: urina 24h iodo, TSH, T3/T4, anticorpos TPO/TG
   - Checklist Hashimoto: selênio 200mcg 2-4 sem ANTES iodo
   - **Dosagens ALINHADAS M1:** iniciante 1 gota/6,25mg sem 1-2, progressão 1→2→3-4 gotas em 4-8 sem
   - Nota explícita: guia = resumo M1, não substitui
   - Cofatores: selênio 200mcg, vit C 1-3g, magnésio 400-600mg, sal integral
   - Bromismo (detox bromo) + referência M3

4. **`ferramentas/PSICOLOGIA_EVOLUTIVA.md`** (~620 linhas)
   - Framework conceitual (não protocolo suplementação)
   - Corpo adaptado ambiente ancestral: movimento ~30km/dia, jejum periódico, exposição solar 8-12h/dia, escuridão total noturna, alimentação densa
   - Mismatches modernos: sedentarismo→déficit piezoelétrico, luz artificial noturna→desregulação melatonina, ultraprocessados→inflamação, isolamento→disfunção imune
   - Framework raciocínio decisões saúde (checklist: alinha ambiente moderno com expectativas evolutivas?)
   - M10 corrige 6 mismatches via 6 pilares

5. **`ferramentas/PROTOCOLO_TRAUMA_SOMATICO.md`** (~450 linhas)
   - Mecanismo: trauma não processado → cortisol crônico → miofibroblastos → colágeno denso → armadura fascial
   - Sinais: rigidez matinal, nó garganta, bruxismo, respiração superficial, aperto peito
   - Protocolo 5 fases: (1) Consciência Corporal (body scan 10 min/dia), (2) Liberação Fascial + Presença (foam roller consciente 15 min), (3) Respiração (Wim Hof, Buteyko, diafragmática), (4) Movimento Expressivo (shaking, dança livre), (5) Somatic Experiencing (profissional Peter Levine)
   - Integração PNEI (Psique→Neuro→Endócrino→Imune→Fáscia)
   - Requer M11 completo

6. **`ferramentas/PROTOCOLO_PIEZOELETRICIDADE.md`** (~580 linhas)
   - Cascata mecano-elétrica: movimento → deformação colágeno → separação cargas → microcorrentes → sinalização celular + regeneração
   - Materiais piezoelétricos corpo: colágeno (principal), osso/hidroxiapatita, DNA, fáscia
   - Lei de Wolff via piezoeletricidade: stress mecânico → osteoblastos via microcorrentes
   - Efeito duplo: direto (pressão→eletricidade) + inverso (eletricidade→movimento/PEMF)
   - Protocolos: WBV (whole body vibration 30-50 Hz, 10 min 3-5x/sem, +2-4% densidade óssea 6 meses), PEMF (aprovado FDA pseudoartrose, 10-20 min 3x/sem 50 Hz), pliométrico (saltos controlados)
   - Protocolo mínimo (caminhada descalço + saltos) vs intensificado (WBV/PEMF)

#### Atualizações (4):
- `modulos/index.md` — M11 adicionado, bloco "QUANDO USAR M11", diagrama interconexão
- `ferramentas/GLOSSARIO.md` — 11 verbetes: Miofibroblasto, Anatomy Trains, Grundsubstanz, Mismatch Evolutivo, Mecanotransdução, Tensegridade/Biotensegridade, PEMF, WBV, Viscosidade tixotrópica, TGF-β, Interleucinas
- `ferramentas/MATRIZ_INTERACOES.md` — Estrogenicos + Iodo (competição receptores tireoidianos)
- `00-meta/changelog.md` — Entrada v4.2 Fase 2 expandida

**Gaps resolvidos:** G3, G4, G5, G9, G10, G14

**Estatísticas Fase 2:** 10→11 módulos, 15→20 ferramentas, ~36→~47 termos GLOSSARIO, ~3720 linhas novas

---

### 4.3 FASE 3: FUNDAMENTOS TEÓRICOS (06-02-2026)

**Entregas: 4 novos documentos + 2 atualizações**

#### Novos Documentos (4):
1. **`ferramentas/FRAMEWORK_SISTEMAS_DISSIPITIVOS.md`** (~620 linhas)
   - Ilya Prigogine (Prêmio Nobel 1977)
   - Corpo = sistema dissipativo longe equilíbrio termodinâmico
   - Mantém ordem via dissipação contínua energia (sem input → entropia/morte)
   - Estruturas dissipativas: furacão, chama, célula, corpo humano
   - Shot dos Campeões = otimização inputs bioquímicos
   - **Bifurcações:** pontos críticos mudança (ex: desparasitação quebra equilíbrio falso)
   - **Auto-organização:** corpo restaura ordem quando condições corretas (não precisa "tratamento", precisa **condições**)
   - **Por que 1 causa→1 cura falha:** Doença crônica = estado dissipativo subótimo estável. Sistema adaptou-se ao caos. 1 variável = insuficiente para quebrar estabilidade.
   - Framework raciocínio (checklist 4 perguntas: muda inputs ou suprime sintoma? aborda múltiplas variáveis? remove impedimentos? causa bifurcação?)
   - Hierarquia impacto: Nível 1 inputs energéticos (maior) → Nível 4 sintomático (menor)
   - Conexões: Heine (MEC = meio sistema dissipativo), HUMAN-OS (software sobre hardware dissipativo), Psicologia Evolutiva (mismatches = inputs errados)

2. **`ferramentas/FRAMEWORK_MEDICINA_BIOLOGICA.md`** (~780 linhas)
   - Hartmut Heine — Sistema Básico Pischinger
   - **Célula + Matriz Extracelular (Grundsubstanz) + Microcirculação = unidade funcional inseparável**
   - MEC = gel viscoso 70-90% água estruturada + proteoglicanos + colágeno
   - 4 funções críticas MEC: (1) transporte molecular sangue↔célula, (2) buffer pH/íons, (3) comunicação (mecânica/piezo 700 m/s, química/citocinas, elétrica/gradientes), (4) defesa/imunidade (primeira linha, macrófagos)
   - **Toxinas afetam MEC ANTES célula** (buffer protetor)
   - **Homotoxicologia (Reckeweg):** 6 fases progressão doença (Excreção→Reação→Deposição MEC→Impregnação célula→Degeneração→Neoplasia)
   - **Doença crônica = "falsa norma"** (setpoint disfuncional estável)
   - Tratar sintomas sem restaurar MEC = falha garantida
   - Como protocolos restauram MEC: M2 (remineralização→condutividade), M10 Água (hidratação→gel viscoso), M5 (desparasitação→remove endotoxinas), M11 (Fáscia = MEC musculoesquelética)
   - Medicina Biológica vs Convencional (tabela: unidade básica, causa doença, diagnóstico, tratamento, inflamação, febre, dor crônica, fadiga, prevenção)
   - Exemplo clínico: Artrite Reumatoide (Convencional: imunossupressor/sintoma/progressão; Biológica: M4+M5+M3→MEC restaurada→autoimunidade regride)
   - Avaliação 4D da MEC (checklist: bioquímica hidratação/eletrólitos/pH/cofatores, estrutura fáscia/aderências/colágeno, toxicidade fase/intestino/parasitas/halogênios, eletromagnetismo condutividade/piezo/grounding)

3. **`ferramentas/GUIA_CINESIOLOGIA_APLICADA.md`** (~640 linhas)
   - **⚠️ AVISO claro:** Biofeedback complementar, NÃO diagnóstico médico
   - Sistema teste muscular (George Goodheart 1964)
   - Princípio: músculos específicos relacionam órgãos/sistemas via meridianos MTC + inervação neural. Disfunção orgânica → fraqueza muscular reflexa
   - Modelo Tríade Saúde (Estrutura/Bioquímica/Psique interdependentes)
   - Procedimento padronizado: (1) linha base (músculo indicador forte), (2) desafio (químico/alimento, estrutural/vértebra, emocional/memória, funcional/ponto reflexo), (3) interpretação (forte=neutro/benéfico, fraco=estressor/tóxico)
   - Pontos reflexos: Neurovasculares NV (crânio, fluxo cerebral), Neurolinfáticos NL (tronco, órgãos/linfático)
   - **4 Desafios:** (1) Estrutural/Mecânico (subluxações, aderências), (2) Emocional/Psicológico (traumas, armadura fascial), (3) Funcional/Neurológico (disfunção órgão), (4) Químico/Nutricional (alimentos, suplementos, toxinas)
   - Atlas muscular: supraespinhal→cérebro, peitoral maior clavicular→estômago, latíssimo dorso→pâncreas, quadríceps→intestino delgado, psoas→rins
   - **Limitações explícitas:** (1) viés examinador (Haas 1994: 50% chance duplo-cego), (2) falta padronização (ICAK/Touch for Health), (3) mecanismo não elucidado (hipóteses: biocampo, meridianos, reflexos neurais, placebo)
   - Uso responsável: ✅ triagem complementar + exames lab + validação clínica; ❌ único diagnóstico, substituir exames críticos, prometer precisão
   - Protocolo teste 5 fases: baseline → desafio químico → estrutural → emocional → funcional
   - Integração Protocolo Mestre (exemplo: fadiga crônica → teste tireoide fraco → teste iodo fica forte → usar M1)

4. **`ferramentas/ORIGEM_PARASITARIA_CANCER.md`** (~720 linhas)
   - **🚨 AVISO CRÍTICO destacado:** NÃO É PROTOCOLO TRATAMENTO CÂNCER
   - Conteúdo: exploração histórica hipótese minoritária, revisão evidências séc. XIX-XX, contexto filosofia desparasitação preventiva
   - Se câncer: (1) oncologista qualificado, (2) tratamento convencional padrão, (3) desparasitação adjuvante (discutir médico), nunca primário
   - **Hipótese histórica:** Parasitas (coccídios/esporozoários) em tumores (Plasse 1844, Russell 1890, Warren 1892, Roux & Wickham 1896-1900, Darier 1900, Sjöbring 1909-1921)
   - Proposta: câncer = infecção crônica parasita intracelular
   - **Status: NÃO confirmada ciência moderna**
   - Por que abandonada: (1) falta replicabilidade (ninguém isolou/cultivou), (2) teorias robustas (Boveri mutação 1914, Rous vírus Nobel 1966, **Warburg metabolismo Nobel 1931**), (3) microscopia eletrônica 1950s+ (resolução 1000x superior, "parasitas" = artefatos + mitocôndrias alteradas)
   - **Efeito Warburg** (consenso científico): células cancerosas fermentam glicose MESMO com O₂ (glicólise aeróbica). Mitocôndrias disfuncionais. Proliferação rápida requer blocos construção, não apenas ATP.
   - Causas estabelecidas (OMS/NCI): genética 5-10%, tabagismo 30%, dieta 30%, infecções HPV/HBV/HCV/H.pylori/EBV 15-20%, radiação 5-10%, químicos 5-10%, obesidade 15-20%
   - Parasitas mencionados: *Schistosoma haematobium* (câncer bexiga África/Oriente Médio — mecanismo: inflamação crônica→mutações)
   - **Parasitas causa direta primária: NÃO estabelecido cânceres comuns** (mama, pulmão, cólon, próstata)
   - **Conexão M5:** desparasitação prioritária INDEPENDENTE hipótese por 4 razões: (1) carga subclínica comum (30-50% OMS), (2) parasitas→inflamação crônica→fator risco confirmado, (3) parasitas drenam nutrientes→disfunção mitocondrial, (4) protocolo baixo risco/alto benefício (ivermectina Nobel 2015, seguro, barato)
   - **Posição oficial:** Evidência causa parasitária fraca, valor preventivo alto independentemente
   - Ivermectina & câncer: estudos in vitro/animais (efeitos antitumorais mama/ovário/glioblastoma/colorretal/leucemia, mecanismo WNT/mTOR/STAT3), ensaios clínicos humanos (NENHUM RCT publicado 2026, relatos caso anedóticos, FDA/EMA NÃO aprovado)
   - Protocolo prevenção (ciência estabelecida): (1) reduzir inflamação (M5+M4+M6+M10), (2) otimizar mitocôndrias (M2+M10), (3) fortalecer vigilância imune (M1+Zn+VitD+VitC), (4) detox (M3+M5+hidratação+jejum), (5) reduzir exposições (tabaco, álcool, processados, açúcar, óleos vegetais)
   - Monitoramento preventivo: hemograma anual, marcadores tumorais (histórico familiar), colonoscopia 45+, mamografia 40+, PSA 50+, Papanicolau 21+
   - **Lição histórica *H. pylori*** (1982 Marshall/Warren propõem bactéria úlcera→ridicularização→1984 Marshall bebe cultura→cura antibióticos→2005 Nobel→hoje *H. pylori* = causa úlcera E câncer gástrico)
   - Lição: consenso≠verdade absoluta. Manter mente aberta + testar rigorosamente + ser honesto limitações + priorizar ciência estabelecida.

#### Atualizações (2):
- `ferramentas/GLOSSARIO.md` — 4 verbetes v4.3: Applied Kinesiology, Coccídio, Estrutura Dissipativa, Homotoxicologia
- `00-meta/changelog.md` — Seção Fase 3 completa, estatísticas finais, conclusão Plano de Integração

**Gaps resolvidos:** G6, G7, G8, G12

**Estatísticas Fase 3:** 11 módulos (sem mudança), 20→24 ferramentas, ~47→~51 termos GLOSSARIO, ~2760 linhas novas

---

## 5. ESTATÍSTICAS FINAIS — PROJETO v4.2

| Métrica | v4.1 | v4.2 (COMPLETO) | Δ |
|---------|------|-----------------|---|
| **Módulos** | 9 | **11** | +2 (M10, M11) |
| **Ferramentas** | 12 | **24** | +12 |
| **Termos GLOSSARIO** | ~30 | **~51** | +21 |
| **Playbooks** | 8 | **8** | — |
| **Conteúdo criado (linhas)** | — | **~9280** | 3 fases |

**Breakdown por fase:**
- Fase 1: ~2800 linhas (4 docs novos + 6 updates)
- Fase 2: ~3720 linhas (6 docs novos + 4 updates)
- Fase 3: ~2760 linhas (4 docs novos + 2 updates)

---

## 6. GAPS RESOLVIDOS — 14/14 (100%)

| Fase | Gaps | Documentos Criados | Status |
|------|------|-------------------|--------|
| **Fase 1** | G1, G2, G11, G13 + M10 | M10, Xarope Cravo+Alho, Azul Metileno, Reintrodução | ✅ |
| **Fase 2** | G3, G4, G5, G9, G10, G14 | M11, Estrogenicos, Guia Iodo, Psicologia Evol., Trauma Somático, Piezoeletricidade | ✅ |
| **Fase 3** | G6, G7, G8, G12 | Cinesiologia, Medicina Biológica/Heine, Sistemas Dissipitivos/Prigogine, Origem Parasitária Câncer | ✅ |

---

## 7. PROBLEMAS ENCONTRADOS E SOLUÇÕES

### 7.1 Tentativa Edit Paralelo Mesmo Arquivo
**Problema:** Múltiplos Edit tool calls no mesmo arquivo (modulos/index.md) em paralelo → erro
**Causa:** Tool Edit não pode ser chamado em paralelo no mesmo arquivo
**Solução:** Edit sequencial OU verificar se arquivo já foi atualizado previamente
**Descoberta:** modulos/index.md já tinha sido atualizado na Fase 1, não precisava re-editar

### 7.2 Consistência Dosagem Iodo
**Problema:** GUIA_BASICO_IODO inicialmente com 2 gotas dose inicial (conflito com M1)
**Solução:** Corrigido para 1 gota (6,25mg) + nota explícita "guia = resumo M1, não substitui"
**Prevenção:** Cross-check dosagens entre documentos relacionados

### 7.3 Conteúdo Investigativo sem Flag
**Problema:** Hipótese parasitária câncer pode ser mal interpretada
**Solução:** Aviso crítico destacado no topo do documento + honestidade sobre limitações evidência
**Princípio:** Transparência > marketing

---

## 8. ESTADO ATUAL — PLANO DE INTEGRAÇÃO

### ✅ COMPLETO (3 Fases)
- [x] Fase 1: Fundação (M10 + 3 ferramentas + 6 updates)
- [x] Fase 2: Expansão (M11 + 5 ferramentas + 4 updates)
- [x] Fase 3: Fundamentos Teóricos (4 frameworks + 2 updates)
- [x] **Cross-Check Automático (07-02-2026)** — Claude Opus 4.6

### ⏳ EM ANDAMENTO

#### Cross-Check Executado (07-02-2026)

**Status:** ✅ COMPLETO
**Analista:** Claude Opus 4.6 (Automação)
**Documentos Verificados:** 14
**Resultado:** Conteúdo técnico excelente; 15 problemas de infraestrutura

**Resumo Executivo:**
- **P0 (Crítica):** 0 problemas
- **P1 (Alta):** 5 ações — Links quebrados críticos
- **P2 (Média):** 7 ações — YAML faltando, padronização footer
- **P3 (Baixa):** 3 ações — Harmonização menor

**Achados Principais:**

✅ **CONTEÚDO TÉCNICO EXCELENTE:**
- Dosagens consistentes (Iodo 1 gota inicial = OK; Azul Metileno = OK)
- Contraindicações alinhadas (ISRS, G6PD, anticoagulantes)
- M10 e M11 com 10/10 seções obrigatórias completas
- Zero erros científicos

❌ **PROBLEMAS DE INFRAESTRUTURA (15 ações):**

**P1 — Links Quebrados (5):**
1. `/modulos/bromismo` não existe → correto: `/modulos/detox-halogenios` (6 ocorrências, 3 arquivos)
2. `/modulos/tireoide` não existe em higienista-moderno.md
3. `/modulos/magnesio` não existe → correto: `/modulos/remineralizacao`
4. `/docs/PILAR_PSICOLOGICO` caminho errado → correto: `/ferramentas/` (5 ocorrências, 4 arquivos)
5. `/playbooks/intestino` não existe em PROTOCOLO_REINTRODUCAO (2 ocorrências)

**P2 — Padronização (7):**
6. YAML Hugo faltando: 12/14 documentos (só M10 e M11 têm)
7. Footer inconsistente: 2 padrões ("Saúde Open Source" vs "Pharmacopeia.info")
8. `/docs/SCREENING-v2` caminho errado → correto: `/ferramentas/`
9. `HUMAN-OS-v4.0.md` não existe (link em FRAMEWORK_SISTEMAS_DISSIPITIVOS)
10. `/changelog.md` não existe (afeta 7 documentos)
11. Link bidirecional faltando: M1 (iodo.md) não linka GUIA_BASICO_IODO
12. Contraindicação faltando: PROTOCOLO_AZUL_METILENO deveria listar Inibidores MAO + Clomipramina

**P3 — Harmonização (3):**
13. Dose manutenção iodo: GUIA diz "4 gotas", M1 diz "2-4" (harmonizar para "2-4")
14. MATRIZ_INTERACOES faltam Dabigatrana + Glicazida
15. Links bidirecionais para frameworks teóricos em M1-M9

**Estimativa Correção:** ~5 horas (P1: 1h, P2: 3-4h, P3: 30min)

---

### ✅ PLANO DE INTEGRAÇÃO v4.3 EXPANDIDA (08-02-2026)

**Status:** ✅ APROVADO (Integração Completa + Protocolo Hulda Clark)
**Decisão João:** v4.3 EXPANDIDA (não v4.4 separada)
**Documento Técnico:** `/home/joaonotebook/Documentos/MEU OSS/02. Projetos/3. Saúde Open Source/PLANO-INTEGRACAO-v4.3.md`

#### Recursos Analisados (4):

1. **COF - AULA 24.md** (863 linhas)
   - **Decisão:** ❌ **NÃO INTEGRAR**
   - **Razão:** Conteúdo filosófico (Olavo de Carvalho - psicologia) fora do escopo técnico do projeto
   - **Tipo:** Filosofia/hermenêutica, não protocolo saúde

2. **Ivermectina, Uma Droga Subestimada...** (2610 linhas)
   - **Decisão:** ✅ **INTEGRAR COMPLETO**
   - **Formato:** `ferramentas/MONOGRAFIA_IVERMECTINA.md`
   - **Prioridade:** P1 (Alta)
   - **Esforço Estimado:** ~10 horas
   - **Conteúdo:**
     - História farmacológica (Nobel 2015)
     - 12 mecanismos de ação
     - Protocolo Lunar de Desparasitação (cronobiologia parasitária)
     - Dosagem 0,2-0,4 mg/kg em dias específicos do ciclo lunar
     - Interações medicamentosas (CYP3A4, P-gp, GABA)
     - Contraindicações (gestação, lactação, <15kg)
     - Estudos científicos + referências
   - **Impacto:**
     - Ferramenta específica dentro de M5 (Desparasitação)
     - Cross-reference com PROTOCOLO_LUNAR.md existente
     - Adiciona rigor farmacológico ao protocolo

3. **Protocolos de Saúde e Bem-Estar Guia Completo.md** (455 linhas)
   - **Decisão:** ✅ **INTEGRAR (PROTOCOLO_GLYNAC)**
   - **Formato:** `ferramentas/PROTOCOLO_GLYNAC.md`
   - **Prioridade:** P1 (Alta)
   - **Esforço Estimado:** ~6 horas
   - **Conteúdo:**
     - GlyNAC = NAC (N-Acetilcisteína) + Glicina
     - Mecanismo: +200% glutationa (GSH), antioxidante mestre
     - 3 protocolos distintos:
       - **Anti-Aging:** 1,33g NAC + 1,33g Glicina 2x/dia (90 dias mínimo)
       - **Sleep Protocol:** Glicina 3g antes dormir (NMDA modulação)
       - **GLP-1 Natural:** Glicina 15g/dia (alternativa Ozempic, -3,5kg 8 sem)
     - Estudos Baylor Medicine (2020-2021): +80% força muscular, -24% estresse oxidativo
     - Contraindicações, interações, monitoramento

4. **Desparasitação Natural com tinturas (Hulda Clark).md** (426 linhas)
   - **Decisão:** ✅ **INTEGRAR (PROTOCOLO_HULDA_CLARK)**
   - **Formato:** `ferramentas/PROTOCOLO_HULDA_CLARK.md`
   - **Prioridade:** P1 (Alta)
   - **Esforço Estimado:** ~6 horas
   - **Conteúdo:**
     - Protocolo fitoterapêutico 30 dias (15 prep + 15 eliminação)
     - Tinturas: Nogueira Negra + Losna + Cravo + Berberis
     - Ciclo completo: ovos (Cravo) + larvas (Losna) + adultos (Nogueira)
     - Proteção orgânica: Silimarina (fígado) + Berberis (rins/microbiota) + Ornitina (amônia)
     - Orégano (fungos/bactérias secundários)
     - Cronobiologia lunar: Lua Nova OU Lua Crescente
     - Calendário Lunar 2026 completo
     - Contraindicações: gravidez (artemísia), amamentação, crianças
   - **Impacto:**
     - Ferramenta específica dentro de M5 (Desparasitação)
     - M5 se torna HUB com 2 vias: Farmacológica (Ivermectina) + Fitoterapêutica (Hulda Clark)
     - Cross-reference com MONOGRAFIA_IVERMECTINA, M4 (Intestino), MONOGRAFIA_XAROPE_CRAVO_ALHO
     - Adiciona opção natural/sem receita para desparasitação familiar

#### Impacto Projetado v4.3 EXPANDIDA:

| Métrica | v4.2 | v4.3 EXPANDIDA (Projetado) | Δ |
|---------|------|---------------------------|---|
| **Módulos** | 11 | **11** | — |
| **Ferramentas** | 24 | **27** | +3 |
| **Termos GLOSSARIO** | ~51 | **~82** | +31 |
| **Conteúdo Total (linhas)** | ~9280 | **~11,800** | +2520 |

**Breakdown v4.3 EXPANDIDA:**
- MONOGRAFIA_IVERMECTINA.md: ~800 linhas (10 seções)
- PROTOCOLO_GLYNAC.md: ~700 linhas (10 seções)
- PROTOCOLO_HULDA_CLARK.md: ~800 linhas (10 seções)
- GLOSSARIO.md update: ~31 novos termos
  - **Ivermectina:** Ivermectina, Protocolo Lunar, Cronobiologia Parasitária, CYP3A4, P-gp, GABA, Avermectinas, Filaricidas, Oncocercose, Estrongiloidíase, Escabiose
  - **GlyNAC:** NAC, Glicina, Glutationa, GlyNAC, GLP-1, NMDA, GSH
  - **Hulda Clark:** Juglona, Absintina, Silimarina, Ornitina, Ciclo da Ureia, Nogueira Negra, Losna/Artemísia/Absinto, Berberis/Berberina, SIBO, Desparasitação Fitoterapêutica, Herxheimer (se não existe), Zapper
- MATRIZ_INTERACOES.md update:
  - Ivermectina + CYP3A4/P-gp/GABA/anticoagulantes
  - NAC + Glicina
  - Tinturas Clark + Anticoagulantes/Ivermectina/Hepatotóxicos
  - Berberina + Hipoglicemiantes/Ciclosporina
  - Artemísia + Medicamentos CYP2C19
  - Silimarina + Substratos CYP3A4
- M5 (desparasitacao.md): Reestruturação como HUB com árvore de decisão
- changelog.md: Seção v4.3 EXPANDIDA

**Conexões Internas:**
- MONOGRAFIA_IVERMECTINA → M5 (Desparasitação), PROTOCOLO_LUNAR existente
- PROTOCOLO_GLYNAC → M2 (Remineralização), M10 (Higienista - Sleep/Anti-aging)
- PROTOCOLO_HULDA_CLARK → M5 (HUB), MONOGRAFIA_IVERMECTINA (complementar), M4 (Intestino pós-desparasitação), MONOGRAFIA_XAROPE_CRAVO_ALHO (eugenol), ORIGEM_PARASITARIA_CANCER (contexto), PROTOCOLO_ESTROGENICOS (berberina)

**Esforço Total Estimado:** 26-30 horas
- 10h MONOGRAFIA_IVERMECTINA
- 6h PROTOCOLO_GLYNAC
- 6h PROTOCOLO_HULDA_CLARK
- 1h M5 reestruturação como HUB
- 1.5h GLOSSARIO (+31 termos)
- 1.5h MATRIZ_INTERACOES (+7 entradas Hulda Clark)
- 1h Cross-references e atualizações diversas

---

### ⏳ PRÓXIMAS AÇÕES (Sequência Recomendada)

#### 1. **INTEGRAÇÃO v4.3 EXPANDIDA (PRIORITÁRIO)**
**Status:** ⏳ Planejado
**Decisão João:** ✅ Integrar Ivermectina + GlyNAC + Hulda Clark (v4.3 EXPANDIDA)
**Esforço Total:** 26-30 horas

**Tarefas:**
- [ ] Criar `ferramentas/MONOGRAFIA_IVERMECTINA.md` (~10h)
  - 10 seções obrigatórias (padrão projeto)
  - Protocolo Lunar de Desparasitação detalhado
  - 12 mecanismos de ação farmacológicos
  - Interações CYP3A4 + P-gp
  - Contraindicações (gestação, lactação, <15kg)
  - Front matter duplo (Markdown + YAML Hugo)

- [ ] Criar `ferramentas/PROTOCOLO_GLYNAC.md` (~6h)
  - 10 seções obrigatórias
  - 3 protocolos distintos: Anti-Aging, Sleep, GLP-1 Natural
  - Mecanismo glutationa (+200% GSH)
  - Estudos Baylor Medicine
  - Dosagens NAC + Glicina
  - Contraindicações e interações

- [ ] Criar `ferramentas/PROTOCOLO_HULDA_CLARK.md` (~6h)
  - 10 seções obrigatórias
  - Protocolo fitoterapêutico 30 dias (prep + eliminação)
  - Bioquímica: Juglona, Absintina, Eugenol, Berberina
  - Proteção orgânica: Silimarina, Berberis, Ornitina, Orégano
  - Cronobiologia lunar (Lua Nova vs Crescente)
  - Calendário Lunar 2026 completo
  - Sistema de evidência (comprovado vs tradicional vs controverso)
  - Contraindicações (gravidez, amamentação, crianças)

- [ ] Reestruturar M5 como HUB (~1h)
  - Adicionar seção "Abordagens de Desparasitação"
  - Árvore de decisão (Farmacológica vs Fitoterapêutica)
  - Links bidirecionais para ferramentas

- [ ] Atualizar `ferramentas/GLOSSARIO.md` (~1.5h)
  - +31 novos termos (Ivermectina, NAC, GlyNAC, Hulda Clark, etc.)

- [ ] Atualizar `ferramentas/MATRIZ_INTERACOES.md` (~1.5h)
  - Ivermectina: CYP3A4, P-gp, GABA, anticoagulantes
  - NAC + Glicina
  - Tinturas Clark + Anticoagulantes/Ivermectina/Hepatotóxicos
  - Berberina + Hipoglicemiantes/Ciclosporina
  - Artemísia + CYP2C19
  - Silimarina + CYP3A4

- [ ] Cross-references (~1h)
  - MONOGRAFIA_IVERMECTINA ↔ M5, PROTOCOLO_HULDA_CLARK
  - PROTOCOLO_GLYNAC ↔ M2, M10
  - PROTOCOLO_HULDA_CLARK ↔ M5, MONOGRAFIA_IVERMECTINA, M4, MONOGRAFIA_XAROPE_CRAVO_ALHO

- [ ] Atualizar `00-meta/changelog.md` (30min)
  - Seção v4.3 EXPANDIDA completa

**Documento Técnico:** `/PLANO-INTEGRACAO-v4.3.md` (atualizado com Hulda Clark)

#### 2. Correção Problemas Cross-Check v4.2
**Status:** Pendente (após v4.3)
**Decisão João:** Opção A (Correção Automática Completa)
**Esforço:** ~5 horas

**Problemas:**
- P1 (5 ações): Links quebrados críticos
- P2 (7 ações): YAML Hugo faltando, padronização footer
- P3 (3 ações): Harmonização menor

#### 3. Arquivos de Controle
**Status:** Planejado
- [ ] **`PROCESS_NOTES-INTEGRACAO-RECURSOS.md`** — Data cada entrega, status, notas ajuste
- [ ] **`BUGS-E-GAPS-ADICIONAIS.md`** — Issues encontrados, prioridade, resolução

#### 4. Ferramentas de Redução de Fricção (Sprint 6 Dias)
**Status:** Planejado pós-v4.3
**Meta:** Facilitar entrada de usuários iniciantes

Criar:
- [ ] `ferramentas/CALCULADORA_CUSTO.md` — Quanto custa Shot dos Campeões?
- [ ] `ferramentas/FORNECEDORES_BRASIL.md` — Onde comprar Lugol, MgCl2, etc.
- [ ] `ferramentas/SCREENING_RAPIDO.md` — Versão simplificada (3 perguntas vs 20)
- [ ] `ferramentas/CONVERSAR_COM_MEDICO.md` — Como apresentar protocolo ao médico

**Justificativa:** Análise dos agentes de produto identificou esses como bloqueios principais de conversão (usuário → início do protocolo).

#### 5. Espelhamento Hugo (Após v4.3 + Correções)
- [ ] Copiar arquivos `01-conteudo-fonte/` → `03-site-hugo/saude.opensource/content/docs/`
- [ ] Testar build Hugo local (`hugo server -D`)
- [ ] Verificar links funcionam no site gerado
- [ ] Build produção (`hugo`)
- [ ] Deploy

---

## 9. PRÓXIMOS PASSOS RECOMENDADOS

### ✅ DECISÃO ATUAL: Integração v4.3 PRIORITÁRIA

**Sequência Executiva:**

1. **Integração v4.3 EXPANDIDA** (26-30h)
   - Criar MONOGRAFIA_IVERMECTINA.md (~10h)
   - Criar PROTOCOLO_GLYNAC.md (~6h)
   - Criar PROTOCOLO_HULDA_CLARK.md (~6h)
   - Reestruturar M5 como HUB (~1h)
   - Atualizar GLOSSARIO + MATRIZ_INTERACOES + changelog (~3h)
   - Cross-references internos (~1h)

2. **Correções v4.2** (5h)
   - Corrigir 15 problemas cross-check
   - P1: Links quebrados (1h)
   - P2: YAML + padronização (3-4h)
   - P3: Harmonização (30min)

3. **Arquivos Controle**
   - PROCESS_NOTES-INTEGRACAO-RECURSOS.md
   - BUGS-E-GAPS-ADICIONAIS.md

4. **Espelhamento Hugo**
   - v4.2 corrigido + v4.3 → Hugo
   - Teste + build + deploy

5. **Ferramentas Fricção** (Sprint 6 dias, opcional)
   - CALCULADORA_CUSTO
   - FORNECEDORES_BRASIL
   - SCREENING_RAPIDO
   - CONVERSAR_COM_MEDICO

**Justificativa Priorização:**
- v4.3 adiciona conteúdo técnico de alto valor (Ivermectina Nobel + GlyNAC estudos Baylor)
- Correções v4.2 são infraestrutura (links, YAML) — não bloqueiam conteúdo
- Faz sentido espelhar para Hugo após v4.3 completo (evita deploy duplo)

---

## 10. COMANDOS ÚTEIS PARA RETOMAR

### Links Importantes

**Plano de Integração (Especificações Técnicas Completas):**
```
/home/joaonotebook/.claude/plans/fizzy-napping-badger.md
```

**Este documento (Resumo Executivo):**
```
/home/joaonotebook/Documentos/MEU OSS/02. Projetos/3. Saúde Open Source/SESSION_NOTES.md
```

---

### Ler Plano Completo
```bash
cat "/home/joaonotebook/.claude/plans/fizzy-napping-badger.md"
```

### Ver Changelog Completo
```bash
cat "/home/joaonotebook/Documentos/MEU OSS/02. Projetos/3. Saúde Open Source/00-meta/changelog.md"
```

### Listar Novos Documentos Criados
```bash
cd "/home/joaonotebook/Documentos/MEU OSS/02. Projetos/3. Saúde Open Source/01-conteudo-fonte"

# Fase 1
ls -lh modulos/higienista-moderno.md
ls -lh ferramentas/MONOGRAFIA_XAROPE_CRAVO_ALHO.md
ls -lh ferramentas/PROTOCOLO_AZUL_METILENO.md
ls -lh ferramentas/PROTOCOLO_REINTRODUCAO.md

# Fase 2
ls -lh modulos/fascia.md
ls -lh ferramentas/PROTOCOLO_ESTROGENICOS.md
ls -lh ferramentas/GUIA_BASICO_IODO.md
ls -lh ferramentas/PSICOLOGIA_EVOLUTIVA.md
ls -lh ferramentas/PROTOCOLO_TRAUMA_SOMATICO.md
ls -lh ferramentas/PROTOCOLO_PIEZOELETRICIDADE.md

# Fase 3
ls -lh ferramentas/FRAMEWORK_SISTEMAS_DISSIPITIVOS.md
ls -lh ferramentas/FRAMEWORK_MEDICINA_BIOLOGICA.md
ls -lh ferramentas/GUIA_CINESIOLOGIA_APLICADA.md
ls -lh ferramentas/ORIGEM_PARASITARIA_CANCER.md
```

### Contar Linhas por Fase
```bash
cd "/home/joaonotebook/Documentos/MEU OSS/02. Projetos/3. Saúde Open Source/01-conteudo-fonte"

# Fase 1
wc -l modulos/higienista-moderno.md ferramentas/MONOGRAFIA_XAROPE_CRAVO_ALHO.md ferramentas/PROTOCOLO_AZUL_METILENO.md ferramentas/PROTOCOLO_REINTRODUCAO.md

# Fase 2
wc -l modulos/fascia.md ferramentas/PROTOCOLO_ESTROGENICOS.md ferramentas/GUIA_BASICO_IODO.md ferramentas/PSICOLOGIA_EVOLUTIVA.md ferramentas/PROTOCOLO_TRAUMA_SOMATICO.md ferramentas/PROTOCOLO_PIEZOELETRICIDADE.md

# Fase 3
wc -l ferramentas/FRAMEWORK_SISTEMAS_DISSIPITIVOS.md ferramentas/FRAMEWORK_MEDICINA_BIOLOGICA.md ferramentas/GUIA_CINESIOLOGIA_APLICADA.md ferramentas/ORIGEM_PARASITARIA_CANCER.md
```

### Buscar Links Quebrados (Exemplo)
```bash
cd "/home/joaonotebook/Documentos/MEU OSS/02. Projetos/3. Saúde Open Source/01-conteudo-fonte"

# Grep todos links Markdown [texto](/caminho)
grep -r '\[.*\](/.*)' modulos/ ferramentas/ playbooks/ | grep -v '.md:.*\[.*\](/modulos/\|/ferramentas/\|/playbooks/\|/protocolo-mestre/\|/docs/\)'
```

---

## 11. DECISÕES CRÍTICAS — NÃO REVERTER

### ✅ M10 e M11 = Módulos (Nível 2)
Justificativa: Playbooks = sintoma-específicos; M10/M11 = estilo de vida/estrutura corporal (precedente: M6 Dieta Carnívora)

### ✅ Dosagem Iodo Inicial = 1 Gota (6,25mg)
Justificativa: Alinhamento M1 (iodo.md) + segurança (progressão gradual)

### ✅ Conteúdo Investigativo com Flags Claras
Justificativa: Transparência sobre limitações evidência > marketing/promessas

### ✅ Padrão Módulo COMPLETO (10 Seções)
Justificativa: Conformidade rigorosa verificada por Claude Opus (plano original)

### ✅ Front Matter Duplo (Markdown + YAML Hugo)
Justificativa: Compatibilidade Hugo + legibilidade Markdown puro

---

## 12. ARQUIVOS MODIFICADOS (RESUMO)

### Novos (14):
1. `modulos/higienista-moderno.md`
2. `modulos/fascia.md`
3. `ferramentas/MONOGRAFIA_XAROPE_CRAVO_ALHO.md`
4. `ferramentas/PROTOCOLO_AZUL_METILENO.md`
5. `ferramentas/PROTOCOLO_REINTRODUCAO.md`
6. `ferramentas/PROTOCOLO_ESTROGENICOS.md`
7. `ferramentas/GUIA_BASICO_IODO.md`
8. `ferramentas/PSICOLOGIA_EVOLUTIVA.md`
9. `ferramentas/PROTOCOLO_TRAUMA_SOMATICO.md`
10. `ferramentas/PROTOCOLO_PIEZOELETRICIDADE.md`
11. `ferramentas/FRAMEWORK_SISTEMAS_DISSIPITIVOS.md`
12. `ferramentas/FRAMEWORK_MEDICINA_BIOLOGICA.md`
13. `ferramentas/GUIA_CINESIOLOGIA_APLICADA.md`
14. `ferramentas/ORIGEM_PARASITARIA_CANCER.md`

### Modificados (6):
1. `modulos/index.md` (Fase 1 + Fase 2)
2. `ferramentas/GLOSSARIO.md` (Fase 1 + Fase 2 + Fase 3)
3. `ferramentas/MATRIZ_INTERACOES.md` (Fase 1 + Fase 2)
4. `playbooks/reset-circadiano.md` (Fase 1)
5. `playbooks/mobilidade-fascia.md` (Fase 1)
6. `00-meta/changelog.md` (Fase 1 + Fase 2 + Fase 3)

---

---

## 13. LINHA DO TEMPO — SESSÕES

| Data | Sessão | Trabalho Realizado | Status |
|------|--------|-------------------|--------|
| **05-02-2026** | Fase 1: Fundação | M10 + 3 ferramentas + 6 updates (~2800 linhas) | ✅ Completo |
| **05-02-2026** | Fase 2: Expansão | M11 + 5 ferramentas + 4 updates (~3720 linhas) | ✅ Completo |
| **06-02-2026** | Fase 3: Fundamentos Teóricos | 4 frameworks + 2 updates (~2760 linhas) | ✅ Completo |
| **07-02-2026** | Cross-Check Automático | Opus 4.6: 8 pontos de verificação, 14 docs, 15 problemas identificados | ✅ Completo |
| **07-02-2026** | Análise Agentes de Produto | Feedback Synthesizer + Sprint Prioritizer + Trend Researcher | ✅ Completo |
| **07-02-2026** | **Planejamento v4.3** | Análise 3 novos recursos + PLANO-INTEGRACAO-v4.3.md | ✅ Completo |
| **07-02-2026** | **Decisão v4.3** | ✅ Integrar Ivermectina + GlyNAC (~1720 linhas projetadas) | ✅ Aprovado |
| **08-02-2026** | **Análise Protocolo Hulda Clark** | Explore (Haiku) + Plan (Opus) agentes | ✅ Completo |
| **08-02-2026** | **Decisão v4.3 EXPANDIDA** | ✅ Integrar Hulda Clark em v4.3 (~2520 linhas total) | ✅ Aprovado |
| **TBD** | Integração v4.3 EXPANDIDA | 3 novos protocolos + M5 HUB + updates | ⏳ Planejado |
| **TBD** | Correções Cross-Check v4.2 | 15 ações (P1 + P2 + P3, ~5h) | ⏳ Planejado |

---

## 14. VERSÃO ATUAL DO PROJETO

**Versão Atual:** v4.2 (Completo — pendente correções infraestrutura)
**Status:** 14 documentos criados, 15 problemas cross-check identificados (não-bloqueantes)

**Próxima Versão:** v4.3 EXPANDIDA (Integração Ivermectina + GlyNAC + Hulda Clark)
**Status v4.3:** ✅ Aprovado para integração EXPANDIDA
**Data Aprovação:** 08-02-2026
**Esforço Estimado:** 26-30 horas

**Versão Futura:** v4.4 (Ferramentas de Fricção — opcional)
**Conteúdo:** CALCULADORA_CUSTO, FORNECEDORES_BRASIL, SCREENING_RAPIDO, CONVERSAR_COM_MEDICO
**Data Projetada:** TBD (Sprint 6 dias)

---

**Roadmap Sequencial:**
1. v4.3 EXPANDIDA: Integração 3 protocolos (Ivermectina + GlyNAC + Hulda Clark) + M5 HUB (prioritário)
2. v4.2 Correções: 15 problemas cross-check (infraestrutura)
3. Hugo Deploy: v4.2 corrigido + v4.3 EXPANDIDA
4. v4.4: Ferramentas Fricção (opcional, baseado feedback usuários)

---

**ATUALIZADO:** 08-02-2026
**PRÓXIMO PASSO:** Integração v4.3 EXPANDIDA (criar MONOGRAFIA_IVERMECTINA.md + PROTOCOLO_GLYNAC.md + PROTOCOLO_HULDA_CLARK.md + M5 HUB)

---

## 15. RECURSOS v4.3 — ARQUIVOS FONTE

### Localização Arquivos de Origem:

```bash
# Recurso 1: Ivermectina (2610 linhas)
/home/joaonotebook/Documentos/MEU OSS/02. Projetos/3. Saúde Open Source/02-recursos/Ivermectina, Uma Droga Subestimada - Uma Monografia Sobre Seus Usos, Mecanismos de Ação e Impacto Global Além da Parasitologia.md

# Recurso 2: GlyNAC (455 linhas)
/home/joaonotebook/Documentos/MEU OSS/02. Projetos/3. Saúde Open Source/02-recursos/Protocolos de Saúde e Bem-Estar Guia Completo.md

# Plano Integração Completo (especificações técnicas)
/home/joaonotbook/Documentos/MEU OSS/02. Projetos/3. Saúde Open Source/PLANO-INTEGRACAO-v4.3.md
```

### Estrutura Proposta v4.3:

**MONOGRAFIA_IVERMECTINA.md** (~800 linhas):
1. 📌 TL;DR
2. ⚠️ Pré-requisitos
3. 💡 Princípio Fundamental (história farmacológica Nobel 2015)
4. 📋 Para Quem é Esta Ferramenta?
5. 🚀 Quick Start (Protocolo Lunar básico)
6. 🔬 Deep Dive (12 mecanismos de ação)
7. 🔧 Protocolo Completo (dosagens 0,2-0,4 mg/kg, cronobiologia)
8. 🚨 Red Flags (interações CYP3A4, contraindicações)
9. 📊 Monitoramento
10. 📖 Referências + 🔗 Navegação (M5, PROTOCOLO_LUNAR)

**PROTOCOLO_GLYNAC.md** (~700 linhas):
1. 📌 TL;DR
2. ⚠️ Pré-requisitos
3. 💡 Princípio Fundamental (glutationa +200%, estudos Baylor)
4. 📋 Para Quem é Este Protocolo?
5. 🚀 Quick Start (3 protocolos: Anti-Aging, Sleep, GLP-1)
6. 🔬 Deep Dive (bioquímica GSH, NMDA, GLP-1)
7. 🔧 Protocolo 4D Completo (dosagens NAC + Glicina por objetivo)
8. 🚨 Red Flags (interações, contraindicações)
9. 📊 Monitoramento (força muscular, estresse oxidativo, sono, peso)
10. 📖 Referências + 🔗 Navegação (M2, M10)

### Comandos Úteis Integração v4.3:

```bash
# Ler recursos fonte
cat "/home/joaonotebook/Documentos/MEU OSS/02. Projetos/3. Saúde Open Source/02-recursos/Ivermectina, Uma Droga Subestimada - Uma Monografia Sobre Seus Usos, Mecanismos de Ação e Impacto Global Além da Parasitologia.md"

cat "/home/joaonotebook/Documentos/MEU OSS/02. Projetos/3. Saúde Open Source/02-recursos/Protocolos de Saúde e Bem-Estar Guia Completo.md"

# Ler plano integração técnico
cat "/home/joaonotebook/Documentos/MEU OSS/02. Projetos/3. Saúde Open Source/PLANO-INTEGRACAO-v4.3.md"

# Verificar padrão documentos existentes (template)
cat "/home/joaonotebook/Documentos/MEU OSS/02. Projetos/3. Saúde Open Source/01-conteudo-fonte/modulos/iodo.md" | head -100

# Verificar GLOSSARIO atual
cat "/home/joaonotebook/Documentos/MEU OSS/02. Projetos/3. Saúde Open Source/01-conteudo-fonte/ferramentas/GLOSSARIO.md"

# Verificar MATRIZ_INTERACOES atual
cat "/home/joaonotebook/Documentos/MEU OSS/02. Projetos/3. Saúde Open Source/01-conteudo-fonte/ferramentas/MATRIZ_INTERACOES.md"
```

### Checklist Integração v4.3:

**Antes de Começar:**
- [ ] Ler PLANO-INTEGRACAO-v4.3.md completo
- [ ] Ler arquivos fonte (Ivermectina + GlyNAC)
- [ ] Revisar padrão 10 seções (iodo.md como template)
- [ ] Confirmar nomenclatura: MONOGRAFIA_IVERMECTINA, PROTOCOLO_GLYNAC

**Durante Criação:**
- [ ] 10 seções obrigatórias completas
- [ ] Front matter duplo (Markdown + YAML Hugo)
- [ ] Dosagens precisas com unidades
- [ ] Contraindicações explícitas
- [ ] Interações farmacológicas detalhadas
- [ ] Referências científicas (PubMed, estudos)
- [ ] Links internos corretos (/modulos/, /ferramentas/, /playbooks/)

**Após Criação:**
- [ ] Atualizar GLOSSARIO.md (+19 termos)
- [ ] Atualizar MATRIZ_INTERACOES.md (Ivermectina CYP3A4, NAC+Glicina)
- [ ] Atualizar changelog.md (seção v4.3)
- [ ] Verificar cross-references bidirecionais (M5→MONOGRAFIA_IVERMECTINA, M2/M10→PROTOCOLO_GLYNAC)
- [ ] Contagem linhas final (~11,000 total projetado)

---
