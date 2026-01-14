---
spec_version: "1.0.0"
valid_from: "2026-01-13"
last_updated: "2026-01-13"
supersedes: null
status: "active"
category: "business"
tags: ["personas", "customer-research", "target-audience", "ux", "product-strategy"]
---

# Personas do Cliente - Thatix

:::version_info
**Versão**: 1.0.0
**Válida desde**: 2026-01-13
**Status**: Ativa
:::

:::breaking_changes
**v1.0.0** (baseline):
- Primeira versão versionada desta spec
- Define 4 personas principais: CTO/VP de Engenharia, Tech Lead, Founder Técnico, Dev Senior
- Estabelece critérios de decisão, objeções típicas e canais de comunicação
- Inclui matriz de atributos por persona
:::

**Versão:** 1.0
**Data:** 2026-01-13

---

## Visão Geral

Este documento define as personas primárias do cliente da Thatix, baseado em análise de mercado, perfil de clientes atendidos e padrões de comportamento observados. As personas estão segmentadas por nível de decisão e envolvimento com a solução.

---

## Persona 1: CTO/VP de Engenharia (Decisor Principal)

### Perfil Demográfico

**Cargo:** CTO, VP de Engenharia, Head of Engineering
**Experiência:** 8-15+ anos em tecnologia
**Formação:** Ciência da Computação, Engenharia de Software
**Localização:** Principalmente capitais brasileiras (SP, RJ, BH, Porto Alegre)
**Indústria:** Fintech, SaaS, E-commerce, Healthtech, Logtech

### Contexto Profissional

**Tamanho de Time:** 5-50 desenvolvedores
**Desafios do Dia a Dia:**
- Pressão por entrega rápida mantendo qualidade
- Gerenciar débito técnico crescente
- Escalar time sem comprometer cultura de engenharia
- Justificar investimentos em tecnologia para C-level

**Responsabilidades:**
- Definir arquitetura e stack tecnológica
- Garantir qualidade e segurança do código
- Escalar operação de desenvolvimento
- Reduzir time-to-market mantendo estabilidade

### Objetivos e Motivações

**Objetivos Primários:**
1. Aumentar produtividade do time sem sacrificar qualidade
2. Adotar IA de forma estruturada e escalável (não experimental)
3. Reduzir débito técnico e retrabalho
4. Entregar features críticas mais rápido

**Motivações Pessoais:**
- Ser reconhecido como líder técnico inovador
- Construir time de alta performance
- Implementar boas práticas e processos sustentáveis
- Evitar falhas em produção que impactem reputação

### Pontos de Dor

**Dor Principal:** "Meu time está experimentando com IA (Copilot, ChatGPT), mas os resultados são inconsistentes. Ganhamos velocidade inicial, mas geramos muito débito técnico e bugs sutis em produção."

**Dores Específicas:**
1. **Context Poisoning:** IA gerando código que não respeita padrões do projeto
2. **Falta de Previsibilidade:** Não consegue estimar entregas com IA no processo
3. **Qualidade Inconsistente:** Code reviews viraram gargalo (muito código de baixa qualidade)
4. **Risco de Compliance:** Código gerado pode violar requisitos regulatórios (especialmente fintech)
5. **Falta de Metodologia:** Cada dev usa IA de forma diferente (vibe coding)

### Objeções Típicas

1. **Preço:** "É caro, preciso justificar ROI para o board"
   - *Tratamento:* Evidenciar 73% ganho de produtividade e redução de débito técnico
2. **Desconhecimento:** "Não entendo como isso é diferente de usar Copilot/ChatGPT"
   - *Tratamento:* Explicar metodologia estruturada vs uso ad-hoc
3. **Timing:** "Estamos muito atarefados agora, talvez no próximo trimestre"
   - *Tratamento:* Mostrar que o problema só piora com o tempo

### Jornada de Decisão

**Tempo Médio de Decisão:** 2-4 semanas
**Stakeholders Envolvidos:** CEO/Founder, CFO (aprovação de budget), Tech Leads (validação técnica)

**Processo de Avaliação:**
1. Pesquisa inicial (artigos, LinkedIn, indicações)
2. Análise do site e cases
3. Reunião de discovery (entender metodologia)
4. Apresentação da proposta ao board
5. Decisão e fechamento

### Critérios de Sucesso

**Como esta persona mede sucesso após contratar Thatix:**
- Time entrega X% mais rápido com mesma qualidade
- Redução mensurável de bugs em produção
- Code reviews mais ágeis (código mais consistente)
- Processo de desenvolvimento previsível e repetível
- Time alinhado em metodologia estruturada

