---
spec_version: "1.0.0"
valid_from: "2026-01-13"
last_updated: "2026-01-13"
supersedes: null
status: "active"
category: "business"
tags: ["customer-journey", "sales-funnel", "onboarding", "retention", "advocacy"]
related_specs:
  - "CUSTOMER_PERSONAS.md"
  - "SALES_PROCESS.md"
  - "PRODUCT_STRATEGY.md"
---

# Jornada do Cliente - Thatix

:::version_info
**Versão**: 1.0.0
**Válida desde**: 2026-01-13
**Status**: Ativa
:::

:::breaking_changes
**v1.0.0** (baseline):
- Primeira versão versionada desta spec
- Define 6 fases: Awareness, Consideration, Adoption, Growth, Advocacy, Churn
- Estabelece duração média: 3-6 semanas (Awareness → Customer)
- Inclui objeções comuns e tratamentos, touchpoints e métricas por fase
:::

**Versão:** 1.0
**Data:** 2026-01-13

---

## Visão Geral

Este documento mapeia o ciclo de vida completo do cliente Thatix, desde o primeiro contato até a advocacia ou churn. A jornada é baseada em padrões observados em clientes atuais e estratégia de aquisição inbound.

**Duração Média do Ciclo (Awareness → Customer):** 3-6 semanas
**Taxa de Conversão Típica:** [A MEDIR]
**Ciclo de Vida do Cliente:** Recorrente (projetos múltiplos ou workshop → desenvolvimento)

---

## Fase 1: Consciência (Awareness)

### Gatilhos de Entrada

**Dores que levam o cliente a buscar solução:**
1. **Débito Técnico Crescente:** "Nosso código com IA está ficando insustentável"
2. **Incidentes em Produção:** Bugs sutis causados por código gerado sem estrutura
3. **Baixa Previsibilidade:** Estimativas de sprint não batem mais (IA acelerou, mas trouxe caos)
4. **Pressão por IA:** Board/investidores querem adoção de IA, mas sem estrutura
5. **Comparação Competitiva:** Concorrentes usando IA de forma mais eficaz

**Momento de Consciência:**
> "Preciso de uma metodologia estruturada para usar IA em desenvolvimento. O vibe coding não está funcionando."

### Canais de Descoberta

**Primários (Inbound):**
- **LinkedIn:** Artigos sobre Context-First, posts técnicos, cases de sucesso
- **Indicações:** Founders e CTOs em comunidades técnicas
- **Google Search:** Termos como "metodologia desenvolvimento IA", "context engineering", "evitar débito técnico IA"
- **Conteúdo Técnico:** Blog posts, whitepapers, webinars

**Secundários:**
- Participação em eventos de tecnologia
- Podcasts de engenharia
- Comunidades técnicas (Discord, Slack groups)
- GitHub (repos públicos com exemplos)

### Ações do Cliente Nesta Fase

- Consome conteúdo educativo (artigos, vídeos)
- Pesquisa sobre "Context-First Development"
- Lê cases e depoimentos
- Compara abordagens diferentes (Thatix vs Copilot puro vs nada)

### Objetivos da Thatix Nesta Fase

**Educar o mercado:**
- Criar consciência sobre "context poisoning" e riscos do vibe coding
- Posicionar Context-First como solução
- Demonstrar autoridade técnica
- Gerar leads qualificados

**Conteúdo Estratégico:**
- "76% dos projetos com IA falham: veja por quê"
- "O custo oculto do vibe coding"
- "Context Engineering: a disciplina que faltava"
- Cases com números reais (73% produtividade)

### Critérios de Sucesso (Transição para Próxima Fase)

Cliente reconhece que:
- ✅ Tem um problema (IA sem estrutura está gerando problemas)
- ✅ O problema é sério e precisa ser resolvido
- ✅ Existe uma solução (metodologia estruturada)
- ✅ Thatix pode ser a fornecedora dessa solução

---

## Fase 2: Avaliação (Consideration)

### Gatilhos de Entrada

Cliente já está consciente do problema e busca ativamente soluções.

**Ações que indicam entrada nesta fase:**
- Visita o site iadojeitocerto.com.br
- Baixa material educativo (whitepaper, guia)
- Preenche formulário de contato
- Envia email ou LinkedIn message
- Agenda call de discovery

### Atividades de Avaliação

