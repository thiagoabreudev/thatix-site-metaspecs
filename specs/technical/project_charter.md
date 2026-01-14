---
spec_version: "1.0.0"
valid_from: "2026-01-13"
last_updated: "2026-01-13"
supersedes: null
status: "active"
category: "technical"
tags: ["project-charter", "scope", "objectives", "timeline"]
---

# Project Charter - Site Institucional Thatix

**Versão:** 1.0
**Data:** 2026-01-13
**Status:** Ativo

---

## 1. Visão do Projeto

### Declaração de Visão

Criar o site institucional da Thatix que sirva como **principal canal de comunicação e marketing** da empresa, apresentando a metodologia Context-First Development, serviços de workshop e consultoria, e estabelecendo a Thatix como **referência em Engenharia de Contexto e desenvolvimento guiado por IA**.

### Proposta de Valor do Site

**Para clientes em potencial (CTOs, Founders, Tech Leads):**
- Compreender rapidamente o que é Context-First Development
- Ver resultados concretos (73% ganho de produtividade)
- Acessar cases de sucesso (Finpass, Embbeda Labs, etc.)
- Entrar em contato facilmente para discovery call

**Para a Thatix:**
- Gerar leads qualificados (formulário de contato)
- Construir autoridade de mercado
- Educar o mercado sobre Context-First
- Reduzir CAC (custo de aquisição de cliente)

---

## 2. Objetivos e Critérios de Sucesso

### Objetivos de Negócio

1. **Gerar Leads Qualificados**
   - Meta: 10-15 MQLs por mês (via formulário de contato)
   - Conversão: 30-40% desses MQLs → SQLs

2. **Construir Autoridade**
   - Posicionar como referência em Context-First Development
   - Aparecer em top 3 de busca orgânica para "context engineering brasil"
   - Share of voice em comunidades técnicas

3. **Educar o Mercado**
   - Explicar claramente metodologia Context-First
   - Mostrar diferença entre vibe coding e engenharia estruturada
   - Demonstrar resultados mensuráveis

### Objetivos Técnicos

1. **Performance**
   - LCP (Largest Contentful Paint) < 2.5s
   - FCP (First Contentful Paint) < 1.8s
   - CLS (Cumulative Layout Shift) < 0.1
   - Lighthouse Score > 90 (Performance, Accessibility, Best Practices, SEO)

2. **SEO**
   - Sitemap automático e robots.txt configurado
   - Meta tags completas em todas as páginas
   - Open Graph para compartilhamento social
   - Schema.org markup (Organization, LocalBusiness)

3. **Responsividade**
   - Design mobile-first
   - Breakpoints: mobile (< 640px), tablet (640-1024px), desktop (> 1024px)
   - Touch-friendly (botões > 44px, espaçamento adequado)

4. **Manutenibilidade**
   - Atomic Design consistente
   - Componentes reutilizáveis
   - Código limpo e bem documentado
   - ESLint sem warnings

### Critérios de Sucesso (Definition of Done)

**Para o Lançamento (MVP):**
- ✅ 5 páginas completas e funcionais
- ✅ Formulário de contato integrado com Firebase
- ✅ Google Analytics implementado e testado
- ✅ Performance: Lighthouse Score > 90
- ✅ SEO: Meta tags, sitemap, robots.txt
- ✅ Responsivo: Testado em mobile, tablet, desktop
- ✅ Deploy em Vercel Pro com domínio thatix.io
- ✅ ESLint sem erros
- ✅ Conteúdo revisado e aprovado

**Para 30 Dias Pós-Lançamento:**
- ✅ 10+ leads gerados via formulário
- ✅ Bounce rate < 60%
- ✅ Tempo médio na página > 1:30min
- ✅ Nenhum erro crítico reportado
- ✅ Zero downtime

**Para 90 Dias Pós-Lançamento:**
- ✅ 50+ leads acumulados
- ✅ Top 5 no Google para keywords principais
- ✅ 3.000+ visitas mensais
- ✅ 5+ SQLs originados do site

---

## 3. Escopo do Projeto

### No Escopo (Fase 1 - MVP)

**Páginas:**
1. **Home**
   - Hero section com proposta de valor clara
   - Overview da metodologia Context-First
   - Prova social (logos clientes, números de resultados)
   - CTA para contato e workshop

