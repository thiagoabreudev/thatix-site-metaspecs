---
spec_version: "1.0.0"
valid_from: "2026-01-13"
last_updated: "2026-01-13"
status: "active"
priority: "high"
category: "feature"
tags: ["workshop", "training", "core-product", "flagship", "context-first"]
related_specs:
  - "../PRODUCT_STRATEGY.md"
  - "../CUSTOMER_JOURNEY.md"
  - "../SALES_PROCESS.md"
---

# Feature: Workshop Imersivo Context-First

:::version_info
**Versão**: 1.0.0
**Válida desde**: 2026-01-13
**Status**: Ativa
**Prioridade**: Alta
:::

:::breaking_changes
**v1.0.0** (baseline):
- Primeira versão versionada desta feature
- Define workshop de 2 dias (60% prática, 40% teoria)
- Estrutura: Dia 1 (Framework CONTEXT + Specify), Dia 2 (WSCI + Plan/Implement/Adopt)
- Precificação: R$ 2.300/pessoa, mínimo 3 pessoas
- Inclui MetaSpec Starter Kit + 2 semanas de suporte
:::

**Versão:** 1.0
**Data:** 2026-01-13
**Tipo:** Core Product / Flagship

---

## 1. Descrição e Propósito

### Visão Geral

O **Workshop Imersivo Context-First** é o principal produto da Thatix: um treinamento prático de 2 dias onde times de desenvolvimento aprendem e aplicam a metodologia Context-First Development em projetos reais.

### Propósito

Transformar times que usam IA de forma ad-hoc (vibe coding) em times que aplicam engenharia estruturada com Context Engineering, gerando ganhos mensuráveis de produtividade mantendo alta qualidade.

### Diferencial

- **60% prática hands-on** (não é palestra teórica)
- **Projeto real do cliente** (não exemplos genéricos)
- **Resultados imediatos** (aplicável no dia seguinte)
- **2 semanas de suporte incluso** (não te deixa sozinho)

---

## 2. Benefícios para o Cliente

### Benefícios Imediatos (Semana 1-2)

- ✅ Time compreende problemas do vibe coding (context poisoning, débito técnico)
- ✅ Conhece frameworks CONTEXT e WSCI
- ✅ Cria primeiras especificações executáveis do próprio projeto
- ✅ Recebe MetaSpec Starter Kit pronto para uso

### Benefícios de Curto Prazo (Mês 1-2)

- ✅ Código gerado com IA é mais consistente e testável
- ✅ Code reviews mais rápidos (menos inconsistências)
- ✅ Menos bugs sutis chegando em produção
- ✅ Estimativas de sprint mais previsíveis

### Benefícios de Médio Prazo (Mês 3-6)

- ✅ **Ganho médio de 73% de produtividade** (comprovado)
- ✅ Redução significativa de débito técnico
- ✅ Time alinhado em metodologia comum
- ✅ Processo escalável para novos membros

---

## 3. Público-Alvo e Participantes

### Perfil Ideal de Participantes

**Quem DEVE participar:**
- CTOs, VPs de Engenharia (visão estratégica)
- Tech Leads, Engineering Managers (implementação)
- Desenvolvedores Senior/Staff (execução hands-on)

**Tamanho Ideal:** 8-10 pessoas

**Tamanho Mínimo:** 3 pessoas (viabilidade econômica)

**Tamanho Máximo:** 12 pessoas (qualidade da experiência)

### Pré-requisitos

**Técnicos:**
- ✅ Time já usa IA em desenvolvimento (Copilot, ChatGPT, Claude)
- ✅ Produto em produção ou estágio avançado
- ✅ Repositório de código existente

**Organizacionais:**
- ✅ Liderança técnica comprometida (presença do CTO/VP)
- ✅ Disponibilidade total de 2 dias (sem interrupções)
- ✅ Projeto real para aplicar a metodologia

**Maturidade:**
- Mínimo: Time sabe git, CI/CD básico, testes unitários
- Ideal: Time já tem práticas de code review e documentação

---

## 4. Estrutura e Conteúdo

### Dia 1: Fundamentos e Context Architecture

#### **Manhã (09:00-12:30) - 40% Teoria**

**Módulo 1: Por que Context-First? (60min)**
- Estatística: 76% dos projetos com IA falham
- Problemas do vibe coding: context poisoning, débito técnico
- Case real: Embedda Labs (R$ 3bi em crédito)
- ROI comprovado: 73% ganho de produtividade

**Módulo 2: Framework CONTEXT (90min)**
- **C**ontext Architecture: Design de informação para IA
- **O**bservability-Driven: Instrumentação e rastreamento
- **N**ormative Specifications: Specs executáveis com anti-patterns
- **T**est-First AI Development: TDD adaptado para IA
- **E**volutionary Refinement: Evolução contínua
- **X**plainability & Governance: Explicabilidade e controle
- Trustworthy Deployment: Deploy confiável

**Coffee Break (30min)**

---

#### **Tarde (14:00-18:00) - 60% Prática**

