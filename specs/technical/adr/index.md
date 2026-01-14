---
spec_version: "1.0.0"
valid_from: "2026-01-13"
last_updated: "2026-01-13"
supersedes: null
status: "active"
category: "technical"
tags: ["index", "adr", "architecture", "decisions", "navigation"]
---

# Architecture Decision Records (ADRs)

:::version_info
**Versão**: 1.0.0
**Válida desde**: 2026-01-13
**Status**: Ativa
:::

:::breaking_changes
**v1.0.0** (baseline):
- Primeira versão do índice de ADRs
- Consolida 6 decisões arquiteturais do projeto
:::

---

## 📋 Visão Geral

Este diretório contém os **Architecture Decision Records (ADRs)** do site institucional Thatix. ADRs documentam decisões arquiteturais importantes, contexto, alternativas consideradas e consequências.

**Por que ADRs?**
- 📝 Documenta **por que** decisões foram tomadas (não apenas o quê)
- 🔍 Fornece contexto histórico para novos desenvolvedores
- 🤔 Previne discussões repetitivas sobre decisões já tomadas
- 📊 Permite avaliar decisões no futuro com dados originais

---

## 🏗️ Decisões Arquiteturais

### [ADR-001: Escolha do Stack Tecnológico](adr_001_tech_stack.md) `v1.0.0`

**Decisão**: Vue 3 + Nuxt 4.2.2 + Tailwind CSS + Firebase

**Contexto**: Site institucional de 5 páginas estáticas, formulário de contato, foco em geração de leads.

**Prioridades**:
- ⚡ **Performance**: LCP < 2.5s, SEO otimizado
- 🛠️ **Manutenibilidade**: Código limpo, fácil de manter com time pequeno
- 🚀 **Produtividade**: MVP em 4-5 semanas
- 🧠 **Expertise da Equipe**: Aproveitar conhecimento existente

**Alternativas Consideradas**:
- React + Next.js (rejeitado: menos expertise da equipe)
- WordPress (rejeitado: menos controle, mais complexidade para site simples)
- HTML/CSS/JS puro (rejeitado: menos produtividade, difícil de escalar)

**Consequências**:
- ✅ Time produtivo desde dia 1 (conhece Vue/Nuxt)
- ✅ Performance excelente (SSG)
- ✅ Fácil manutenção
- ⚠️ Depende de conhecimento Vue (onboarding necessário para novos devs)

---

### [ADR-002: Atomic Design como Design System](adr_002_atomic_design.md) `v1.0.0`

**Decisão**: Adotar Atomic Design para organização de componentes

**Contexto**: 5 páginas com múltiplos componentes reutilizáveis. Sem estrutura, código pode ficar desorganizado.

**Estrutura**:
```
components/
├── atoms/       # Botões, inputs, ícones
├── molecules/   # Cards, formulários, navegação
├── organisms/   # Header, footer, seções complexas
├── templates/   # Layouts de página
└── pages/       # Páginas completas
```

**Alternativas Consideradas**:
- Feature-based (rejeitado: menos claro para time pequeno)
- Flat structure (rejeitado: não escala)

**Consequências**:
- ✅ Componentes bem organizados e fáceis de encontrar
- ✅ Reutilização clara (atoms → molecules → organisms)
- ✅ Onboarding simplificado (padrão conhecido)
- ⚠️ Pode parecer over-engineering para projeto pequeno (mas compensa no médio prazo)

---

### [ADR-003: Componentes Custom vs Bibliotecas UI](adr_003_custom_components.md) `v1.0.0`

**Decisão**: Criar componentes custom ao invés de usar bibliotecas prontas (Vuetify, PrimeVue, etc.)

**Contexto**: Site precisa de identidade visual única, não genérica.

**Razões**:
- 🎨 **Controle total de design**: Brand identity específica da Thatix
- ⚡ **Performance**: Sem bundle bloat de bibliotecas grandes
- 🧠 **Aprendizado**: Time melhora skills de componentes
- 🛠️ **Manutenibilidade**: Código simples e direto

**Alternativas Consideradas**:
- Vuetify (rejeitado: design Material genérico, bundle grande)
- PrimeVue (rejeitado: complexidade desnecessária)
- Tailwind UI (considerado para inspiração, mas components custom)

**Consequências**:
- ✅ Design 100% alinhado com brand identity
- ✅ Performance otimizada
- ⚠️ Mais tempo inicial de desenvolvimento (compensado por manutenibilidade)

