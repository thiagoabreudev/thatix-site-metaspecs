---
spec_version: "1.0.0"
valid_from: "2026-01-13"
last_updated: "2026-01-13"
supersedes: null
status: "active"
category: "meta"
tags: ["versioning", "governance", "policy", "semver"]
---

# Política de Versionamento de MetaSpecs

:::version_info
**Versão**: 1.0.0
**Válida desde**: 2026-01-13
**Status**: Ativa
:::

:::breaking_changes
**v1.0.0** (baseline):
- Primeira versão da política de versionamento
- Estabelece SemVer para todas as specs
- Define processo de atualização e governança
- Implementa Context Governance
:::

---

## 1. Visão Geral

Este documento define a política oficial de versionamento de especificações (MetaSpecs) do projeto, garantindo **Context Governance** e evitando problemas como Context Drift, Context Clash e regressão semântica.

### Por Que Versionar Specs?

**Problema sem versionamento**:
- Context Drift (contexto desatualizado)
- Regressão semântica (significado de termos muda sem controle)
- Conflitos entre documentação e código
- Decisões inconsistentes entre execuções da IA

**Solução**:
Versionamento semântico de contexto, assim como APIs e contratos.

---

## 2. Formato de Versionamento

Usamos **Semantic Versioning (SemVer)** adaptado para especificações:

```
MAJOR.MINOR.PATCH
```

### 2.1 MAJOR (x.0.0)

**Breaking Changes** - Mudanças incompatíveis que afetam interpretação ou uso:

**Exemplos em Specs de Negócio**:
- Mudança de significado de termos-chave (ex: "limite" passa a significar algo diferente)
- Remoção de persona principal
- Mudança estrutural na jornada do cliente
- Alteração incompatível de precificação
- Remoção de seção obrigatória

**Exemplos em ADRs**:
- Reversão de decisão arquitetural
- Mudança de stack tecnológico
- Alteração de padrão de design system

**Quando NÃO é MAJOR**:
- Adição de nova persona (mantendo as existentes)
- Expansão de seção existente
- Novos exemplos ou casos de uso

### 2.2 MINOR (0.x.0)

**Adições Compatíveis** - Novo conteúdo sem quebrar existente:

**Exemplos**:
- Nova seção adicionada
- Nova persona adicionada (mantendo existentes)
- Novos campos opcionais
- Novos exemplos e casos de uso
- Expansão de métricas
- Adição de ADR novo

**Quando NÃO é MINOR**:
- Correção de typos → PATCH
- Mudança de significado → MAJOR

### 2.3 PATCH (0.0.x)

**Correções e Clarificações** - Sem impacto semântico:

**Exemplos**:
- Correção de typos
- Atualização de links
- Ajustes de formatação
- Clarificações de texto existente
- Correção de datas
- Ajustes de exemplos sem mudar estrutura

---

## 3. Estrutura de Frontmatter

Toda spec DEVE ter o seguinte frontmatter YAML:

```yaml
---
spec_version: "1.0.0"
valid_from: "2026-01-13"
last_updated: "2026-01-13"
supersedes: null  # ou "0.9.0" se aplicável
status: "active"  # active | deprecated | draft
category: "business|technical|meta|product"
tags: ["tag1", "tag2", "tag3"]
---
```

### Campos Obrigatórios

- **spec_version**: Versão SemVer (MAJOR.MINOR.PATCH)
- **valid_from**: Data de início de validade (YYYY-MM-DD)
- **last_updated**: Data da última modificação (YYYY-MM-DD)
- **supersedes**: Versão anterior substituída (ou `null` se primeira versão)
- **status**: Estado atual da spec
  - `active`: Spec em uso
  - `deprecated`: Obsoleta, substituída por nova versão
  - `draft`: Em desenvolvimento, não usar em produção
- **category**: Tipo de spec (business, technical, meta, product)
- **tags**: Array de tags para categorização

### Campos Específicos por Tipo

**Para ADRs**, adicionar:
```yaml
adr_number: "001"
title: "Título da Decisão"
date: "2026-01-13"
deciders: ["tech-lead", "founders"]
consulted: []
informed: ["all-developers"]
superseded_by: null  # ou "adr_number" se aplicável
```