**Módulo 3: Fase SPECIFY (2h hands-on)**
- Como transformar requisitos ambíguos em especificações executáveis
- Técnicas de elicitação de contexto
- Anti-patterns e guardrails
- **Exercício:** Participantes criam specs do próprio projeto

**Módulo 4: Framework WSCI Parte 1 (1.5h)**
- **Write:** Salvar contexto eficientemente
- **Select:** RAG e retrieval strategies
- **Exercício:** Estruturar contexto de projeto real

**Wrap-up Dia 1 (30min)**
- Review do que foi construído
- Homework: Refinar specs criadas

---

### Dia 2: Implementação e Escalabilidade

#### **Manhã (09:00-12:30) - Prática Intensiva**

**Módulo 5: Framework WSCI Parte 2 (90min)**
- **Compress:** Summarização e trimming de contexto
- **Isolate:** Separação e organização de contextos
- **Exercício:** Otimizar contextos criados no Dia 1

**Módulo 6: Fase PLAN (60min)**
- Arquitetura de contextos para features complexas
- Estratégias de decomposição
- **Exercício:** Planejar feature real usando Context-First

**Coffee Break (30min)**

---

#### **Tarde (14:00-18:00) - Implementação e Adoção**

**Módulo 7: Fase TASKS & IMPLEMENT (90min)**
- Desenvolvimento orientado por specs
- Code review de código gerado
- Test-First AI Development na prática
- **Exercício:** Implementar feature planejada (pair programming)

**Módulo 8: Fase ADOPT - Escalabilidade (60min)**
- Como escalar metodologia para todo o time
- Train-the-trainer interno
- Integração com workflow existente
- Métricas de sucesso e acompanhamento

**Módulo 9: Plano 30-60-90 Dias (30min)**
- Plano customizado para o cliente
- Próximos passos e milestones
- Como aproveitar suporte pós-workshop

**Encerramento e Q&A (30min)**

---

## 5. Entregáveis

### Durante o Workshop

- ✅ **Especificações criadas** do projeto real do cliente
- ✅ **Contextos estruturados** usando Framework WSCI
- ✅ **Feature implementada** com metodologia Context-First

### Pós-Workshop

- ✅ **MetaSpec Starter Kit:**
  - Templates de especificações
  - Exemplos de contextos
  - Checklists de qualidade
  - Guias de implementação
  - Scripts e ferramentas
- ✅ **Plano 30-60-90 Dias** customizado
- ✅ **Acesso a repositório** de exemplos e recursos
- ✅ **2 semanas de suporte** via Slack/WhatsApp

---

## 6. Modalidades de Entrega

### Presencial

**Vantagens:**
- Engajamento máximo
- Pair programming facilitado
- Networking e team building

**Logística:**
- Local: Escritório do cliente ou espaço da Thatix
- Equipamentos: Projetor, flip charts, Wi-Fi robusto
- Alimentação: Coffee breaks e almoço inclusos

---

### Remoto (Zoom/Google Meet)

**Vantagens:**
- Sem custo de deslocamento
- Flexibilidade geográfica
- Gravação das sessões

**Logística:**
- Plataforma: Zoom com breakout rooms
- Ferramentas: Miro/FigJam para colaboração
- Câmeras ON obrigatório (engajamento)

---

### Híbrido

**Quando usar:**
- Time distribuído geograficamente
- Parte presencial, parte remoto

**Desafio:** Garantir experiência equivalente para ambos

---

## 7. Precificação e Modelo Comercial

### Estrutura de Preços

**Base:** R$ 2.300 por pessoa

**Incluso:**
- 2 dias de workshop
- MetaSpec Starter Kit
- 2 semanas de suporte
- Plano 30-60-90 dias
- Material digital (slides, guias)

**Exemplos:**
- 3 pessoas (mínimo): R$ 6.900
- 8 pessoas (ideal): R$ 18.400
- 10 pessoas: R$ 23.000

### Opções de Customização (Add-ons)

**Suporte Estendido:**
- +R$ 5.000: 1 mês adicional de suporte
- +R$ 12.000: 3 meses de suporte (check-ins semanais)

**Sessões Adicionais:**
- +R$ 3.000: Sessão de follow-up (4h) em 30 dias

**On-site (se aplicável):**
- +Custo de deslocamento e hospedagem

---

## 8. Padrões de Uso

### Caso de Uso 1: Startup Adotando IA Estruturadamente

**Contexto:**
- Startup Series A, 15 desenvolvedores
- Usando Copilot há 6 meses, resultados caóticos
- CTO quer estruturar antes de escalar time

**Aplicação:**
- Workshop com 8 pessoas (CTO + 2 Tech Leads + 5 Seniors)
- Foco em estabelecer processo desde o início
- Resultado: Metodologia embedding in cultura desde cedo

---

### Caso de Uso 2: Fintech Refatorando Sistema Crítico

**Contexto:**
- Fintech estabelecida, 40 desenvolvedores
- Sistema legado precisa refatoração urgente
- Compliance crítico, zero margem para erro