---

### [ADR-004: Firebase para Backend](adr_004_firebase_backend.md) `v1.0.0`

**Decisão**: Usar Firebase Functions para formulário de contato e possíveis expansões

**Contexto**: Site estático precisa de backend para formulário de contato, analytics, possíveis features futuras.

**Razões**:
- 🚀 **Serverless**: Sem gestão de infra
- 💰 **Custo**: Free tier generoso, escala automática
- ⚡ **Rapidez**: Setup em minutos
- 📈 **Escalabilidade**: Automática conforme uso

**Alternativas Consideradas**:
- API Node.js custom (rejeitado: mais complexo, requer infra)
- Netlify Functions (considerado, mas Firebase tem mais features)
- Email direto (rejeitado: sem tracking, sem validação)

**Consequências**:
- ✅ Backend funcional sem gestão de servidor
- ✅ Fácil adicionar features futuras (auth, database, etc)
- ⚠️ Vendor lock-in Firebase (mitigado por API padrão)

---

### [ADR-005: Hospedagem Vercel Pro](adr_005_vercel_hosting.md) `v1.0.0`

**Decisão**: Hospedar na Vercel Pro

**Contexto**: Nuxt 4 precisa de hosting otimizado, foco em performance e DX.

**Razões**:
- ⚡ **Performance**: Edge network, cache inteligente
- 🚀 **DX**: Deploy automático, preview branches
- 📊 **Analytics**: Web Vitals integrado
- 🔧 **Nuxt-optimized**: Suporte nativo

**Alternativas Consideradas**:
- Netlify (bom, mas Vercel tem melhor integração Nuxt)
- AWS Amplify (mais complexo)
- Hosting tradicional (sem otimizações modernas)

**Consequências**:
- ✅ Performance excelente (LCP < 2.5s garantido)
- ✅ Deploy simples (git push → live)
- ✅ Preview de PRs automático
- 💰 Custo: Vercel Pro (justificado por features)

---

### [ADR-006: Conteúdo Estático (Sem CMS)](adr_006_static_content.md) `v1.0.0`

**Decisão**: Conteúdo hardcoded em componentes Vue (sem CMS na fase inicial)

**Contexto**: Site de 5 páginas com conteúdo que não muda frequentemente.

**Razões**:
- ⚡ **Performance**: SSG puro, sem overhead de CMS
- 🛠️ **Simplicidade**: Menos moving parts
- 🚀 **MVP rápido**: Foco em funcionalidade core
- 💰 **Custo**: Zero custo adicional

**Alternativas Consideradas**:
- Contentful/Sanity (rejeitado: complexidade desnecessária para MVP)
- Markdown files (considerado para futuro blog)
- Git-based CMS (Netlify CMS) (possível futuro)

**Consequências**:
- ✅ MVP mais rápido e simples
- ✅ Performance máxima
- ⚠️ Mudanças de conteúdo requerem deploy (aceitável para fase inicial)
- 📋 Futuro: Adicionar CMS se conteúdo mudar frequentemente

---

## 📊 Matriz de Decisões

| ADR | Área | Impacto | Status | Relacionados |
|-----|------|---------|--------|--------------|
| [001](adr_001_tech_stack.md) | Stack | Alto | ✅ Ativo | Todos |
| [002](adr_002_atomic_design.md) | Arquitetura | Médio | ✅ Ativo | ADR-003 |
| [003](adr_003_custom_components.md) | UI/UX | Médio | ✅ Ativo | ADR-002 |
| [004](adr_004_firebase_backend.md) | Backend | Médio | ✅ Ativo | ADR-001 |
| [005](adr_005_vercel_hosting.md) | Infra | Alto | ✅ Ativo | ADR-001 |
| [006](adr_006_static_content.md) | Conteúdo | Baixo | ✅ Ativo | - |

---

## 🎯 Stack Resultante (Resumo)

```
Frontend:
- Vue 3 (Composition API)
- Nuxt 4.2.2 (SSG/SSR)
- Tailwind CSS (utility-first)
- JavaScript (ES6+, sem TypeScript)

Backend:
- Firebase Functions (formulário)
- Firebase Firestore (storage futuro)

Hosting:
- Vercel Pro (edge network)

Design:
- Atomic Design (organização)
- Componentes custom (brand identity)
- Conteúdo estático (fase MVP)
```