**Primeira Interação (Call de Discovery - 30-45min):**
- Time Thatix entende contexto do cliente:
  - Tamanho do time
  - Problemas específicos que estão enfrentando
  - Estágio de adoção de IA
  - Orçamento disponível
  - Urgência da solução
- Cliente entende a metodologia:
  - Diferença entre Context-First e uso ad-hoc de IA
  - Como o Workshop funciona
  - Casos de sucesso semelhantes
  - Próximos passos

**Análise de Fit:**

Cliente avalia:
- ✅ A metodologia faz sentido tecnicamente?
- ✅ Resolve nossos problemas específicos?
- ✅ O investimento é justificável?
- ✅ Conseguimos implementar com nosso time atual?
- ✅ Thatix tem credibilidade (cases, expertise)?

Thatix avalia:
- ✅ Cliente tem problema que a metodologia resolve?
- ✅ Time tem maturidade mínima para adotar?
- ✅ Há fit de budget?
- ✅ Stakeholders estão alinhados?

### Objeções Comuns Nesta Fase

**1. Preço (Principal objeção)**

**Manifestação:** "R$ 2.300/pessoa está fora do nosso budget"

**Tratamento:**
- Calcular ROI: 73% ganho de produtividade = quanto em salários?
- Mostrar custo de NÃO fazer: débito técnico, retrabalho, bugs em produção
- Oferecer comparação: contratar mais um dev vs tornar time atual 73% mais produtivo
- Flexibilizar: pode começar com grupo piloto (3-5 pessoas)

**2. Falta de Conhecimento**

**Manifestação:** "Não entendo como isso é diferente de usar ChatGPT/Copilot"

**Tratamento:**
- Explicar analogia: "Copilot é como ter uma ferramenta poderosa; Context-First é o manual de como usar essa ferramenta de forma profissional"
- Demonstrar problemas do uso ad-hoc (context poisoning, inconsistência)
- Mostrar Framework CONTEXT e WSCI
- Oferecer conteúdo técnico detalhado

**3. Timing**

**Manifestação:** "Estamos muito ocupados agora, talvez no próximo trimestre"

**Tratamento:**
- Mostrar que problema só piora (débito técnico é juros compostos)
- Evidenciar que workshop é 2 dias + 2 semanas de suporte
- ROI começa a aparecer em semanas, não meses
- Agendar para data futura (garantir slot)

**4. Validação Interna**

**Manifestação:** "Preciso validar com o time / board / CFO"

**Tratamento:**
- Fornecer material para apresentação interna (deck, one-pager)
- Oferecer call com stakeholders adicionais
- Compartilhar cases e referências
- Propor projeto piloto de menor escopo

### Materiais de Suporte

**Fornecidos pela Thatix:**
- Proposta comercial detalhada
- Case studies com números
- Deck de apresentação para board
- Referências de clientes (sob solicitação)
- Cronograma de implementação
- Plano 30-60-90 dias

### Duração Típica Desta Fase

- **Startups (Founder decide):** 1-2 semanas
- **Empresas médias/grandes (CTO + validação):** 2-4 semanas

### Critérios de Sucesso (Transição para Próxima Fase)

Cliente está pronto para avançar quando:
- ✅ Validou tecnicamente que a solução resolve o problema
- ✅ Obteve aprovação de budget (ou está confiante que terá)
- ✅ Stakeholders-chave estão alinhados
- ✅ Agenda e próximos passos estão claros
- ✅ Confia na Thatix (credibilidade, expertise, cases)

**Ação de Conversão:** Assinatura de contrato + agendamento de Workshop

---

## Fase 3: Adoção (Onboarding)

### Gatilhos de Entrada

Contrato assinado, pagamento confirmado, data de Workshop agendada.

### Milestone 1: Preparação Pré-Workshop (1 semana antes)

**Responsabilidades do Cliente:**
- Selecionar participantes (CTOs, Tech Leads, Seniors - máx 8-10 pessoas)
- Preparar contexto do projeto:
  - Repositório de código (acesso)
  - Documentação existente
  - Desafios técnicos atuais
  - Objetivos do workshop
- Garantir disponibilidade total dos participantes (2 dias completos)

**Responsabilidades da Thatix:**
- Enviar guia de preparação
- Agendar kickoff call (30min)
- Preparar ambiente e materiais
- Customizar exemplos com contexto do cliente

