---
spec_version: "1.0.0"
valid_from: "2026-01-13"
last_updated: "2026-01-13"
supersedes: null
status: "active"
category: "technical"
tags: ["readme", "documentation", "navigation", "guide"]
---

# Documentação Técnica - Site Institucional Thatix

Este diretório contém toda a documentação técnica e arquitetural do projeto, seguindo a metodologia Context-First.

---

## 🚀 Início Rápido

**Para começar a desenvolver:**
1. Leia [index.md](index.md) - Visão geral completa
2. Revise [project_charter.md](project_charter.md) - Objetivos e escopo
3. Entenda [adr/](adr/) - Decisões arquiteturais

**Stack Tecnológico:**
- Vue 3 + Nuxt 4 + Tailwind CSS
- Firebase (backend)
- Vercel Pro (hospedagem)
- ESLint (qualidade)

---

## 📁 Estrutura de Documentação

```
specs/technical/
├── README.md                    # Este arquivo
├── index.md                     # Índice master e navegação
├── project_charter.md           # Visão, objetivos, stakeholders
│
├── adr/                         # Architecture Decision Records
│   ├── adr_001_tech_stack.md   # Vue 3 + Nuxt 4 + Tailwind
│   ├── adr_002_atomic_design.md # Design System
│   ├── adr_003_custom_components.md # Componentes do zero
│   ├── adr_004_firebase_backend.md  # Firebase backend
│   ├── adr_005_vercel_hosting.md    # Hospedagem Vercel Pro
│   └── adr_006_static_content.md    # Conteúdo estático
│
└── [A ser criado quando houver código]
    ├── CLAUDE.meta.md           # Guia de desenvolvimento com IA
    ├── CODEBASE_GUIDE.md        # Navegação da codebase
    ├── ATOMIC_DESIGN_GUIDE.md   # Implementação Atomic Design
    ├── FIREBASE_INTEGRATION.md  # Setup Firebase
    ├── SEO_OPTIMIZATION.md      # Estratégias SEO
    ├── CONTRIBUTING.md          # Guia de contribuição
    ├── TROUBLESHOOTING.md       # Resolução de problemas
    └── ARCHITECTURE_CHALLENGES.md # Desafios conhecidos
```

---

## 📊 Status da Documentação

| Documento | Status | Descrição |
|-----------|--------|-----------|
| **index.md** | ✅ Completo | Índice master |
| **project_charter.md** | ✅ Completo | Charter do projeto |
| **ADR-001** | ✅ Completo | Stack tecnológico |
| **ADR-002** | ✅ Completo | Atomic Design |
| **ADR-003** | ✅ Completo | Componentes custom |
| **ADR-004** | ✅ Completo | Firebase backend |
| **ADR-005** | ✅ Completo | Vercel hosting |
| **ADR-006** | ✅ Completo | Conteúdo estático |

**Documentos a serem criados após setup do código:**
- CLAUDE.meta.md
- CODEBASE_GUIDE.md
- ATOMIC_DESIGN_GUIDE.md
- FIREBASE_INTEGRATION.md
- SEO_OPTIMIZATION.md
- CONTRIBUTING.md
- TROUBLESHOOTING.md
- ARCHITECTURE_CHALLENGES.md

---

## 🎯 Decisões Arquiteturais Principais

### Stack Tecnológico ([ADR-001](adr/adr_001_tech_stack.md))
- **Frontend:** Vue 3 + Nuxt 4 (expertise da equipe, SSG/SSR, performance)
- **Styling:** Tailwind CSS (utility-first, produtividade)
- **Backend:** Firebase (simplicidade, escalabilidade)
- **Hospedagem:** Vercel Pro (otimizado, CI/CD, analytics)

### Design System ([ADR-002](adr/adr_002_atomic_design.md))
- **Atomic Design** - Componentes organizados em atoms → molecules → organisms → templates → pages
- Hierarquia clara, reutilização máxima, escalável

### Componentes ([ADR-003](adr/adr_003_custom_components.md))
- **Todos do zero** - Zero bibliotecas UI
- Controle total, performance, alinhamento com brand
- ~25-30 componentes estimados

### Backend ([ADR-004](adr/adr_004_firebase_backend.md))
- **Firebase Cloud Functions** - Formulário de contato
- Serverless, escalável, free tier suficiente

### Hospedagem ([ADR-005](adr/adr_005_vercel_hosting.md))
- **Vercel Pro** - $20/mês
- Deploy automático, CDN global, analytics

### Conteúdo ([ADR-006](adr/adr_006_static_content.md))
- **Estático (hard-coded)** - Sem CMS para MVP
- Simplicidade, performance, versionamento Git

---

## 🏗️ Estrutura do Projeto (Futuro)

```
thatix-site/
├── components/
│   ├── atoms/           # Primitivos: Button, Input, Icon
│   ├── molecules/       # FormField, Card, NavItem
│   ├── organisms/       # Navbar, Footer, ContactForm
│   └── templates/       # PageTemplate, SectionTemplate
│
├── pages/               # Rotas (Nuxt file-based routing)
│   ├── index.vue        # Home
│   ├── metodologia.vue
│   ├── servicos.vue
│   ├── clientes.vue
│   └── contato.vue
│
├── composables/         # Lógica reutilizável
├── layouts/             # Layouts do site
├── public/              # Assets estáticos
├── server/              # Firebase integration
└── assets/              # CSS, Tailwind config
```

