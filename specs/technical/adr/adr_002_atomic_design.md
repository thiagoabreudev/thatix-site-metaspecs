---
adr_number: "002"
title: "Atomic Design como Design System"
date: "2026-01-13"
status: "accepted"
deciders: ["tech-lead", "founders"]
consulted: []
informed: ["all-developers"]
supersedes: null
superseded_by: null
tags: ["architecture", "design-system", "atomic-design", "components"]
related_adrs:
  - "adr_003_custom_components.md"
spec_version: "1.0.0"
---

# ADR 002: Atomic Design como Design System

:::version_info
**Versão**: 1.0.0
**Data da Decisão**: 2026-01-13
**Status**: Aceito
:::

:::breaking_changes
**v1.0.0** (baseline):
- Primeira versão desta decisão arquitetural
- Adoção de Atomic Design: Atoms, Molecules, Organisms, Templates, Pages
- Estrutura de diretórios definida em components/
- Relacionado com ADR-003 (Componentes Custom)
:::

**Status:** Aceito
**Data:** 2026-01-13
**Decisores:** Tech Lead, Founders
**Relacionado:** [ADR-003](adr_003_custom_components.md)

---

## Contexto

Precisamos de uma estratégia clara para organizar e estruturar componentes Vue do site institucional. Com 5 páginas e múltiplos componentes reutilizáveis, sem uma estrutura definida o código pode rapidamente se tornar desorganizado e difícil de manter.

**Requisitos:**
- Componentes reutilizáveis e escaláveis
- Estrutura clara para equipe pequena
- Fácil onboarding de novos desenvolvedores
- Manutenção simplificada

---

## Decisão

Adotamos **Atomic Design** de Brad Frost como metodologia de organização de componentes.

### Estrutura de Diretórios

```
/components
  /atoms          # Elementos indivisíveis (Button, Input, Icon, Text)
  /molecules      # Combinações de atoms (FormField, Card, NavItem)
  /organisms      # Seções complexas (Navbar, ContactForm, HeroSection)
  /templates      # Layouts de página (PageTemplate, SectionTemplate)
/pages            # Pages compostas de templates e organisms
```

### Hierarquia

```
Pages (Home, Metodologia, etc.)
  ↓
Templates (PageTemplate, SectionTemplate)
  ↓
Organisms (Navbar, Footer, HeroSection)
  ↓
Molecules (Card, FormField, NavItem)
  ↓
Atoms (Button, Input, Icon, Text)
```

---

## Justificativa

### Por que Atomic Design?

**1. Hierarquia Clara**
- Estrutura intuitiva do mais simples (atoms) ao mais complexo (pages)
- Fácil entender onde criar/encontrar componentes