**Para Features**, adicionar:
```yaml
priority: "high|medium|low"
related_specs:
  - "../PRODUCT_STRATEGY.md"
  - "../CUSTOMER_JOURNEY.md"
```

---

## 4. Blocos de Informação

Após o título principal, toda spec DEVE ter:

### 4.1 Bloco version_info

```markdown
:::version_info
**Versão**: 1.0.0
**Válida desde**: 2026-01-13
**Status**: Ativa
:::
```

### 4.2 Bloco breaking_changes

```markdown
:::breaking_changes
**v2.0.0**:
- Mudança X que quebra compatibilidade
- Remoção de campo Y

**v1.1.0**:
- Adição de seção Z

**v1.0.0** (baseline):
- Primeira versão versionada
:::
```

---

## 5. Processo de Atualização

### 5.1 Fluxo de Atualização

```
1. Identificar mudança necessária
   ↓
2. Classificar tipo (MAJOR/MINOR/PATCH)
   ↓
3. Atualizar spec_version no frontmatter
   ↓
4. Atualizar last_updated
   ↓
5. Se MAJOR: atualizar supersedes
   ↓
6. Documentar em :::breaking_changes
   ↓
7. Registrar em VERSION_HISTORY.md
   ↓
8. Atualizar índice com nova versão
   ↓
9. Comunicar stakeholders (se relevante)
```

### 5.2 Exemplo de Atualização MAJOR

**Antes (v1.2.3)**:
```yaml
spec_version: "1.2.3"
last_updated: "2026-01-10"
supersedes: null
```

**Depois (v2.0.0)**:
```yaml
spec_version: "2.0.0"
last_updated: "2026-01-20"
supersedes: "1.2.3"
```

E no bloco breaking_changes:
```markdown
:::breaking_changes
**v2.0.0**:
- "Limite" agora significa "pré-aprovado por CPF" (antes era "limite contratual do convênio")
- Removida persona "Gerente de Operações" (consolidada em "CTO/VP")

**v1.2.3**:
...
:::
```

---

## 6. Deprecação de Specs

### 6.1 Quando Deprecar

Uma spec é marcada como `deprecated` quando:
- Foi substituída por nova versão incompatível
- Decisão arquitetural foi revertida (ADRs)
- Feature foi descontinuada

### 6.2 Processo de Deprecação

1. **Criar nova versão** com mudanças necessárias
2. **Atualizar spec antiga**:
   - `status: "deprecated"`
   - Adicionar aviso no topo
3. **Documentar no histórico**
4. **Manter arquivo antigo** por 6 meses (não deletar)

### 6.3 Template de Aviso de Deprecação

```markdown
:::warning
⚠️ **SPEC OBSOLETA**

Esta spec foi substituída por [nova_spec.md](nova_spec.md) v2.0.0.

**Data de Deprecação**: 2026-01-20
**Remover após**: 2026-07-20
:::
```

---

## 7. Context Governance

### 7.1 Princípio Jidoka

**Se encontrar spec sem versionamento durante desenvolvimento**:
- 🛑 **PARE** a execução
- ⚠️ **ALERTE** que a spec precisa ser versionada
- 📋 **SUGIRA** executar `/metaspecs:governance:add-versioning`

### 7.2 Validação Automática

IA deve validar antes de usar spec:
```javascript
if (!spec.frontmatter.spec_version) {
  throw new Error("Spec não versionada. Execute /add-versioning primeiro.");
}

if (spec.frontmatter.status === "deprecated") {
  warn("Usando spec obsoleta. Verifique nova versão.");
}
```

### 7.3 Compatibilidade de Versões

**Regras**:
- Specs com MAJOR diferente são **incompatíveis**
- Specs com mesmo MAJOR mas MINOR diferente são **compatíveis forward**
- PATCH sempre é compatível

**Exemplo**:
- v1.0.0 e v1.5.2 → Compatíveis
- v1.9.9 e v2.0.0 → Incompatíveis (breaking change)

---

## 8. Responsabilidades

### 8.1 Tech Lead
- Aprovar mudanças MAJOR em specs técnicas
- Revisar ADRs antes de versionar
- Garantir consistência de versões

### 8.2 Product Owner
- Aprovar mudanças MAJOR em specs de negócio
- Validar impacto de breaking changes
- Comunicar mudanças a stakeholders

