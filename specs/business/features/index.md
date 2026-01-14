---
spec_version: "1.0.0"
valid_from: "2026-01-13"
last_updated: "2026-01-13"
supersedes: null
status: "active"
category: "business"
tags: ["index", "features", "products", "services", "navigation"]
---

# Features e Serviços - Thatix

:::version_info
**Versão**: 1.0.0
**Válida desde**: 2026-01-13
**Status**: Ativa
:::

:::breaking_changes
**v1.0.0** (baseline):
- Primeira versão do índice de features
- Consolida 4 features: Workshop, Framework CONTEXT, Framework WSCI, Consultoria
:::

---

## 📋 Visão Geral

Este diretório contém especificações detalhadas de **produtos, serviços e metodologias** da Thatix. Cada feature spec documenta funcionalidade, benefícios, precificação, casos de uso e métricas de sucesso.

---

## 🎯 Produtos e Serviços

### Core Products

#### [workshop-imersivo.md](workshop-imersivo.md) `v1.0.0` ⭐ **Flagship**

**Workshop de 2 dias** Context-First Development (produto principal da Thatix).

**Resumo**:
- 🕐 **Duração**: 2 dias (60% prática, 40% teoria)
- 💰 **Preço**: R$ 2.300/pessoa (mínimo 3 pessoas)
- 📦 **Inclui**: MetaSpec Starter Kit + 2 semanas de suporte
- 🎯 **Resultado**: 73% ganho de produtividade

**Estrutura**:
- **Dia 1**: Framework CONTEXT (7 pilares) + Fase Specify
- **Dia 2**: Framework WSCI + Plan/Implement/Adopt

**Para quem**:
- CTOs, VPs de Engenharia (decisão estratégica)
- Tech Leads, Engineering Managers (implementação)
- Desenvolvedores Senior/Staff (execução hands-on)

**Quando usar esta spec**:
- Vendas: Apresentar produto para prospects
- Marketing: Criar materiais promocionais
- Delivery: Preparar e executar workshop
- Produto: Evoluir o workshop baseado em feedback

---

### Metodologias

#### [framework-context.md](framework-context.md) `v1.0.0`

**Framework CONTEXT** - Metodologia proprietária de 7 pilares para desenvolvimento estruturado com IA.

**Os 7 Pilares**:
1. **C**ontext Architecture - Design de informação para IA
2. **O**bservability-Driven - Instrumentação e rastreamento
3. **N**ormative Specifications - Specs executáveis com anti-patterns
4. **T**est-First AI Development - TDD adaptado para IA
5. **E**volutionary Refinement - Evolução contínua
6. **X**plainability & Governance - Explicabilidade e controle
7. **T**rustworthy Deployment - Deploy confiável

**Quando usar esta spec**:
- Explicar metodologia Context-First para clientes
- Treinar time interno na metodologia
- Criar conteúdo educativo (blog, webinars)
- Desenvolver features do workshop

---

#### [framework-wsci.md](framework-wsci.md) `v1.0.0`

**Framework WSCI** - Engenharia de contexto baseada em LangChain.

**WSCI = Write, Select, Compress, Isolate**:
- **Write**: Salvar contexto eficientemente
- **Select**: RAG e estratégias de retrieval
- **Compress**: Summarização e trimming
- **Isolate**: Separação e organização de contextos

**Quando usar esta spec**:
- Implementar context engineering em projetos
- Otimizar uso de contexto com LLMs
- Treinar desenvolvedores em técnicas avançadas
- Criar ferramentas de context management

---

### Serviços Premium

#### [consultoria-desenvolvimento.md](consultoria-desenvolvimento.md) `v1.0.0`

**Consultoria técnica e desenvolvimento** aplicando Context-First.

**Modalidades**:
- **Consultoria de Arquitetura**: Acompanhamento em projeto complexo
- **Desenvolvimento Full**: Time Thatix desenvolvendo com metodologia
- **Refatoração Crítica**: Reestruturação de código legado

