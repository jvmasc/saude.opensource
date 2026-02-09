# Notas de Processo - Reorganização v4.1

**Data:** 28-01-2026
**Status:** Concluído ✅
**Responsável:** Farm. João + Claude Sonnet 4.5

---

## Objetivo da Reorganização

Transformar a pasta "3. Saúde Open Source" de uma estrutura desorganizada em uma arquitetura profissional com separação clara entre:
- Camada de autoria (authoring layer)
- Camada de publicação (publishing layer)
- Meta-documentação
- Recursos de referência
- Arquivos históricos

---

## Decisões Principais

### 1. Estrutura de 4 Camadas + Archive

**Decisão:** Criar estrutura numerada (00-, 01-, 02-, 03-, 99-) para indicar hierarquia e função.

**Justificativa:**
- Separação clara de responsabilidades
- Prefixos numéricos facilitam ordenação e navegação
- Workflow explícito: onde editar vs onde publicar

**Estrutura implementada:**
```
00-meta/          → Meta-documentação do projeto
01-conteudo-fonte/ → Fonte autoritativa (AUTHORING)
02-recursos/      → Material de referência externo
03-site-hugo/     → Site Hugo (PUBLISHING)
99-archive/       → Arquivos históricos/deprecated
```

### 2. Nomenclatura Consistente

**Decisão:** Todas as pastas em minúsculas, sem emojis em nomes de arquivo.

**Mudanças realizadas:**
- `Playbooks/` → `playbooks/` (minúsculo)
- `docs/` → `ferramentas/` (mais descritivo)
- `Recursos/` → `analises-livros/` (mais específico)
- `🔬 HUMAN OS v4.0.md` → `HUMAN-OS-v4.0.md` (sem emoji)

**Justificativa:**
- Compatibilidade com sistemas Unix/Linux
- Facilita automação e scripts
- Nomenclatura descritiva e profissional

### 3. Separação Authoring vs Publishing

**Decisão:** `01-conteudo-fonte/` é a fonte de verdade, `03-site-hugo/` é read-only após sync.

**Workflow estabelecido:**
1. Editar conteúdo → `01-conteudo-fonte/`
2. Sincronizar → `03-site-hugo/saude.opensource/content/docs/`
3. Adicionar frontmatter YAML
4. Commit e push → Hugo Actions deploya

**Justificativa:**
- Evita edições conflitantes
- Fonte de verdade única
- Separação de camadas (content vs presentation)

### 4. Meta-Documentação Separada

**Decisão:** Criar pasta `00-meta/` para documentação sobre o projeto.

**Conteúdo:**
- `README.md` (mantido na raiz, documenta estrutura)
- `SAUDE-OPEN-SOURCE-CLAUDE.md` (docs para Claude AI)
- `changelog.md` (histórico de versões)
- `HUMAN-OS-v4.0.md` (filosofia/homepage conceitual)

**Justificativa:**
- Meta-documentação ≠ conteúdo de saúde
- Facilita manutenção do projeto
- Clareza sobre "docs do projeto" vs "conteúdo publicável"

### 5. Archive Histórico

**Decisão:** Mover arquivos deprecated para `99-archive/`, excluir do Git (.gitignore).

**Arquivado:**
- `core/` (arquitetura v3, desatualizada)
- `estrategia/` (business strategy, arquivada)
- `sistemas/` (docs técnicos desatualizados)
- `fundacionais/` (deprecated, conteúdo movido para modulos/)
- `debugging/` (deprecated)
- `_archive/` (archive original)
- `README-v4.0.md` (backup do README antigo)

**Justificativa:**
- Preserva histórico sem poluir workspace
- Permite recuperação futura se necessário
- Reduz confusão sobre o que está ativo

### 6. Git Strategy

**Decisão:** Usar Git para rastrear mudanças, excluir Hugo repo e archive via .gitignore.

