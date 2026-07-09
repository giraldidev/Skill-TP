# 🚀 Skill de Tráfego Pago — Meta Ads (Andromeda)

Uma [Agent Skill](https://code.claude.com/docs/en/skills) para **Claude Code**
que transforma o Claude em um **Analista e Gestor de Tráfego Pago sênior**,
especializado em Meta Ads (Facebook e Instagram), alinhado ao algoritmo
**Meta Andromeda** e às **Políticas de Publicidade da Meta**.

## O que a skill faz

Pipeline completo de gestão de tráfego em 7 etapas, com entregáveis prontos
para subir no Gerenciador de Anúncios:

| Etapa | Entregável |
|---|---|
| 1. Análise de Persona & ICP | Dossiê de persona (dores, desejos, objeções, nível de consciência) + ICP e anti-ICP |
| 2. Análise de Produto/Serviço | Matriz de Oferta: promessa, mecanismo único, provas, objeções × respostas, ângulos priorizados |
| 3. Estrutura de Campanhas | Blueprint campanha → conjunto → anúncio por faixa de orçamento, com eventos de otimização e plano de escala |
| 4. Kits de Anúncios | 3+ kits por campanha, cada um com ângulo/persona diferente (diversidade exigida pelo Andromeda) |
| 5. Entrega de cada Kit | Template padronizado: copies, títulos, descrições, arte, carrossel, roteiro de vídeo e CTA |
| 6. Copy para Arte & Carrosséis | Hierarquia de texto para estáticos + estrutura narrativa card a card para carrosséis |
| 7. Otimização Contínua | Métricas de decisão (CPM, hook rate, CTR, CPA/ROAS), regras de pausa/escala e cadência de renovação criativa |

Toda peça passa por um **checklist de compliance das Políticas da Meta**
(atributos pessoais, promessas de resultado, antes/depois, categorias
especiais…) antes de ser entregue.

## Instalação

### Opção 1 — Plugin do Claude Code (recomendado)

No Claude Code, rode:

```
/plugin marketplace add giraldidev/Skill-TP
/plugin install trafego-pago@skill-tp
```

### Opção 2 — Skill pessoal (disponível em todos os seus projetos)

```bash
git clone https://github.com/giraldidev/Skill-TP.git
mkdir -p ~/.claude/skills
cp -r Skill-TP/skills/trafego-pago ~/.claude/skills/
```

### Opção 3 — Skill de projeto (só em um repositório específico)

Na raiz do seu projeto:

```bash
mkdir -p .claude/skills
git clone --depth 1 https://github.com/giraldidev/Skill-TP.git /tmp/skill-tp
cp -r /tmp/skill-tp/skills/trafego-pago .claude/skills/
rm -rf /tmp/skill-tp
```

Depois de instalar, verifique com `/skills` (a skill aparece como `trafego-pago`).

## Como usar

A skill ativa automaticamente quando o pedido envolve tráfego pago/Meta Ads.
Exemplos:

- **Projeto completo:** "Monte a estratégia de tráfego pago completa para meu
  curso de inglês online, ticket R$ 497, orçamento de R$ 5.000/mês"
- **Persona:** "Analise a persona e o ICP deste negócio: …"
- **Kits:** "Gere 3 kits de anúncios para a campanha de vendas"
- **Peça pontual:** "Escreva a copy do carrossel do kit 2" ou "Meu CPA subiu
  40%, diagnostique a campanha"

Em projetos completos o Claude segue as 7 etapas em ordem; em pedidos pontuais
ele vai direto à etapa certa, perguntando o contexto mínimo se faltar.

## Estrutura do repositório

```
.claude-plugin/
├── plugin.json                   # Manifesto do plugin
└── marketplace.json              # Marketplace para /plugin marketplace add
skills/trafego-pago/
├── SKILL.md                      # Persona + modos de operação + pipeline
├── references/
│   ├── persona-icp.md            # Etapa 1 — Dossiê de Persona & ICP
│   ├── produto-servico.md        # Etapa 2 — Matriz de Oferta
│   ├── estrutura-campanhas.md    # Etapa 3 — Estruturas por orçamento
│   ├── kits-anuncios.md          # Etapa 4 — Composição e diversidade dos kits
│   ├── copywriting.md            # Frameworks, ganchos e regras de linguagem
│   ├── carrosseis.md             # Estrutura narrativa card a card
│   ├── copy-arte-grafica.md      # Hierarquia de texto + direção de arte
│   ├── politicas-meta.md         # Checklist de compliance Meta Ads
│   └── otimizacao-melhorias.md   # Etapa 7 — métricas, testes e renovação
└── templates/
    └── kit-entrega.md            # Formato padrão de entrega de cada kit
```

## Princípios da skill (era Andromeda)

1. **O criativo é a segmentação** — diversidade real de ângulos e formatos,
   nunca variações cosméticas do mesmo anúncio.
2. **Broad targeting + Advantage+ como padrão** — segmentação detalhada só
   com justificativa.
3. **Estruturas consolidadas** — poucas campanhas e conjuntos, orçamento em
   CBO, saída rápida da fase de aprendizagem.
4. **Renovação criativa por dados** — fadiga medida por frequência + CTR,
   não por ansiedade.
5. **Compliance inegociável** — nenhuma peça sai sem passar pelo checklist
   das políticas da Meta.

## Licença

[MIT](LICENSE) — use, adapte e distribua à vontade.