2. **Metodologia**
   - Explicação detalhada do Framework CONTEXT (7 pilares)
   - Framework WSCI (Write, Select, Compress, Isolate)
   - Diferenciação: Context-First vs Vibe Coding
   - Infográficos e diagramas

3. **Serviços**
   - Workshop Imersivo (2 dias)
   - Consultoria e Desenvolvimento
   - Precificação transparente (R$ 2.300/pessoa)
   - Processo de contratação

4. **Clientes**
   - Cases de sucesso (Finpass, Embbeda Labs, Demarco, Crypteras)
   - Resultados mensuráveis (73% produtividade, etc.)
   - Depoimentos (quando disponíveis)
   - Logos de clientes

5. **Contato**
   - Formulário integrado com Firebase
   - Campos: Nome, Email, Empresa, Cargo, Mensagem
   - Informações de contato (email, LinkedIn)
   - Localização (se aplicável)

**Componentes:**
- Header (navegação, logo, CTA)
- Footer (links, redes sociais, copyright)
- Atomic Design completo:
  - Atoms: Button, Input, Label, Icon, Text, Link
  - Molecules: FormField, Card, NavItem, SocialLink
  - Organisms: Navbar, ContactForm, HeroSection, TestimonialSlider, FeatureGrid
  - Templates: PageTemplate, SectionTemplate
  - Pages: HomePage, MetodologiaPage, ServicosPage, ClientesPage, ContatoPage

**Integrações:**
- Firebase (formulário de contato)
- Google Analytics 4 (tracking)
- Vercel Analytics (web vitals)

**Funcionalidades:**
- Navegação responsiva (mobile menu)
- Smooth scroll entre seções
- Animações sutis (fade-in, slide-up)
- Form validation (client-side e server-side)
- Loading states (form submission)
- Error handling (form, Firebase)

---

### Fora do Escopo (Futuras Fases)

**Fase 2 (3-6 meses pós-lançamento):**
- Blog/Artigos técnicos
- Página de cases detalhados (páginas individuais)
- Recursos downloadáveis (whitepapers, ebooks)
- Newsletter signup
- Calculadora de ROI interativa

**Fase 3 (6-12 meses):**
- Portal do cliente (login)
- Agendamento de workshops (Calendly integration)
- Chat/Chatbot (Intercom, Drift)
- Internacionalização (EN, ES)
- Dark mode

**Explicitamente Fora:**
- CMS headless (conteúdo será hard-coded)
- Sistema de comentários
- E-commerce/pagamentos online
- Área de membros/comunidade
- Integração com Slack/Discord

---

## 4. Stakeholders

### Stakeholders Principais

| Nome/Papel | Responsabilidade | Interesse | Poder de Decisão |
|------------|------------------|-----------|------------------|
| **Founders Thatix** | Aprovação final, direcionamento estratégico | Alto | Alto |
| **Product Owner** | Definir requisitos, priorizar features, aceitar entregas | Alto | Médio-Alto |
| **Desenvolvedores (2)** | Implementação, qualidade técnica, manutenção | Alto | Médio |
| **QA** | Garantir qualidade, testar funcionalidades | Médio | Baixo-Médio |
| **Marketing/Vendas** | Geração de leads, conteúdo, conversão | Alto | Médio |

### Matriz RACI

| Atividade | Founders | PO | Devs | QA | Marketing |
|-----------|----------|----|----- |----|-----------|
| **Aprovação de Conteúdo** | A | R | I | I | C |
| **Definição de Features** | A | R | C | C | C |
| **Implementação Técnica** | I | C | R | I | I |
| **Testes de Qualidade** | I | C | C | R | I |
| **Deploy em Produção** | A | C | R | I | I |
| **Monitoramento Pós-Launch** | I | R | C | I | A |

*R = Responsible, A = Accountable, C = Consulted, I = Informed*

---

## 5. Restrições

### Restrições Técnicas

1. **Stack Fixo:** Vue 3 + Nuxt 4 + Tailwind CSS (decisão já tomada)
2. **Sem TypeScript:** JavaScript puro (expertise da equipe)
3. **Sem Testes Automatizados (MVP):** Foco em entrega rápida
4. **Conteúdo Estático:** Sem CMS (simplicidade)
5. **Firebase Backend:** Para formulário (não backend completo)

