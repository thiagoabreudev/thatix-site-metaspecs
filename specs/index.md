---
spec_version: "1.0.0"
valid_from: "2026-01-13"
last_updated: "2026-01-13"
supersedes: null
status: "active"
category: "meta"
tags: ["index", "navigation", "overview", "root"]
---

# MetaSpecs - Site Institucional Thatix

:::version_info
**Versão**: 1.0.0
**Válida desde**: 2026-01-13
**Status**: Ativa
:::

:::breaking_changes
**v1.0.0** (baseline):
- Primeira versão do índice raiz de MetaSpecs
- Consolida 28 especificações em 4 categorias principais
- Implementa Context Governance com versionamento SemVer
- Estabelece arquitetura de contexto completa para o projeto
:::

---

## 📋 Visão Geral

Este repositório contém a **arquitetura completa de contexto** do site institucional da Thatix, seguindo a metodologia **Context-First Development**. Todas as especificações são versionadas, rastreáveis e estruturadas para consumo tanto humano quanto por IA.

### Estatísticas do Projeto

- **Total de Especificações**: 28 arquivos
- **Specs de Negócio**: 11 principais + 4 features
- **Specs Técnicas**: 3 principais + 6 ADRs
- **Specs de Produto**: 1 PRD
- **Meta-Specs**: 3 (governança + identidade)
- **Versão Base**: v1.0.0 (todas as specs)
- **Última Atualização**: 2026-01-13

---

## 🗺️ Navegação Rápida

### Para Entender o Negócio
👉 [Contexto Empresarial](business/index.md) - Visão completa de negócio, clientes e produto

### Para Desenvolvimento
👉 [Contexto Técnico](technical/index.md) - Arquitetura, decisões e stack tecnológico

### Para Governança
👉 [Política de Versionamento](_meta/VERSIONING_POLICY.md) - Como versionar e atualizar specs
👉 [Histórico de Versões](_meta/VERSION_HISTORY.md) - Tracking de todas as mudanças

### Para Identidade Visual
👉 [Brand Identity](meta/brand_identity_spec.md) - Paleta, tipografia e diretrizes de marca

---

## 📁 Arquitetura de Contexto

### 🎯 Meta (Governança e Identidade)

**Governança de Contexto**:
- [VERSIONING_POLICY.md](_meta/VERSIONING_POLICY.md) `v1.0.0` - Política de versionamento SemVer
- [VERSION_HISTORY.md](_meta/VERSION_HISTORY.md) `v1.0.0` - Histórico de todas as versões

**Identidade**:
- [brand_identity_spec.md](meta/brand_identity_spec.md) `v1.0.0` - Paleta, tipografia e logo

---

### 💼 Business (Estratégia e Contexto de Negócio)

**Índice**: [business/index.md](business/index.md) `v1.0.0`

#### Camada 1: Contexto do Cliente
- [CUSTOMER_PERSONAS.md](business/CUSTOMER_PERSONAS.md) `v1.0.0` - 4 personas: CTO/VP, Tech Lead, Founder, Dev Senior
- [CUSTOMER_JOURNEY.md](business/CUSTOMER_JOURNEY.md) `v1.0.0` - 6 fases: Awareness → Advocacy/Churn
- [VOICE_OF_CUSTOMER.md](business/VOICE_OF_CUSTOMER.md) `v1.0.0` - Feedback, linguagem e padrões

#### Camada 2: Contexto do Produto
- [PRODUCT_STRATEGY.md](business/PRODUCT_STRATEGY.md) `v1.0.0` - Visão, missão, roadmap 2026-2028
- [PRODUCT_METRICS.md](business/PRODUCT_METRICS.md) `v1.0.0` - North Star Metric e KPIs

**Features**:
- [workshop-imersivo.md](business/features/workshop-imersivo.md) `v1.0.0` - Core product (2 dias, R$ 2.300/pessoa)
- [framework-context.md](business/features/framework-context.md) `v1.0.0` - Framework CONTEXT (7 pilares)
- [framework-wsci.md](business/features/framework-wsci.md) `v1.0.0` - Framework WSCI (Write, Select, Compress, Isolate)
- [consultoria-desenvolvimento.md](business/features/consultoria-desenvolvimento.md) `v1.0.0` - Serviços premium

