---
spec_version: "1.0.0"
valid_from: "2026-01-13"
last_updated: "2026-01-13"
supersedes: null
status: "active"
category: "technical"
tags: ["index", "overview", "technical-context", "architecture"]
---

# Contexto Técnico - Site Institucional Thatix

**Versão:** 1.0
**Data:** 2026-01-13
**Última Atualização:** 2026-01-13

---

## Perfil de Contexto do Projeto

### Informações Básicas

**Nome do Projeto:** Site Institucional Thatix
**Repositório MetaSpecs:** thatix-site-metaspecs
**Repositório Código:** [A ser criado]
**Domínio:** thatix.io
**Hospedagem:** Vercel Pro

**Descrição:**
Site institucional da Thatix, consultoria especializada em Context-First Development. O site serve como principal canal de comunicação e marketing, apresentando metodologia, serviços e expertise em desenvolvimento de software com IA.

---

### Stack Tecnológica

**Frontend:**
- Vue 3 (Composition API)
- Nuxt 4 (SSG/SSR)
- Tailwind CSS (utility-first styling)
- JavaScript (ES6+, sem TypeScript)

**Backend/Serviços:**
- Firebase (formulário de contato, cloud functions)
- Google Analytics 4 (tracking e analytics)

**Hospedagem e Deploy:**
- Vercel Pro
- Deploy automático via GitHub integration
- Custom domain: thatix.io

**Qualidade de Código:**
- ESLint (Vue + Nuxt recommended config)
- Prettier (code formatting)

---

### Estrutura da Equipe

**Desenvolvimento:**
- 2 Desenvolvedores (conhecimento em Vue/Nuxt)
- 1 Product Owner
- 1 QA

**Capacidade:** 4 projetos simultâneos (incluindo este site)

---

### Restrições e Princípios de Desenvolvimento

**Restrições Técnicas:**
- ✅ Conteúdo estático (sem CMS dinâmico)
- ✅ 5 páginas principais (Home, Metodologia, Serviços, Clientes, Contato)
- ✅ Máxima customização (componentes do zero)
- ✅ Performance: LCP < 2.5s
- ✅ SEO otimizado (sitemap, meta tags, Open Graph)
- ✅ Responsivo (mobile-first)

**Fora do Escopo Inicial:**
- ❌ TypeScript
- ❌ Testes automatizados (fase inicial)
- ❌ CMS headless
- ❌ Blog dinâmico
- ❌ Internacionalização (i18n)
- ❌ Dark mode
- ❌ Funcionalidades avançadas (chat, calculadora ROI)

**Princípios Arquiteturais:**
1. **Atomic Design** - Componentes organizados em atoms, molecules, organisms, templates, pages
2. **Context-First** - Desenvolvimento guiado por especificações claras
3. **Performance-First** - Otimização de performance desde o início
4. **SEO-First** - Estrutura otimizada para mecanismos de busca
5. **Simplicidade** - Evitar over-engineering, código limpo e direto

---

## Camada 1: Contexto Central do Projeto

### Documentação Estratégica

- **[Project Charter](project_charter.md)**
  Visão, objetivos, escopo, stakeholders e critérios de sucesso

### Architecture Decision Records (ADRs)

- **[ADR-001: Escolha do Stack Tecnológico](adr/adr_001_tech_stack.md)** `v1.0.0`
  Por que Vue 3 + Nuxt 4 + Tailwind CSS

- **[ADR-002: Atomic Design como Design System](adr/adr_002_atomic_design.md)** `v1.0.0`
  Organização de componentes e estrutura de arquivos

- **[ADR-003: Componentes Custom vs Bibliotecas](adr/adr_003_custom_components.md)** `v1.0.0`
  Decisão de criar componentes do zero ao invés de usar libs prontas

- **[ADR-004: Firebase para Backend](adr/adr_004_firebase_backend.md)** `v1.0.0`
  Firebase Functions para formulário de contato e possíveis expansões

- **[ADR-005: Hospedagem Vercel Pro](adr/adr_005_vercel_hosting.md)** `v1.0.0`
  Vercel como plataforma de hospedagem e deploy

- **[ADR-006: Conteúdo Estático](adr/adr_006_static_content.md)** `v1.0.0`
  Decisão de não usar CMS na fase inicial

---

## Camada 2: Arquivos de Contexto Otimizados para IA

### Guias de Desenvolvimento

- **[CLAUDE.meta.md](CLAUDE.meta.md)**
  Guia completo de desenvolvimento com IA: padrões de código, convenções, estrutura de componentes Atomic Design, integração Firebase, e workflows

- **[CODEBASE_GUIDE.md](CODEBASE_GUIDE.md)**
  Navegação da base de código: estrutura de diretórios, arquivos-chave, fluxo de dados, pontos de integração

---

## Camada 3: Contexto Específico do Domínio

