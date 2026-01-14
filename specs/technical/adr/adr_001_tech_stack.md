---
adr_number: "001"
title: "Escolha do Stack Tecnológico"
date: "2026-01-13"
status: "accepted"
deciders: ["founders", "tech-lead"]
consulted: []
informed: ["all-developers"]
supersedes: null
superseded_by: null
tags: ["architecture", "stack", "vue", "nuxt", "tailwind", "firebase"]
spec_version: "1.0.0"
---

# ADR 001: Escolha do Stack Tecnológico

:::version_info
**Versão**: 1.0.0
**Data da Decisão**: 2026-01-13
**Status**: Aceito
:::

:::breaking_changes
**v1.0.0** (baseline):
- Primeira versão desta decisão arquitetural
- Stack escolhido: Vue 3 + Nuxt 4.2.2 + Tailwind CSS + Firebase
- Hospedagem: Vercel Pro
- Prioridades: Performance (LCP < 2.5s), Manutenibilidade, Produtividade
:::

**Status:** Aceito
**Data:** 2026-01-13
**Decisores:** Founders, Tech Lead
**Contexto Atualizado:** 2026-01-13

---

## Contexto

Precisamos definir a stack tecnológica para o desenvolvimento do site institucional da Thatix, priorizando:
1. **Performance** - LCP < 2.5s, SEO otimizado
2. **Manutenibilidade** - Código limpo, fácil de manter com equipe pequena
3. **Produtividade** - Desenvolvimento rápido (MVP em 4-5 semanas)
4. **Expertise da Equipe** - Aproveitar conhecimento existente

**Tipo de Projeto:** Site institucional com 5 páginas estáticas, formulário de contato, e foco em geração de leads.

---

## Decisão

Optamos pela seguinte stack:

### Frontend
- **Vue 3** (Composition API, `<script setup>`)
- **Nuxt 4** (SSG/SSR, file-based routing, auto-imports)
- **Tailwind CSS** (utility-first styling)
- **JavaScript ES6+** (sem TypeScript)

### Backend/Serviços
- **Firebase** (Cloud Functions, Firestore para formulário)
- **Google Analytics 4** (tracking e analytics)

### Hospedagem e Deploy
- **Vercel Pro** (hosting, CI/CD, analytics)
- **Domínio:** thatix.io

### Qualidade de Código
- **ESLint** (Vue + Nuxt recommended rules)
- **Prettier** (code formatting, integrado com ESLint)

---

## Justificativa

### Por que Vue 3 + Nuxt 4?

**Vue 3:**
- ✅ **Expertise da equipe** - Desenvolvedores já têm conhecimento em Vue
- ✅ **Composition API** - Código mais organizado e reutilizável
- ✅ **Performance** - Reactivity system otimizado, menor bundle size
- ✅ **Developer Experience** - Sintaxe intuitiva, curva de aprendizado suave
- ✅ **Ecossistema maduro** - Bibliotecas e ferramentas estáveis

**Nuxt 4:**
- ✅ **SSG/SSR out-of-the-box** - Performance e SEO otimizados automaticamente
- ✅ **File-based routing** - Convenção sobre configuração, rotas automáticas
- ✅ **Auto-imports** - Componentes e composables importados automaticamente
- ✅ **Server routes** - API routes integradas (útil para Firebase functions)
- ✅ **Otimizações built-in** - Code splitting, lazy loading, image optimization
- ✅ **SEO-friendly** - Meta tags, sitemap, robots.txt com plugins oficiais

**Nuxt 4 vs Nuxt 3:**
- Nuxt 4 é evolutivo (não breaking changes massivos)
- Melhorias de performance e DX
- Equipe prefere estar na versão mais recente e estável

### Por que Tailwind CSS?

- ✅ **Produtividade** - Desenvolvimento rápido sem escrever CSS custom
- ✅ **Consistência** - Design system baseado em utility classes
- ✅ **Performance** - PurgeCSS remove classes não usadas (bundle pequeno)
- ✅ **Customização** - Theme customizável (cores, espaçamentos, etc.)
- ✅ **Mobile-first** - Responsive design por padrão
- ✅ **Integração perfeita** - First-class support do Nuxt

### Por que Firebase?

- ✅ **Simplicidade** - Setup rápido, sem necessidade de backend completo
- ✅ **Escalabilidade** - Escala automaticamente conforme uso
- ✅ **Free tier generoso** - Suficiente para volume inicial
- ✅ **Cloud Functions** - Para processar formulário de contato
- ✅ **Firestore** - Armazenar submissões de formulário (opcional)
- ✅ **Segurança** - Regras de segurança robustas

### Por que Vercel Pro?

- ✅ **Otimizado para frameworks modernos** - Suporte de primeira classe para Nuxt
- ✅ **Deploy automático** - CI/CD integrado com GitHub
- ✅ **Edge Network** - Performance global
- ✅ **Analytics integrado** - Web Vitals tracking
- ✅ **Custom domain** - thatix.io com SSL automático
- ✅ **Preview deployments** - Review de PRs com URL temporária
- ✅ **Custo-benefício** - $20/mês vs alternativas

### Por que JavaScript (sem TypeScript)?