### Canais de Comunicação Preferidos

**Profissional:**
- LinkedIn (conteúdo técnico, cases, thought leadership)
- Email (comunicação formal)
- WhatsApp (após primeiro contato)

**Consumo de Conteúdo:**
- Artigos técnicos detalhados
- Case studies com números reais
- Webinars e workshops
- Podcasts de engenharia

### Citações Representativas

> "Nosso time está usando IA, mas virou o velho oeste. Cada um faz do seu jeito e estamos gerando muito débito técnico."

> "Preciso de um processo estruturado para usar IA em produção. Não posso arriscar em sistemas críticos sem metodologia."

> "Meu CFO quer números: quanto vamos economizar? Quanto vamos acelerar? Preciso de evidências."

---

## Persona 2: Tech Lead / Engineering Manager (Influenciador)

### Perfil Demográfico

**Cargo:** Tech Lead, Engineering Manager, Lead Developer
**Experiência:** 5-10 anos em desenvolvimento
**Formação:** Ciência da Computação, Engenharia de Software, Sistemas de Informação
**Localização:** Brasil (todas as regiões)
**Indústria:** Diversas (tech-driven companies)

### Contexto Profissional

**Tamanho de Time:** Lidera squad de 3-8 desenvolvedores
**Desafios do Dia a Dia:**
- Balancear hands-on coding com gestão de pessoas
- Garantir qualidade do código do time
- Fazer code review de volume crescente
- Mentoria de devs júnior/pleno
- Entregar sprints no prazo

**Responsabilidades:**
- Revisar código e arquitetura
- Definir padrões de desenvolvimento do time
- Fazer pair programming e mentoria
- Reportar progresso para CTO/VP

### Objetivos e Motivações

**Objetivos Primários:**
1. Elevar nível técnico do time
2. Estabelecer padrões de qualidade consistentes
3. Reduzir tempo em code review sem comprometer qualidade
4. Adotar ferramentas que acelerem sem gerar débito técnico

**Motivações Pessoais:**
- Crescer para cargos de liderança (Engineering Manager → VP)
- Ser reconhecido como referência técnica
- Construir processos que escalam
- Desenvolver o time sob sua liderança

### Pontos de Dor

**Dor Principal:** "Estou passando 60% do meu tempo em code review porque a IA está gerando código inconsistente. Meu time está rápido, mas a qualidade caiu."

**Dores Específicas:**
1. **Code Review Bottleneck:** Volume de código aumentou mas qualidade caiu
2. **Inconsistência de Padrões:** IA não respeita style guide e arquitetura
3. **Retrabalho Constante:** Código aceito em sprint precisa ser refatorado depois
4. **Dificuldade de Mentoria:** Como ensinar boas práticas quando IA gera código ad-hoc?
5. **Falta de Documentação:** Código gerado vem sem contexto adequado

### Papel na Decisão

**Tipo de Influência:** Validador Técnico
**Poder de Decisão:** Baixo (não aprova budget) / Alto (pode vetar tecnicamente)

Este persona geralmente:
- É consultado pelo CTO antes da decisão
- Valida se a solução é viável tecnicamente
- Identifica se resolve dores reais do time
- Será responsável por adoção no dia a dia

### Critérios de Avaliação

**O que este persona busca:**
- Praticidade e facilidade de adoção
- Ferramentas e templates prontos
- Metodologia clara e documentada
- Suporte durante implementação
- Resultados rápidos (quick wins)

### Canais de Comunicação Preferidos

**Profissional:**
- Slack/Discord de comunidades técnicas
- GitHub / GitLab (código e discussões)
- Twitter/X (tech community)
- LinkedIn (networking)

**Consumo de Conteúdo:**
- Tutoriais práticos e hands-on
- Repositories com exemplos
- Vídeos técnicos (YouTube)
- Newsletters técnicas

### Citações Representativas

> "Preciso de um framework que o time inteiro siga. Não dá mais pra cada um usar IA do seu jeito."

> "Meus code reviews viraram um inferno. O código funciona, mas não é sustentável."

> "Quero que meu time seja mais rápido, mas sem virar uma bomba-relógio de débito técnico."

---

## Persona 3: Founder Técnico (Decisor em Startups)

### Perfil Demográfico

**Cargo:** CEO/CTO (founder), Co-founder técnico
**Experiência:** Variável (3-15+ anos)
**Formação:** Diversa (pode ou não ter formação formal em tech)
**Localização:** Brasil (principalmente SP, RJ, BH)
**Indústria:** Startups early-stage a Series A/B