---

## 🎨 Atomic Design - Resumo

### Atoms (10-12 componentes)
Elementos indivisíveis: Button, Input, Label, Icon, Text, Link, Image, Spinner, Badge, Divider

### Molecules (6-8 componentes)
Composições simples: FormField, Card, NavItem, SocialLink, FeatureCard, TestimonialCard

### Organisms (8-10 componentes)
Seções complexas: Navbar, Footer, ContactForm, HeroSection, FeatureGrid, TestimonialSlider, ClientLogos

### Templates
Layouts: PageTemplate, SectionTemplate

### Pages
Rotas: Home, Metodologia, Serviços, Clientes, Contato

---

## 📈 Objetivos e KPIs

### Performance
- LCP < 2.5s
- FCP < 1.8s
- Lighthouse Score > 90

### SEO
- Top 5 Google para keywords principais em 90 dias
- Sitemap, meta tags, Open Graph implementados

### Negócio
- 10-15 MQLs/mês via formulário
- 50+ leads em 90 dias pós-lançamento
- 1+ cliente fechado originado do site

---

## 🚀 Cronograma de Alto Nível

**Sprint 1 (Semana 1-2):** Fundação
- Setup do projeto (Nuxt 4, Tailwind, Firebase)
- Atomic Design: Atoms e Molecules
- Header e Footer
- Página Home (estrutura básica)

**Sprint 2 (Semana 3):** Páginas Core
- Página Metodologia
- Página Serviços
- Organisms principais

**Sprint 3 (Semana 4):** Páginas Finais + Integrações
- Página Clientes
- Página Contato + Firebase
- Google Analytics
- Animações

**Sprint 4 (Semana 5):** Testes e Deploy
- QA completo
- Performance optimization
- SEO final
- Deploy produção (thatix.io)

---

## 💡 Princípios de Desenvolvimento

1. **Context-First** - Especificações claras antes de código
2. **Atomic Design** - Componentes organizados hierarquicamente
3. **Performance-First** - Otimização desde o início
4. **SEO-First** - Estrutura otimizada para buscadores
5. **Simplicidade** - Evitar over-engineering

---

## 🔗 Links Úteis

### Documentação Externa
- [Nuxt 4 Docs](https://nuxt.com)
- [Vue 3 Docs](https://vuejs.org)
- [Tailwind CSS](https://tailwindcss.com)
- [Firebase Docs](https://firebase.google.com/docs)
- [Atomic Design Book](https://atomicdesign.bradfrost.com/)

### Documentação do Projeto
- [PRD](../product/prd_site_thatix.md) - Product Requirements
- [Brand Identity](../meta/brand_identity_spec.md) - Identidade visual
- [Business Context](../business/) - Contexto empresarial

---

## 📝 Como Contribuir

1. Leia este README completo
2. Revise [project_charter.md](project_charter.md)
3. Entenda ADRs em [adr/](adr/)
4. Siga padrões de Atomic Design
5. Use ESLint (zero warnings)

**Quando o código existir:**
- CONTRIBUTING.md terá workflow detalhado
- CLAUDE.meta.md terá padrões de código
- CODEBASE_GUIDE.md terá navegação completa

---

## 🔄 Manutenção

**Este é um documento vivo**. Atualize conforme:
- Novas decisões arquiteturais → Criar novo ADR
- Mudanças de escopo → Atualizar project_charter.md
- Stack muda → Atualizar ADR relevante
- Código criado → Adicionar guias práticos

**Responsáveis:** Tech Lead + Product Owner
**Frequência:** A cada milestone ou mudança significativa

---

## ✅ Checklist de Validação

**Antes de Iniciar Desenvolvimento:**
- [ ] Todas as ADRs lidas e compreendidas
- [ ] Project Charter aprovado por stakeholders
- [ ] Stack tecnológico validado (Nuxt 4 estável)
- [ ] Domínio thatix.io configurado
- [ ] Firebase project criado
- [ ] Vercel Pro account ativo

**Durante Desenvolvimento:**
- [ ] Componentes seguem Atomic Design
- [ ] ESLint sem warnings
- [ ] Performance targets sendo atingidos
- [ ] SEO implementado desde início

**Antes do Deploy:**
- [ ] Lighthouse Score > 90
- [ ] Formulário de contato testado
- [ ] Google Analytics funcionando
- [ ] Todas as 5 páginas completas
- [ ] Responsividade testada (mobile, tablet, desktop)

---

**Versão da Documentação:** 1.0
**Última Atualização:** 2026-01-13
**Próxima Revisão:** Início do desenvolvimento (quando código for criado)

---

Esta documentação técnica está pronta para guiar o desenvolvimento do site institucional da Thatix seguindo os princípios da metodologia Context-First. ✨