### Restrições de Recursos

1. **Equipe Pequena:** 2 devs + 1 PO + 1 QA (capacidade limitada)
2. **Projetos Simultâneos:** Time trabalha em 4 projetos (não dedicação exclusiva)
3. **Budget:** Vercel Pro + Firebase (custo controlado)

### Restrições de Tempo

1. **Time-to-Market:** Lançamento desejado em 4-6 semanas
2. **Iterações Rápidas:** Sprints de 1 semana
3. **MVP First:** Evitar scope creep, focar no essencial

### Restrições de Escopo

1. **5 Páginas Apenas:** Home, Metodologia, Serviços, Clientes, Contato
2. **Funcionalidades Mínimas:** Sem blog, sem portal, sem chat (MVP)
3. **PT-BR Apenas:** Sem internacionalização inicial

---

## 6. Premissas

### Premissas Técnicas

- ✅ Vercel Pro suporta custom domain thatix.io sem problemas
- ✅ Firebase free tier é suficiente para volume inicial de formulários
- ✅ Google Analytics 4 fornece insights necessários
- ✅ Nuxt 4 está estável o suficiente para produção
- ✅ Equipe tem conhecimento suficiente em Vue/Nuxt

### Premissas de Negócio

- ✅ Conteúdo do site será fornecido por Marketing/Founders
- ✅ Assets visuais (logos, imagens) estão disponíveis em /assets
- ✅ Identidade visual está definida (brand_identity_spec.md)
- ✅ Haverá aprovação rápida de conteúdo/design (não bloqueador)

### Premissas de Usuário

- ✅ Público-alvo tem acesso a internet de boa qualidade
- ✅ Uso majoritário de desktop (70%) vs mobile (30%)
- ✅ Browsers modernos (últimas 2 versões Chrome, Firefox, Safari, Edge)
- ✅ JavaScript habilitado

---

## 7. Riscos e Mitigações

### Riscos Técnicos

| Risco | Probabilidade | Impacto | Mitigação |
|-------|---------------|---------|-----------|
| **Nuxt 4 instável** | Baixa | Alto | Avaliar estabilidade antes, fallback para Nuxt 3 se necessário |
| **Performance abaixo do target** | Média | Médio | Lazy loading, code splitting, otimização de imagens desde início |
| **Problemas de integração Firebase** | Baixa | Médio | Testar integração cedo, ter fallback (email direto) |
| **Deploy failures Vercel** | Baixa | Alto | Testes de build local, staging environment |

### Riscos de Projeto

| Risco | Probabilidade | Impacto | Mitigação |
|-------|---------------|---------|-----------|
| **Scope creep** | Alta | Alto | Escopo rígido documentado, PO como gatekeeper |
| **Atrasos de conteúdo** | Média | Médio | Definir deadlines claros, usar lorem ipsum se necessário |
| **Falta de capacidade (4 projetos)** | Média | Alto | Priorização clara, comunicação transparente |
| **Mudanças de design de última hora** | Média | Médio | Aprovar design antes de implementar, limitar revisões |

### Riscos de Negócio

| Risco | Probabilidade | Impacto | Mitigação |
|-------|---------------|---------|-----------|
| **Site não gera leads esperados** | Média | Alto | A/B testing de CTAs, otimização contínua pós-launch |
| **SEO lento para ranquear** | Média | Médio | Estratégia de conteúdo, backlinks, patience |
| **Bounce rate alto** | Baixa | Médio | UX research, heatmaps, iterações baseadas em dados |

---

## 8. Cronograma de Alto Nível

### Fase de Planejamento (Concluída)
- ✅ Definição de escopo e requisitos
- ✅ Escolha de stack tecnológica
- ✅ Criação de MetaSpecs (business + technical)

### Fase de Desenvolvimento (4-5 semanas)

**Sprint 1 (Semana 1-2): Fundação**
- Setup do projeto (Nuxt 4, Tailwind, Firebase)
- Atomic Design: Atoms e Molecules
- Header e Footer
- Página Home (estrutura básica)

