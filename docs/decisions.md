# 📋 Log de Decisões — Clone de Angry Birds 2

> **Propósito:** Registro de todas as decisões tomadas durante o planejamento. Para humanos lerem e entenderem o contexto.
> **Estrutura:** Cronologia das decisões + checklist de confirmações.
> **Data:** 2026-07-24
> **Estrutura JSON:** [`decisions.json`](./decisions.json)

---

## 🗓️ Cronologia das Decisões

### 1. Análise do Prompt Inicial
**Contexto:** Usuário forneceu um prompt para criar um clone de Angry Birds 2.

**Decisões:**
- **Física:** Recomendação de Matter.js (vs Box2D) — mais fácil de integrar com Phaser, sem build.
- **Sugestões de gameplay:** Incluir pontuação/combos, condições de vitória/derrota, controles extras.
- **Riscos identificados:** Ambiguidade de stack (WebGPU/WebGL), dependência de internet para assets, física caseira.

---

### 2. Esclarecimento de Requisitos
**Contexto:** Usuário respondeu perguntas sobre stack e gameplay.

**Decisões:**
- **Stack:** Retirado JS Vanilla → **TypeScript + Bun** (nunca Node.js).
- **Renderização:** **WebGL** (não WebGPU).
- **Engine:** **Phaser** (2D).
- **Pássaros:** **Ilimitados** (como o original).
- **Fase 4:** **Timer** para concluir o nível.
- **Gameplay:** OK para todas as sugestões (pontuação, combos, etc.).
- **Física:** Matter.js ou Box2D → **Matter.js** recomendado.
- **Assets:** Baixar sprites gratuitos; se não possível, gerar proceduralmente (modelo multimodal).
- **Estrutura:** Seguir boas práticas (SOLID, DRY, Clean Code).
- **Testes:** Playwright + unit tests.

---

### 3. Esclarecimento de Stack e Gameplay
**Contexto:** Confirmação de stack e gameplay.

**Decisões:**
- **2D (Phaser)** confirmado.
- **WebGL** confirmado.
- **Pássaros ilimitados** confirmado.
- **Fase 4 = timer** confirmado.
- **Sistema de pontuação/combos** confirmado (incluir).
- **Física:** Matter.js recomendado.
- **Assets:** Confirmado baixar gratuitos; criar ferramenta de pesquisa se necessário (Python/Rust instalados).

---

### 4. Decisões de Infraestrutura
**Contexto:** Decisões de infraestrutura e tooling.

**Decisões:**
- **Runtime:** 100% Bun (sem Node.js, nem compatibilidade).
- **Vercel:** Roda Bun nativamente (`vercel.json`).
- **Context7:** Usar para documentação atualizada; não insistir em erros.
- **Licença:** Incluir `LICENSE` (MIT).
- **Privacidade:** COPPA + LGPD.
- **PWA:** Sim, mas para atualização futura.
- **Acessibilidade:** Sempre (PWA para futuro).
- **Tutorial mode:** Incluir.
- **Tela de aviso:** Antes da Splash Screen.
- **Favicon/ícones/manifest/Open Graph:** Incluir tudo.

---

### 5. Decisões de Testes e CI/CD
**Contexto:** Decisões de testes e CI/CD.

**Decisões:**
- **Testes por fase:** TDD, só commitar se testes passarem.
- **CI/CD:** Testes locais (Bun) como primário; GitHub Actions opcional (só se repo público).
- **2000 minutos:** Generoso para projeto pequeno; repo público = grátis.
- **Hooks:** Nativos do Git (sem Node).

---

### 6. Decisões Finais
**Contexto:** Decisões finais de repo, diretório e deploy.

**Decisões:**
- **Repo:** `clone-angry-birds-2` (público desde o início).
- **Diretório:** Renomeado para `clone-angry-birds-2`.
- **Deploy:** Gratuito (local + opcional CI público).
- **Documentação:** Em `./docs` (markdown para humanos + JSON para agentes).

---

## ✅ Checklist de Decisões Confirmadas

- [x] Stack: TS + Bun + WebGL + Phaser + Matter.js + Howler.js + Vite
- [x] 5 fases, dificuldade progressiva
- [x] Pássaros ilimitados
- [x] Fase 4 com timer
- [x] Pontuação/combos
- [x] Assets: baixar gratuitos ou gerar proceduralmente
- [x] Testes por fase (TDD)
- [x] Regras de commit (Conventional Commits)
- [x] PT-BR
- [x] Responsivo (horizontal → vertical)
- [x] Deploy: gratuito (local + opcional CI público)
- [x] GitHub Projects Kanban
- [x] LICENSE (MIT)
- [x] COPPA/Privacidade + LGPD
- [x] PWA (futuro)
- [x] Acessibilidade (sempre)
- [x] Tutorial mode
- [x] Tela de aviso antes da Splash
- [x] Favicon/ícones/manifest/Open Graph
- [x] CI/CD: local (Bun) primário + GitHub Actions opcional (só se público)
- [x] Hooks: nativos do Git (sem Node)
- [x] Repo: `clone-angry-birds-2` (público desde o início)

---

*Última atualização: 2026-07-24. Este log é consultado por humanos para entender o contexto das decisões.*
