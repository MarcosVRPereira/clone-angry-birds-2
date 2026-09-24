# 📚 Documentação — Clone de Angry Birds 2

> **Propósito:** Documentação do projeto, organizada por tarefa/fase. Cada tarefa concluída deve ser documentada aqui para evitar alucinações e perda de contexto.
> **Público:** Humanos (Markdown) e Agentes (JSON).
> **Regra:** Toda tarefa concluída deve ter docs atualizadas.

---

## 📖 Para Humanos (Markdown)

Esta pasta contém documentação em Markdown, legível por humanos:

| Arquivo | Descrição |
|---|---|
| [`README.md`](./README.md) | Índice geral da documentação |
| [`decisions.md`](./decisions.md) | Log de decisões (por que e como decidimos) |
| [`phases/`](./phases/) | Documentação de cada fase (o que foi feito e como) |

### Como ler
1. Comece pelo [`README.md`](./README.md) para entender a estrutura.
2. Veja [`decisions.md`](./decisions.md) para entender o histórico de decisões.
3. Consulte [`phases/`](./phases/) para detalhes de cada tarefa implementada.

---

## 🤖 Para Agentes (JSON)

Para consultas estruturadas e rápidas, use os arquivos JSON:

| Arquivo | Descrição |
|---|---|
| [`decisions.json`](./decisions.json) | Log de decisões estruturado (para agentes consultarem) |
| [`phases/`](./phases/) | Resumo estruturado de cada fase (JSON + README) |

### Como consultar
1. Para decisões rápidas, use [`decisions.json`](./decisions.json).
2. Para detalhes de uma fase, use [`phases/<fase>/summary.json`](./phases/).
3. Para contexto humano, veja os arquivos Markdown correspondentes.

---

## 🗂️ Estrutura

```
docs/
├── README.md              # Índice (humanos)
├── decisions.md           # Log de decisões (humanos)
├── decisions.json          # Log de decisões (agentes)
└── phases/
    ├── 00-setup/
    │   ├── README.md       # Docs da fase (humanos)
    │   └── summary.json    # Resumo estruturado (agentes)
    ├── 01-core-engine/
    │   ├── README.md
    │   └── summary.json
    └── ... (criado conforme implementação)
```

---

## 📝 Regra de Documentação

> **Toda tarefa concluída deve ser documentada em `./docs`:**
> 1. Crie `docs/phases/<fase>/README.md` (para humanos).
> 2. Crie `docs/phases/<fase>/summary.json` (para agentes).
> 3. Atualize `docs/decisions.md` e `docs/decisions.json` com novas decisões.

---

*Documentação inicial em 2026-07-24. Atualize conforme o progresso.*