**Sprint 2 (Semana 3): Páginas Core**
- Página Metodologia
- Página Serviços
- Organisms principais

**Sprint 3 (Semana 4): Páginas Finais + Integrações**
- Página Clientes
- Página Contato + Firebase integration
- Google Analytics integration
- Animações e polish

**Sprint 4 (Semana 5): Testes e Deploy**
- QA completo (responsividade, funcionalidades)
- Performance optimization
- SEO final checks (meta tags, sitemap)
- Deploy em produção (thatix.io)

### Fase Pós-Lançamento (Contínua)
- Monitoramento de analytics
- Correção de bugs reportados
- Otimizações baseadas em dados
- Iterações de conteúdo

---

## 9. Orçamento

### Custos Mensais Recorrentes

| Item | Custo | Justificativa |
|------|-------|---------------|
| **Vercel Pro** | ~$20/mês | Hospedagem, analytics, custom domain |
| **Firebase** | $0-$25/mês | Free tier suficiente inicialmente, escala conforme uso |
| **Domínio thatix.io** | ~$15/ano | Registro de domínio |
| **Total Mensal** | ~$25-$45 | Custo operacional baixo |

### Custos de Desenvolvimento

- **Desenvolvimento Interno:** Já contabilizado no custo da equipe
- **Assets/Design:** Recursos internos (já disponíveis)
- **Ferramentas:** ESLint, Prettier (gratuitas)

**Total Investimento:** Principalmente tempo de equipe (4-5 semanas de esforço distribuído)

---

## 10. Comunicação

### Canais de Comunicação

- **Daily Standup:** Async (Slack) - updates diários
- **Sprint Planning:** Semanal (1h) - planejar próxima sprint
- **Sprint Review:** Semanal (30min) - demo do que foi feito
- **Retrospectiva:** Bi-semanal (30min) - melhorias de processo

### Reportes

- **Status Report:** Semanal (Sexta) - progresso, blockers, próximos passos
- **Métricas Pós-Launch:** Semanal (primeiras 4 semanas), depois mensal

### Ferramentas

- **Documentação:** Este repositório MetaSpecs
- **Gestão de Tarefas:** [A definir - Trello, Linear, GitHub Projects]
- **Comunicação:** Slack/WhatsApp
- **Code Review:** GitHub Pull Requests

---

## 11. Aprovações

### Aprovação de Fases

| Fase | Aprovador | Critério |
|------|-----------|----------|
| **Design/Wireframes** | Founders + PO | Alinhamento com brand, UX intuitiva |
| **Desenvolvimento (cada sprint)** | PO | Features funcionais conforme spec |
| **QA** | QA + PO | Zero bugs críticos, funcionalidades OK |
| **Deploy Produção** | Founders | Aprovação final, conteúdo revisado |

### Mudanças de Escopo

Qualquer mudança de escopo deve:
1. Ser documentada (issue/proposta)
2. Avaliada por PO (impacto, prioridade)
3. Aprovada por Founders (se impacto significativo)
4. Comunicada para toda equipe

---

## 12. Definição de Sucesso (90 Dias Pós-Launch)

**Sucesso Técnico:**
- ✅ Uptime > 99.9%
- ✅ Lighthouse Score > 90 mantido
- ✅ Zero bugs críticos não resolvidos
- ✅ Tempo de resposta médio < 1s

**Sucesso de Negócio:**
- ✅ 50+ leads gerados
- ✅ 5+ SQLs (clientes qualificados) do site
- ✅ 1+ cliente fechado originado do site
- ✅ Top 5 Google para "context-first development brasil"

**Sucesso de Usuário:**
- ✅ Bounce rate < 60%
- ✅ Tempo na página > 1:30min
- ✅ 3.000+ visitas mensais
- ✅ Feedback positivo de usuários/clientes

---

**Assinaturas de Aprovação:**

- [ ] **Founders Thatix** - Aprovação Estratégica
- [ ] **Product Owner** - Aprovação de Escopo
- [ ] **Tech Lead** - Aprovação Técnica

**Data de Aprovação:** _____________

---

**Este Project Charter é um documento vivo e pode ser atualizado conforme o projeto evolui. Mudanças significativas requerem aprovação dos stakeholders principais.**