**Commits realizados:**
1. `f0ac1d1` - Reorganização da estrutura do projeto v4.1 (71 arquivos)
2. `46d94c5` - Atualizar SAUDE-OPEN-SOURCE-CLAUDE.md

**.gitignore criado:**
```
# Repositório Hugo (tem seu próprio Git)
03-site-hugo/saude.opensource/

# Archive histórico
99-archive/
```

**Justificativa:**
- Hugo repo é Git independente (evita nested repos)
- Archive não precisa versionamento (backup estático)
- Foco no conteúdo fonte

---

## Mudanças de Caminhos

### Antes → Depois

| Antes | Depois | Motivo |
|-------|--------|--------|
| `modulos/` | `01-conteudo-fonte/modulos/` | Organização em camadas |
| `Playbooks/` | `01-conteudo-fonte/playbooks/` | Minúsculo + camada |
| `protocolo-mestre/` | `01-conteudo-fonte/protocolo-mestre/` | Camada de autoria |
| `docs/` | `01-conteudo-fonte/ferramentas/` | Renomeado + camada |
| `Recursos/` | `02-recursos/analises-livros/` | Especificidade |
| `saude.opensource/` | `03-site-hugo/saude.opensource/` | Camada de publicação |
| `🔬 HUMAN OS v4.0.md` | `00-meta/HUMAN-OS-v4.0.md` | Sem emoji + meta |
| `SAUDE-OPEN-SOURCE-CLAUDE.md` | `00-meta/SAUDE-OPEN-SOURCE-CLAUDE.md` | Meta-docs |
| `changelog.md` | `00-meta/changelog.md` | Meta-docs |
| `core/`, `estrategia/`, etc. | `99-archive/[pasta]/` | Arquivamento |

---

## Atualização de Documentação

### README.md

**Antes:** Documentava v4.0 com estrutura antiga.

**Depois:** Novo README criado documentando:
- Estrutura de 4 camadas
- Workflow de edição
- Links rápidos
- Propósito de cada pasta
- Versão v4.1

**Backup:** `99-archive/README-v4.0.md`

### SAUDE-OPEN-SOURCE-CLAUDE.md

**Atualizações realizadas:**
- Seção "DIRECTORY STRUCTURE" reescrita com nova estrutura
- Todas as referências de caminhos atualizadas:
  - `/Playbooks/` → `01-conteudo-fonte/playbooks/`
  - `/docs/` → `01-conteudo-fonte/ferramentas/`
  - `/Recursos/` → `02-recursos/analises-livros/`
  - `🔬 HUMAN OS v4.0` → `HUMAN-OS-v4.0` (global replace)
- Adicionadas notas sobre workflow authoring vs publishing
- Documentada separação clara de camadas

---

## Verificações Realizadas

### ✅ Checklist Pós-Implementação

- [x] Todas as pastas criadas corretamente
- [x] Nenhum arquivo perdido (38 arquivos em 01-conteudo-fonte/)
- [x] README.md atualizado e documentando nova estrutura
- [x] Hugo ainda funciona (`hugo` build executado com sucesso)
- [x] Nenhuma pasta "solta" na raiz (apenas 5 principais + README.md)
- [x] `99-archive/` contém backup do README antigo
- [x] Nomenclatura consistente (minúsculas, sem emojis)
- [x] `SAUDE-OPEN-SOURCE-CLAUDE.md` atualizado
- [x] Git commits realizados
- [x] .gitignore criado

### Contagem de Arquivos

| Pasta | Arquivos |
|-------|----------|
| `00-meta/` | 3 arquivos |
| `01-conteudo-fonte/modulos/` | 10 arquivos |
| `01-conteudo-fonte/playbooks/` | 8 arquivos |
| `01-conteudo-fonte/protocolo-mestre/` | 7 arquivos |
| `01-conteudo-fonte/ferramentas/` | 13 arquivos |
| `02-recursos/analises-livros/` | 7 arquivos |
| `99-archive/` | 7 itens (pastas + README) |

