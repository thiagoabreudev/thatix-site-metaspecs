---
adr_number: "004"
title: "Firebase para Backend"
date: "2026-01-13"
status: "accepted"
deciders: ["founders", "tech-lead"]
consulted: []
informed: ["all-developers"]
supersedes: null
superseded_by: null
tags: ["architecture", "backend", "firebase", "database"]
---

# ADR 004: Firebase para Backend

**Status:** Aceito
**Data:** 2026-01-13
**Decisores:** Founders, Tech Lead

---

## Contexto

Site institucional precisa de funcionalidade backend para:
- Processar formulário de contato
- Armazenar submissões (opcional)
- Enviar notificações por email
- Possíveis expansões futuras (newsletter, downloads)

**Requisitos:**
- Setup rápido
- Escalável
- Custo controlado (free tier se possível)
- Confiável

---

## Decisão

Usar **Firebase** (Cloud Functions + Firestore) para backend.

**Escopo Inicial:**
- Cloud Function para processar formulário de contato
- Firebase Admin para enviar emails
- (Opcional) Firestore para armazenar submissões

---

## Justificativa

**Por que Firebase?**

1. **Simplicidade** - Setup em minutos, sem servidor para gerenciar
2. **Escalabilidade** - Auto-scale, serverless
3. **Free Tier Generoso** - 2M invocações/mês (suficiente para volume inicial)
4. **Integração Nuxt** - Módulos oficiais, DX excelente
5. **Ecosistema Completo** - Auth, Storage, Analytics (futuro)

---

## Alternativas Consideradas

### 1. Netlify Forms
**Contras:** ❌ Limitado a forms, sem flexibilidade

### 2. API própria (Node.js + Express)
**Contras:** ❌ Precisa gerenciar servidor, custo, complexidade

### 3. Formspree / SendGrid direto
**Contras:** ❌ Sem controle, vendor lock-in pior

---

## Implementação

```javascript
// Cloud Function exemplo
export const submitContact = functions.https.onCall(async (data) => {
  // Validação
  // Armazenar em Firestore
  // Enviar email
  return { success: true }
})
```

---

## Consequências

**Positivas:**
- ✅ Backend funcional em dias
- ✅ Custo zero inicial
- ✅ Escalável automaticamente

**Negativas:**
- ⚠️ Vendor lock-in Firebase (aceitável para MVP)
- ⚠️ Cold starts em Cloud Functions (< 1s, aceitável)

---

**Status:** ✅ ACEITO
