<p align="center">
  <a href="#english">🇺🇸 English</a> |
  <a href="#portugues-br">🇧🇷 Português</a>
</p>

<h1 align="center">Skills</h1>

<p align="center">
  A collection of <a href="https://cursor.com">Cursor</a> Agent Skills for improving AI-assisted development workflows.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/platform-Cursor-blue" alt="Cursor">
  <img src="https://img.shields.io/badge/format-Markdown-orange" alt="Markdown">
  <img src="https://img.shields.io/badge/license-BSD--2--Clause-green" alt="BSD-2-Clause">
</p>

---

<a id="english"></a>

# 🇺🇸 English

This repository contains **Cursor Agent Skills** — markdown-based instruction sets that teach AI agents how to perform specialized tasks with higher quality and consistency.

Each skill lives in its own directory and includes a `SKILL.MD` file with YAML frontmatter, plus optional reference documents for deeper guidance.

---

## Available Skills

| Skill | Description |
|-------|-------------|
| [go-engineering](#go-engineering) | Idiomatic Go code generation, review, and refactoring |

---

## Installation

Skills can be installed globally (available in all projects) or per-project (shared with the team via the repository).

### Global (recommended for personal use)

Clone or copy the skill directory into your personal skills folder:

```bash
git clone https://github.com/ricrsantos/skills.git
cp -r skills/go-engineering ~/.cursor/skills/
```

### Per-project

Copy the skill into your project's `.cursor/skills/` directory:

```bash
mkdir -p .cursor/skills
cp -r /path/to/skills/go-engineering .cursor/skills/
```

Once installed, Cursor automatically discovers skills and applies them when the task matches the skill's description.

---

## go-engineering

**Improves the quality of Go code generation** by enforcing idiomatic Go, modern engineering practices, maintainability, performance, testing, and project organization.

Designed for implementation, code review, and refactoring tasks — **not** for defining application architecture or business rules.

### When to use

- Backend implementation
- Refactoring existing Go code
- Code review
- Bug fixing
- Performance improvements
- Test generation

### Engineering principles

The skill teaches agents to prioritize:

1. Correctness over cleverness
2. Readability over brevity
3. Simplicity over abstraction
4. Small, focused functions
5. Explicit behavior
6. Standard library whenever possible
7. Low coupling and high cohesion
8. Composition over unnecessary abstraction
9. Idiomatic Go

### What the agent always follows

- Produce idiomatic Go following Effective Go principles
- Keep APIs small and easy to understand
- Use meaningful names and self-explanatory code
- Return wrapped errors and respect context cancellation
- Write code that is easy to test
- Keep packages focused on a single responsibility
- Prefer standard library solutions first

### What the agent avoids

- Using `panic` for normal error handling
- Ignoring returned errors
- Creating unnecessary abstractions or generic interfaces without clear need
- Large utility packages, reflection, or premature optimization
- Deeply nested code and global mutable state

### Included documents

The skill is composed of specialized reference documents. The agent loads only what is relevant to the current task:

| Document | Focus |
|----------|-------|
| `effective-go.md` | Fundamental idiomatic Go principles |
| `package-design.md` | Package organization and API design |
| `error-handling.md` | Error wrapping, sentinel errors, and patterns |
| `concurrency.md` | Goroutines, channels, and synchronization |
| `testing.md` | Table-driven tests, mocks, and test structure |
| `performance.md` | Profiling, allocations, and optimization |
| `logging.md` | Structured logging and observability |
| `security.md` | Input validation, secrets, and safe defaults |
| `review-checklist.md` | Final review process before delivery |
| `examples/examples.md` | Practical before/after code examples |

### Skill metadata

```yaml
name: go-engineering
description: Improves the quality of Go code generation by enforcing idiomatic Go,
  modern engineering practices, maintainability, performance, testing, and project
  organization. This skill is intended for implementation, code review, and
  refactoring tasks.
version: 1.0.0
author: ricrsantos
```

---

## Project Structure

```text
.
├── go-engineering/
│   ├── SKILL.MD
│   ├── effective-go.md
│   ├── package-design.md
│   ├── error-handling.md
│   ├── concurrency.md
│   ├── testing.md
│   ├── performance.md
│   ├── logging.md
│   ├── security.md
│   ├── review-checklist.md
│   └── examples/
│       └── examples.md
├── LICENSE
└── README.md
```

---

## Contributing

Contributions are welcome.

1. Open an issue for bugs, feedback, or new skill ideas.
2. Fork the repository and create a branch from `main`.
3. Keep changes focused and follow the existing skill structure.
4. Open a Pull Request with a clear description.

---

## License

BSD 2-Clause. See [LICENSE](LICENSE).

---

<a id="portugues-br"></a>

# 🇧🇷 Português (BR)

Este repositório contém **Cursor Agent Skills** — conjuntos de instruções em markdown que ensinam agentes de IA a executar tarefas especializadas com maior qualidade e consistência.

Cada skill fica em seu próprio diretório e inclui um arquivo `SKILL.MD` com frontmatter YAML, além de documentos de referência opcionais para orientação mais detalhada.

---

## Skills Disponíveis

| Skill | Descrição |
|-------|-----------|
| [go-engineering](#go-engineering-1) | Geração, revisão e refatoração de código Go idiomático |

---

## Instalação

As skills podem ser instaladas globalmente (disponíveis em todos os projetos) ou por projeto (compartilhadas com a equipe via repositório).

### Global (recomendado para uso pessoal)

Clone ou copie o diretório da skill para a pasta pessoal de skills:

```bash
git clone https://github.com/ricrsantos/skills.git
cp -r skills/go-engineering ~/.cursor/skills/
```

### Por projeto

Copie a skill para o diretório `.cursor/skills/` do seu projeto:

```bash
mkdir -p .cursor/skills
cp -r /caminho/para/skills/go-engineering .cursor/skills/
```

Após a instalação, o Cursor descobre as skills automaticamente e as aplica quando a tarefa corresponde à descrição da skill.

---

## go-engineering

**Melhora a qualidade da geração de código Go** ao aplicar Go idiomático, práticas modernas de engenharia, manutenibilidade, performance, testes e organização de projetos.

Projetada para implementação, revisão de código e refatoração — **não** para definir arquitetura de aplicação ou regras de negócio.

### Quando usar

- Implementação de backend
- Refatoração de código Go existente
- Revisão de código
- Correção de bugs
- Melhorias de performance
- Geração de testes

### Princípios de engenharia

A skill ensina os agentes a priorizar:

1. Correção em vez de esperteza
2. Legibilidade em vez de brevidade
3. Simplicidade em vez de abstração
4. Funções pequenas e focadas
5. Comportamento explícito
6. Biblioteca padrão sempre que possível
7. Baixo acoplamento e alta coesão
8. Composição em vez de abstração desnecessária
9. Go idiomático

### O que o agente sempre segue

- Produzir Go idiomático seguindo os princípios do Effective Go
- Manter APIs pequenas e fáceis de entender
- Usar nomes significativos e código autoexplicativo
- Retornar erros encapsulados e respeitar cancelamento de contexto
- Escrever código fácil de testar
- Manter pacotes focados em uma única responsabilidade
- Preferir soluções da biblioteca padrão

### O que o agente evita

- Usar `panic` para tratamento normal de erros
- Ignorar erros retornados
- Criar abstrações desnecessárias ou interfaces genéricas sem necessidade clara
- Pacotes utilitários grandes, reflection ou otimização prematura
- Código profundamente aninhado e estado global mutável

### Documentos incluídos

A skill é composta por documentos de referência especializados. O agente carrega apenas o que é relevante para a tarefa atual:

| Documento | Foco |
|-----------|------|
| `effective-go.md` | Princípios fundamentais de Go idiomático |
| `package-design.md` | Organização de pacotes e design de APIs |
| `error-handling.md` | Encapsulamento de erros, sentinel errors e padrões |
| `concurrency.md` | Goroutines, channels e sincronização |
| `testing.md` | Testes table-driven, mocks e estrutura de testes |
| `performance.md` | Profiling, alocações e otimização |
| `logging.md` | Logging estruturado e observabilidade |
| `security.md` | Validação de entrada, secrets e defaults seguros |
| `review-checklist.md` | Processo de revisão final antes da entrega |
| `examples/examples.md` | Exemplos práticos de código antes/depois |

### Metadados da skill

```yaml
name: go-engineering
description: Improves the quality of Go code generation by enforcing idiomatic Go,
  modern engineering practices, maintainability, performance, testing, and project
  organization. This skill is intended for implementation, code review, and
  refactoring tasks.
version: 1.0.0
author: ricrsantos
```

---

## Estrutura do Projeto

```text
.
├── go-engineering/
│   ├── SKILL.MD
│   ├── effective-go.md
│   ├── package-design.md
│   ├── error-handling.md
│   ├── concurrency.md
│   ├── testing.md
│   ├── performance.md
│   ├── logging.md
│   ├── security.md
│   ├── review-checklist.md
│   └── examples/
│       └── examples.md
├── LICENSE
└── README.md
```

---

## Como Contribuir

Contribuições são muito bem-vindas.

1. Abra uma issue para bugs, feedback ou ideias de novas skills.
2. Faça fork do repositório e crie uma branch a partir da `main`.
3. Mantenha as alterações focadas e siga a estrutura existente das skills.
4. Abra um Pull Request com uma descrição clara.

---

## Licença

BSD 2-Clause. Veja [LICENSE](LICENSE).
