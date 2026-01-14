---
adr_number: "006"
title: "Conteúdo Estático (Sem CMS)"
date: "2026-01-13"
status: "accepted"
deciders: ["product-owner", "tech-lead"]
consulted: ["founders"]
informed: ["all-developers"]
supersedes: null
superseded_by: null
tags: ["architecture", "content", "cms", "static"]
---

# ADR 006: Conteúdo Estático (Sem CMS)

**Status:** Aceito
**Data:** 2026-01-13
**Decisores:** Product Owner, Tech Lead

---

## Contexto

Decidir como gerenciar conteúdo do site:
- Hard-coded nos componentes Vue
- CMS headless (Contentful, Strapi, Sanity)
- Markdown files
- CMS tradicional (WordPress)

**Contexto do Projeto:**
- 5 páginas estáticas
- Conteúdo não muda frequentemente
- Sem blog (por enquanto)
- Equipe pequena

---

## Decisão

**Conteúdo hard-coded** nos componentes Vue (estático).

**Sem CMS** na fase MVP.

---

## Justificativa

**Por que Estático?**

1. **Simplicidade** - Zero complexidade adicional
2. **Performance** - SSG puro, sem API calls
3. **Versionamento** - Conteúdo no Git (histórico, review)
4. **Custo** - Zero (sem CMS pago)
5. **MVP-First** - Conteúdo estável, mudanças raras

**Quando NÃO usar CMS:**
- ✅ Conteúdo muda < 1x por mês
- ✅ Desenvolvedores editam conteúdo
- ✅ Sem necessidade de editor visual
- ✅ Projeto pequeno

---

## Estrutura de Conteúdo

```vue
<!-- pages/metodologia.vue -->
<template>
  <PageTemplate>
    <HeroSection
      title="Context-First Development"
      description="Metodologia que transforma vibe coding..."
    />

    <Section>
      <h2>Framework CONTEXT</h2>
      <p>Os 7 pilares...</p>
    </Section>
  </PageTemplate>
</template>
```

**Conteúdo vive em:**
- Props de componentes
- Data/constants no `<script setup>`
- Eventualmente: arquivos `.json` ou `.ts` para conteúdo maior

---

## Quando Migrar para CMS?

**Gatilhos para Adicionar CMS:**
- ✅ Blog com > 10 artigos
- ✅ Time de marketing precisa editar sem devs
- ✅ Conteúdo muda semanalmente
- ✅ Múltiplos editores não-técnicos

**Opções Futuras:**
- Nuxt Content (Markdown)
- Contentful / Sanity (Headless CMS)

---

## Alternativas Consideradas

### 1. Nuxt Content (Markdown)
**Contras:** ❌ Overkill para 5 páginas estáticas

### 2. Contentful
**Contras:** ❌ Custo, complexidade, não justifica para MVP

### 3. WordPress Headless
**Contras:** ❌ Muito complexo para caso de uso simples

---

## Consequências

**Positivas:**
- ✅ Setup instantâneo
- ✅ Performance máxima
- ✅ Conteúdo versionado (Git)
- ✅ Zero custos adicionais

**Negativas:**
- ⚠️ Mudanças de conteúdo requerem deploy
  - *Aceitável:* Mudanças são raras
- ⚠️ Não-devs não podem editar
  - *Aceitável:* Equipe técnica gerencia conteúdo

---

**Status:** ✅ ACEITO - Estático para MVP, reavaliar ao adicionar blog