### 8.3 Desenvolvedores
- Seguir política ao criar/atualizar specs
- Documentar mudanças em breaking_changes
- Atualizar VERSION_HISTORY.md

### 8.4 IA (Claude)
- Validar versionamento antes de usar spec
- Alertar sobre specs não versionadas
- Sugerir tipo de mudança (MAJOR/MINOR/PATCH)

---

## 9. Casos Especiais

### 9.1 Primeira Versão (Baseline)

Specs existentes sendo versionadas pela primeira vez:
- Versão: `1.0.0`
- `supersedes: null`
- Breaking changes: "v1.0.0 (baseline): Primeira versão versionada"

### 9.2 Specs em Draft

Specs em desenvolvimento:
- Versão: `0.x.y` (MAJOR = 0)
- `status: "draft"`
- Não precisa seguir SemVer estrito até v1.0.0

### 9.3 Hot Fixes

Correções urgentes:
- Incrementar PATCH
- Documentar no breaking_changes
- Comunicar imediatamente

---

## 10. Ferramentas e Automação

### 10.1 Slash Commands

- `/metaspecs:governance:add-versioning` - Adicionar versionamento a specs existentes
- `/metaspecs:governance:validate` - Validar frontmatter de specs
- `/metaspecs:governance:bump-version` - Incrementar versão de spec

### 10.2 Pre-commit Hooks

TODO: Implementar validação automática de:
- Frontmatter obrigatório
- Formato SemVer correto
- Atualização de VERSION_HISTORY.md

---

## 11. Exemplos Práticos

### Exemplo 1: Adicionando Nova Persona (MINOR)

**Mudança**: Adicionar "Product Manager" às personas

**Tipo**: MINOR (adição compatível)

**Ações**:
1. `spec_version: "1.0.0"` → `"1.1.0"`
2. `last_updated: "2026-01-13"` → `"2026-01-20"`
3. Adicionar no breaking_changes:
   ```
   **v1.1.0**:
   - Adicionada nova persona: Product Manager (foca em métricas e roadmap)
   ```
4. Registrar em VERSION_HISTORY.md

### Exemplo 2: Mudando Significado de Termo (MAJOR)

**Mudança**: "Limite" passa a significar "pré-aprovado" ao invés de "contratual"

**Tipo**: MAJOR (breaking change semântico)

**Ações**:
1. `spec_version: "1.5.2"` → `"2.0.0"`
2. `supersedes: null` → `"1.5.2"`
3. `last_updated: "2026-01-13"` → `"2026-02-01"`
4. Adicionar no breaking_changes:
   ```
   **v2.0.0**:
   - BREAKING: "Limite" agora significa "limite pré-aprovado por CPF" (antes era "limite contratual do convênio")
   - Todas as referências a "limite" devem ser reinterpretadas
   ```
5. Deprecar v1.5.2 com aviso

### Exemplo 3: Corrigindo Typo (PATCH)

**Mudança**: Corrigir "preço" → "preço"

**Tipo**: PATCH (correção)

**Ações**:
1. `spec_version: "1.2.3"` → `"1.2.4"`
2. `last_updated` → data atual
3. Não precisa documentar em breaking_changes (opcional)

---

## 12. Checklist de Conformidade

Antes de mergear PR com mudança em spec:

- [ ] Frontmatter YAML completo e válido
- [ ] `spec_version` seguindo SemVer
- [ ] `last_updated` atualizado
- [ ] `supersedes` correto (se MAJOR)
- [ ] Bloco `:::version_info` atualizado
- [ ] Mudança documentada em `:::breaking_changes`
- [ ] Registrado em `VERSION_HISTORY.md`
- [ ] Índice atualizado com nova versão
- [ ] Se MAJOR: comunicado a stakeholders

---

## 13. Referências

- [Semantic Versioning 2.0.0](https://semver.org/)
- [Context Governance](../business/PRODUCT_STRATEGY.md)
- [VERSION_HISTORY.md](VERSION_HISTORY.md)

---

**Última Atualização**: 2026-01-13
**Próxima Revisão**: Semestral ou após feedback significativo
**Responsável**: Tech Lead + Product Owner
**Aprovado por**: Founders