#### Camada 3: Contexto de Mercado
- [COMPETITIVE_LANDSCAPE.md](business/COMPETITIVE_LANDSCAPE.md) `v1.0.0` - Análise competitiva
- [INDUSTRY_TRENDS.md](business/INDUSTRY_TRENDS.md) `v1.0.0` - Tendências de IA e desenvolvimento

#### Camada 4: Contexto Operacional
- [SALES_PROCESS.md](business/SALES_PROCESS.md) `v1.0.0` - Funil de vendas e conversão
- [MESSAGING_FRAMEWORK.md](business/MESSAGING_FRAMEWORK.md) `v1.0.0` - Voz da marca
- [CUSTOMER_COMMUNICATION.md](business/CUSTOMER_COMMUNICATION.md) `v1.0.0` - Diretrizes de comunicação

---

### 🔧 Technical (Arquitetura e Decisões Técnicas)

**Índice**: [technical/index.md](technical/index.md) `v1.0.0`

#### Documentação Principal
- [project_charter.md](technical/project_charter.md) `v1.0.0` - Visão, escopo e objetivos do projeto

#### Architecture Decision Records (ADRs)
- [ADR-001: Tech Stack](technical/adr/adr_001_tech_stack.md) `v1.0.0` - Vue 3 + Nuxt 4 + Tailwind + Firebase
- [ADR-002: Atomic Design](technical/adr/adr_002_atomic_design.md) `v1.0.0` - Design system e estrutura de componentes
- [ADR-003: Custom Components](technical/adr/adr_003_custom_components.md) `v1.0.0` - Componentes custom vs bibliotecas
- [ADR-004: Firebase Backend](technical/adr/adr_004_firebase_backend.md) `v1.0.0` - Firebase para backend serverless
- [ADR-005: Vercel Hosting](technical/adr/adr_005_vercel_hosting.md) `v1.0.0` - Hospedagem na Vercel Pro
- [ADR-006: Static Content](technical/adr/adr_006_static_content.md) `v1.0.0` - Sem CMS na fase inicial

---

### 📦 Product (Requisitos de Produto)

- [prd_site_thatix.md](product/prd_site_thatix.md) `v1.0.0` - PRD completo do site institucional

---

## 🎯 Uso das MetaSpecs

### Para Novos Membros da Equipe

**Onboarding recomendado**:
1. Leia este [index.md](index.md) para visão geral
2. Aprofunde em [business/index.md](business/index.md) para entender o negócio
3. Estude [CUSTOMER_PERSONAS.md](business/CUSTOMER_PERSONAS.md) para conhecer os clientes
4. Explore [technical/index.md](technical/index.md) para entender a arquitetura
5. Revise [_meta/VERSIONING_POLICY.md](_meta/VERSIONING_POLICY.md) para governança

### Para Vendas e Marketing

**Foco em**:
1. [CUSTOMER_PERSONAS.md](business/CUSTOMER_PERSONAS.md) - Quem são os clientes
2. [CUSTOMER_JOURNEY.md](business/CUSTOMER_JOURNEY.md) - Como clientes compram
3. [SALES_PROCESS.md](business/SALES_PROCESS.md) - Processo de vendas
4. [MESSAGING_FRAMEWORK.md](business/MESSAGING_FRAMEWORK.md) - O que e como comunicar
5. [features/workshop-imersivo.md](business/features/workshop-imersivo.md) - Detalhes do core product

### Para Desenvolvimento de Produto

**Foco em**:
1. [PRODUCT_STRATEGY.md](business/PRODUCT_STRATEGY.md) - Visão e princípios
2. [PRODUCT_METRICS.md](business/PRODUCT_METRICS.md) - Como medir sucesso
3. [prd_site_thatix.md](product/prd_site_thatix.md) - Requisitos de produto
4. [VOICE_OF_CUSTOMER.md](business/VOICE_OF_CUSTOMER.md) - O que clientes precisam