**Aplicação:**
- Workshop com 10 pessoas (squad dedicado à refatoração)
- Foco intenso em specs normativas e governança
- Consultoria adicional pós-workshop
- Resultado: Refatoração 73% mais rápida mantendo qualidade

---

### Caso de Uso 3: Scale-up Escalando Time

**Contexto:**
- Scale-up Series B, crescendo de 20 para 50 devs
- Quer onboard novos devs com metodologia estruturada

**Aplicação:**
- Workshop inicial com time atual (12 pessoas)
- Workshops subsequentes para novas ondas de contratação
- Train-the-trainer para Tech Leads internalizarem
- Resultado: Onboarding consistente e escalável

---

## 9. Métricas de Sucesso

### Métricas Imediatas (Pós-Workshop)

- **NPS:** > 70 (target)
- **Completion Rate:** > 95%
- **Compreensão da Metodologia:** > 90% (quiz pós-workshop)

### Métricas de Curto Prazo (30 dias)

- **Adoption Rate:** > 80% aplicando metodologia
- **Especificações Criadas:** Média de 5+ specs por time
- **Suporte Utilizado:** > 70% dos clientes usam suporte incluso

### Métricas de Médio Prazo (60-90 dias)

- **Ganho de Produtividade:** > 50% (target 73%)
- **Redução de Code Review Time:** > 30%
- **Redução de Bugs:** > 25%
- **Satisfação do Cliente:** > 4.5/5

---

## 10. Problemas Comuns e Soluções

### Problema: Baixo Engajamento Durante Workshop

**Sintomas:**
- Participantes dispersos, no celular
- Exercícios não são concluídos
- Perguntas superficiais

**Causas:**
- Conteúdo não ressoa (muito teórico)
- Participantes errados (devs junior sem contexto)
- Interrupções externas (emergências do dia a dia)

**Soluções:**
- Reforçar pré-requisitos de participantes
- Garantir "zona de silêncio" (sem interrupções)
- Mais hands-on, menos slides
- Usar projeto REAL do cliente (não exemplo genérico)

---

### Problema: Time Não Aplica Metodologia Pós-Workshop

**Sintomas:**
- Suporte incluso não é utilizado
- Após 30 dias, voltaram ao vibe coding
- NPS positivo, mas sem adoção real

**Causas:**
- Falta de champion interno
- Gap entre entender e executar
- Resistência de alguns desenvolvedores
- Ferramentas não integradas ao workflow

**Soluções:**
- Identificar e empoderar champion durante workshop
- Check-in proativo em 1 semana (não esperar cliente pedir ajuda)
- Sessão de follow-up em 30 dias (inclusa ou add-on)
- Facilitar integração com ferramentas existentes

---

### Problema: Expectativas Desalinhadas com Resultados

**Sintomas:**
- Cliente esperava resultados em dias, não semanas
- Frustração com curva de aprendizado
- Questionamento de ROI

**Causas:**
- Expectativas não alinhadas na venda
- Cliente não investe tempo necessário
- Contexto da empresa não é favorável (muito caos)

**Soluções:**
- Alinhar expectativas claramente na discovery call
- Reforçar que resultados levam 2-4 semanas
- Definir métricas específicas desde o início
- Qualificar melhor clientes (não aceitar qualquer um)

---

## 11. Roadmap de Evolução

### V1.0 (Atual - 2026)

- Workshop presencial/remoto de 2 dias
- MetaSpec Starter Kit básico
- 2 semanas de suporte

### V1.5 (Q2 2026)

- Melhorias no conteúdo baseadas em feedback
- MetaSpec Starter Kit expandido
- Gravações e materiais complementares

### V2.0 (Q4 2026)

- Certificação opcional pós-workshop
- Acesso a comunidade privada de clientes
- Plataforma digital para acompanhamento

### V3.0 (2027)

- Workshop modular (possibilidade de fazer módulos separados)
- Train-the-trainer program (cliente pode treinar internamente)
- Integração com ferramentas Context Engineering da Thatix

---

## 12. Diretrizes de Interação com IA

### Para Sistemas de IA Vendendo o Workshop:

**Enfatizar:**
- ✅ **Prática hands-on** (60%, não palestra)
- ✅ **Resultados comprovados** (73% produtividade)
- ✅ **Projeto real** do cliente (não exemplo genérico)
- ✅ **Suporte incluso** (2 semanas)

**Tratar Objeções:**
- **"É caro":** Calcular ROI (1 dev x 73% produtividade = quanto?)
- **"Não temos tempo":** Apenas 2 dias + ROI em semanas
- **"Já usamos Copilot":** Workshop é COMO usar Copilot profissionalmente
- **"Time pequeno":** Justamente! Cada dev precisa ser super produtivo

**Quando Escalar para Humano:**
- Customização de conteúdo
- Negociação de preço para múltiplos workshops
- Cliente com contexto muito específico
- Dúvidas sobre viabilidade técnica

---

**Última Atualização:** 2026-01-13
**Responsável:** Equipe Thatix
**Próxima Revisão:** Após cada batch de 5 workshops