---

## 📝 Como Usar ADRs

### Para Novos Desenvolvedores

**Onboarding técnico**:
1. Leia [ADR-001](adr_001_tech_stack.md) primeiro (entenda o stack)
2. Leia [ADR-002](adr_002_atomic_design.md) (entenda estrutura de componentes)
3. Leia demais ADRs conforme necessário
4. Se tem dúvida sobre "por que fizemos assim?" → Procure o ADR relevante

### Para Propor Nova Decisão

**Template de ADR**:
```markdown
---
adr_number: "007"
title: "[Título da Decisão]"
date: "YYYY-MM-DD"
status: "proposed|accepted|rejected|deprecated"
deciders: ["tech-lead", "founders"]
consulted: ["developers"]
informed: ["all-team"]
supersedes: null
superseded_by: null
tags: ["architecture", "decision"]
spec_version: "1.0.0"
---

# ADR 007: [Título]

## Contexto
[Por que estamos tomando esta decisão?]

## Decisão
[O que decidimos fazer?]

## Alternativas Consideradas
[O que mais avaliamos e por que rejeitamos?]

## Consequências
### Positivas
- [Benefício 1]
- [Benefício 2]

### Negativas
- [Trade-off 1]
- [Trade-off 2]

## Implementação
[Como implementar? Próximos passos?]
```

**Processo**:
1. Criar arquivo `adr_00X_nome.md`
2. Status inicial: `proposed`
3. Discutir com deciders
4. Atualizar para `accepted` ou `rejected`
5. Registrar em [VERSION_HISTORY.md](../../_meta/VERSION_HISTORY.md)
6. Atualizar este índice

### Para Reverter Decisão

**Se decisão não funciona**:
1. Criar novo ADR superseding o antigo
2. Marcar ADR antigo como `deprecated`
3. Atualizar `superseded_by` no ADR antigo
4. Documentar **por que** decisão mudou

**Exemplo**:
```yaml
# adr_001_tech_stack.md
status: "deprecated"
superseded_by: "adr_007_new_stack.md"
```

---

## 🔗 Relação com Outras Specs

### ADRs conectam com:

**Product**:
- [prd_site_thatix.md](../../product/prd_site_thatix.md) - Requisitos que guiaram decisões
- [project_charter.md](../project_charter.md) - Escopo e objetivos do projeto

**Business**:
- [PRODUCT_STRATEGY.md](../../business/PRODUCT_STRATEGY.md) - Visão de longo prazo influencia decisões
- [CUSTOMER_PERSONAS.md](../../business/CUSTOMER_PERSONAS.md) - Público-alvo influencia escolhas

**Meta**:
- [brand_identity_spec.md](../../meta/brand_identity_spec.md) - Brand identity guiou ADR-003

---

## 🔗 Navegação

**Voltar para**: [Technical Index](../index.md)

**Índice Raiz**: [Specs Root](../../index.md)

**Outras Categorias**:
- [Business Specs](../../business/index.md) - Contexto empresarial
- [Product Specs](../../product/index.md) - PRDs
- [Context Governance](../../_meta/index.md) - Versionamento

---

## 🤝 Manutenção

**Responsáveis**: Tech Lead + Desenvolvedores

**Quando criar novo ADR**:
- ✅ Decisão arquitetural significativa
- ✅ Múltiplas alternativas viáveis
- ✅ Impacto de longo prazo
- ✅ Decisão controversa ou não óbvia

**Quando NÃO criar ADR**:
- ❌ Decisão trivial ou óbvia
- ❌ Decisão facilmente reversível
- ❌ Decisão de implementação (não arquitetural)

**Frequência de Revisão**: Anual ou quando arquitetura mudar significativamente

---

## 📚 Recursos Adicionais

### Sobre ADRs
- [ADR GitHub](https://adr.github.io/)
- [Michael Nygard's ADR Template](https://github.com/joelparkerhenderson/architecture-decision-record)

### Versionamento
- [VERSIONING_POLICY.md](../../_meta/VERSIONING_POLICY.md) - Como versionar ADRs
- [VERSION_HISTORY.md](../../_meta/VERSION_HISTORY.md) - Histórico de mudanças

---

**Última Atualização**: 2026-01-13
**Versão**: 1.0.0
**Status**: ✅ Ativo
**Total de ADRs**: 6 (todos aceitos e ativos)