### Milestone 2: Workshop Imersivo (2 dias)

**Estrutura do Workshop:**

**Dia 1: Fundamentos e Contexto**
- **Manhã (40% teoria):**
  - Por que 76% dos projetos com IA falham
  - Introdução ao Framework CONTEXT (7 pilares)
  - Framework WSCI (Write, Select, Compress, Isolate)
  - Context Architecture na prática
- **Tarde (60% prática):**
  - Fase 1: **Specify** - Transformar requisitos em specs executáveis
  - Exercício hands-on com projeto real do cliente
  - Criar especificações normativas

**Dia 2: Implementação e Adoção**
- **Manhã (prática):**
  - Fase 2: **Plan** - Arquitetura de contextos
  - Fase 3: **Tasks & Implement** - Desenvolvimento orientado por specs
  - Code review de código gerado com metodologia
- **Tarde (prática + estratégia):**
  - Fase 4: **Adopt** - Estratégia de escalabilidade
  - Entrega de **MetaSpec Starter Kit**
  - Plano 30-60-90 dias customizado
  - Q&A e próximos passos

**Entregáveis do Workshop:**
- ✅ Especificações criadas para caso real do cliente
- ✅ MetaSpec Starter Kit (templates, ferramentas, guias)
- ✅ Plano 30-60-90 dias de implementação
- ✅ Acesso a 2 semanas de suporte pós-workshop

### Milestone 3: Implementação Inicial (2 semanas - Suporte Incluso)

**Semana 1-2 Pós-Workshop:**
- Cliente começa a aplicar metodologia em projeto real
- Time Thatix disponível para:
  - Dúvidas de implementação
  - Revisão de especificações criadas
  - Ajustes de processo
  - Troubleshooting
- Comunicação via Slack/WhatsApp (SLA: resposta em 24h)

**Eventos de Sucesso:**
- ✅ Primeira feature entregue com metodologia
- ✅ Time segue os processos sem necessidade de consulta constante
- ✅ Code review mais rápidos (código mais consistente)
- ✅ Feedback positivo do time sobre a metodologia

**Sinais de Alerta:**
- ⚠️ Time não está seguindo as specs
- ⚠️ Dúvidas recorrentes (pode indicar gap de compreensão)
- ⚠️ Resistência de alguns desenvolvedores
- ⚠️ Falta de uso do MetaSpec Starter Kit

**Ações da Thatix em Sinais de Alerta:**
- Call de check-in para entender blockers
- Sessão de pair programming (se necessário)
- Materiais de reforço específicos
- Ajuste de processo para realidade do time

### Duração Típica Desta Fase

**Onboarding total:** 2 dias (workshop) + 2 semanas (implementação com suporte) = ~3 semanas

### Critérios de Sucesso (Transição para Próxima Fase)

Cliente está "onboarded" quando:
- ✅ Time compreendeu e internalizou a metodologia
- ✅ Primeiras features foram entregues com Context-First
- ✅ Processo está integrado no workflow (não é "extra")
- ✅ Ganhos iniciais são perceptíveis (velocidade, qualidade)
- ✅ Cliente não precisa mais de suporte constante

---

## Fase 4: Crescimento (Growth)

### Gatilhos de Entrada

Cliente está usando a metodologia de forma autônoma e colhendo resultados.

### Padrões de Crescimento

**Expansão Horizontal (dentro da empresa):**
- Metodologia adotada por 1 squad → expande para outros times
- Novos membros do time são treinados internamente
- Outras áreas da empresa (produto, QA) adotam Context-First

**Expansão Vertical (profundidade de uso):**
- Uso básico → uso avançado dos frameworks
- Customização de MetaSpecs para contexto da empresa
- Criação de specs reutilizáveis e bibliotecas internas

**Novos Projetos:**
- Cliente retorna para consultoria em projeto específico
- Contratação de desenvolvimento full com metodologia Thatix
- Workshops adicionais para novos times

### Oportunidades de Upsell/Cross-sell

**1. Consultoria de Arquitetura (projeto específico)**
- Cliente tem projeto complexo e quer Thatix acompanhando
- Típico: refatoração crítica, nova arquitetura, integração complexa
- Formato: Consultoria por sprint ou projeto fechado

**2. Desenvolvimento Full com Context-First**
- Cliente quer Thatix desenvolvendo features com metodologia
- Time Thatix aumenta temporariamente a capacidade do cliente
- Modelo: Time as a Service ou projeto fechado