### Para Desenvolvimento de Software

**Foco em**:
1. [technical/index.md](technical/index.md) - Visão geral técnica
2. [project_charter.md](technical/project_charter.md) - Escopo e objetivos
3. Todos os [ADRs](technical/adr/) - Decisões arquiteturais
4. [brand_identity_spec.md](meta/brand_identity_spec.md) - Paleta e tipografia

### Para Sistemas de IA (Claude)

Todo o contexto foi estruturado para consumo por IA, permitindo:
- ✅ Suporte ao cliente contextualmente apropriado
- ✅ Assistência de vendas com tratamento de objeções
- ✅ Geração de conteúdo alinhado com voz da marca
- ✅ Desenvolvimento guiado por especificações versionadas
- ✅ Validação automática de compatibilidade de versões

---

## 📊 Metodologia Context-First

Este projeto é um **exemplo prático** da metodologia Context-First Development da própria Thatix:

### Princípios Aplicados

**1. Context Architecture**
- Estrutura modular em camadas (Meta, Business, Technical, Product)
- Separação clara de responsabilidades
- Interconexões explícitas via `related_specs`

**2. Normative Specifications**
- Frontmatter YAML obrigatório com versionamento
- Blocos `:::version_info` e `:::breaking_changes`
- Specs como artefatos de primeira classe

**3. Evolutionary Refinement**
- Versionamento SemVer (MAJOR.MINOR.PATCH)
- Histórico completo em [VERSION_HISTORY.md](_meta/VERSION_HISTORY.md)
- Política clara de atualização em [VERSIONING_POLICY.md](_meta/VERSIONING_POLICY.md)

**4. Explainability & Governance**
- Context Governance para evitar Context Drift
- Rastreamento de breaking changes
- Validação automática de versões

**5. AI-Optimized**
- Estrutura consumível por humanos E IA
- Metadados estruturados (YAML frontmatter)
- Links e referências explícitas

---

## 🔄 Context Governance

### Versionamento

Todas as specs seguem **Semantic Versioning (SemVer)**:

- **MAJOR (x.0.0)**: Breaking changes (mudança de significado, remoção de seções obrigatórias)
- **MINOR (0.x.0)**: Adições compatíveis (novas seções, exemplos, campos opcionais)
- **PATCH (0.0.x)**: Correções e clarificações (typos, formatação, links)

### Processo de Atualização

Ao atualizar uma spec:
1. Atualizar `spec_version` no frontmatter
2. Atualizar `last_updated` para data atual
3. Se MAJOR: atualizar `supersedes` para versão anterior
4. Documentar mudança em `:::breaking_changes`
5. Registrar em [VERSION_HISTORY.md](_meta/VERSION_HISTORY.md)
6. Atualizar versão nos índices

**Documentação completa**: [VERSIONING_POLICY.md](_meta/VERSIONING_POLICY.md)

### Princípio Jidoka

🛑 **Se encontrar spec sem versionamento**: PARE e execute `/metaspecs:governance:add-versioning`

⚠️ **Se spec está deprecated**: Alerte e sugira usar versão atual

---

## 🎨 Identidade Visual

**Paleta de Cores**:
- **Primária**: Deep Navy (`#0A192F`)
- **Secundária**: Electric Blue (`#00BFFF`)
- **Acento**: White (`#FFFFFF`)
- **Texto**: Light Grey (`#A0A0A0`)

**Tipografia**:
- **Títulos**: Montserrat, Bold
- **Corpo**: Inter, Regular

**Detalhes completos**: [brand_identity_spec.md](meta/brand_identity_spec.md)

---

## 🏗️ Stack Tecnológico

**Frontend**:
- Vue 3 (Composition API)
- Nuxt 4.2.2 (SSG/SSR)
- Tailwind CSS

**Backend**:
- Firebase (formulário, cloud functions)

**Hospedagem**:
- Vercel Pro

**Detalhes e justificativa**: [ADR-001](technical/adr/adr_001_tech_stack.md)

---

## 📈 Métricas de Sucesso

