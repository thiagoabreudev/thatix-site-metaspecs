# Comandos de Metaspecs - Context Governance

Comandos para aplicar conceitos avançados de **Engenharia de Contexto** às metaspecs do site da Thatix.

A Thatix é uma consultoria especializada em desenvolvimento com IA, e este repositório contém as especificações que direcionam o desenvolvimento do site institucional.

---

## 📚 Índice

- [Visão Geral](#visão-geral)
- [Comandos de Governance](#comandos-de-governance)
- [Comandos de Validation](#comandos-de-validation)
- [Comandos de Observability](#comandos-de-observability)
- [Fluxo de Uso Recomendado](#fluxo-de-uso-recomendado)
- [Benefícios](#benefícios)

---

## 🎯 Visão Geral

Estes comandos implementam os **10 conceitos críticos** de engenharia de contexto:

### 1. Context Governance
Versionamento semântico e governança de contexto.

### 2. Intent as Code
Formalização de intenções com goals, constraints e non-goals.

### 3. Failure Modes as Specs
Documentação de falhas conhecidas e mitigações.

### 4. Explainability by Design
IA deve explicar decisões importantes.

### 5. Jidoka (Fail-Fast Validation)
Validação rigorosa antes de execução.

### 6. Context Drift Detection
Detectar desalinhamento entre specs e código.

### 7. Spec Audit
Auditoria de qualidade e completude.

### 8. Context Hierarchy
Precedência clara quando specs conflitam.

### 9. Context Observability
Rastreamento de decisões da IA.

### 10. Anti-Patterns Documentation
Documentar padrões a evitar.

---

## 📁 Estrutura de Comandos

```
.claude/commands/metaspecs/
├── governance/                 # Context Governance
│   ├── add-versioning.md       # Versionamento semântico
│   ├── add-intent.md           # Intent as Code
│   ├── add-failure-modes.md    # Failure Modes
│   └── add-explainability.md   # Explainability Requirements
├── validation/                 # Validação e Auditoria
│   ├── validate-context.md     # Jidoka (fail-fast)
│   ├── check-drift.md          # Context Drift detection
│   ├── audit-spec.md           # Auditoria de specs
│   └── validate-hierarchy.md   # Hierarquia de contexto
├── observability/              # Rastreamento
│   ├── track-context.md        # Context observability
│   └── add-anti-patterns.md    # Anti-patterns doc
└── README.md                   # Este arquivo
```

---

## 🔧 Comandos de Governance

### `/add-versioning`

**Conceito**: Context Governance

**O que faz**: Adiciona versionamento semântico (SemVer) às specs.

**Campos adicionados**:
- `spec_version` (MAJOR.MINOR.PATCH)
- `valid_from` (data de início)
- `last_updated` (última modificação)
- `supersedes` (versão anterior)
- `status` (active/deprecated/draft)
- `:::breaking_changes` (histórico de mudanças)

**Uso**:
```bash
/add-versioning                 # Todas as specs
/add-versioning business        # Apenas specs de negócio
/add-versioning technical       # Apenas specs técnicas
/add-versioning <caminho>       # Spec específica
```

**Benefícios**:
- ✅ Evita Context Clash
- ✅ Facilita auditoria
- ✅ Permite rollback semântico
- ✅ Detecta context drift

---

### `/add-intent`

**Conceito**: Intent as Code

**O que faz**: Adiciona seção `:::intent` com goals, constraints e non-goals.

**Template**:
```markdown
:::intent
**Goal**: [O que queremos alcançar]

**Constraints** (limites obrigatórios):
- [Constraint 1]
- [Constraint 2]

**Non-Goals** (o que NÃO fazer):
- [Non-goal 1]
- [Non-goal 2]
:::
```

**Uso**:
```bash
/add-intent                     # Todas as specs críticas
/add-intent technical           # Specs técnicas
/add-intent <caminho>           # Spec específica
```

**Benefícios**:
- ✅ Limita autonomia da IA
- ✅ Previne scope creep
- ✅ Documenta o que NÃO fazer
- ✅ Cria guardrails para decisões

---

### `/add-failure-modes`

**Conceito**: Failure Modes as Specs

**O que faz**: Documenta falhas conhecidas e mitigações.

**Template**:
```markdown
:::failure_modes
1. **[Nome da Falha]**
   - **Tipo**: context_clash | hallucination | integration | validation | security
   - **Descrição**: [O que acontece]
   - **Gatilho**: [Quando ocorre]
   - **Impacto**: 🔴 Crítico | 🟡 Médio | 🟢 Baixo
   - **Mitigação**: [Como prevenir]
   - **Detecção**: [Como identificar]
:::
```

**Uso**:
```bash
/add-failure-modes              # Todas as specs técnicas
/add-failure-modes <caminho>    # Spec específica
```

**Benefícios**:
- ✅ Previne erros conhecidos
- ✅ Mitiga alucinações da IA
- ✅ Documenta estratégias de recuperação
- ✅ Evita repetição de falhas

---

### `/add-explainability`

**Conceito**: Explainability by Design

**O que faz**: Adiciona requisitos de explainability (IA deve explicar decisões).

**Template**:
```markdown
:::explainability
**Requirement**: ✅ Required | ⚠️ Recommended | ⭕ Optional

**Output Format**:
- **Decision**: [O que foi decidido]
- **Source**: [Qual spec/seção]
- **Rationale**: [Por que]
- **Alternatives**: [Outras opções]
- **Trade-offs**: [Prós e contras]

**Audit Trail**:
- Timestamp de decisão
- Specs consultadas (nome + versão)
:::
```

**Uso**:
```bash
/add-explainability             # Todas as specs críticas
/add-explainability <caminho>   # Spec específica
```

**Benefícios**:
- ✅ Decisões auditáveis
- ✅ Transparência
- ✅ Facilita debugging
- ✅ Aumenta confiança

---

## ✅ Comandos de Validation

### `/validate-context`

**Conceito**: Jidoka (Fail-Fast)

**O que faz**: Valida contexto ANTES de execução (princípio de parar quando erro detectado).

**Validações**:
1. **Estrutural**: Arquivos obrigatórios existem
2. **Versionamento**: Todas as specs versionadas
3. **Intent**: Specs críticas têm Intent (warning)
4. **Failure Modes**: Specs documentam falhas (warning)
5. **Explainability**: Requirements configurados
6. **Consistência**: Sem conflitos entre specs
7. **Hierarquia**: Precedência clara

**Uso**:
```bash
/validate-context               # Valida tudo
/validate-context business      # Apenas business specs
/validate-context --strict      # Warnings = erros
/validate-context --quick       # Só validações bloqueantes
```

**Saída**: Relatório com ✅ / ⚠️ / ❌ para cada validação.

**Ação**: 🛑 BLOQUEIA execução se críticos detectados.

**Benefícios**:
- ✅ Previne erros antes de acontecer
- ✅ Garante qualidade do contexto
- ✅ Jidoka aplicado à IA

---

### `/check-drift`

**Conceito**: Context Drift Detection

**O que faz**: Detecta desalinhamento entre specs e código real.

**Tipos de Drift**:
1. **Documentation Drift**: Spec documenta o que não existe
2. **Implementation Drift**: Código tem o que spec não documenta
3. **Semantic Drift**: Termo muda de significado sem atualização
4. **Architectural Drift**: Stack real ≠ stack documentada

**Verificações**:
- Stack tecnológica (specs vs package.json)
- Features (specs vs endpoints/componentes)
- ADRs (decisões vs código real)
- Componentes (doc vs arquivos)
- Termos (definições vs uso)
- Atualização (idade das specs)

**Uso**:
```bash
/check-drift                    # Verifica tudo
/check-drift stack              # Apenas stack
/check-drift --critical-only    # Só drifts críticos
/check-drift --age-threshold=90 # Specs > 90 dias
```

**Saída**: Relatório com drifts detectados (🔴🟡🟢).

**Benefícios**:
- ✅ Identifica specs desatualizadas
- ✅ Encontra código não documentado
- ✅ Previne decisões baseadas em contexto obsoleto

---

### `/audit-spec`

**Conceito**: Spec Quality Audit

**O que faz**: Auditoria completa de qualidade de uma spec.

**Dimensões auditadas**:
1. **Estrutura**: Frontmatter, seções, formatação (10 pontos)
2. **Qualidade**: Clareza, precisão, completude (12 pontos)
3. **Padrões**: Nomenclatura, Intent, Failure Modes (9 pontos)
4. **Usabilidade**: Estrutura acessível, info acionável (9 pontos)
5. **Consistência**: Sem contradições internas (5 pontos)
6. **Alinhamento**: Compatibilidade com outras specs (5 pontos)

**Uso**:
```bash
/audit-spec <caminho>           # Audita spec específica
/audit-spec CLAUDE.meta.md --strict  # Score mínimo 90%
/audit-spec CLAUDE.meta.md --fix     # Sugerir correções
```

**Saída**: Score 0-100% + ações recomendadas (🔴🟡🟢).

**Classificação**:
- 90-100%: ✅ Excelente
- 75-89%: ⚠️ Bom (melhorias recomendadas)
- 60-74%: 🟡 Regular (melhorias necessárias)
- < 60%: 🔴 Crítico (revisão completa)

**Benefícios**:
- ✅ Garante qualidade das specs
- ✅ Identifica melhorias específicas
- ✅ Padroniza documentação

---

### `/validate-hierarchy`

**Conceito**: Context Hierarchy

**O que faz**: Valida que hierarquia de contexto está definida e respeitada.

**Hierarquia**:
```
1. Meta Specs (_meta/)         → Maior precedência
2. Business Specs (business/)  → Alta precedência
3. Technical Specs (technical/) → Média precedência
4. Execution Context (sessions/) → Menor precedência
```

**Validações**:
1. **Documentação**: `CONTEXT_HIERARCHY.md` existe
2. **Estrutura**: Camadas organizadas corretamente
3. **Conflitos**: Detecta e valida resoluções
4. **ADRs**: ADRs > Guidelines
5. **Referências**: Camadas inferiores → superiores (não vice-versa)

**Uso**:
```bash
/validate-hierarchy             # Valida hierarquia completa
/validate-hierarchy --strict    # Warnings = erros
/validate-hierarchy --fix       # Sugere correções
```

**Saída**: Relatório de conflitos e violações de hierarquia.

**Benefícios**:
- ✅ Resolução clara de conflitos
- ✅ Precedência sempre definida
- ✅ IA sabe qual spec seguir

---

## 📊 Comandos de Observability

### `/track-context`

**Conceito**: Context Observability

**O que faz**: Rastreia qual contexto foi usado pela IA.

**Tracking**:
- **Decision Log**: Histórico de decisões com sources
- **Spec Usage Metrics**: Quais specs são consultadas e frequência
- **Version Usage**: Quais versões estão sendo usadas

**Arquivos criados**:
- `specs/_meta/DECISION_LOG.md`
- `specs/_meta/SPEC_USAGE_METRICS.md`

**Uso**:
```bash
/track-context init             # Inicializa tracking
/track-context log <decision>   # Adiciona decisão manual
/track-context metrics          # Gera relatório de uso
/track-context analyze          # Análise de padrões
/track-context --format=json    # Output JSON
```

**Benefícios**:
- ✅ Auditoria completa de decisões
- ✅ Identifica specs mais/menos usadas
- ✅ Detecta specs candidatas a remoção
- ✅ Mede impacto de atualizações

---

### `/add-anti-patterns`

**Conceito**: Anti-Patterns Documentation

**O que faz**: Documenta padrões a evitar no desenvolvimento com IA.

**10 Anti-Patterns Principais**:
1. Prompt-Only Development
2. Context Dump
3. Specs Não Versionadas
4. RAG Sem Governança
5. Agentes Sem Limites
6. Specs Genéricas (Copy-Paste)
7. Documentação e Código Divergentes
8. Sem Failure Modes Documentados
9. Explainability Ausente
10. Hierarquia de Contexto Inexistente

**Arquivo criado**: `specs/_meta/ANTI_PATTERNS.md`

**Uso**:
```bash
/add-anti-patterns              # Cria doc com os 10 principais
/add-anti-patterns add <name>   # Adiciona anti-pattern específico
/add-anti-patterns check        # Verifica código contra anti-patterns
/add-anti-patterns list         # Lista anti-patterns documentados
```

**Benefícios**:
- ✅ Previne erros comuns
- ✅ Educa desenvolvedores
- ✅ Melhora qualidade do código
- ✅ Reduz retrabalho

---

## 🔄 Fluxo de Uso Recomendado

### Setup Inicial (Uma vez)

```bash
# 1. Adicionar versionamento
/add-versioning

# 2. Adicionar Intent às specs críticas
/add-intent

# 3. Documentar failure modes conhecidos
/add-failure-modes

# 4. Configurar explainability
/add-explainability

# 5. Criar documentação de anti-patterns
/add-anti-patterns

# 6. Validar hierarquia
/validate-hierarchy

# 7. Inicializar tracking
/track-context init
```

### Antes de Cada Desenvolvimento

```bash
# Validar contexto (Jidoka)
/validate-context

# Se validação falhar: corrigir antes de prosseguir
# Se validação passar: prosseguir com desenvolvimento
```

### Durante Desenvolvimento

```bash
# IA automaticamente:
# - Consulta specs versionadas
# - Respeita Intent (constraints + non-goals)
# - Evita failure modes conhecidos
# - Explica decisões importantes
# - Registra em DECISION_LOG.md
```

### Após Desenvolvimento

```bash
# Verificar drift
/check-drift

# Se drift detectado: atualizar specs
```

### Manutenção Periódica

```bash
# Semanal: Analisar métricas de uso
/track-context metrics

# Mensal: Auditar specs críticas
/audit-spec specs/technical/CLAUDE.meta.md

# Trimestral: Validar hierarquia
/validate-hierarchy
```

---

## 🎯 Benefícios Gerais

### Para o Projeto

✅ **Context Governance**: Contexto versionado e governado
✅ **Qualidade**: Specs padronizadas e auditadas
✅ **Consistência**: IA toma decisões previsíveis
✅ **Rastreabilidade**: Decisões 100% auditáveis
✅ **Manutenibilidade**: Fácil atualizar e evoluir

### Para a IA

✅ **Clareza**: Intent explícito, sem ambiguidade
✅ **Guardrails**: Constraints e non-goals claros
✅ **Prevenção**: Failure modes documentados
✅ **Confiança**: Explainability obrigatório
✅ **Validação**: Jidoka previne erros

### Para o Time

✅ **Educação**: Anti-patterns documentados
✅ **Autonomia**: IA pode tomar decisões com confiança
✅ **Eficiência**: Menos retrabalho, mais qualidade
✅ **Transparência**: Decisões explicadas e rastreáveis
✅ **Evolução**: Métricas mostram o que melhorar

---

## 📚 Referências

- **Site Thatix**: [thatix.com](https://thatix.com)
- **Metaspecs Framework**: Baseado em melhores práticas de engenharia de contexto para IA

---

## 🚀 Próximos Passos

1. ✅ **Executar setup inicial** (comandos acima)
2. ✅ **Integrar no workflow** (validação antes de /start)
3. ✅ **Educar time** (compartilhar anti-patterns)
4. ✅ **Monitorar métricas** (tracking de uso)
5. ✅ **Iterar e melhorar** (adicionar novos anti-patterns, failure modes)

---

**A vantagem competitiva não está em usar IA, mas em usar IA melhor que os outros.**

Estes comandos implementam as melhores práticas de engenharia de contexto para desenvolvimento orientado por IA.
