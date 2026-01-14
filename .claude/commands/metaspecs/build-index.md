# Construtor de Índice - Site Thatix

Este é o repositório de metaspecs para o site da Thatix - uma consultoria especializada em desenvolvimento com IA. A ideia deste repositório é ser a especificação única que direciona todas as especificações de negócio, técnicas, código, design e artefatos de teste. É nossa fonte canônica de verdade para o projeto do site.

## Estrutura do Projeto

As especificações estão organizadas em:
- `specs/business/` - Especificações de negócio e estratégia
- `specs/technical/` - Especificações técnicas e arquiteturais
- `specs/_meta/` - Meta-informações e governança de contexto

## Uso

### /build-index

Se nenhum argumento for fornecido, o comando construirá o arquivo [index.md](../../../specs/index.md) raiz que aponta para todas as especificações do projeto.

Este índice deve fornecer:
- Links para especificações de negócio
- Links para especificações técnicas
- Links para governança e meta-informações
- Visão geral da arquitetura de contexto

### /build-index business

Reconstrói o índice das especificações de negócio em [specs/business/index.md](../../../specs/business/index.md).
Analisa a estrutura de pastas e arquivos em `specs/business/` e cria/atualiza o índice apontando para todos os recursos úteis.

### /build-index technical

Reconstrói o índice das especificações técnicas em [specs/technical/index.md](../../../specs/technical/index.md).
Analisa a estrutura de pastas e arquivos em `specs/technical/` e cria/atualiza o índice apontando para todos os recursos úteis.

Argumentos fornecidos: #$ARGUMENTS