**3. Workshop para Novos Times**
- Empresa cresceu, contratou novos desenvolvedores
- Novos squads precisam de treinamento
- Repetição do workshop imersivo

**4. Ferramentas e Produtos (futuro)**
- Quando Thatix lançar plataforma/ferramenta
- Migração de cliente de consultoria para produto SaaS

### Indicadores de Saúde do Cliente

**Sinais Positivos (Health Score Alto):**
- ✅ Usa metodologia consistentemente
- ✅ Compartilha resultados e casos internos
- ✅ Evangeliza Context-First internamente
- ✅ Recomenda Thatix para outras empresas
- ✅ Retorna para novos projetos/workshops
- ✅ Responde pesquisas de NPS com 9-10

**Sinais de Alerta (Health Score Baixo):**
- ⚠️ Não responde comunicações de check-in
- ⚠️ Não usa mais a metodologia (voltou ao vibe coding)
- ⚠️ Feedback negativo ou neutro em pesquisas
- ⚠️ Não renova projetos ou não contrata novos serviços
- ⚠️ Rotatividade alta no time (perdeu pessoas treinadas)

### Touchpoints com Cliente Nesta Fase

**Proativo (Thatix inicia):**
- Email de check-in em 30-60-90 dias pós-workshop
- Compartilhamento de novos conteúdos, features, cases
- Pesquisa de NPS e feedback
- Convites para eventos, webinars, comunidade

**Reativo (Cliente inicia):**
- Solicitações de consultoria adicional
- Dúvidas pontuais (fora do período de suporte)
- Pedidos de referência e indicações
- Feedback espontâneo e sugestões

### Duração Típica Desta Fase

**Indeterminada** - Cliente maduro que continua usando a metodologia e pode gerar receita recorrente via novos projetos.

### Critérios de Sucesso (Manutenção Nesta Fase)

- Cliente continua usando e obtendo valor
- Relacionamento forte e comunicação ativa
- Oportunidades de expansão identificadas e cultivadas
- NPS alto (9-10)

---

## Fase 5: Advocacia (Advocacy)

### Gatilhos de Entrada

Cliente teve tanto sucesso que se torna promotor ativo da Thatix.

### Comportamentos de Advocacia

**Advocacia Passiva:**
- Responde pesquisas de satisfação com notas altas
- Aceita ser case study público
- Permite que Thatix use seu logo como cliente
- Fornece depoimento escrito ou em vídeo

**Advocacia Ativa:**
- Indica Thatix proativamente para outras empresas
- Compartilha conteúdo da Thatix no LinkedIn
- Participa de webinars como convidado
- Escreve artigos sobre a experiência
- Fala em eventos sobre a metodologia

### Programa de Incentivo (Futuro)

**Possíveis Incentivos:**
- Desconto em novos workshops/projetos por indicação bem-sucedida
- Acesso antecipado a novas ferramentas/produtos
- Selo "Context-First Certified Company"
- Destaque em marketing e eventos da Thatix

### Impacto no Negócio

**Valor do Advocate:**
- Cada indicação tem taxa de conversão 3-5x maior (confiança pré-estabelecida)
- Reduz custo de aquisição de cliente (CAC)
- Fornece prova social poderosa
- Gera conteúdo autêntico (testemunhos, cases)

### Cultivo de Advocates

**Ações da Thatix:**
1. Identificar clientes com maior sucesso e satisfação
2. Fazer pedido personalizado de advocacia (não genérico)
3. Facilitar ao máximo (templates prontos, suporte de marketing)
4. Reconhecer publicamente (tag em posts, agradecimentos)
5. Manter relacionamento próximo (tratar como VIP)

### Critérios de Sucesso

Cliente se torna advocate quando:
- ✅ NPS 9-10 sustentado
- ✅ Resultados mensuráveis e impressionantes
- ✅ Já fez pelo menos 1 ação de advocacia
- ✅ Relacionamento próximo com time Thatix
- ✅ Vê sucesso próprio atrelado ao sucesso da metodologia

---

## Fase 6: Churn (Saída do Cliente)

### Tipos de Churn

**1. Churn Natural (Positivo ou Neutro):**
- Cliente atingiu objetivos e não precisa mais de suporte externo
- Internalizou completamente a metodologia
- Mudança de estratégia da empresa (não relacionado à Thatix)