### Contexto Profissional

**Tamanho de Time:** 2-15 pessoas (time enxuto)
**Estágio da Empresa:** Seed, Series A ou early Series B
**Desafios do Dia a Dia:**
- Fazer mais com menos (budget limitado)
- Velocidade é crítica (competição acirrada)
- Vestir múltiplos chapéus (tech + negócio)
- Construir MVP ou evoluir produto rapidamente

**Responsabilidades:**
- Decisões estratégicas de produto e tecnologia
- Captação de investimento
- Contratação e liderança do time
- Velocidade de go-to-market

### Objetivos e Motivações

**Objetivos Primários:**
1. Validar product-market fit rapidamente
2. Escalar produto sem escalar custos proporcionalmente
3. Impressionar investidores com tração e tecnologia
4. Construir base tecnológica sólida desde o início

**Motivações Pessoais:**
- Construir empresa de sucesso e escalável
- Usar tecnologia de ponta (early adopter)
- Atrair e reter talentos de engenharia
- Ser eficiente com runway (capital disponível)

### Pontos de Dor

**Dor Principal:** "Preciso entregar rápido para validar com o mercado, mas não posso criar débito técnico que me atrapalhe depois no scale."

**Dores Específicas:**
1. **Velocidade vs Qualidade:** Dilema constante entre ship fast e build right
2. **Limitação de Budget:** Precisa fazer escolhas assertivas de investimento
3. **Risco Técnico:** Refatorações custosas no futuro podem inviabilizar a empresa
4. **Contratação:** Difícil encontrar devs que equilibrem velocidade e qualidade
5. **Credibilidade com Investidores:** Precisa mostrar processos maduros

### Objeções Típicas

1. **Budget:** "Estou com runway limitado, cada investimento precisa gerar ROI claro"
   - *Tratamento:* Mostrar que evitar débito técnico economiza muito mais depois
2. **Urgência:** "Preciso de resultados ontem, não tenho tempo para workshop"
   - *Tratamento:* Workshop de 2 dias + implementação imediata gera resultado em semanas
3. **Time Pequeno:** "Tenho só 3 devs, faz sentido pra mim?"
   - *Tratamento:* Justamente por ter poucos devs, cada um precisa ser super produtivo

### Jornada de Decisão

**Tempo Médio de Decisão:** 1-2 semanas (mais ágil que enterprises)
**Stakeholders Envolvidos:** Co-founders, eventualmente advisor técnico

**Processo de Avaliação:**
1. Descoberta rápida (indicação ou conteúdo)
2. Call de 30min para entender solução
3. Análise de ROI e fit com momento da empresa
4. Decisão rápida (founder tem autonomia)

### Critérios de Sucesso

**Como esta persona mede sucesso após contratar Thatix:**
- Features críticas entregues em semanas (não meses)
- Código que não precisa ser reescrito quando escalar
- Time pequeno produzindo como time grande
- Investidores impressionados com maturidade de processo
- Redução de bugs e incidentes em produção

### Canais de Comunicação Preferidos

**Profissional:**
- WhatsApp (rápido e direto)
- LinkedIn (networking e conteúdo)
- Email (quando formal)
- Telegram (comunidades de founders)

**Consumo de Conteúdo:**
- Podcasts (multitask enquanto trabalha)
- Newsletter resumidas
- Vídeos curtos
- Indicações de outros founders

### Citações Representativas

> "Não posso escolher entre velocidade e qualidade. Preciso dos dois ou minha startup morre."

> "Cada decisão técnica errada hoje pode custar a empresa no futuro. Preciso acertar."

> "Meu runway é de 18 meses. Preciso usar IA para acelerar, mas não posso criar uma bomba-relógio."

---

## Persona 4: Desenvolvedor Senior/Staff (Usuário Final)

### Perfil Demográfico

**Cargo:** Senior Developer, Staff Engineer, Senior Software Engineer
**Experiência:** 4-8+ anos em desenvolvimento
**Formação:** Ciência da Computação, Engenharia, autodidata
**Localização:** Brasil (todas as regiões, pode ser remoto)
**Indústria:** Empresas de tecnologia diversas

### Contexto Profissional

**Papel no Time:** Execução hands-on, referência técnica
**Responsabilidades:**
- Desenvolver features complexas
- Participar de decisões de arquitetura
- Mentoria informal de devs mais junior
- Code review de peers

**Ferramentas Atuais:**
- GitHub Copilot, ChatGPT, Claude (uso ad-hoc)
- IDEs: VSCode, JetBrains
- Stack: Varia (full-stack, backend, frontend)

