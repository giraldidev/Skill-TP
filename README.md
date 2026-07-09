# Skill-TP — Skill de Tráfego Pago (Meta Ads / Andromeda)

Skill para Claude Code que transforma o agente em um **Analista e Gestor de
Tráfego Pago sênior** especializado em Meta Ads, alinhado ao algoritmo
**Meta Andromeda** e às **Políticas de Publicidade da Meta**.

## Estrutura

```
.claude/skills/trafego-pago/
├── SKILL.md                          # Persona + pipeline de 7 etapas
├── references/
│   ├── persona-icp.md                # Etapa 1 — Dossiê de Persona & ICP
│   ├── produto-servico.md            # Etapa 2 — Matriz de Oferta
│   ├── estrutura-campanhas.md        # Etapa 3 — Blueprint de estrutura
│   ├── kits-anuncios.md              # Etapa 4 — Geração de kits
│   ├── copywriting.md                # Diretrizes de copywriting
│   ├── carrosseis.md                 # Diretrizes específicas de carrossel
│   ├── copy-arte-grafica.md          # Copy + direção de arte para estáticos
│   ├── politicas-meta.md             # Checklist de compliance Meta Ads
│   └── otimizacao-melhorias.md       # Etapa 7 — testes, métricas, referências
└── templates/
    └── kit-entrega.md                # Formato padrão de entrega de cada kit
```

## Como usar

Com o repositório aberto no Claude Code, a skill é carregada automaticamente.
Exemplos de pedidos que a ativam:

- "Monte a estratégia de tráfego pago para [produto]"
- "Analise a persona e o ICP deste negócio: …"
- "Gere 3 kits de anúncios para minha campanha de vendas"
- "Escreva a copy do carrossel do kit 2"

O agente segue o pipeline: briefing/persona → oferta → estrutura → kits →
entrega → copy/arte/carrossel → plano de otimização, com verificação de
compliance em toda peça entregue.