**Total conteúdo fonte:** 38 arquivos

---

## Benefícios Alcançados

### 1. Clareza Estrutural
- Separação explícita entre authoring e publishing
- Fácil identificar onde editar conteúdo
- Meta-documentação isolada

### 2. Nomenclatura Profissional
- Consistência: tudo em minúsculas
- Prefixos numéricos indicam hierarquia
- Nomes descritivos em português

### 3. Workflow Explícito
- `01-conteudo-fonte/` = editar aqui ✏️
- `03-site-hugo/` = publicar aqui 🚀 (read-only após sync)
- Camadas claramente separadas

### 4. Manutenibilidade
- Adicionar novos módulos → `01-conteudo-fonte/modulos/`
- Adicionar recursos → `02-recursos/analises-livros/`
- Archive histórico preservado mas separado

### 5. Git Strategy Limpa
- Fonte versionada
- Hugo repo independente
- Archive excluído do versionamento

---

## Riscos Mitigados

### ✅ Git History
**Risco:** Perder histórico ao mover arquivos.
**Mitigação:** Arquivos não estavam rastreados ainda (fresh repo). Primeiro commit preserva estrutura completa.

### ✅ Links Quebrados
**Risco:** Referências antigas quebrarem.
**Mitigação:** Atualizado `SAUDE-OPEN-SOURCE-CLAUDE.md` com todos os novos caminhos. Hugo usa caminhos relativos dentro de `content/`.

### ✅ Hugo Sync
**Risco:** Processo de sync quebrar.
**Mitigação:** Documentado workflow. Hugo testado e funciona. Sync manual até criar script automático.

### ✅ Nested Git Repos
**Risco:** Hugo repo nested causar problemas.
**Mitigação:** Adicionado `03-site-hugo/saude.opensource/` ao .gitignore. Hugo mantém seu próprio Git.

---

## Próximos Passos Sugeridos

### Curto Prazo
1. ✅ Revisar estrutura (FEITO)
2. 🔄 Atualizar `changelog.md` com esta reorganização
3. 🔄 Push para remote (se houver)

### Médio Prazo
1. Criar script de sync: `01-conteudo-fonte/` → `03-site-hugo/`
2. Automatizar adição de frontmatter YAML
3. Documentar processo de sync detalhado no README

### Longo Prazo
1. Considerar separar Hugo em repo completamente independente
2. CI/CD para sync automático
3. Testes automatizados de links internos

---

## Lições Aprendidas

### O que funcionou bem:
- Prefixos numéricos (00-, 01-, 02-, 03-, 99-) são intuitivos
- Separação authoring/publishing evita confusão
- Archive preserva histórico sem poluir workspace
- Git + .gitignore mantém foco no essencial

### O que evitar:
- Emojis em nomes de arquivo (incompatibilidade)
- Misturar fonte e publicação na mesma pasta
- Deixar arquivos deprecated na raiz
- Nomenclatura inconsistente (CamelCase vs minúsculas)

### Decisões que podem ser revisitadas:
- Nome "ferramentas" (pode virar "docs" novamente se preferir)
- Estrutura de `02-recursos/` (pode subdividir mais no futuro)
- .gitignore do archive (pode querer versionar no futuro)

---

## Conclusão

A reorganização v4.1 transformou a pasta de uma coleção desordenada em uma estrutura profissional com:
- ✅ Separação clara de responsabilidades
- ✅ Nomenclatura consistente e profissional
- ✅ Workflow explícito de authoring → publishing
- ✅ Arquivos históricos preservados mas isolados
- ✅ Documentação atualizada e sincronizada
- ✅ Hugo funcionando perfeitamente

O projeto agora está preparado para escalar com uma base organizacional sólida.

---

**Pharmacopeia.info** — The Open Source Health Repository
`v4.1` | Reorganizado em 28-01-2026