### Objetivos e Motivações

**Objetivos Primários:**
1. Escrever código de alta qualidade
2. Ser mais produtivo sem comprometer craft
3. Aprender novas tecnologias e metodologias
4. Ser reconhecido como referência técnica

**Motivações Pessoais:**
- Orgulho do código que escreve
- Crescimento técnico contínuo
- Eficiência no trabalho (não fazer hora extra)
- Contribuir com ferramentas e processos melhores

### Pontos de Dor

**Dor Principal:** "Uso IA todos os dias, mas às vezes fico inseguro. O código gerado funciona, mas será que é o jeito certo? Estou criando problemas futuros?"

**Dores Específicas:**
1. **Falta de Confiança:** Não tem certeza se código IA é production-ready
2. **Context Switching:** Perde tempo explicando contexto para IA a cada interação
3. **Inconsistência:** IA gera código diferente do resto da codebase
4. **Testabilidade:** Código gerado muitas vezes vem sem testes
5. **Documentação:** Falta contexto e explicação em código IA

### Papel na Decisão

**Tipo de Influência:** Usuário Final / Early Adopter
**Poder de Decisão:** Muito baixo (não decide compra) / Alto (determina sucesso da adoção)

Este persona:
- Será o usuário direto da metodologia no dia a dia
- Pode sabotar ou impulsionar adoção
- Dá feedback para liderança sobre eficácia
- É crítico para o sucesso da implementação

### Critérios de Avaliação

**O que este persona busca:**
- Ferramentas que facilitam (não complicam) o trabalho
- Padrões claros e fáceis de seguir
- Autonomia mantida (não processo burocrático)
- Resultado tangível (código melhor, mais rápido)
- Aprendizado técnico (não só processo)

### Canais de Comunicação Preferidos

**Profissional:**
- GitHub / GitLab (código)
- Slack do time
- Discord de comunidades técnicas
- Twitter/X (tech community)

**Consumo de Conteúdo:**
- Documentação técnica detalhada
- Exemplos de código
- Vídeos técnicos hands-on
- Blog posts técnicos
- Reddit (r/programming, r/machinelearning)

### Citações Representativas

> "Quero usar IA de forma profissional, não amadora. Preciso de estrutura."

> "Cansei de ficar na dúvida se o código que a IA gerou é bom ou vai me dar problema depois."

> "Quero ser rápido sem deixar de ser bom. IA me dá velocidade, mas cadê a qualidade?"

---

## Matriz de Personas por Atributos

| Atributo | CTO/VP Eng | Tech Lead | Founder | Dev Senior |
|----------|-----------|-----------|---------|------------|
| **Poder de Decisão** | Alto | Baixo | Alto | Muito Baixo |
| **Influência Técnica** | Alta | Muito Alta | Média | Média |
| **Urgência de Solução** | Média-Alta | Alta | Muito Alta | Média |
| **Sensibilidade a Preço** | Média | Baixa* | Alta | Baixa* |
| **Busca por ROI** | Muito Alta | Baixa* | Muito Alta | Baixa* |
| **Profundidade Técnica** | Média-Alta | Muito Alta | Variável | Muito Alta |
| **Foco em Processo** | Alto | Muito Alto | Médio | Baixo-Médio |
| **Early Adopter** | Médio | Alto | Muito Alto | Alto |

*Não decide budget, mas influencia percepção de valor

---

## Diretrizes de Interação com IA

### Para Sistemas de IA atendendo essas personas:

**Tom e Linguagem:**
- **CTO/VP:** Profissional, orientado a resultados, com dados e evidências
- **Tech Lead:** Técnico-prático, focado em implementação
- **Founder:** Direto, rápido, orientado a ROI e impacto no negócio
- **Dev Senior:** Técnico-detalhado, com exemplos de código e arquitetura

**Prioridades de Informação:**
- **CTO/VP:** ROI, cases, riscos mitigados, escalabilidade
- **Tech Lead:** Metodologia, ferramentas, processo de adoção, suporte
- **Founder:** Velocidade de resultados, custo-benefício, diferenciais competitivos
- **Dev Senior:** Como funciona na prática, qualidade do código, learning curve

**Tratamento de Objeções:**
- Sempre basear em dados reais (73% produtividade, cases reais)
- Reconhecer a objeção como válida antes de tratar
- Oferecer próximo passo claro (call, workshop, demo)
- Nunca pressionar; educar e permitir decisão informada

**Escalação para Humano:**
- Negociação de preço
- Customização de proposta
- Dúvidas técnicas muito específicas
- Solicitação de referências de clientes