**2. Churn Negativo:**
- Insatisfação com metodologia ou suporte
- Não viu ROI esperado
- Problemas de implementação não resolvidos
- Questões comerciais (preço, contrato)

**3. Churn Involuntário:**
- Empresa fechou ou foi adquirida
- Mudança radical de liderança técnica
- Cortes drásticos de budget

### Sinais de Alerta Precoce

**Indicadores de Risco de Churn (60-90 dias antes):**
- ⚠️ Redução drástica de uso da metodologia
- ⚠️ NPS em queda (de 9-10 para 6-7)
- ⚠️ Saída de champion interno (CTO, Tech Lead que defendia)
- ⚠️ Falta de resposta a comunicações
- ⚠️ Feedback negativo em check-ins
- ⚠️ Não renovação de contratos ou novos projetos

### Ações de Retenção

**Quando sinais aparecem:**
1. **Call de Emergência:** Entender o que está acontecendo
2. **Diagnóstico:** Identificar problema real (metodologia, suporte, comercial, timing)
3. **Plano de Recuperação:**
   - Se problema técnico: sessão de reforço, materiais adicionais
   - Se problema comercial: renegociação, condições especiais
   - Se problema de valor: revisitar objetivos, ajustar expectativas
4. **Follow-up Intensivo:** Check-ins semanais até situação estabilizar

### Processo de Offboarding

**Se churn é inevitável:**
1. **Exit Interview:** Entender razões reais (aprendizado)
2. **Feedback Estruturado:** Pesquisa de churn
3. **Porta Aberta:** Deixar claro que podem voltar
4. **Relacionamento Pós-Churn:** Não queimar pontes, manter contato leve

**Aprendizados:**
- Toda saída gera learning para melhorar produto/serviço
- Alguns churns são saudáveis (cliente internalizou, não precisa mais)
- Foco em reduzir churn negativo

### Métricas de Churn

**Metas (a definir com dados reais):**
- **Churn Rate:** < 10% ao ano (ideal para B2B consultoria)
- **Razão Principal de Churn:** Churn natural (sucesso) > Churn negativo

---

## Resumo: Jornada Ideal

| Fase | Duração | Marco de Sucesso | Ação-Chave |
|------|---------|------------------|------------|
| **Awareness** | 1-2 semanas | Cliente reconhece problema | Educar com conteúdo |
| **Consideration** | 1-4 semanas | Contrato assinado | Call de discovery, tratar objeções |
| **Onboarding** | 3 semanas | Metodologia adotada | Workshop + suporte |
| **Growth** | Indeterminada | Cliente satisfeito e expandindo | Cultivo de upsell, check-ins |
| **Advocacy** | Indeterminada | Cliente promove ativamente | Facilitar advocacia |
| **Churn** | N/A | Learning extraído | Exit interview |

---

## Oportunidades de Otimização (Contínua)

**Reduzir Tempo de Awareness → Consideration:**
- Melhorar SEO e conteúdo educativo
- Aumentar presença em comunidades técnicas
- Webinars e eventos para acelerar educação

**Aumentar Taxa de Conversão (Consideration → Customer):**
- Simplificar processo de venda
- Melhorar materiais de proposta
- Oferecer trial ou piloto de menor risco

**Acelerar Onboarding:**
- Melhorar preparação pré-workshop
- Otimizar conteúdo do workshop com feedback contínuo
- Criar mais recursos self-service

**Reduzir Churn:**
- Identificar sinais precoces e agir rápido
- Melhorar suporte pós-workshop
- Criar comunidade de clientes para troca de experiências

---

## Diretrizes de Interação com IA

### Para Sistemas de IA acompanhando clientes:

**Em cada fase, priorizar:**
- **Awareness:** Educar, não vender
- **Consideration:** Responder objeções com dados, não pressionar
- **Onboarding:** Suportar, remover blockers, facilitar
- **Growth:** Identificar oportunidades, fortalecer relacionamento
- **Advocacy:** Facilitar e reconhecer, não forçar
- **Churn Risk:** Escalar para humano IMEDIATAMENTE

**Sinais de Escalação para Humano:**
- Cliente expressa frustração ou insatisfação
- Dúvidas sobre preço ou renegociação
- Sinais de churn
- Solicitação de customização ou projeto especial
- Decisão de compra iminente
