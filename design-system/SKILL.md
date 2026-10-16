---
name: luso-bonsai
description: Usa esta skill sempre que fizeres qualquer peça da Luso Bonsai ou das suas linhas (Bonsai, Orchis by Luso Bonsai, Goshin, Basic Bonsai Tools) — site, loja, landing page, post, carrossel, reel, email, catálogo, etiqueta, autocolante, lona, apresentação. Contém a carta da marca, os tokens e os logótipos oficiais.
user-invocable: true
---

# Luso Bonsai

Antes de desenhar seja o que for, **lê `DESIGN.md`** nesta pasta. Os números vivem em `tokens.css`; quando os dois discordam, ganha o `tokens.css`. Logótipos e fotos estão em `assets/` (origem de cada logótipo em `assets/logos/LEIA-ME.md`): copia-os, nunca os recries.

**Regra guardiã:** se um valor não existe no `tokens.css`, não existe. Não inventes cores, fontes, tamanhos, cantos ou espaços, mesmo que o pedido os nomeie pelo código. Recusa, explica a regra numa frase e propõe acrescentar o valor ao `tokens.css` com nome e uso. Só avanças depois de aprovado.

## Regras duras (secção 6 do `DESIGN.md`)
1. **Cada linha tem a sua cor e o seu logótipo** (tabela «As linhas da marca»):
   - Luso Bonsai (marca-mãe): vermelho + preto sobre branco; símbolo «círculo rasurado».
   - Bonsai e Basic: fundo `--linha-bonsai` (vermelho); símbolo pequeno no rodapé.
   - Orquídeas: fundo `--linha-orquideas` (preto), nunca vermelho; logótipo `orchis-by-luso-bonsai.svg`.
   - Goshin: preto e branco, cinza `--linha-goshin-alt` como alternativa. **Nunca vermelho**, nem no hover. Logótipo `goshin-premium-bonsai-tools-circulo.svg`. Se levar o símbolo Luso Bonsai («Aproved by»), é `luso-bonsai-simbolo-preto.svg` (ou `luso-bonsai-simbolo-com-letras-por-baixo-preto.svg`): árvore preta, sol cinza K50, vector oficial da peça 11. Sobre branco. Nunca o símbolo vermelho na Goshin.
   - Na dúvida, é Luso Bonsai.
2. **Vermelho como texto só em letra grande:** `--marca-vermelho` só é texto a partir de 18 px bold (4,38:1). Texto corrido branco sobre vermelho nunca abaixo de 18 px bold no ecrã nem de `--tipo-min-impressao` (6 pt) impresso.
3. **Preto é `--marca-preto` (#231F20), nunca #000000.** Vermelho é `--marca-vermelho`, nunca o #FF0000 dos JPG antigos. Nada de azul, magenta ou roxo.
4. **Logótipo só de `assets/logos/`.** Para ecrã, `luso-bonsai-simbolo-com-letras-por-baixo-transparente.png`. Nunca redesenhar, recolorir, esticar ou pôr sombra. Nunca escrever «LUSO BONSAI» numa fonte a imitar o wordmark.
5. **Fontes:** `--fonte-display` (Russo One no ecrã) uma vez por peça, sempre em maiúsculas; tudo o resto `--fonte-texto` (Fira Sans) ou, impresso, `--fonte-texto-impressao`. Nunca Inter, Roboto, Arial, Agency FB, Arial Rounded.
6. **Padrões, só três e um de cada vez:** pincelada, círculo de pincel e 盆栽 num canto (tamanhos em `--padrao-*`). Os 盆栽 só como `caracteres-bonsai-pincel.jpg`, nunca em fonte. Nunca atrás de texto corrido, nunca em papel de parede.
7. **Cantos 0** (`--raio-cartao`, `--raio-botao`, `--raio-campo`) ou círculo (`--raio-circulo`). Sem gradientes, brilhos, sombras coloridas, nem emoji como ícone (Lucide, `--icone-traco`).
8. Nunca inventar preços, prazos, espécies ou idades de árvores.

## Impressão e ecrã
- **Impressão:** vermelho CMYK 0/100/100/0, preto K100, cinzas K10 a K50; Calamitech e Clan OT; margem `--margem-impressao` ao corte; logótipo mínimo `--logo-min-impressao`. Para gráfica, o JPG `-CMYK`.
- **Ecrã:** hex do `tokens.css`, Russo One e Fira Sans, grelha `--e-*` (múltiplos de 8), logótipo mínimo `--logo-min-ecra`. Medidas por superfície na secção 7 do `DESIGN.md`.

## Língua e tratamento
Português de Portugal, tratamento por **«você»**, muitas vezes sem pronome («visite-nos»). «Bonsai» com B maiúsculo e invariável no plural. Rótulos em PT, ES, EN, FR, por esta ordem. Slogans manuscritos: só a arte que já existe.

## PROPOSTAS abertas
Muitos valores de ecrã levam PROPOSTA (hex, fontes de ecrã, tamanhos, botões). A lista e o estado de cada uma estão em `PROPOSTAS.md`. Usa-as, mas marca-as como PROPOSTA na resposta. Não perguntes nada ao cliente: as PROPOSTAS decidem-se entre o Rui e o David.

## Ao entregar
Diz em 3 linhas: que linha da marca usaste, que tokens usaste e o que ficou marcado como PROPOSTA. Se te afastaste de algum valor, diz porquê e propõe acrescentá-lo ao `tokens.css` em vez de o deixares só na peça.
