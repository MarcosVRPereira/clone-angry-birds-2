# 🎮 Clone de Angry Birds 2

> Jogo web 2D inspirado em Angry Birds 2, com física realista, 5 fases progressivas e sistema de pontuação.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Bun](https://img.shields.io/badge/built%20with-Bun-326626.svg?style=flat-square)](https://bun.sh/)
[![TypeScript](https://img.shields.io/badge/typescript-%23007033.svg?style=flat-square)](https://www.typescriptlang.org/)
[![Phaser](https://img.shields.io/badge/Phaser-2D-%23CF553D.svg?style=flat-square)](https://phaser.io/)
[![Matter.js](https://img.shields.io/badge/Matter.js-Física-%238E44AD.svg?style=flat-square)](https://brm.io/matter-js/)

---

## 🎯 Visão Geral

Um clone de Angry Birds 2 desenvolvido como projeto web, utilizando as tecnologias modernas para jogos na web. O jogo permite lançar pássaros com física realista (slingshot), destruir blocos e estruturas, e eliminar todos os inimigos em 5 fases progressivas.

### ✨ Características
- 🎯 **Física realista** — Slingshot com tração, resistência do ar e colisões elásticas (Matter.js)
- 🗺️ **5 fases** — Layouts diferentes com dificuldade progressiva
- 🐦 **Pássaros ilimitados** — Como no jogo original
- ⏱️ **Desafio de tempo** — Fase 4 com timer
- 🏆 **Sistema de pontuação** — Score, combos e multiplicadores
- ♿ **Acessível** — Navegável por teclado, modo reduzido movimento
- 📱 **Responsivo** — Funciona em desktop e mobile (horizontal → vertical)
- 🎨 **PWA** — Instalável e offline (atualização futura)

---

## 🛠️ Stack Técnica

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

---

## 🚀 Como Rodar

### Pré-requisitos
- [Bun](https://bun.sh/) instalado (v1.x ou superior)

### Instalação
```bash
# Instalar dependências
bun install

# Iniciar servidor de desenvolvimento
bun run dev
```

### Scripts Disponíveis
```bash
bun run dev      # Iniciar servidor de desenvolvimento (Vite)
bun run build    # Build de produção
bun run preview  # Preview do build
bun run test     # Rodar todos os testes (unit + E2E)
bun run test:unit # Rodar testes unit
bun run test:e2e  # Rodar testes E2E
bun run lint     # Rodar linter
bun run typecheck # Verificar tipos TypeScript
```

---

## 📁 Estrutura do Projeto

```
clone-angry-birds-2/
├── src/                     # Código-fonte (TypeScript)
│   ├── core/                # Engine, estado, física
│   ├── entities/            # Pássaros, blocos, inimigos
│   ├── systems/             # Slingshot, colisão, dano, partículas
│   ├── ui/                  # UI, menus, HUD
│   └── levels/               # Dados de níveis (JSON)
├── assets/                  # Sprites, sons, ícones
├── levels/                  # Dados de níveis (JSON)
├── scripts/                 # Scripts utilitários (Bun)
├── tests/                   # Testes (unit + E2E)
├── docs/                    # Documentação (humanos + agentes)
└── public/                  # Arquivos estáticos (PWA, etc.)
```

---

## 📚 Documentação

- **[ROADMAP.md](ROADMAP.md)** — Roadmap completo do projeto
- **[HISTORY.md](HISTORY.md)** — Log de decisões
- **[docs/README.md](docs/README.md)** — Índice de documentação
- **[docs/decisions.md](docs/decisions.md)** — Log de decisões (humanos)
- **[docs/decisions.json](docs/decisions.json)** — Log de decisões (agentes)
- **[docs/phases/](docs/phases/)** — Documentação de cada fase

---

## 🧪 Testes

O projeto segue **TDD por fase** — testes são escritos antes de cada implementação, e só se commita se os testes passarem.

```bash
bun run test          # Rodar todos os testes
bun run test:unit     # Testes unit (Vitest)
bun run test:e2e      # Testes E2E (Playwright)
```

---

## 🎮 Como Jogar

1. Acesse `http://localhost:5173` (ou o URL do servidor de desenvolvimento)
2. Arraste o pássaro para ajustar força e ângulo
3. Solte para lançar
4. Destrua todos os inimigos antes do tempo acabar
5. Avance pelas 5 fases!

---

## 🤝 Contribuindo

1. Faça um fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m "Add some AmazingFeature"`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

### Regras de Commit
Siga as regras de [Conventional Commits](CONVENTIONAL_COMMITS.md):
- `feat: ` — Nova feature
- `fix: ` — Correção de bug
- `docs: ` — Documentação
- `style: ` — Formatação, sem mudança de lógica
- `refactor: ` — Refatoração
- `test: ` — Adicionar/corriger testes
- `chore: ` — Alterações de processo/tooling

---

## 📄 Licença

Este projeto está licenciado sob a [MIT License](LICENSE).

---

## 🙏 Agradecimentos

- [Phaser](https://phaser.io/) — Engine 2D
- [Matter.js](https://brm.io/matter-js/) — Física 2D
- [Howler.js](https://howlerjs.com/) — Áudio
- [Bun](https://bun.sh/) — Runtime
- [Vite](https://vitejs.dev/) — Build tool

---

## 📞 Contato

- **Autor:** Marcos V R Pereira
- **Email:** mvrpj@msn.com
- **GitHub:** [github.com/MarcosVRPereira/clone-angry-birds-2](https://github.com/MarcosVRPereira/clone-angry-birds-2)

---

*Projeto criado em 2026. Desenvolvido com 💛 usando Bun, TypeScript e Phaser.*
