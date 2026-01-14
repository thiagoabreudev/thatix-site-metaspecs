---
spec_version: "1.0.0"
valid_from: "2026-01-13"
last_updated: "2026-01-13"
supersedes: null
status: "active"
category: "meta"
tags: ["index", "governance", "navigation", "context-governance"]
---

# Context Governance - MetaSpecs

:::version_info
**Versão**: 1.0.0
**Válida desde**: 2026-01-13
**Status**: Ativa
:::

:::breaking_changes
**v1.0.0** (baseline):
- Primeira versão do índice de governança
- Estabelece sistema de versionamento SemVer para todas as specs
- Implementa Context Governance para evitar Context Drift
:::

---

## 📋 Visão Geral

Este diretório contém as **meta-especificações** que governam todo o sistema de especificações do projeto. São as "specs das specs" - definem como versionar, atualizar e manter a consistência de toda a documentação.

---

## 📚 Especificações de Governança

### [VERSIONING_POLICY.md](VERSIONING_POLICY.md) `v1.0.0`

**Política oficial de versionamento** de todas as especificações do projeto.

**Conteúdo**:
- ✅ Definição de SemVer para specs (MAJOR.MINOR.PATCH)
- ✅ Estrutura obrigatória de frontmatter YAML
- ✅ Blocos `:::version_info` e `:::breaking_changes`
- ✅ Processo de atualização passo a passo
- ✅ Política de deprecação de specs
- ✅ Princípio Jidoka (validação automática)
- ✅ Responsabilidades por papel (Tech Lead, Product Owner, Dev, IA)
- ✅ Exemplos práticos de todos os cenários

**Quando usar**:
- Antes de criar nova spec
- Ao atualizar spec existente
- Para entender quando incrementar MAJOR, MINOR ou PATCH
- Para deprecar specs obsoletas

---

### [VERSION_HISTORY.md](VERSION_HISTORY.md) `v1.0.0`

**Histórico completo** de versões de todas as especificações do projeto.

**Conteúdo**:
- ✅ Tabelas organizadas por categoria (Meta, Business, Technical, Product)
- ✅ Tracking de 28 especificações
- ✅ Data, tipo e descrição de cada versão
- ✅ Tipos de mudança documentados (major, minor, patch, baseline)
- ✅ Processo de atualização

**Quando usar**:
- Após atualizar qualquer spec (registrar mudança)
- Para auditar evolução do contexto
- Para identificar breaking changes históricos
- Para rastrear quando specs foram criadas/atualizadas

---

## 🎯 Context Governance

### O Que é Context Governance?

**Context Governance** é o conjunto de práticas que garantem que o contexto fornecido à IA seja:
- ✅ **Correto**: Informações precisas e validadas
- ✅ **Atual**: Versionamento rastreia mudanças
- ✅ **Consistente**: Não há contradições entre specs
- ✅ **Intencional**: Mudanças são deliberadas e documentadas

### Problemas que Context Governance Resolve

**Sem Governança**:
- ❌ Context Drift (contexto desatualizado)
- ❌ Regressão semântica (significado de termos muda sem controle)
- ❌ Context Clash (versões incompatíveis se misturam)
- ❌ Decisões inconsistentes entre execuções da IA

**Com Governança**:
- ✅ Versionamento semântico (SemVer)
- ✅ Breaking changes documentados
- ✅ Histórico completo de evolução
- ✅ Validação automática de compatibilidade

---

## 🔄 Como Usar Este Sistema

### Para Desenvolvedores

**Criar nova spec**:
1. Leia [VERSIONING_POLICY.md](VERSIONING_POLICY.md)
2. Use frontmatter YAML obrigatório
3. Adicione blocos `:::version_info` e `:::breaking_changes`
4. Inicie com versão `1.0.0`
5. Registre em [VERSION_HISTORY.md](VERSION_HISTORY.md)

**Atualizar spec existente**:
1. Identifique tipo de mudança (MAJOR/MINOR/PATCH)
2. Atualize `spec_version` e `last_updated`
3. Se MAJOR: atualize `supersedes`
4. Documente em `:::breaking_changes`
5. Registre em [VERSION_HISTORY.md](VERSION_HISTORY.md)
6. Atualize versão nos índices

### Para IA (Claude)

**Antes de usar uma spec**:
```javascript
// Validar versionamento
if (!spec.frontmatter.spec_version) {
  throw new Error("Spec não versionada. Execute /metaspecs:governance:add-versioning");
}

// Checar status
if (spec.frontmatter.status === "deprecated") {
  warn("Usando spec obsoleta. Verifique nova versão.");
}

// Validar compatibilidade
if (spec.frontmatter.spec_version.split('.')[0] !== expectedMajor) {
  throw new Error("Versão incompatível (breaking change)");
}
```

**Princípio Jidoka**:
- 🛑 PARE se encontrar spec sem versionamento
- ⚠️ ALERTE o problema
- 📋 SUGIRA executar comando apropriado

---

## 📊 Tipos de Mudança (SemVer)

### MAJOR (x.0.0) - Breaking Changes

**Quando usar**:
- Mudança de significado de termos-chave
- Remoção de seções obrigatórias
- Alteração incompatível de estrutura
- Mudança de personas principais
- Alteração de precificação que quebra compatibilidade

**Exemplo**:
```yaml
spec_version: "1.5.2" → "2.0.0"
supersedes: "1.5.2"
```

### MINOR (0.x.0) - Adições Compatíveis

**Quando usar**:
- Nova seção adicionada
- Nova persona adicionada (mantendo existentes)
- Novos campos opcionais
- Novos exemplos ou casos de uso
- Expansão de conteúdo compatível

**Exemplo**:
```yaml
spec_version: "1.5.2" → "1.6.0"
```

### PATCH (0.0.x) - Correções

**Quando usar**:
- Correção de typos
- Atualização de links
- Ajustes de formatação
- Clarificações de texto
- Correção de datas

**Exemplo**:
```yaml
spec_version: "1.5.2" → "1.5.3"
```

---

## 🔗 Navegação

**Voltar para**: [Índice Raiz](../index.md)

**Outras Categorias**:
- [Business Specs](../business/index.md) - Contexto empresarial
- [Technical Specs](../technical/index.md) - Arquitetura e decisões técnicas
- [Product Specs](../product/index.md) - Requisitos de produto
- [Meta Specs](../meta/index.md) - Identidade e marca

---

## 📈 Estatísticas

- **Total de Specs Versionadas**: 28
- **Sistema de Governança**: Implementado
- **Política de Versionamento**: Ativa
- **Histórico**: Completo desde 2026-01-13

---

## 🤝 Manutenção

**Responsáveis**: Tech Lead + Product Owner

**Frequência de Atualização**:
- [VERSIONING_POLICY.md](VERSIONING_POLICY.md): Semestral ou após feedback
- [VERSION_HISTORY.md](VERSION_HISTORY.md): Toda vez que uma spec é atualizada

**Processo**:
1. Spec é atualizada → Desenvolvedor registra em VERSION_HISTORY.md
2. Padrão muda → Tech Lead atualiza VERSIONING_POLICY.md
3. Auditoria trimestral → Product Owner valida consistência

---

**Última Atualização**: 2026-01-13
**Versão**: 1.0.0
**Status**: ✅ Ativo
