# 🗺️ Roadmap — Clone de Angry Birds 2

> **Projeto:** Jogo web 2D inspirado em Angry Birds 2
> **Repositório:** [github.com/MarcosVRPereira/clone-angry-birds-2](https://github.com/MarcosVRPereira/clone-angry-birds-2)
> **Status:** Planejamento concluído — Implementação pendente (Fase 0 em diante)
> **Data de criação:** 2026-07-24
> **Idioma:** Português Brasileiro (PT-BR)

---

## 🎯 Visão Geral

Desenvolver um jogo web 2D completo inspirado em Angry Birds 2, com física realista, 5 fases progressivas, sistema de pontuação, e seguindo boas práticas de código e testes.

### Stack Técnica Confirmada
| Categoria | Tecnologia |
|---|---|
| Runtime | **Bun** (100% — sem Node.js) |
| Linguagem | **TypeScript** |
| Renderização | **WebGL** |
| Engine 2D | **Phaser** |
| Física | **Matter.js** |
| Áudio | **Howler.js** |
| Build/Dev | **Vite** |
| Testes Unit | **Vitest** |
| Testes E2E | **Playwright** |
| Gerenciamento | **Bun** (package manager, scripts, test runner) |

### Princípios Transversais (aplicam-se a TODAS as fases)
1. **TDD por fase**: Escrever testes antes de cada implementação. **Só commitar se os testes passarem.**
2. **Context7**: Consultar documentação atualizada via Context7 para qualquer dúvida técnica. **Não insistir em erros — pesquisar.**
3. **100% Bun**: Sem Node.js em nenhum script (build/test/dev). Usar `bun run --bun` quando necessário.
4. **Gratuito**: Testes locais (Bun) como primário. GitHub Actions só se repo público (então grátis).
5. **PT-BR**: Interface e documentação em português brasileiro.
6. **Conventional Commits**: Regras de commit padronizadas (ver `CONVENTIONAL_COMMITS.md`).
7. **Documentação progressiva**: Documentar cada tarefa concluída em `./docs` (ver `docs/README.md`).

---

## 📦 Estrutura do Projeto

```
clone-angry-birds-2/
├── ROADMAP.md              # Este arquivo
├── HISTORY.md               # Log de decisões (humanos + agentes)
├── HISTORY.json             # Log de decisões estruturado (agentes)
├── ROADMAP.json             # Roadmap estruturado (agentes)
├── .git/                    # Repositório Git
├── src/                     # Código-fonte (TypeScript)
│   ├── core/                # Engine, estado, física
│   ├── entities/            # Pássaros, blocos, inimigos
│   ├── systems/             # Slingshot, colisão, dano, partículas
│   ├── ui/                  # UI, menus, HUD
│   ├── levels/              # Dados de níveis (JSON)
│   └── main.ts              # Entry point
├── assets/                  # Sprites, sons, ícones
├── levels/                  # Dados de níveis (JSON)
├── scripts/                 # Scripts utilitários (Bun)
├── tests/                   # Testes (unit + E2E)
├── docs/                    # Documentação (humanos + agentes)
└── public/                  # Arquivos estáticos (PWA, etc.)
```

---

## 🚀 Roadmap de Implementação

### Fase 0 — Setup & Tooling
- Inicializar projeto (Vite + TS + Bun)
- `package.json` com scripts via `bun run`
- Config: TS, ESLint, Prettier, Vitest
- Estrutura de pastas
- Git init + **hooks nativos** (`.git/hooks`, sem Node)
- `LICENSE` (MIT)
- Regras de commit (Conventional Commits)
- **Context7:** Vite+TS+Bun, ESLint, estrutura de pastas
- 🎯 *Recomendação:* validar `bun run dev` roda antes de prosseguir
- 📄 *Docs:* `docs/phases/00-setup/README.md` + `docs/phases/00-setup/summary.json`

### ⚙️ Fase 1 — Core Engine
- Bootstrap, cena principal, loop de render (WebGL)
- Input: mouse, touch, teclado
- Estado do jogo (State Machine)
- **Testes:** unit para state machine, input
- **Context7:** Phaser scene setup, WebGL rendering loop
- 🎯 *Recomendação:* testar que o loop renderiza sem crashar

### 🎱 Fase 2 — Física (Matter.js)
- Mundo Matter.js integrado ao Phaser
- Gravidade, colisões, collision masks
- Eventos de colisão
- **Testes:** unit para colisões, gravidade
- **Context7:** Matter.js integration with Phaser
- 🎯 *Recomendação:* testar que a física é estável (sem tunneling)

### 🏹 Fase 3 — Slingshot (gameplay central)
- Mecânica de arrastar/alisar (força + ângulo)
- Lançamento do pássaro
- Feedback visual de trajetória
- **Testes:** unit para cálculo de força/ângulo, E2E para arrastar/lançar
- **Context7:** slingshot mechanics, drag-to-aim UI
- 🎯 *Recomendação:* testar que o lançamento voa na direção correta

### 🐦 Fase 4 — Entidades
- Pássaros (**ilimitados**)
- Blocos/estruturas (madeira, concreto, vidro)
- Inimigos (porcos/alvos)
- Pool de objetos
- **Testes:** unit para spawn/destruição, E2E
- **Context7:** entity pooling, component patterns
- 🎯 *Recomendação:* testar que entidades spawnam e destroem corretamente

### 💥 Fase 5 — Colisão & Dano
- Detecção de impacto
- Cálculo de dano por material
- Destruição de blocos
- Vitória/derrota por inimigo
- **Testes:** unit para cálculo de dano, E2E
- **Context7:** collision detection, damage calculation
- 🎯 *Recomendação:* testar que dano é calculado corretamente por material

### 🗺️ Fase 6 — Sistema de Níveis
- Dados de nível (JSON)
- 5 fases com layouts
- Dificuldade progressiva
- Fase 4 com timer
- **Testes:** unit para loading/validação, E2E por fase
- **Context7:** level data structure, JSON-based levels
- 🎯 *Recomendação:* testar que todos os 5 níveis carregam e são jogáveis

### 🏆 Fase 7 — Pontuação & HUD
- Score, combos, multiplicadores
- Condições de vitória/derrota
- Timer (Fase 4)
- HUD: score, timer, pássaros
- **Testes:** unit para scoring, E2E para vitória/derrota
- **Context7:** scoring systems, HUD patterns
- 🎯 *Recomendação:* testar que pontuação e timer funcionam corretamente

### 🖥️ Fase 8 — UI & Menus
- Menu principal, seleção de nível
- Telas de vitória/derrota
- Configurações (som)
- **Tela de aviso** (antes da Splash)
- **Tutorial mode**
- **Testes:** E2E para navegação de menus
- **Context7:** UI state management, menu patterns
- 🎯 *Recomendação:* testar que todos os menus navegam corretamente

### 🔊 Fase 9 — Áudio (Howler.js)
- Efeitos sonoros
- Gerenciador de áudio
- **Testes:** E2E para verificação de sons
- **Context7:** Howler.js audio management
- 🎯 *Recomendação:* testar que sons tocam nos eventos corretos

### 🎨 Fase 10 — Assets
- Baixar sprites gratuitos (Python/Rust) **ou** gerar proceduralmente
- Sons + organização
- **Testes:** verificar carregamento de assets
- **Context7:** asset loading, sprite optimization
- 🎯 *Recomendação:* validar que todos os assets carregam sem erros

### ✨ Fase 11 — Partículas & Efeitos
- Efeitos de destruição
- Trails, "juice"
- **Testes:** E2E visual
- **Context7:** particle systems, visual effects
- 🎯 *Recomendação:* verificar que efeitos não quebram o jogo

### ♿ Fase 12 — Acessibilidade
- Modo reduzido movimento
- Contraste, telas de leitura
- Atalhos de teclado
- **Testes:** E2E de acessibilidade
- **Context7:** accessibility in web games, ARIA
- 🎯 *Recomendação:* verificar que o jogo é navegável por teclado

### 📱 Fase 13 — PWA & Responsividade
- Manifest, ícones, service worker
- Responsivo (horizontal → vertical)
- Favicon, Open Graph
- **Testes:** E2E responsivo, PWA install
- **Context7:** PWA setup, responsive design
- 🎯 *Recomendação:* testar install e offline

### 🧪 Fase 14 — Testes & Docs Finais
- Revisão completa de testes
- README, docs de arquitetura e níveis
- Configuração de deploy (gratuito)
- **Testes:** E2E completo, cross-browser
- **Context7:** deployment, documentation best practices
- 🎯 *Recomendação:* testar deploy e jogabilidade completa

---

## 💰 Estratégia de Deploy (Gratuito)

| Serviço | Custo | Observação |
|---|---|---|
| **Testes locais** (Bun) | 🆓 Grátis | Primário — sempre disponível |
| **GitHub Actions** | 🆓 Grátis | Só se repo público (ilimitado) |
| **GitHub Actions** (privado) | 💰 2000 min/mês grátis | Depois cobrado (~$0.008/min) |
| **Vercel** | 🆓 Free tier | Roda Bun nativamente (`vercel.json`) |
| **Netlify** | 🆓 Free tier | Alternativa |
| **GitHub Pages** | 🆓 Grátis | Para repos públicos |

> **Decisão:** Testes locais (Bun) como primário. GitHub Actions opcional (só se repo público). Deploy via Vercel/Netlify/GitHub Pages (gratuito).

---

## 📋 Checklist de Decisões (Confirmado)

- [x] Stack: TS + Bun + WebGL + Phaser + Matter.js + Howler.js + Vite
- [x] 5 fases, dificuldade progressiva
- [x] Pássaros ilimitados (como o original)
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

## 📚 Documentação

- **`docs/README.md`** — Índice de documentação (humanos)
- **`docs/decisions.md`** — Log de decisões (humanos)
- **`docs/decisions.json`** — Log de decisões estruturado (agentes)
- **`docs/phases/<fase>/README.md`** — Docs de cada fase (humanos)
- **`docs/phases/<fase>/summary.json`** — Resumo estruturado de cada fase (agentes)

> Cada tarefa concluída deve ser documentada em `./docs` para evitar alucinações e perda de contexto.

---

## 🚦 Próximos Passos

1. ✅ Repo criado: `github.com/MarcosVRPereira/clone-angry-birds-2` (público)
2. ✅ Diretório renomeado para `clone-angry-birds-2`
3. ⏳ **Aguardando início da Fase 0** (implementação)

---

*Roadmap gerado em 2026-07-24. Atualize conforme o progresso.*
