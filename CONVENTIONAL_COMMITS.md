# 📝 Regras de Commit — Conventional Commits

> **Propósito:** Padronizar commits para manter o histórico legível e gerenciar changelogs.
> **Regra de ouro:** **Só commitar se os testes passarem.**

---

## 📐 Formato

```
<type>(<scope>): <subject>

<body>

<footer>
```

### Tipos de Commit
| Tipo | Quando usar | Exemplo |
|---|---|---|
| `feat` | Nova funcionalidade | `feat(core): adiciona sistema de pontuação` |
| `fix` | Correção de bug | `fix(phaser): corrige loop de render` |
| `docs` | Documentação | `docs(roadmap): atualiza roadmap` |
| `style` | Formatação (sem mudança de lógica) | `style: formata código` |
| `refactor` | Refatoração (sem mudança de comportamento) | `refactor(core): simplifica state machine` |
| `perf` | Otimização de performance | `perf(phaser): otimiza loop de render` |
| `test` | Adicionar/ajustar testes | `test(core): adiciona testes de state machine` |
| `build` | Alterações de build/config | `build: atualiza dependências` |
| `ci` | Configurações de CI/CD | `ci: configura GitHub Actions` |
| `chore` | Tarefas de manutenção | `chore: atualiza LICENSE` |
| `revert` | Reverter commit anterior | `revert: reverte commit #123` |

### Escopo (opcional)
Áreas do código: `core`, `entities`, `systems`, `ui`, `levels`, `physics`, `audio`, `assets`, `docs`, `tests`, `build`, `ci`.

### Subject
- Imperativo, presente: "adiciona", "corrige", "remove".
- Máximo 50 caracteres.
- Sem ponto final no final.

### Body (opcional)
- Explicação detalhada da mudança.
- Motivação (por que a mudança).

### Footer (opcional)
- Referências de issues: `Closes #123`, `Refs #456`.

---

## ✅ Exemplos

### Bom
```
feat(physics): adiciona cálculo de dano por material

- Implementa função calcularDano(material, impacto)
- Adiciona testes unitários para cada material

Closes #45
```

### Ruim
```
melhorei o jogo:
- fiz umas coisas
```

---

## 🚦 Fluxo de Commit

1. Faça as mudanças.
2. Rode os testes: `bun run test`.
3. Se **todos os testes passarem**, faça o commit.
4. Se **algum teste falhar**, corrija antes de commitar.

```bash
# Rode os testes
bun run test

# Se passar, faça o commit
git add .
git commit -m "feat(core): adiciona sistema de pontuação"
```

---

## 🤖 Hooks (Nativos do Git)

Os hooks são nativos do Git (`.git/hooks`), sem dependência de Node.js.

### Pre-commit
Antes de cada commit, roda os testes:
```bash
bun run test
```

### Commit-msg
Valida o formato do commit:
- Verifica se segue Conventional Commits.
- Verifica se os testes passaram.

---

## 📌 Regras Adicionais

- **Nunca** use Node.js nos hooks (use scripts Bun ou nativos do Git).
- **Sempre** rode os testes antes de commitar.
- **Mantenha** commits pequenos e focados.
- **Documente** mudanças em `./docs` conforme a regra de documentação progressiva.

---

*Regras de commit em 2026-07-24. Atualize conforme necessário.*