- ✅ **Expertise da equipe** - Time confortável com JavaScript
- ✅ **Velocidade de desenvolvimento** - Menos overhead de types
- ✅ **Projeto pequeno** - 5 páginas, baixa complexidade
- ✅ **ESLint compensa** - Linting rigoroso detecta erros comuns

**Nota:** TypeScript pode ser adicionado no futuro se projeto crescer significativamente.

---

## Alternativas Consideradas

### Alternativa 1: React + Next.js

**Prós:**
- Ecossistema maior
- Mais recursos de aprendizado
- Vercel é feito pela equipe do Next.js

**Contras:**
- ❌ **Equipe não tem expertise em React**
- ❌ Curva de aprendizado maior
- ❌ Setup mais complexo (comparado a Nuxt)

**Decisão:** Rejeitado por falta de expertise

---

### Alternativa 2: Vue 3 + Vite (sem Nuxt)

**Prós:**
- Mais controle e flexibilidade
- Bundle menor (sem framework overhead)
- Setup simples

**Contras:**
- ❌ Sem SSR/SSG out-of-the-box (precisa configurar manualmente)
- ❌ Sem file-based routing (precisa vue-router manual)
- ❌ SEO mais trabalhoso
- ❌ Menos convenções (mais decisões a tomar)

**Decisão:** Rejeitado - Nuxt fornece features essenciais (SSG, routing) com zero config

---

### Alternativa 3: Astro + Vue Islands

**Prós:**
- Performance excepcional (MPA, zero JS por padrão)
- Vue islands para interatividade
- Ótimo para sites estáticos

**Contras:**
- ❌ Equipe não tem experiência com Astro
- ❌ Ecossistema menor
- ❌ Overkill para projeto que precisa de interatividade

**Decisão:** Rejeitado - Learning curve não justifica para MVP

---

### Alternativa 4: Gatsby + React

**Prós:**
- SSG performático
- Plugin ecosystem rico

**Contras:**
- ❌ Mesmos problemas de React (falta de expertise)
- ❌ Build times lentos em projetos maiores
- ❌ Menos popular que Next.js (comunidade menor)

**Decisão:** Rejeitado

---

## Consequências

### Positivas

- ✅ **Desenvolvimento rápido** - Equipe produtiva desde dia 1
- ✅ **Performance garantida** - SSG/SSR + Vercel = LCP < 2.5s facilmente
- ✅ **SEO otimizado** - Nuxt cuida de meta tags, sitemap, etc.
- ✅ **Escalabilidade** - Stack suporta crescimento futuro (blog, portal, etc.)
- ✅ **Custo controlado** - ~$25-45/mês operacional
- ✅ **Developer Experience** - Nuxt 4 + Tailwind = DX excelente

### Negativas (Trade-offs Aceitos)

- ⚠️ **Sem TypeScript** - Menos type safety (mitigado com ESLint rigoroso)
- ⚠️ **Firebase vendor lock-in** - Migrar backend seria trabalhoso (baixo risco para MVP)
- ⚠️ **Vercel Pro custo** - $20/mês vs alternativas free (justificado pelo valor)
- ⚠️ **Nuxt 4 early adoption** - Possível instabilidade (mitigado: equipe monitora issues)

### Riscos Identificados

1. **Nuxt 4 ainda não 100% estável**
   - *Mitigação:* Avaliar estabilidade antes de começar, fallback para Nuxt 3 se necessário

2. **Performance pode não atingir targets**
   - *Mitigação:* Lazy loading, code splitting, image optimization desde início

3. **Curva de aprendizado Nuxt 4 (features novas)**
   - *Mitigação:* Documentação oficial, comunidade ativa, tempo de onboarding

---

## Validação

### Como Validar Esta Decisão

**Após 1 Sprint:**
- ✅ Setup do projeto concluído sem blockers
- ✅ Primeiros componentes criados produtivamente
- ✅ Build e deploy funcionando

**Após 2 Sprints:**
- ✅ Páginas renderizando com SSG
- ✅ Performance: Lighthouse > 80
- ✅ Equipe confortável com stack

**Após MVP (4-5 semanas):**
- ✅ Site em produção com LCP < 2.5s
- ✅ SEO: Indexado no Google
- ✅ Zero bugs críticos relacionados ao stack

**Critérios de Falha (Gatilhos para Revisão):**
- ❌ Performance consistentemente abaixo de targets
- ❌ Bugs críticos não resolúveis no framework
- ❌ Equipe extremamente improdutiva
- ❌ Custo operacional explodindo

---

## Referências

- [Nuxt 4 Documentation](https://nuxt.com)
- [Vue 3 Docs](https://vuejs.org)
- [Tailwind CSS](https://tailwindcss.com)
- [Firebase Docs](https://firebase.google.com/docs)
- [Vercel Docs](https://vercel.com/docs)

---

## Histórico de Revisões

| Data | Versão | Mudança | Autor |
|------|--------|---------|-------|
| 2026-01-13 | 1.0 | ADR inicial | Tech Lead |
| 2026-01-13 | 1.1 | Corrigido para Nuxt 4 (estava Next.js) | Tech Lead |

---

**Status Final:** ✅ ACEITO - Stack definido e validado por equipe