**Precificação**:
- Day rate: R$ 3.000 - R$ 5.000/dia
- Sprint: R$ 60.000 - R$ 100.000/sprint
- Projeto Fechado: Cotação personalizada

**Quando usar esta spec**:
- Upsell após workshop
- Projetos específicos de clientes
- Desenvolvimento full de features críticas

---

## 📊 Matriz de Features

| Feature | Tipo | Prioridade | Status | Público |
|---------|------|------------|--------|---------|
| [Workshop Imersivo](workshop-imersivo.md) | Core Product | 🔴 Alta | ✅ Ativo | CTOs, Tech Leads |
| [Framework CONTEXT](framework-context.md) | Methodology | 🔴 Alta | ✅ Ativo | Todos |
| [Framework WSCI](framework-wsci.md) | Methodology | 🔴 Alta | ✅ Ativo | Devs avançados |
| [Consultoria](consultoria-desenvolvimento.md) | Premium Service | 🟡 Média | ✅ Ativo | Clientes enterprise |

---

## 🎯 Jornada do Cliente por Feature

### Entry Point: Workshop Imersivo
```
Prospect → Discovery Call → Workshop (2 dias) → Implementação (2 semanas suporte)
    ↓
Cliente Satisfeito
    ↓
Expansão: Consultoria/Desenvolvimento OU Novos Workshops
```

### Upsell Path
```
Workshop → [Opções]
    ├─→ Consultoria de Arquitetura (projeto específico)
    ├─→ Desenvolvimento Full (features críticas)
    ├─→ Novos Workshops (para outros times)
    └─→ Certificação (futuro)
```

---

## 💰 Precificação Resumida

| Produto/Serviço | Preço Base | Modelo |
|-----------------|------------|--------|
| Workshop Imersivo | R$ 2.300/pessoa | Por participante (mín. 3) |
| Consultoria Arquitetura | R$ 3.000-5.000/dia | Day rate |
| Desenvolvimento Sprint | R$ 60.000-100.000 | Sprint fechado |
| Projeto Fechado | Variável | Cotação |

**ROI Típico**: Workshop para 10 devs = R$ 23.000 → ~5.700% ROI no primeiro ano (baseado em 73% produtividade).

---

## 📈 Métricas de Sucesso por Feature

### Workshop Imersivo
- **NPS pós-workshop**: > 70 (target)
- **Adoption rate (30 dias)**: > 80%
- **Ganho de produtividade**: > 50% (target 73%)
- **Repeat business**: > 40% em 12 meses

### Consultoria/Desenvolvimento
- **On-time delivery**: > 90%
- **Client satisfaction**: > 4.5/5
- **Repeat business rate**: > 50%

**Detalhes completos**: [PRODUCT_METRICS.md](../PRODUCT_METRICS.md)

---

## 🚀 Roadmap de Features

### Q1 2026 (Atual)
- ✅ Workshop Imersivo v1.0
- ✅ Framework CONTEXT documentado
- ✅ Framework WSCI documentado
- ✅ Consultoria estruturada

### Q2-Q3 2026
- 📋 Workshop v1.5 (melhorias baseadas em feedback)
- 📋 Certificação Context-First Developer
- 📋 Comunidade privada de clientes

### Q4 2026
- 📋 Workshop modular (possibilidade de módulos separados)
- 📋 Train-the-trainer program

### 2027+
- 📋 Context Engineering Platform (SaaS)
- 📋 Ferramentas de automação

**Roadmap completo**: [PRODUCT_STRATEGY.md](../PRODUCT_STRATEGY.md)

---

## 🔗 Relação com Outras Specs

### Features conectam com:

**Strategy**:
- [PRODUCT_STRATEGY.md](../PRODUCT_STRATEGY.md) - Visão e posicionamento
- [COMPETITIVE_LANDSCAPE.md](../COMPETITIVE_LANDSCAPE.md) - Diferenciação

