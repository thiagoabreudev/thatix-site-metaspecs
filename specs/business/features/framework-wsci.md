---
spec_version: "1.0.0"
valid_from: "2026-01-13"
last_updated: "2026-01-13"
status: "active"
priority: "high"
category: "feature"
tags: ["framework", "wsci", "context-engineering", "langchain"]
related_specs:
  - "framework-context.md"
  - "../PRODUCT_STRATEGY.md"
---

# Feature: Framework WSCI (LangChain)

**Versão:** 1.0
**Data:** 2026-01-13
**Tipo:** Context Engineering Methodology

---

## 1. Descrição

O **Framework WSCI** é uma metodologia de engenharia de contexto baseada no trabalho da LangChain, que agrupa estratégias para gerenciar contextos de forma eficiente em desenvolvimento com IA.

**WSCI** = **Write, Select, Compress, Isolate**

---

## 2. Os 4 Componentes

### Write: Salvar Contexto

**Propósito:** Escrever e salvar contexto fora da janela de contexto da IA

**Técnicas:**
- Memory systems (short-term, long-term)
- Vector databases para contexto semântico
- State management em agentes
- Checkpointing de conversas

**Quando usar:** Contexto que será relevante futuramente

**Benefício:** IA não precisa "lembrar" tudo na janela de contexto

---

### Select: Selecionar Contexto

**Propósito:** Puxar contexto relevante para a janela de contexto

**Técnicas:**
- RAG (Retrieval-Augmented Generation)
- Semantic search
- Filtering por metadata
- Hybrid search (keyword + semantic)

**Quando usar:** IA precisa de informação específica para task atual

**Benefício:** IA recebe apenas contexto relevante (não tudo)

---

### Compress: Comprimir Contexto

**Propósito:** Reter apenas tokens necessários

**Técnicas:**
- Summarization (resumir conversas longas)
- Trimming (remover partes menos relevantes)
- Abstraction (generalizar detalhes)
- Token optimization

**Quando usar:** Contexto é grande demais para janela disponível

**Benefício:** Maximiza uso de janela de contexto finita

---

### Isolate: Isolar Contexto

**Propósito:** Separar contextos para uso específico

**Técnicas:**
- Context partitioning (dividir em pedaços)
- Namespace separation
- Tool-specific contexts
- State isolation em multi-agent systems

**Quando usar:** Diferentes partes do sistema precisam de contextos diferentes

**Benefício:** Evita context pollution e melhora precisão

---

## 3. Integração com LangGraph

O WSCI é implementado nativamente em **LangGraph**, framework de orquestração low-level da LangChain:

- **Nodes:** Cada node pode aplicar estratégias WSCI
- **State:** Gerenciamento de contexto entre nodes
- **Edges:** Fluxo de contexto otimizado

**Thatix usa LangGraph:** Referência técnica e cases de uso

---

## 4. Aplicação Prática na Thatix

### Exemplo: Feature de Autenticação

**Write:**
- Salvar specs de segurança do projeto
- Documentar padrões de autenticação existentes
- Armazenar anti-patterns (o que NÃO fazer)

**Select:**
- Recuperar apenas specs de autenticação (não todo o projeto)
- Buscar exemplos similares no repositório
- Trazer requisitos de compliance relevantes

**Compress:**
- Resumir specs longas em bullets
- Abstrair detalhes de implementação antiga
- Focar em princípios, não código específico

**Isolate:**
- Contexto de autenticação separado de contexto de UI
- Security concerns isolados de performance concerns
- Frontend context vs backend context

**Resultado:** IA gera código de autenticação alinhado com padrões, seguro e consistente

---

## 5. Benefícios Mensuráveis

- **Redução de context poisoning:** > 60%
- **Precisão de código gerado:** > 40% melhor
- **Tokens economizados:** ~30-50% por interação
- **Consistência:** > 80% de código alinhado com padrões

---

## 6. Ferramentas e Implementação

**Stack Recomendada:**
- **LangChain / LangGraph:** Framework base
- **Vector DB:** Pinecone, Weaviate, Chroma (para Select)
- **Memory:** Redis, Postgres (para Write)
- **Observability:** LangSmith, Weights & Biases

**Thatix fornece:**
- Templates de implementação
- Exemplos de código
- Best practices documentadas

---

## 7. Diretrizes de Uso

**Use WSCI quando:**
- ✅ Projeto tem contexto grande (>100k tokens)
- ✅ Múltiplas features com contextos específicos
- ✅ Necessidade de precisão alta (fintech, health)
- ✅ Time quer escalar uso de IA

**Não use WSCI quando:**
- ❌ Projeto muito simples (< 10k tokens)
- ❌ Uso ocasional de IA (não vale complexidade)
- ❌ Time não tem maturidade técnica

---

**Última Atualização:** 2026-01-13
**Referência:** [LangChain Context Engineering](https://docs.langchain.com/context-engineering)