### North Star Metric
**Número de Desenvolvedores Usando Context-First Ativamente**

### Metas 2026
- 500 desenvolvedores treinados
- 50-100 clientes (empresas)
- NPS > 70

**Métricas completas**: [PRODUCT_METRICS.md](business/PRODUCT_METRICS.md)

---

## 🚀 Problema que Resolvemos

**Estatística**: 76% dos projetos com IA falham não por limitações tecnológicas, mas pela ausência de metodologia estruturada.

**Sintomas**:
- "Vibe coding" gerando débito técnico
- Context poisoning e falta de previsibilidade
- Experimentos isolados que não escalam
- Falhas em ambientes de missão crítica

**Solução Thatix**:
Metodologia proprietária baseada em Engenharia de Contexto que transforma desenvolvimento com IA em processo previsível, testável e escalável.

---

## 📚 Recursos Adicionais

### Comandos Slash Úteis

- `/metaspecs:add-frontmatter` - Adicionar frontmatter a specs sem versionamento
- `/metaspecs:governance:add-versioning` - Adicionar sistema de versionamento completo
- `/metaspecs:build-index` - Reconstruir este índice
- `/metaspecs:build-index business` - Reconstruir índice de business
- `/metaspecs:build-index technical` - Reconstruir índice técnico

### Estrutura de Diretórios

```
specs/
├── _meta/                  # Governança e meta-informações
│   ├── VERSIONING_POLICY.md
│   └── VERSION_HISTORY.md
├── meta/                   # Identidade e marca
│   └── brand_identity_spec.md
├── business/               # Contexto empresarial
│   ├── index.md
│   ├── README.md
│   ├── CUSTOMER_PERSONAS.md
│   ├── CUSTOMER_JOURNEY.md
│   ├── PRODUCT_STRATEGY.md
│   ├── PRODUCT_METRICS.md
│   ├── [... mais 7 specs]
│   └── features/           # Features detalhadas
│       ├── workshop-imersivo.md
│       ├── framework-context.md
│       ├── framework-wsci.md
│       └── consultoria-desenvolvimento.md
├── technical/              # Contexto técnico
│   ├── index.md
│   ├── README.md
│   ├── project_charter.md
│   └── adr/                # Architecture Decision Records
│       ├── adr_001_tech_stack.md
│       ├── adr_002_atomic_design.md
│       ├── [... mais 4 ADRs]
├── product/                # Requisitos de produto
│   └── prd_site_thatix.md
└── index.md                # Este arquivo (índice raiz)
```

---

## 🤝 Manutenção

**Responsáveis**: Founders + Tech Lead + Product Owner

**Frequência de Revisão**:
- **Trimestral**: Todas as especificações
- **Ad-hoc**: Quando mudanças significativas ocorrerem

**Versionamento**: Toda mudança significativa deve atualizar:
1. Campo `spec_version` no frontmatter
2. Campo `last_updated`
3. Bloco `:::breaking_changes`
4. [VERSION_HISTORY.md](_meta/VERSION_HISTORY.md)

---

## 📞 Feedback e Contribuições

Se você encontrar:
- ❌ Informações desatualizadas
- ❌ Lacunas importantes
- ❌ Oportunidades de melhoria

Entre em contato com os responsáveis ou abra uma issue.

---

## ✅ Status do Projeto

| Categoria | Status | Última Atualização |
|-----------|--------|-------------------|
| Meta Specs | ✅ Completo | 2026-01-13 |
| Business Specs | ✅ Completo | 2026-01-13 |
| Technical Specs | ✅ Completo | 2026-01-13 |
| Product Specs | ✅ Completo | 2026-01-13 |
| Governança | ✅ Implementada | 2026-01-13 |
| Versionamento | ✅ v1.0.0 | 2026-01-13 |

**Projeto**: Site Institucional Thatix
**Status Geral**: ✅ Especificações Completas
**Próxima Fase**: Desenvolvimento

---

**Última Atualização**: 2026-01-13
**Versão**: 1.0.0
**Status**: ✅ Ativo e Completo
**Total de Specs**: 28 arquivos versionados