**2. Reutilização Máxima**
- Atoms são usados em molecules
- Molecules são usados em organisms
- DRY (Don't Repeat Yourself) por design

**3. Escalabilidade**
- Adicionar novos componentes sem quebrar estrutura
- Fácil refatorar (mudança em atom afeta todos que usam)

**4. Manutenibilidade**
- Componentes pequenos = mais fácil de testar e manter
- Separação de responsabilidades clara

**5. Onboarding Rápido**
- Novos devs entendem estrutura rapidamente
- Padrão conhecido da indústria

**6. Alinhamento com Context-First**
- Metodologia estruturada (não ad-hoc)
- Documentação clara de organização
- Previsibilidade e escalabilidade

---

## Categorização de Componentes

### Atoms (Primitivos)

**Definição:** Elementos indivisíveis, não podem ser quebrados em partes menores.

**Exemplos:**
- `Button.vue` - Botão genérico
- `Input.vue` - Input de formulário
- `Label.vue` - Label de texto
- `Icon.vue` - Ícones (wrapper para SVG)
- `Text.vue` - Textos tipográficos
- `Link.vue` - Links/âncoras
- `Image.vue` - Imagens otimizadas

**Características:**
- Props para customização (variant, size, color)
- Sem lógica de negócio
- Máxima reutilização

---

### Molecules (Composições Simples)

**Definição:** Combinações de atoms que formam unidades funcionais simples.

**Exemplos:**
- `FormField.vue` - Label + Input + Error message
- `Card.vue` - Container com título e conteúdo
- `NavItem.vue` - Link + Icon (para menu)
- `SocialLink.vue` - Icon + Link (redes sociais)
- `FeatureCard.vue` - Icon + Title + Description

**Características:**
- Compostos de 2-5 atoms
- Lógica simples de apresentação
- Ainda genéricos e reutilizáveis

---

### Organisms (Seções Complexas)

**Definição:** Componentes complexos que formam seções distintas da interface.

**Exemplos:**
- `Navbar.vue` - Logo + NavItems + MobileMenu + CTA
- `Footer.vue` - Links + SocialLinks + Copyright
- `ContactForm.vue` - FormFields + Button + Validation
- `HeroSection.vue` - Heading + Text + Image + CTA
- `TestimonialSlider.vue` - Cards + Navigation
- `FeatureGrid.vue` - Múltiplos FeatureCards em grid

**Características:**
- Compostos de molecules e/ou atoms
- Lógica de negócio (ex: form validation)
- Específicos de contexto mas ainda reutilizáveis

---

### Templates (Layouts)

**Definição:** Estruturas de página que definem layout e posicionamento de organisms.

**Exemplos:**
- `PageTemplate.vue` - Navbar + Slot para conteúdo + Footer
- `SectionTemplate.vue` - Container com spacing e background

**Características:**
- Define estrutura, não conteúdo
- Usa slots para flexibilidade
- Responsável por layout responsivo

---

### Pages (Rotas)

**Definição:** Páginas completas no diretório `/pages` (Nuxt file-based routing).

**Exemplos:**
- `index.vue` - Home
- `metodologia.vue` - Metodologia
- `servicos.vue` - Serviços
- `clientes.vue` - Clientes
- `contato.vue` - Contato

**Características:**
- Compostas de templates + organisms
- Conteúdo específico da página
- Integração com Nuxt (useHead, useFetch, etc.)

---

## Convenções de Nomenclatura

### Arquivos

```
PascalCase.vue - Para componentes
ex: Button.vue, FormField.vue, HeroSection.vue
```

### Props

```javascript
camelCase - Para props
ex: variant, buttonSize, isDisabled
```

### Classes CSS (Tailwind)

```html
<!-- Prefixo por tipo de componente -->
<button class="btn-primary">     <!-- Atom -->
<div class="card-default">        <!-- Molecule -->
<nav class="navbar-main">         <!-- Organism -->
```

---

## Exemplo Prático

### Atom: Button.vue

```vue
<template>
  <button
    :class="buttonClasses"
    :disabled="disabled"
    @click="$emit('click')"
  >
    <slot />
  </button>
</template>

<script setup>
const props = defineProps({
  variant: {
    type: String,
    default: 'primary', // primary, secondary, outline
    validator: (value) => ['primary', 'secondary', 'outline'].includes(value)
  },
  size: {
    type: String,
    default: 'md', // sm, md, lg
    validator: (value) => ['sm', 'md', 'lg'].includes(value)
  },
  disabled: Boolean
})

const buttonClasses = computed(() => {
  const base = 'font-semibold rounded transition-colors'

  const variants = {
    primary: 'bg-blue-600 text-white hover:bg-blue-700',
    secondary: 'bg-gray-600 text-white hover:bg-gray-700',
    outline: 'border-2 border-blue-600 text-blue-600 hover:bg-blue-50'
  }

  const sizes = {
    sm: 'px-3 py-1.5 text-sm',
    md: 'px-4 py-2 text-base',
    lg: 'px-6 py-3 text-lg'
  }

  return `${base} ${variants[props.variant]} ${sizes[props.size]}`
})
</script>
```

### Molecule: FormField.vue

```vue
<template>
  <div class="form-field">
    <Label :for="inputId">{{ label }}</Label>
    <Input
      :id="inputId"
      :type="type"
      :modelValue="modelValue"
      @update:modelValue="$emit('update:modelValue', $event)"
      :error="!!error"
    />
    <span v-if="error" class="text-red-500 text-sm mt-1">
      {{ error }}
    </span>
  </div>
</template>

<script setup>
import Label from '@/components/atoms/Label.vue'
import Input from '@/components/atoms/Input.vue'

defineProps({
  label: String,
  inputId: String,
  type: { type: String, default: 'text' },
  modelValue: String,
  error: String
})

defineEmits(['update:modelValue'])
</script>
```

### Organism: ContactForm.vue

```vue
<template>
  <form @submit.prevent="handleSubmit" class="contact-form">
    <FormField
      v-model="form.name"
      label="Nome"
      inputId="name"
      :error="errors.name"
    />
    <FormField
      v-model="form.email"
      label="Email"
      inputId="email"
      type="email"
      :error="errors.email"
    />
    <Button type="submit" :disabled="isSubmitting">
      {{ isSubmitting ? 'Enviando...' : 'Enviar' }}
    </Button>
  </form>
</template>

<script setup>
import FormField from '@/components/molecules/FormField.vue'
import Button from '@/components/atoms/Button.vue'

// Lógica de form, validação, Firebase...
</script>
```

---

## Alternativas Consideradas

### 1. Component Folders (Flat Structure)

```
/components
  Button.vue
  Input.vue
  ContactForm.vue
  Navbar.vue
  ...
```

**Contras:**
- ❌ Sem organização hierárquica
- ❌ Difícil encontrar componentes em projeto grande
- ❌ Não escala bem

---

### 2. Feature-Based Structure

```
/features
  /contact
    ContactForm.vue
    ContactButton.vue
  /navigation
    Navbar.vue
    NavItem.vue
```

**Contras:**
- ❌ Dificulta reutilização entre features
- ❌ Duplicação de componentes genéricos
- ❌ Não adequado para site institucional (poucas features)

---

### 3. Biblioteca de Componentes Pronta (PrimeVue, Naive UI)

**Contras:**
- ❌ Menos controle visual (customização limitada)
- ❌ Bundle size maior
- ❌ Decisão já tomada em [ADR-003](adr_003_custom_components.md): componentes custom

---

## Consequências

### Positivas

- ✅ **Código organizado** - Estrutura clara e previsível
- ✅ **Reutilização máxima** - DRY enforcement
- ✅ **Onboarding rápido** - Devs entendem hierarquia facilmente
- ✅ **Escalável** - Adicionar componentes sem bagunça
- ✅ **Manutenível** - Componentes pequenos e focados
- ✅ **Testável** - Atoms e molecules fáceis de testar isoladamente

### Negativas (Trade-offs)

- ⚠️ **Overhead inicial** - Precisa pensar onde categorizar componente
- ⚠️ **Possível over-engineering** - Para projeto pequeno, pode parecer excessivo
- ⚠️ **Decisões subjetivas** - Nem sempre claro se é molecule ou organism

**Mitigação:** Documentação clara com exemplos (ver [ATOMIC_DESIGN_GUIDE.md](../ATOMIC_DESIGN_GUIDE.md))

---

## Critérios de Sucesso

**Após 2 Sprints:**
- ✅ 15+ componentes criados seguindo Atomic Design
- ✅ Zero discussões sobre "onde colocar este componente"
- ✅ Reutilização: pelo menos 3 molecules/organisms usados em múltiplas páginas

**Após MVP:**
- ✅ Estrutura mantida consistentemente
- ✅ Equipe satisfeita com organização (retrospectiva positiva)
- ✅ Novo dev consegue contribuir em < 2 dias

---

## Referências

- [Atomic Design by Brad Frost](https://atomicdesign.bradfrost.com/chapter-2/)
- [ATOMIC_DESIGN_GUIDE.md](../ATOMIC_DESIGN_GUIDE.md) - Guia específico do projeto

---

**Status:** ✅ ACEITO - Estrutura de componentes definida
