# Pharmacopeia.info | Saúde Open Source

> **The Open Source Health Repository**

![Version](https://img.shields.io/badge/version-v4.1-blue)
![License](https://img.shields.io/badge/license-CC%20BY%204.0-green)
![Hugo](https://img.shields.io/badge/hugo-0.147.0-FF4088?logo=hugo)
![Build](https://github.com/jvmasc/saude.opensource/workflows/Deploy%20Hugo%20site%20to%20Pages/badge.svg)
![Language](https://img.shields.io/badge/PT--BR%20%7C%20EN-blue)

---

## ⚠️ AVISO MÉDICO CRÍTICO

**ESTE É CONTEÚDO EDUCACIONAL. NÃO SUBSTITUI CONSULTA MÉDICA.**

**OBRIGATÓRIO ANTES DE INICIAR:**
- [Faça o Screening Completo](https://jvmasc.github.io/saude.opensource/pt/docs/ferramentas/screening-v2/) (exames laboratoriais + avaliação 4D)
- Consulte profissional de saúde qualificado
- NUNCA interrompa medicamentos sem orientação médica

**VÁ AO HOSPITAL IMEDIATAMENTE SE:**
- Dor no peito
- Desmaio ou perda de consciência
- Vômito com sangue
- Febre alta persistente (>39°C por mais de 3 dias)
- Dificuldade respiratória severa
- Dor abdominal intensa

---

## Sobre o Projeto

**Pharmacopeia.info** é um repositório open source de protocolos de saúde integrativa baseados em evidência científica.

### Filosofia: Autonomia Biológica

Este não é um blog de saúde. É o **código-fonte do seu corpo** — aberto, documentado, hackeável.

> *"A doença surge quando Energia, Informação e Sentido entram em conflito.*
> *A cura não é conserto. Cura é atualização."*

### O que você encontra aqui:

- **119 arquivos markdown** de conteúdo educacional
- **Evidence-based**: referências a Pollack, Warburg, Barnes, Heine, Myers, Ingber
- **Open source**: livre para usar, modificar e distribuir (CC BY 4.0)
- **Bilíngue**: Português-BR e Inglês
- **Site deployado**: [https://jvmasc.github.io/saude.opensource/](https://jvmasc.github.io/saude.opensource/)

---

## 🎯 Quick Links

- 🌐 [**Site Ao Vivo**](https://jvmasc.github.io/saude.opensource/)
- 📖 [**Protocolo Mestre**](https://jvmasc.github.io/saude.opensource/pt/docs/protocolo-mestre/)
- 🧬 [**Módulos**](https://jvmasc.github.io/saude.opensource/pt/docs/modulos/)
- 🩺 [**Playbooks**](https://jvmasc.github.io/saude.opensource/pt/docs/playbooks/)
- 🛠️ [**Ferramentas**](https://jvmasc.github.io/saude.opensource/pt/docs/ferramentas/)
- 📝 [**Changelog**](content/docs/ferramentas/CHANGELOG.md)

---

## 🏗️ Arquitetura do Projeto

### Hierarquia 4 Níveis

```
┌─────────────────────────────────────────────┐
│  NÍVEL 0: SCREENING (Obrigatório)          │
│  └─ Assessment 4D + Exames laboratoriais   │
└─────────────────┬───────────────────────────┘
                  │
┌─────────────────▼───────────────────────────┐
│  NÍVEL 1: PROTOCOLO MESTRE                  │
│  └─ Shot dos Campeões (4 componentes)      │
└─────────────────┬───────────────────────────┘
                  │
┌─────────────────▼───────────────────────────┐
│  NÍVEL 2: MÓDULOS (9 Deep Dives)           │
│  └─ Iodo • Intestino • Detox • Dieta...    │
└─────────────────┬───────────────────────────┘
                  │
┌─────────────────▼───────────────────────────┐
│  NÍVEL 3: PLAYBOOKS (8 Sintomas)           │
│  └─ Fadiga • Insônia • Ansiedade...        │
└─────────────────────────────────────────────┘
```

### Framework 4D

Todo o conteúdo está organizado em 4 dimensões da saúde:

1. **Bioquímica** - Nutrientes, hormônios, metabolismo
2. **Estrutura** - Fáscia, postura, biotensegridade
3. **Psicologia** - Stress, trauma, padrões mentais
4. **Eletromagnetismo** - Luz, ritmo circadiano, campos EM

---

## 📁 Estrutura de Conteúdo

| Seção | Arquivos | Descrição |
|-------|----------|-----------|
| **Protocolo Mestre** | 8 | Protocolo base: Shot dos Campeões, Timeline 90 dias, FAQ, Monitoramento |
| **Módulos** | 11 | Deep dives: Iodo, Intestino, Desparasitação, Dieta Carnívora, Boro, etc. |
| **Playbooks** | 10 | Guias específicos: Fadiga, Insônia, Ansiedade, Refluxo, Imunidade, etc. |
| **Ferramentas** | 12 | Screening, Calculadoras, Glossário, Protocolos de Emergência, etc. |

---

## 🚀 Como Começar (Para Usuários)

### Passo 1: Fazer Screening Obrigatório

**NUNCA pule esta etapa.** O screening identifica contraindicações e estabelece linha de base.

[→ Acessar Screening v2](https://jvmasc.github.io/saude.opensource/pt/docs/ferramentas/screening-v2/)

**Exames obrigatórios:**
- Painel tireoidiano completo (TSH, T3 Total, T3 Livre, T4 Total, T4 Livre, Anti-TPO, Anti-Tireoglobulina)
- Painel de ferro (Ferritina, Ferro Sérico, Saturação de Transferrina)
- Vitamina D (25-OH)
- Vitamina B12
- Homocisteína
- Teste de Broda Barnes (temperatura basal por 7 dias consecutivos)

### Passo 2: Ler Protocolo Mestre

[→ Shot dos Campeões](https://jvmasc.github.io/saude.opensource/pt/docs/protocolo-mestre/shot-matinal/)

**O protocolo básico consiste em 4 componentes:**

1. **Bicarbonato de Sódio** - 2.5g (½ colher de chá)
2. **Sal Integral** - 2.5g (½ colher de chá)
3. **Lugol 5%** - 2-8 gotas (progressão gradual)
4. **Cloreto de Magnésio** - 500mg (1 cápsula)

**Como tomar:**
- Em jejum, entre 5h-10h da manhã
- Dissolver em 200ml de água filtrada
- Aguardar 30-60 minutos para primeira refeição

**Duração:**
- Protocolo mínimo: 21 dias
- Protocolo ideal: 90 dias
- Manutenção: conforme orientação profissional

### Passo 3: Escolher seu Caminho

**Quick Start (Prático):**
- Seguir apenas o Shot dos Campeões
- Monitorar sintomas semanalmente
- Ajustar dosagens conforme resposta

**Deep Dive (Investigador):**
- Estudar os 9 módulos em profundidade
- Entender a bioquímica por trás dos protocolos
- Customizar abordagem baseada em seu perfil

### Passo 4: Seguir Protocolos de Segurança

- **Progressão gradual**: sempre começar com doses mínimas
- **Monitoramento**: medir temperatura basal diariamente
- **Journaling**: registrar sintomas e reações
- **Reavaliação**: repetir exames a cada 90 dias
- **Red flags**: suspender protocolo e buscar atendimento médico imediatamente se houver reações adversas graves

---

## 💻 Para Desenvolvedores

### Tech Stack

- **Hugo**: v0.147.0 Extended
- **Theme**: [PaperMod](https://github.com/adityatelange/hugo-PaperMod)
- **Deploy**: GitHub Pages via GitHub Actions
- **Linguagens**: Português-BR (primário), Inglês (secundário)
- **Markdown**: CommonMark + Hugo shortcodes

### Setup Local

```bash
# Clonar repositório
git clone https://github.com/jvmasc/saude.opensource.git
cd saude.opensource

# Inicializar submódulo do tema
git submodule update --init --recursive

# Instalar Hugo Extended v0.147.0
# https://github.com/gohugoio/hugo/releases/tag/v0.147.0

# Rodar servidor local
hugo server -D

# Acessar em http://localhost:1313
```

### Build de Produção

```bash
# Build com minificação
hugo --gc --minify

# Output vai para /public
```

### Estrutura Hugo

```
saude.opensource/
├── content/           # Conteúdo markdown (PT/EN)
│   ├── _index.md     # Homepage
│   └── docs/         # Documentação principal
│       ├── protocolo-mestre/
│       ├── modulos/
│       ├── playbooks/
│       └── ferramentas/
├── themes/           # PaperMod theme (submodule)
├── layouts/          # Templates customizados
├── static/           # Assets estáticos
├── i18n/            # Traduções
└── hugo.toml        # Configuração do site
```

### Deploy Automático

O site é automaticamente deployado no GitHub Pages quando há push para `main`:

- Workflow: `.github/workflows/deploy.yml`
- URL: https://jvmasc.github.io/saude.opensource/

---

## 🔬 Fundação Científica

Este projeto é baseado em trabalhos de pesquisadores de ponta:

### Referências Principais

- **Gerald Pollack** - Água estruturada (EZ water), hidratação celular, 4ª fase da água
- **Otto Warburg** - Metabolismo celular, efeito Warburg, pH e câncer
- **Broda Barnes** - Temperatura basal, função tireoidiana, hipotireoidismo subclínico
- **Hartmut Heine** - Regulação da matriz extracelular, medicina biológica
- **Thomas Myers** - Fáscia, Anatomy Trains, continuidade fascial
- **Donald Ingber** - Biotensegridade, arquitetura celular, mecanotransdução

### Abordagem Evidence-Based

- Protocolos baseados em literatura científica revisada por pares
- Referências bibliográficas incluídas em cada módulo
- Atualização contínua conforme novos estudos emergem
- Filosofia: "Open source não significa sem rigor"

### Autor

**Farm. João** - Farmacêutico Clínico
- Especialização em Farmácia Clínica e Medicina Integrativa
- 10+ anos de prática clínica
- Foco em protocolos de regulação metabólica

---

## 📚 Conteúdo Principal

### Shot dos Campeões (Protocolo Mestre)

Protocolo matinal de 2 minutos que combina 4 componentes sinérgicos:

- **Alcalinização**: Bicarbonato de sódio (pH sistêmico)
- **Mineralização**: Sal integral (eletrólitos, oligoelementos)
- **Tireóide**: Lugol 5% (iodo + iodeto)
- **Relaxamento**: Cloreto de magnésio (ativação parassimpática)

**Protocolo completo:** [shot-matinal.md](content/docs/protocolo-mestre/shot-matinal.md)

---

### 9 Módulos (Deep Dives)

| Módulo | Foco | Duração |
|--------|------|---------|
| 1. Iodo | Função tireoidiana, detox halogênios | 90 dias |
| 2. Intestino | Microbioma, permeabilidade intestinal | 60 dias |
| 3. Desparasitação | Parasitas, protozoários, helmintos | 30 dias |
| 4. Dieta Carnívora | Eliminação de antinutrientes | 90 dias |
| 5. Boro | Hormônios, osteoporose, artrite | 90 dias |
| 6. Remineralização | Oligoelementos, deficiências minerais | Contínuo |
| 7. Detox Halogênios | Flúor, bromo, cloro | 180 dias |
| 8. Água Oxigenada | Oxigenação celular, mitocôndrias | 21 dias |
| 9. Bicarbonato Extra | Alcalinização profunda, câncer | 90 dias |

---

### 8 Playbooks (Sintomas Específicos)

| Playbook | Indicação | Tempo de Resposta |
|----------|-----------|-------------------|
| Fadiga Crônica | Cansaço sem causa aparente | 7-21 dias |
| Insônia | Dificuldade para dormir/manter sono | 3-14 dias |
| Ansiedade | Nervosismo, pânico, preocupação excessiva | 7-30 dias |
| Refluxo | Azia, queimação, regurgitação | 3-7 dias |
| Imunidade Baixa | Infecções recorrentes | 30-90 dias |
| Dor Lombar | Dor nas costas, ciática | 7-21 dias |
| Reset Circadiano | Jet lag, sono desregulado | 3-7 dias |
| Mobilidade Fascial | Rigidez, falta de flexibilidade | 14-30 dias |

---

### Ferramentas

- **Screening v2**: Checklist completo de exames e avaliações
- **Calculadora de Dosagens**: Ajuste personalizado baseado em peso/idade
- **Glossário**: Termos técnicos explicados
- **Protocolo de Emergência**: O que fazer em caso de reação adversa
- **Tracker de Sintomas**: Planilha para monitoramento
- **Timeline 90 Dias**: Cronograma de implementação
- **FAQ**: Perguntas frequentes
- **Changelog**: Histórico de versões e atualizações

---

## 🤝 Como Contribuir

### Quem pode contribuir

- **Profissionais de saúde** (médicos, farmacêuticos, nutricionistas, fisioterapeutas)
- **Desenvolvedores** (melhorias no site Hugo, UX, acessibilidade)
- **Tradutores** (PT-BR ↔ EN, outros idiomas)
- **Pesquisadores** (adicionar referências científicas atualizadas)

### Tipos de contribuição aceitos

✅ **Aceitos:**
- Casos clínicos anônimos (sem dados pessoais)
- Referências científicas recentes
- Melhorias de clareza e gramática
- Traduções PT↔EN
- Correções de bugs/typos
- Melhorias de UX/UI

❌ **NÃO aceitos:**
- Opiniões sem base científica
- Conteúdo promocional/comercial
- Recomendações sem referências
- Dados pessoais de pacientes
- Conteúdo plágio

### Processo de Contribuição

1. **Fork** este repositório
2. **Crie um branch** para sua feature (`git checkout -b feature/minha-contribuicao`)
3. **Faça commit** das mudanças (`git commit -m 'Adiciona nova referência sobre X'`)
4. **Push** para o branch (`git push origin feature/minha-contribuicao`)
5. **Abra um Pull Request** com descrição detalhada

### Requisitos para PRs

- **Referências obrigatórias** para conteúdo clínico (estudos revisados por pares)
- **Markdown lint** passando (usar `markdownlint`)
- **Build Hugo** sem erros (`hugo --gc --minify`)
- **Descrição clara** do que foi modificado e por quê
- **Atribuição de autoria** se aplicável

### Guidelines de Conteúdo

- **Tom**: Profissional mas acessível, direto, sem sensacionalismo
- **Formato**: Markdown padrão + Hugo shortcodes quando necessário
- **Idioma primário**: Português-BR (traduções para EN são bem-vindas)
- **Referências**: Formato APA, links para DOI/PubMed quando disponível
- **Disclaimers**: Sempre incluir avisos médicos apropriados

---

## ⚖️ Licença

Este projeto está licenciado sob **Creative Commons Attribution 4.0 International (CC BY 4.0)**.

### Você pode:

- ✅ **Compartilhar** — copiar e redistribuir o material em qualquer meio ou formato
- ✅ **Adaptar** — remixar, transformar e criar a partir do material para qualquer finalidade, mesmo comercial

### Sob as seguintes condições:

- **Atribuição** — Você deve dar o crédito apropriado a **Farm. João**, prover um link para a licença e indicar se mudanças foram feitas.

### Sem garantias:

Este conteúdo é fornecido "como está", sem garantias de qualquer tipo, expressas ou implícitas, incluindo mas não limitado a garantias de adequação a um propósito específico.

**Licença completa:** https://creativecommons.org/licenses/by/4.0/

---

## 📊 Status do Projeto

- **Versão atual**: v4.1
- **Última atualização**: 28-01-2026
- **Status**: Em desenvolvimento ativo
- **Roadmap**: Ver [Issues](https://github.com/jvmasc/saude.opensource/issues)

### Changelog

Para histórico completo de versões e mudanças, consulte:
[→ CHANGELOG.md](content/docs/ferramentas/CHANGELOG.md)

---

## ⚠️ Disclaimer Legal Detalhado

**LEIA COM ATENÇÃO ANTES DE USAR ESTE CONTEÚDO:**

### Propósito Educacional

Este repositório tem **propósito exclusivamente educacional**. O conteúdo aqui apresentado:

- NÃO constitui aconselhamento médico profissional
- NÃO substitui consulta com profissional de saúde qualificado
- NÃO deve ser usado para diagnóstico ou tratamento de condições médicas
- NÃO cria relação médico-paciente

### Não Avaliado por Agências Reguladoras

As informações e protocolos aqui descritos:

- NÃO foram avaliados pela ANVISA (Brasil) ou FDA (EUA)
- NÃO têm aprovação para diagnóstico, tratamento ou prevenção de doenças
- NÃO substituem medicamentos prescritos por médicos

### Responsabilidade do Usuário

Ao usar este conteúdo, você reconhece e concorda que:

- É **exclusivamente responsável** por suas decisões de saúde
- Deve **consultar profissional qualificado** antes de iniciar qualquer protocolo
- Deve **realizar exames laboratoriais** antes de suplementar
- Deve **monitorar reações adversas** e suspender uso se necessário
- Compreende os **riscos inerentes** à automedicação

### Isenção de Responsabilidade

O autor e contribuidores deste repositório:

- NÃO se responsabilizam por danos diretos ou indiretos resultantes do uso deste conteúdo
- NÃO garantem resultados específicos
- NÃO endossam produtos ou marcas específicas (quando mencionados, são exemplos educacionais)

### Quando Buscar Atendimento Médico

**Procure atendimento médico imediatamente** se experimentar:

- Reações alérgicas graves (anafilaxia)
- Dor no peito ou dificuldade respiratória
- Vômito com sangue ou fezes escuras (melena)
- Desmaio ou perda de consciência
- Febre alta persistente (>39°C por mais de 3 dias)
- Dor abdominal intensa
- Qualquer sintoma que você considere grave ou preocupante

### Interações Medicamentosas

Muitos dos protocolos aqui descritos podem:

- Interferir com medicamentos prescritos
- Potencializar ou reduzir efeitos de drogas
- Contraindicar condições médicas preexistentes

**NUNCA interrompa medicamentos sem orientação médica.**

### Crianças, Gestantes e Lactantes

**Protocolos NÃO são adequados para:**

- Crianças menores de 18 anos (sem supervisão médica)
- Mulheres grávidas ou planejando gravidez
- Mulheres em período de lactação

Populações especiais requerem protocolos adaptados e supervisão médica especializada.

---

## 👨‍⚕️ Sobre o Autor

**Farm. João** - Farmacêutico Clínico

- Especialização em Farmácia Clínica e Medicina Integrativa
- 10+ anos de experiência em regulação metabólica
- Filosofia: "Open source não significa sem rigor"

### Contato

- **GitHub Issues**: Para problemas técnicos, sugestões de conteúdo, reportar bugs
- **Pull Requests**: Para contribuições diretas ao projeto
- **Questões de saúde**: Consulte seu médico ou farmacêutico local (não respondemos questões clínicas individuais via GitHub)

---

## 🌟 Apoie o Projeto

Este projeto é **100% gratuito e open source**. Se você acha este conteúdo valioso:

- ⭐ **Star** este repositório no GitHub
- 🔀 **Fork** e contribua com melhorias
- 📢 **Compartilhe** com profissionais de saúde e pesquisadores
- 📝 **Cite** este trabalho em suas pesquisas (ver [Licença](#️-licença))

**Não aceitamos doações financeiras.** Contribua com conhecimento, não dinheiro.

---

## 🗺️ Roadmap

### Em Desenvolvimento (v4.2)

- [ ] Versão em Espanhol (ES)
- [ ] Calculadora interativa de dosagens
- [ ] Sistema de tracking de sintomas integrado
- [ ] Casos clínicos anônimos (seção nova)
- [ ] API REST para acesso programático ao conteúdo

### Planejado (v5.0)

- [ ] Chatbot de triagem (screening automatizado)
- [ ] Integração com wearables (monitoramento contínuo)
- [ ] Protocolo de IA para personalização de dosagens
- [ ] Comunidade de profissionais (fórum/discussões)

**Sugestões?** Abra uma [Issue](https://github.com/jvmasc/saude.opensource/issues/new) com tag `enhancement`.

---

## 📖 Leitura Recomendada

Se você quer se aprofundar na ciência por trás dos protocolos, comece por aqui:

### Livros Fundamentais

- **The Fourth Phase of Water** - Gerald Pollack (hidratação celular)
- **Hypothyroidism: The Unsuspected Illness** - Broda Barnes (tireóide)
- **Anatomy Trains** - Thomas Myers (fáscia)
- **The Biology of Belief** - Bruce Lipton (epigenética)

### Artigos Científicos-Chave

- Warburg O. (1956) "On the Origin of Cancer Cells" - Science
- Pollack GH. (2013) "The Fourth Phase of Water" - Annual Review of Analytical Chemistry
- Ingber DE. (1997) "Tensegrity: The Architectural Basis of Cellular Mechanotransduction" - Annual Review of Physiology

### Sites de Referência

- PubMed: https://pubmed.ncbi.nlm.nih.gov/
- Google Scholar: https://scholar.google.com/
- SciHub: (acesso a artigos pagos - use com responsabilidade)

---

## 🔍 Navegação Rápida

### Por Objetivo

- **Quero começar rápido**: [Shot dos Campeões](https://jvmasc.github.io/saude.opensource/pt/docs/protocolo-mestre/shot-matinal/)
- **Quero entender tudo**: [Módulos](https://jvmasc.github.io/saude.opensource/pt/docs/modulos/)
- **Tenho sintoma específico**: [Playbooks](https://jvmasc.github.io/saude.opensource/pt/docs/playbooks/)
- **Quero fazer screening**: [Screening v2](https://jvmasc.github.io/saude.opensource/pt/docs/ferramentas/screening-v2/)

### Por Tema

- **Tireóide**: [Módulo Iodo](content/docs/modulos/01-iodo.md)
- **Intestino**: [Módulo Intestino](content/docs/modulos/02-intestino.md)
- **Energia**: [Playbook Fadiga](content/docs/playbooks/fadiga-cronica.md)
- **Sono**: [Playbook Insônia](content/docs/playbooks/insonia.md)
- **Stress**: [Playbook Ansiedade](content/docs/playbooks/ansiedade.md)

### Para Desenvolvedores

- **Contribuir**: [Como Contribuir](#-como-contribuir)
- **Setup local**: [Para Desenvolvedores](#-para-desenvolvedores)
- **Issues**: [GitHub Issues](https://github.com/jvmasc/saude.opensource/issues)
- **Pull Requests**: [GitHub PRs](https://github.com/jvmasc/saude.opensource/pulls)

---

## 📞 FAQ - Perguntas Frequentes

<details>
<summary><strong>Posso usar estes protocolos sem consultar médico?</strong></summary>

**NÃO.** Este conteúdo é educacional. Você DEVE consultar profissional de saúde qualificado antes de iniciar qualquer protocolo. Muitos dos compostos aqui descritos podem interagir com medicamentos ou contraindicar condições médicas.
</details>

<details>
<summary><strong>O Shot dos Campeões é seguro?</strong></summary>

Para maioria das pessoas, sim, **MAS** você deve:
1. Fazer screening laboratorial antes (especialmente tireóide)
2. Começar com doses mínimas (2 gotas de Lugol, não 8)
3. Monitorar reações adversas diariamente
4. Suspender se houver reações graves (palpitações, tremores, insônia severa)
5. Consultar profissional se tiver condições preexistentes

Hipertireoidismo, Hashimoto, gravidez e outras condições exigem protocolos adaptados.
</details>

<details>
<summary><strong>Quanto tempo até ver resultados?</strong></summary>

Varia por pessoa e protocolo:
- **Energia/disposição**: 7-21 dias
- **Sono**: 3-14 dias
- **Digestão**: 3-7 dias
- **Hormônios/tireóide**: 30-90 dias
- **Condições crônicas**: 90-180 dias

Se não houver melhora em 30 dias, reavalie com profissional.
</details>

<details>
<summary><strong>Posso modificar as dosagens?</strong></summary>

**Sim, mas com cuidado.** As dosagens são referências baseadas em literatura, mas cada pessoa é única:
- Sempre comece com doses mínimas
- Aumente gradualmente (10-20% por semana)
- Monitore sintomas diariamente
- Use exames laboratoriais para guiar ajustes
- Consulte profissional para personalização
</details>

<details>
<summary><strong>Este projeto é comercial?</strong></summary>

**NÃO.** Este projeto é 100% open source e sem fins lucrativos:
- Não vendemos produtos
- Não aceitamos doações
- Não fazemos publicidade
- Licença CC BY 4.0 (livre para usar)

Filosofia: conhecimento de saúde deve ser livre e acessível.
</details>

<details>
<summary><strong>Como contribuir se não sou desenvolvedor?</strong></summary>

Você pode contribuir de várias formas:
- Reportar erros de digitação/gramática (via Issues)
- Sugerir melhorias de clareza
- Compartilhar casos clínicos anônimos
- Traduzir conteúdo (PT↔EN)
- Adicionar referências científicas atualizadas
- Dar Star ⭐ no repositório

Toda contribuição é valiosa!
</details>

---

<div align="center">

**[⬆ Voltar ao Topo](#pharmacopeiainfo--saúde-open-source)**

---

Feito com ❤️ e rigor científico por **Farm. João**

**v4.1** | Janeiro 2026 | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

</div>
