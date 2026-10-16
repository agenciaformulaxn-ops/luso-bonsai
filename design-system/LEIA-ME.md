# Design system do cliente

Faz-se com o **kit da aula de design systems**:
`~/Documents/FormulaXN/Aulas ao Vivo /Design System/04-KIT-DESIGN-SYSTEM/`
(atenção: o nome da pasta «Aulas ao Vivo » acaba com um espaço)

- `CHECKLIST-novo-cliente.md` — os passos, por ordem.
- `PROMPTS.md` — os prompts para colar.
- `TEMPLATE-DESIGN.md`, `TEMPLATE-tokens.css`, `TEMPLATE-SKILL.md` — os moldes.

## O que vive aqui

| Pasta / ficheiro | O que é |
|---|---|
| `entrada/` | O que o cliente deu: site (URL.txt), manual em PDF, logótipos, capturas, peças de que gosta e de que não gosta. |
| `output/` | A medição automática do site (Dembrandt). Criada pela ferramenta. |
| `DESIGN.md` | A carta da marca (7 secções, menos de 300 linhas). |
| `tokens.css` | Os valores. Se não está aqui, não existe. |
| `SKILL.md` | A skill `luso-bonsai`. Feita a 2026-10-16. |
| `PROPOSTAS.md` | As decisões que o Rui e o David ainda têm de aprovar. |
| `assets/` | Logótipos e fotos oficiais. |
| `backups/` | Cópias antigas destes ficheiros. |

## A skill

A skill já existe e está instalada em `~/.claude/skills/luso-bonsai/` (cópia de `SKILL.md`, `DESIGN.md`, `tokens.css`, `PROPOSTAS.md` e `assets/`). Para a usar, peça «com a skill luso-bonsai» ou peça qualquer peça da Luso Bonsai.

**A fonte é esta pasta.** Quando mudar `DESIGN.md`, `tokens.css`, `PROPOSTAS.md`, `SKILL.md` ou `assets/`, volte a copiar para `~/.claude/skills/luso-bonsai/`. Nunca copiar `backups/`, `entrada/` nem `output/`: uma pasta `backups/` dentro das skills aparece como skill falsa.

Perguntas para enviar ao cliente: `ferramentas/questionario-marca-cliente.md`.

Exemplo acabado: `clientes/dr-peanut/design-system/`.
