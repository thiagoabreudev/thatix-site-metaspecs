---
adr_number: "005"
title: "Hospedagem Vercel Pro"
date: "2026-01-13"
status: "accepted"
deciders: ["founders"]
consulted: ["tech-lead"]
informed: ["all-developers"]
supersedes: null
superseded_by: null
tags: ["architecture", "hosting", "vercel", "deployment"]
---

# ADR 005: Hospedagem Vercel Pro

**Status:** Aceito
**Data:** 2026-01-13
**Decisores:** Founders

---

## Contexto

Precisamos de hospedagem para site institucional com:
- Deploy automático (CI/CD)
- Custom domain (thatix.io)
- Performance global (CDN)
- SSL automático
- Analytics

---

## Decisão

**Vercel Pro** ($20/mês)

**Features Utilizadas:**
- Deploy automático via GitHub
- Custom domain thatix.io
- Edge Network (CDN global)
- Web Vitals Analytics
- Preview deployments (PRs)

---

## Justificativa

**Por que Vercel Pro?**

1. **Otimizado para Nuxt** - First-class support
2. **CI/CD Built-in** - Push → Deploy automático
3. **Performance** - Edge network, otimizações automáticas
4. **Analytics** - Web Vitals tracking incluso
5. **DX Excelente** - Interface intuitiva, logs claros
6. **Custo-Benefício** - $20/mês vs alternativas

---

## Alternativas Consideradas

### 1. Netlify
**Contras:** ❌ Menos otimizado para Nuxt que Vercel

### 2. AWS Amplify
**Contras:** ❌ Complexidade maior, custo variável

### 3. Cloudflare Pages
**Prós:** Free
**Contras:** ❌ Menos features, analytics limitado

---

## Consequências

**Positivas:**
- ✅ Deploy em < 2min
- ✅ SSL e domain management automático
- ✅ Preview environments para QA

**Negativas:**
- ⚠️ Custo mensal ($20) - justificado pelo valor

---

**Status:** ✅ ACEITO