### Lógica de Negócio e Especificações

- **[ATOMIC_DESIGN_GUIDE.md](ATOMIC_DESIGN_GUIDE.md)**
  Guia detalhado de implementação do Atomic Design no projeto: categorização de componentes, exemplos práticos, convenções de nomenclatura

- **[FIREBASE_INTEGRATION.md](FIREBASE_INTEGRATION.md)**
  Integração Firebase: setup, cloud functions, formulário de contato, segurança e variáveis de ambiente

- **[SEO_OPTIMIZATION.md](SEO_OPTIMIZATION.md)**
  Estratégias e implementação de SEO: meta tags, sitemap, Open Graph, performance

---

## Camada 4: Contexto do Fluxo de Desenvolvimento

### Processos e Workflows

- **[CONTRIBUTING.md](CONTRIBUTING.md)**
  Guia de contribuição: setup do projeto, workflow de desenvolvimento, padrões de commit, processo de review

- **[TROUBLESHOOTING.md](TROUBLESHOOTING.md)**
  Guia de resolução de problemas: erros comuns, debug, performance issues, problemas de deploy

- **[ARCHITECTURE_CHALLENGES.md](ARCHITECTURE_CHALLENGES.md)**
  Desafios arquiteturais conhecidos e melhorias futuras planejadas

---

## Navegação Rápida por Necessidade

### 🚀 Para Começar a Desenvolver
1. Leia [CONTRIBUTING.md](CONTRIBUTING.md) - Setup e workflow
2. Entenda [CODEBASE_GUIDE.md](CODEBASE_GUIDE.md) - Estrutura do projeto
3. Consulte [CLAUDE.meta.md](CLAUDE.meta.md) - Padrões e convenções

### 🎨 Para Criar Componentes
1. Leia [ATOMIC_DESIGN_GUIDE.md](ATOMIC_DESIGN_GUIDE.md) - Como organizar componentes
2. Veja [ADR-002](adr/adr_002_atomic_design.md) - Decisão e contexto
3. Consulte [CLAUDE.meta.md](CLAUDE.meta.md) - Padrões de código Vue

### 🔥 Para Integrar Firebase
1. Leia [FIREBASE_INTEGRATION.md](FIREBASE_INTEGRATION.md) - Setup completo
2. Veja [ADR-004](adr/adr_004_firebase_backend.md) - Contexto da decisão

### 🔍 Para Otimizar SEO
1. Leia [SEO_OPTIMIZATION.md](SEO_OPTIMIZATION.md) - Estratégias completas
2. Consulte PRD ([specs/product/prd_site_thatix.md](../product/prd_site_thatix.md)) - Requisitos

### 🐛 Para Resolver Problemas
1. Consulte [TROUBLESHOOTING.md](TROUBLESHOOTING.md) - Problemas comuns
2. Veja logs do Vercel e Firebase

### 🏗️ Para Entender Decisões Arquiteturais
1. Leia todos os ADRs em [adr/](adr/)
2. Consulte [Project Charter](project_charter.md)
3. Revise [ARCHITECTURE_CHALLENGES.md](ARCHITECTURE_CHALLENGES.md)

---

## Status de Documentação

| Documento | Status | Última Atualização |
|-----------|--------|-------------------|
| index.md | ✅ Completo | 2026-01-13 |
| project_charter.md | ✅ Completo | 2026-01-13 |
| ADR-001 a ADR-006 | ✅ Completo | 2026-01-13 |
| CLAUDE.meta.md | ✅ Completo | 2026-01-13 |
| CODEBASE_GUIDE.md | ✅ Completo | 2026-01-13 |
| ATOMIC_DESIGN_GUIDE.md | ✅ Completo | 2026-01-13 |
| FIREBASE_INTEGRATION.md | ✅ Completo | 2026-01-13 |
| SEO_OPTIMIZATION.md | ✅ Completo | 2026-01-13 |
| CONTRIBUTING.md | ✅ Completo | 2026-01-13 |
| TROUBLESHOOTING.md | ✅ Completo | 2026-01-13 |
| ARCHITECTURE_CHALLENGES.md | ✅ Completo | 2026-01-13 |

---

## Manutenção desta Documentação

**Responsáveis:** Product Owner + Desenvolvedores
**Frequência de Revisão:** A cada milestone ou mudança arquitetural significativa
**Versionamento:** Seguir Semantic Versioning para documentação

**Quando Atualizar:**
- Nova decisão arquitetural → Criar novo ADR
- Mudança de processo → Atualizar CONTRIBUTING.md
- Novo padrão de código → Atualizar CLAUDE.meta.md
- Problema recorrente → Documentar em TROUBLESHOOTING.md

---

**Este documento é a porta de entrada para todo o contexto técnico do projeto. Comece aqui e navegue conforme necessidade.**
