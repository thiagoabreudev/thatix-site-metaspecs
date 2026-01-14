---
spec_version: "1.0.0"
valid_from: "2026-01-13"
last_updated: "2026-01-13"
status: "active"
priority: "high"
category: "feature"
tags: ["framework", "methodology", "context-first", "core-methodology"]
related_specs:
  - "framework-wsci.md"
  - "../PRODUCT_STRATEGY.md"
---

# Feature: Framework CONTEXT

**Versão:** 1.0
**Data:** 2026-01-13
**Tipo:** Core Methodology

---

## 1. Descrição

O **Framework CONTEXT** é a metodologia proprietária da Thatix para desenvolvimento estruturado com IA, baseada em 7 pilares que garantem previsibilidade, qualidade e escalabilidade.

### Acrônimo CONTEXT

- **C**ontext Architecture
- **O**bservability-Driven
- **N**ormative Specifications
- **T**est-First AI Development
- **E**volutionary Refinement
- **X**plainability & Governance
- (+ **T**rustworthy Deployment)

---

## 2. Os 7 Pilares

### Pilar 1: Context Architecture

**Propósito:** Design estratégico da informação entregue à IA

**Conceitos-Chave:**
- Arquitetura de contextos como artefato de primeira classe
- Hierarquia e organização de informação
- Context boundaries (isolamento)
- Versionamento de contextos

**Benefício:** IA recebe informação estruturada, não caótica

---

### Pilar 2: Observability-Driven

**Propósito:** Instrumentação e rastreamento contínuo de contextos

**Conceitos-Chave:**
- Logging de interações com IA
- Métricas de qualidade de contexto
- Identificação de context poisoning
- Feedback loops automáticos

**Benefício:** Visibilidade do que IA está "vendo" e gerando

---

### Pilar 3: Normative Specifications

**Propósito:** Especificações executáveis com anti-patterns explícitos

**Conceitos-Chave:**
- Specs que dizem o que fazer E o que NÃO fazer
- Guard rails e constraints
- Padrões e anti-padrões documentados
- Verificação automatizada

**Benefício:** IA gera código consistente com padrões do projeto

---

### Pilar 4: Test-First AI Development

**Propósito:** Desenvolvimento orientado por testes adaptado para IA

**Conceitos-Chave:**
- TDD + Context-First
- Testes como especificação de comportamento
- Validação automática de código gerado
- Coverage de testes como métrica de qualidade

**Benefício:** Código gerado é testável e testado desde o início

---

### Pilar 5: Evolutionary Refinement

**Propósito:** Evolução contínua de especificações

**Conceitos-Chave:**
- Specs são documentos vivos
- Feedback de implementação → Refinamento de specs
- Versionamento de MetaSpecs
- Aprendizado contínuo do sistema

**Benefício:** Metodologia melhora com uso (não é estática)

---

### Pilar 6: eXplainability & Governance

**Propósito:** Explicabilidade e controle sobre decisões da IA

**Conceitos-Chave:**
- Rastreabilidade de decisões
- Auditoria de código gerado
- Compliance e governança
- Explicação de "por que" código foi gerado assim

**Benefício:** Confiança em ambientes regulados (fintech, health)

---

### Pilar 7: Trustworthy Deployment

**Propósito:** Implementação confiável em produção

**Conceitos-Chave:**
- Validação pré-deploy automática
- Retrocompatibilidade verificada
- Rollback strategies
- Monitoring pós-deploy

**Benefício:** Deploy com IA é tão seguro quanto sem IA

---

## 3. Aplicação Prática

### Workflow Context-First

```
1. Specify (Normative Specifications)
   ↓
2. Design (Context Architecture)
   ↓
3. Implement (Test-First AI Development)
   ↓
4. Observe (Observability-Driven)
   ↓
5. Refine (Evolutionary Refinement)
   ↓
6. Audit (Explainability & Governance)
   ↓
7. Deploy (Trustworthy Deployment)
   ↓
[Loop back to 1 with learnings]
```

---

## 4. Diferencial Competitivo

**vs Uso Ad-hoc de IA:**
- Estruturado vs caótico
- Previsível vs imprevisível
- Escalável vs não-escalável

**vs Outras Metodologias:**
- Específico para IA (não adaptação forçada de Agile)
- Baseado em Context Engineering (não apenas processo)
- Comprovado (73% ganho de produtividade)

---

## 5. Métricas de Sucesso

**Adoção Correta do Framework:**
- Time usa os 7 pilares consistentemente
- Specs são normativas (não apenas descritivas)
- Observability implementada
- Código gerado passa por governança

**Resultados:**
- Ganho de produtividade > 50%
- Débito técnico reduzido > 40%
- Bugs em produção reduzidos > 30%

---

**Última Atualização:** 2026-01-13