**Customer**:
- [CUSTOMER_PERSONAS.md](../CUSTOMER_PERSONAS.md) - Quem compra cada feature
- [CUSTOMER_JOURNEY.md](../CUSTOMER_JOURNEY.md) - Como clientes descobrem e adotam
- [SALES_PROCESS.md](../SALES_PROCESS.md) - Como vender cada feature

**Marketing**:
- [MESSAGING_FRAMEWORK.md](../MESSAGING_FRAMEWORK.md) - Como comunicar value proposition
- [VOICE_OF_CUSTOMER.md](../VOICE_OF_CUSTOMER.md) - Linguagem e objeções

**Technical**:
- [project_charter.md](../../technical/project_charter.md) - Como implementar no site
- [ADRs](../../technical/adr/) - Decisões técnicas relacionadas

---

## 🎓 Como Usar Este Diretório

### Para Vendas e Marketing

**Preparar materiais**:
1. Leia [workshop-imersivo.md](workshop-imersivo.md) completo
2. Use seção "Benefícios para o Cliente" em pitches
3. Referencie "Tratamento de Objeções" em discovery calls
4. Cite métricas de sucesso (73% produtividade)

**Criar conteúdo**:
- Blog posts: Explique frameworks ([framework-context.md](framework-context.md), [framework-wsci.md](framework-wsci.md))
- Case studies: Use resultados de [workshop-imersivo.md](workshop-imersivo.md)
- Webinars: Estruture com base em metodologias

### Para Product Management

**Evoluir features**:
1. Coletar feedback de clientes
2. Identificar tipo de mudança (MAJOR/MINOR/PATCH)
3. Atualizar spec apropriada
4. Versionar conforme [VERSIONING_POLICY.md](../../_meta/VERSIONING_POLICY.md)
5. Comunicar mudanças

**Criar novas features**:
1. Seguir template de feature spec existente
2. Definir benefícios, público, precificação, métricas
3. Linkar com specs relacionadas
4. Versionar desde v1.0.0

### Para Delivery (Execução)

**Preparar workshop**:
1. Seguir estrutura exata de [workshop-imersivo.md](workshop-imersivo.md)
2. Customizar exemplos com contexto do cliente
3. Preparar MetaSpec Starter Kit
4. Planejar suporte pós-workshop (2 semanas)

**Executar consultoria**:
1. Seguir modalidades de [consultoria-desenvolvimento.md](consultoria-desenvolvimento.md)
2. Aplicar frameworks CONTEXT e WSCI
3. Documentar aprendizados para melhorar specs

---

## 🔗 Navegação

**Voltar para**: [Business Index](../index.md)

**Índice Raiz**: [Specs Root](../../index.md)

**Outras Categorias**:
- [Technical Specs](../../technical/index.md) - Arquitetura
- [Product Specs](../../product/index.md) - PRDs
- [Meta Specs](../../meta/index.md) - Brand identity

---

## 🤝 Manutenção

**Responsáveis**: Product Owner + Founders + Delivery Team

**Frequência de Revisão**:
- **Após cada workshop**: Coletar feedback e identificar melhorias
- **Mensal**: Revisar métricas de sucesso
- **Trimestral**: Avaliar roadmap e prioridades

**Processo de Atualização**:
1. Identificar necessidade de mudança (feedback, nova feature, pivot)
2. Classificar tipo (MAJOR/MINOR/PATCH)
3. Atualizar spec e versionamento
4. Registrar em [VERSION_HISTORY.md](../../_meta/VERSION_HISTORY.md)
5. Comunicar a stakeholders (Vendas, Marketing, Delivery)

---

**Última Atualização**: 2026-01-13
**Versão**: 1.0.0
**Status**: ✅ Ativo
**Total de Features**: 4 (1 core product + 2 methodologies + 1 premium service)
