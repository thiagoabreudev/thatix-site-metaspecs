---
adr_number: "003"
title: "Componentes Custom vs Bibliotecas UI"
date: "2026-01-13"
status: "accepted"
deciders: ["founders", "tech-lead"]
consulted: []
informed: ["all-developers"]
supersedes: null
superseded_by: null
tags: ["architecture", "components", "ui-library", "custom"]
related_adrs:
  - "adr_002_atomic_design.md"
---

# ADR 003: Componentes Custom vs Bibliotecas UI

**Status:** Aceito
**Data:** 2026-01-13
**Decisores:** Founders, Tech Lead
**Relacionado:** [ADR-002](adr_002_atomic_design.md)

---

## Contexto

Para construir a interface do site institucional, precisamos decidir entre:
1. Criar componentes do zero (custom)
2. Usar biblioteca de componentes pronta (PrimeVue, Naive UI, Headless UI)
3. Abordagem híbrida

**Fatores:**
- Controle visual total (brand identity única)
- Performance (bundle size)
- Velocidade de desenvolvimento
- Manutenibilidade

---

## Decisão

**Criar todos os componentes do zero** usando Atomic Design + Tailwind CSS.

**Sem bibliotecas de componentes** (nem headless, nem styled).

---

## Justificativa

### Por que Custom?

**1. Controle Visual Máximo**
- ✅ Design 100% alinhado com brand identity Thatix
- ✅ Sem limitações de customização
- ✅ Cada pixel controlado

**2. Performance**
- ✅ Bundle size mínimo (apenas código que usamos)
- ✅ Sem overhead de biblioteca
- ✅ Tree-shaking perfeito

**3. Learning & Ownership**
- ✅ Equipe aprende profundamente
- ✅ Sem dependência de biblioteca externa
- ✅ Total controle sobre bugs e updates

**4. Simplicidade**
- ✅ Projeto pequeno (5 páginas) não justifica lib complexa
- ✅ Componentes diretos, sem abstrações desnecessárias

**5. Alinhamento com Context-First**
- ✅ Máxima especificação e controle
- ✅ Sem "magic" de bibliotecas
- ✅ Código limpo e previsível

---

## Alternativas Consideradas

### Opção A: Headless UI (Tailwind Labs)

**Prós:**
- Componentes acessíveis (a11y)
- Unstyled (total controle visual)
- Mantido por criadores do Tailwind

**Contras:**
- ❌ Overhead desnecessário para componentes simples
- ❌ Mais uma dependência
- ❌ Learning curve (API específica)

**Decisão:** Rejeitado - simplicidade > acessibilidade avançada (por enquanto)

---

### Opção B: PrimeVue / Naive UI

**Prós:**
- Componentes prontos
- Desenvolvimento muito rápido

**Contras:**
- ❌ Customização limitada (theming complexo)
- ❌ Bundle size grande
- ❌ Design genérico (não reflete brand Thatix)
- ❌ Vendor lock-in

**Decisão:** Rejeitado - controle visual é prioridade

---

### Opção C: Radix Vue / Ark UI

**Prós:**
- Componentes headless modernos
- Acessibilidade excelente
- Composable

**Contras:**
- ❌ Ainda em desenvolvimento (menos maduro que Headless UI)
- ❌ Overkill para projeto pequeno

**Decisão:** Rejeitado

---

### Opção D: Híbrido (Lib para alguns + Custom para outros)

**Prós:**
- "Best of both worlds"

**Contras:**
- ❌ Inconsistência de código
- ❌ Dois padrões diferentes
- ❌ Confusão para equipe

**Decisão:** Rejeitado - consistência é chave

---

## Componentes a Criar

### Atoms (10-12 componentes)
- Button
- Input
- Label
- Icon (SVG wrapper)
- Text (Typography)
- Link
- Image
- Spinner (loading)
- Badge
- Divider

### Molecules (6-8 componentes)
- FormField (Label + Input + Error)
- Card
- NavItem
- SocialLink
- FeatureCard
- TestimonialCard

### Organisms (8-10 componentes)
- Navbar
- Footer
- ContactForm
- HeroSection
- FeatureGrid
- TestimonialSlider
- ClientLogos
- ServiceCard
- MethodologyDiagram

**Total:** ~25-30 componentes

**Estimativa de Desenvolvimento:** 1.5-2 sprints para componentes base

---

## Padrões de Implementação

### Usando Tailwind Utilities

```vue
<!-- Atom: Button.vue -->
<template>
  <button
    class="px-4 py-2 rounded font-semibold transition-colors"
    :class="variantClasses"
  >
    <slot />
  </button>
</template>

<script setup>
const props = defineProps({
  variant: { type: String, default: 'primary' }
})

const variantClasses = computed(() => ({
  'bg-blue-600 text-white hover:bg-blue-700': props.variant === 'primary',
  'bg-gray-200 text-gray-800 hover:bg-gray-300': props.variant === 'secondary'
}))
</script>
```

### Composables para Lógica Compartilhada

```javascript
// composables/useFormValidation.js
export function useFormValidation() {
  const errors = ref({})

  const validate = (field, value, rules) => {
    // Validação logic
  }

  return { errors, validate }
}
```

---

## Consequências

### Positivas

- ✅ **Controle total** - Design e performance
- ✅ **Bundle size mínimo** - ~30-40% menor que com lib
- ✅ **Sem vendor lock-in** - Fácil migrar ou refatorar
- ✅ **Learning profundo** - Equipe domina componentes
- ✅ **Código limpo** - Sem abstrações desnecessárias

### Negativas (Trade-offs Aceitos)

- ⚠️ **Tempo de desenvolvimento inicial maior** - Criar componentes do zero
  - *Mitigação:* Atomic Design acelera depois dos atoms/molecules prontos

- ⚠️ **Acessibilidade manual** - Precisa implementar a11y manualmente
  - *Mitigação:* Checklist de a11y, ESLint plugin, testes manuais

- ⚠️ **Manutenção total nossa** - Bugs são responsabilidade da equipe
  - *Mitigação:* Código simples e bem documentado

---

## Validação

**Após 1 Sprint:**
- ✅ 50% dos atoms criados e funcionais
- ✅ Nenhum blocker por falta de lib
- ✅ Equipe confortável criando componentes

**Após 2 Sprints:**
- ✅ 80%+ dos componentes necessários prontos
- ✅ Performance: bundle JS < 100KB (gzipped)
- ✅ Zero necessidade de adicionar biblioteca

**Critérios de Falha (Gatilhos para Revisão):**
- ❌ Desenvolvimento de componentes toma > 3 sprints
- ❌ Bugs recorrentes em componentes custom
- ❌ Equipe sobrecarregada com manutenção

---

## Referências

- [Tailwind CSS Components](https://tailwindui.com/components) - Inspiração
- [ATOMIC_DESIGN_GUIDE.md](../ATOMIC_DESIGN_GUIDE.md) - Como criar componentes
- [CLAUDE.meta.md](../CLAUDE.meta.md) - Padrões de código

---

**Status:** ✅ ACEITO - Componentes custom, zero bibliotecas UI
