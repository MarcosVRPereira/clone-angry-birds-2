# 📜 Histórico de Decisões — Clone de Angry Birds 2

> **Propósito:** Log de tudo que foi acordado durante o planejamento. Para que agentes (e humanos) possam consultar e lembrar de todas as decisões.
> **Formato:** Markdown (legível por humanos e agentes).
> **Data:** 2026-07-24
> **Repo:** [github.com/MarcosVRPereira/clone-angry-birds-2](https://github.com/MarcosVRPereira/clone-angry-birds-2)

---

## 📌 Resumo Executivo

Foi planejado um **clone de Angry Birds 2** (jogo web 2D) com as seguintes características principais:
- Física realista (slingshot), 5 fases progressivas, sistema de pontuação.
- Stack: **TypeScript + Bun + WebGL + Phaser + Matter.js + Howler.js + Vite**.
- Testes por fase (TDD), Conventional Commits, documentação progressiva.
- 100% Bun (sem Node.js), deploy gratuito.

---

## 🗓️ Cronologia das Decisões

### 1. Análise do Prompt Inicial
- **Contexto:** Usuário forneceu um prompt para criar um clone de Angry Birds 2.
- **Ações:** Analisado o prompt, identificadas ambiguidades e lacunas.
- **Decisões:**
  - Recomendação de física: **Matter.js** (vs Box2D).
  - Sugestões de gameplay: pontuação/combos, condições de vitória/derrota, controles extras.
  - Riscos: ambiguidade de stack, dependência de internet para assets, física caseira.

### 2. Esclarecimento de Requisitos
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

### 3. Esclarecimento de Stack e Gameplay
- **2D (Phaser)** confirmado.
- **WebGL** confirmado.
- **Pássaros ilimitados** confirmado.
- **Fase 4 = timer** confirmado.
- **Sistema de pontuação/combos** confirmado (incluir).
- **Física:** Matter.js recomendado.
- **Assets:** Confirmado baixar gratuitos; criar ferramenta de pesquisa se necessário (Python/Rust instalados).

### 4. Decisões de Infraestrutura
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

### 5. Decisões de Testes e CI/CD
- **Testes por fase:** TDD, só commitar se testes passarem.
- **CI/CD:** Testes locais (Bun) como primário; GitHub Actions opcional (só se repo público).
- **2000 minutos:** Generoso para projeto pequeno; repo público = grátis.
- **Hooks:** Nativos do Git (sem Node).

### 6. Decisões Finais
- **Repo:** `clone-angry-birds-2` (público desde o início).
- **Diretório:** Renomeado para `clone-angry-birds-2`.
- **Deploy:** Gratuito (local + opcional CI público).
- **Documentação:** Em `./docs` (markdown para humanos + JSON para agentes).

---

## ✅ Decisões Confirmadas (Checklist)

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

## 📊 Status Atual

- **Repo:** Criado (público) — `github.com/MarcosVRPereira/clone-angry-birds-2`
- **Diretório:** `clone-angry-birds-2` (renomeado)
- **Roadmap:** Concluído (`ROADMAP.md`)
- **Implementação:** Pendente (Fase 0 em diante)

---

*Última atualização: 2026-07-24. Este arquivo é consultado por agentes para manter o contexto.*
