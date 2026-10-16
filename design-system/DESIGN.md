# DESIGN.md — Luso Bonsai

> **O que é este ficheiro.** A carta da marca: o que a IA lê antes de desenhar seja o que for para a Luso Bonsai.
> Quando este ficheiro e o `tokens.css` discordam, ganha o `tokens.css`.
> **Regra guardiã:** se um valor não existe aqui nem no `tokens.css`, não existe. Propõe-se, não se inventa.
> **Fonte que manda:** as 24 peças impressas enviadas pelo cliente. A imagem da marca está definida e aprovada nelas. Os números estão em `output/medicao.md`.
> **Site-actual** (luso-bonsai.com): é o site antigo, que vai ser substituído. Foi medido só como referência do «antes». Nenhum valor desta carta vem dele. O site novo, quando estiver pronto, serve para confirmar.
> Linhas com **PROPOSTA** são decisões nossas, sem base directa nas peças. Aguardam aprovação interna em `PROPOSTAS.md`.

---

## 1. Quem é a marca e como fala

- **O que faz:** produz, importa e distribui Bonsai desde 1996, em Santo Isidro de Pegões (Montijo). Também orquídeas, plantas especiais, ferramentas, adubos, substratos e vasos. Vende ao público (loja, encomendas, feiras) e a revendedores (catálogos).
- **Para quem:** amadores e coleccionadores de Bonsai e orquídeas; lojas e garden centers que revendem.
- **Personalidade em 3 palavras:** tradicional, conhecedora, próxima.
- **Tratamento:** **«você»**, muitas vezes sem pronome («Deixe o seu Bonsai num Hotel», «visite-nos»).
- **Língua:** português de Portugal. Rótulos em PT, ES, EN e FR, por esta ordem. Slogans de feira em inglês.
- **Escrita da palavra:** «Bonsai» com B maiúsculo e invariável no plural («os nossos Bonsai»).
- **3 frases que a marca diz** (copiadas das peças):
  1. «Dedicamo-nos ao Bonsai desde 1996, como produtores, importadores e distribuidores.» (catálogo, peça 21)
  2. «Todos os nossos Bonsai são 100% climatizados ou produzidos em Portugal.» (etiqueta, peça 3)
  3. «Your connection with nature…» (lonas 14 e 15, cartão 6)
- **Nunca diria:** gíria de redes sociais, promessas milagrosas («a planta que nunca morre»), português do Brasil («nosso catálogo» sem artigo).
- **Sentir:** loja de especialista com raiz japonesa — pincel, círculo de sol, caracteres 盆栽. Não é minimalismo «zen» de revista nem garden center genérico.

---

## 2. Cores

As peças usam **sempre as mesmas tintas**: vermelho CMYK 0/100/100/0 e preto K100, sobre branco, com cinzas de preto (K10 a K50). O hex de ecrã é a conversão dessas tintas pelo perfil de impressão padrão, por isso leva PROPOSTA: no ecrã não existe «o» hex de uma tinta.

| Token | Hex (ecrã) | Impressão (medido) | Papel | Texto sobre claro? |
|---|---|---|---|---|
| `--marca-vermelho` | `#ED1C24` PROPOSTA | CMYK 0/100/100/0 · Pantone 485 | Linha Bonsai, símbolo, títulos de secção, preços | **só ≥ 18 px bold** (4,38:1) |
| `--marca-preto` | `#231F20` PROPOSTA | K100; fundos grandes 100/100/100/100 | Texto, linha Orquídeas, linha Goshin, botões | sim (16,3:1) |
| `--marca-branco` | `#FFFFFF` | papel (0/0/0/0) | Fundo de quase todas as peças | — |
| `--marca-cinza-escuro` | `#706D6E` PROPOSTA (pixel) | frente da etiqueta | Frente da etiqueta pendurada; texto secundário | sim (5,12:1) |
| `--marca-cinza-medio` | `#918F8F` PROPOSTA | K50 | Pormenores, contornos | não (3,22:1) |
| `--marca-cinza-goshin` | `#A7A5A6` PROPOSTA | K40 | Fundo alternativo Goshin | não — gráfica |
| `--marca-cinza-claro` | `#E9E8E8` PROPOSTA | K10 | Pincelada de rodapé, filetes, fundos de campo | não — gráfica |

**Regras de cor:**
- Base de quatro cores, como o cliente escreveu: **vermelho, preto, cinza, branco.** Nada mais.
- Uma cor de identidade por peça: **vermelho (Bonsai) ou preto (Orquídeas, Goshin)**. O vermelho do símbolo é a única excepção — vai no logótipo em qualquer linha, menos no Goshin: aí o símbolo Luso Bonsai («Aproved by») vai na versão a uma tinta — árvore e vaso a preto K100, sol a cinza K50 (peça 11). Ficheiro: `assets/logos/luso-bonsai-simbolo-preto.svg` (com letras: `luso-bonsai-simbolo-com-letras-por-baixo-preto.svg`), vector extraído da peça 11. Usar sobre branco, como na peça.
- Sem gradientes de cor. O único efeito da marca é a pincelada (traço de pincel com bordo irregular), sempre numa cor lisa.
- Sem sombras coloridas nem brilhos.
- Branco sobre vermelho: títulos grandes e grossos. Texto corrido branco sobre vermelho só nos rótulos de produto (como na peça 8), com o mínimo da secção 7.

### As linhas da marca: que cor manda, que logótipo

| Linha | Quando se usa | Cor que manda | Logótipo | Peças de referência |
|---|---|---|---|---|
| **Luso Bonsai** (marca-mãe) | Empresa, cartões, catálogos, lonas, site, tudo o que não é de uma linha | vermelho + preto sobre branco | Símbolo «círculo rasurado» (árvore preta sobre sol vermelho), com «LUSO BONSAI» por baixo ou ao lado | 1, 2, 6, 10, 14, 15, 21 |
| **Bonsai** (produtos) | Adubos, substratos, folhetos, etiquetas de árvores — tudo o que é para Bonsai | **fundo vermelho** | Símbolo Luso Bonsai pequeno, no rodapé | 3, 4, 8, 18 (Akadama, Pomice) |
| **Orquídeas · «Orchis by Luso Bonsai»** | Adubos, substratos e catálogo de orquídeas e plantas especiais | **fundo preto** | Logótipo Orchis (a flor faz o «O»; «By:» + símbolo Luso Bonsai pequeno) | 16, 17, 18 (Hidroton, Casca, Coco), 19, 22 |
| **Goshin · Premium Bonsai Tools** | Ferramentas premium (marca própria) | **preto + branco**, cinza K40 como alternativa. **Sem vermelho** (nenhuma das 3 peças o tem) | «GOSHIN / BONSAI TOOLS» com «Premium» na vertical; círculo preto com bordo de pincel. Símbolo Luso Bonsai («Aproved by»): `luso-bonsai-simbolo-preto.svg`, nunca o vermelho | 11, 12, 13 |
| **Basic · Bonsai Tools** (gama económica) | Ferramentas de entrada | vermelho + branco (é linha Bonsai) | Título «BONSAI TOOLS» + caracteres 盆栽 grandes a vermelho; símbolo Luso Bonsai no verso | 9 |

**Como decidir:** é sobre Bonsai ou para quem trata Bonsai → vermelho. É sobre orquídeas → preto + Orchis. É uma ferramenta Goshin → preto e branco, nunca vermelho. Na dúvida, é Luso Bonsai (marca-mãe).

---

## 3. Tipografia

As peças usam fontes pagas ou de autor. Ficam duas colunas: **impressão** (as fontes medidas nas peças) e **ecrã** (substitutas do Google, PROPOSTA).

| Papel | Impressão (medido) | Ecrã | Peso | Tamanho ecrã | Caixa |
|---|---|---|---|---|---|
| Display (título principal, nome do produto) | **Calamitech** (rótulos 2026) · Capital Daren (peças antigas) | **Russo One** PROPOSTA | 400 (a fonte já é grossa) | 56 px PROPOSTA | **SEMPRE MAIÚSCULAS** |
| Título | Clan OT Black | **Fira Sans** PROPOSTA | 700 | 32 px PROPOSTA | frase |
| Subtítulo | Clan OT Bold | Fira Sans | 500 | 24 px PROPOSTA | frase |
| Corpo | **Clan OT News** | Fira Sans | 400 | 16 px, entrelinha 1,5 PROPOSTA | frase |
| Etiqueta | Clan OT Black (prefixos «PT:», «ES:») | Fira Sans | 700 | 12 px, espaçamento 0,08 em PROPOSTA | maiúsculas |
| Botão | — | Fira Sans | 500 | 16 px PROPOSTA | frase |

Tamanhos nas peças: display 48–56 pt no rótulo de 1 l, 80 pt no A4; texto Clan 5,6–7,6 pt nos rótulos, 14 pt no A4.

**A lei da hierarquia:** a fonte de display (letra quadrada e grossa, a do wordmark) aparece **uma vez por peça**, em maiúsculas, para o nome do produto ou o título principal. Tudo o resto é Clan (impressão) ou Fira Sans (ecrã).

**Acentos de assinatura (não são texto):**
- **Letra manuscrita** dos slogans («Your connection with nature…», «“Feel” the Difference», «Beauty in its purest form…»). Nome da fonte desconhecido. Até haver o ficheiro, **reutiliza-se a arte existente; não se escrevem slogans novos à mão.**
- **Brush Script Std** só para o nome da variante («Activ», «Humic») junto ao título display. Ecrã: sem substituta.
- **Caracteres 盆栽** («árvore em vaso»): imagem de pincel `assets/logos/caracteres-bonsai-pincel.jpg`. Nunca escritos com uma fonte qualquer.

**Fontes proibidas em peças novas:** Agency FB, Arial Rounded, Arial Narrow, Angsana New (catálogos antigos), Inter, Roboto, Arial, qualquer fonte de sistema.

---

## 4. Espaço, cantos e sombras

- **Grelha (ecrã):** 8 px; tudo múltiplo de 8 (8, 16, 24, 32, 48, 64, 96), com 4 px só para afinar. PROPOSTA.
- **Largura de conteúdo:** 1200 px; texto corrido até 640 px. PROPOSTA.
- **Cantos:** as peças só têm **cantos rectos** (folheto, blisters, cartões, rótulos) ou **círculo completo** (autocolantes, etiqueta, foto do rótulo). Ecrã: 0 px em botões, campos e cartões; círculo em selos e fotos redondas. Nada de cantos arredondados intermédios.
- **Sombras:** nenhuma nas peças. Ecrã: nenhuma por defeito; uma subtil só para cartões de produto, `0 1px 4px rgba(35,31,32,.10)`. PROPOSTA.
- **Linhas:** 1 px, `--marca-cinza-claro`.
- **Margem nas peças impressas:** conteúdo a 5 mm do corte, no mínimo. PROPOSTA.
- **Movimento (ecrã):** 150 / 250 / 400 ms, `ease-out`. Respeitar `prefers-reduced-motion`. PROPOSTA.

---

## 5. Componentes (os que se vêem nas peças)

- **Símbolo «círculo rasurado»:** árvore preta sobre um sol vermelho de bordo de pincel, vaso com 盆栽 a branco. É a base de tudo. Ficheiros em `assets/logos/`. Nunca redesenhar.
- **Pincelada:** faixa de bordo irregular de pincel — vermelha no topo (folheto, catálogos), cinza K10 no rodapé (cartão, folheto, catálogos), branca a «rasgar» o vermelho (blister Basic) ou o preto (Goshin). É o elemento gráfico que liga as peças.
- **Círculo de pincel:** círculo com bordo rasurado como moldura (verso do cartão, autocolante da caixa B2C, Goshin, terras).
- **Rótulo de produto (adubo):** fundo inteiro na cor da linha; foto da planta num círculo ao centro; nome do produto em display branco; variante em script; texto em 4 línguas em colunas laterais (Clan, branco); código de barras, QR, reciclagem e logótipo pequeno no rodapé.
- **Autocolante circular de substrato:** círculo cheio na cor da linha, nome em display branco no topo, texto em 4 línguas ao centro, logótipos no fundo.
- **Botão (ecrã):** fundo preto, texto branco Fira Sans, cantos 0, padding 8 × 16 px. Hover: vermelho. PROPOSTA (as peças não têm botões).
- **Preço:** preto ou vermelho, bold. Preço antigo riscado em cinza escuro, mais pequeno. PROPOSTA.
- **Selo de desconto:** rectângulo ou círculo vermelho, texto branco bold, cantos 0. PROPOSTA.
- **Logótipo — espaço livre:** à volta, pelo menos a altura do vaso do símbolo. Tamanho mínimo: 15 mm impresso, 48 px no ecrã. PROPOSTA.
- **Ícones:** as peças só usam o símbolo de reciclagem e o QR. Em peças novas: Lucide, traço 1,75 px, preto ou branco. PROPOSTA. Nunca emoji.
- **Fotografia:** a planta recortada sobre branco (lonas, catálogos) ou dentro de um círculo (rótulos). Luz de estúdio limpa, sem cenário. Mãos a trabalhar a árvore são a excepção aceite (Goshin).
- **Fotografia de ambiente** (capas, banners, apresentações): viveiro ou bancada com luz natural lateral e suave, cores verdadeiras, fundo desfocado. Goshin em preto, branco e cinza, sem vermelho; Orchis sobre fundo escuro. Sem filtros, sem texto, sem caracteres nem marcas inventadas. Imagens geradas: `assets/fotos/gerada-ia-*`; prompts em `output/prompts-imagens.md`. PROPOSTA.


### Componentes de ecrã (site e loja) — PROPOSTA

As peças são impressas; estes nascem delas para o ecrã. Todos PROPOSTA.

- **Botões:** principal preto, texto branco, cantos 0; hover vermelho. **Na linha Goshin o hover é cinza K40, nunca vermelho.** Secundário: contorno preto 1 px, fundo branco. Foco: contorno preto 2 px afastado 2 px.
- **Cartão de produto:** foto da planta sobre branco, nome (Fira Sans 500), idade e habitat por baixo, preço em vermelho bold, preço antigo riscado. Selos no canto superior esquerdo. Hover: a foto sobe 4 px e aparece a borda preta.
- **Selos:** desconto (vermelho, «-9%»), Novo (preto), VIP (preto), habitat (contorno: Interior, Exterior, Dupla localização), Sem stock (cinza escuro). Cantos 0.
- **Formulário:** campos com fundo cinza 10, sem borda, 48 px de altura, cantos 0. Foco: contorno preto. Erro: linha vermelha por baixo + mensagem vermelha curta com ícone. Sucesso: bloco branco com visto preto e texto de agradecimento.
- **Avisos:** caixa branca com sombra 2, faixa de 4 px à esquerda (preta = feito; cinza = sem stock). Desaparecem sozinhos ao fim de uns segundos.
- **Carrinho lateral:** entra pela direita (400 px), véu escuro por trás, linhas de produto com foto, quantidade e preço; total e botão preto em baixo.
- **Acordeão de cuidados:** Localização, Rega, Adubo, Poda, Transplante, com o texto do folheto. Ícone de traço à esquerda, chevron à direita.
- **Cabeçalho:** faixa fina preta com portes grátis; logótipo à esquerda, pesquisa ao centro, conta e carrinho à direita; menu por baixo. **Rodapé:** pincelada cinza no topo, 4 colunas (loja, serviços, ajuda, contactos), linha final com o nome legal.
- **Ícones:** Lucide, traço 1,75, 24 px (16 px em linha de texto), preto ou branco. Nunca vermelho sobre vermelho, nunca preenchidos.
- **Fundos e padrões** (origem: pincelada — peças 4, 6, 21, 22; círculo de pincel — peças 5, 6, 12, 18; 盆栽 — peças 9 e 23; tamanhos em `--padrao-*`, PROPOSTA). Sobre vermelho, padrão a branco; sobre branco, a vermelho; Orchis sobre preto, a branco; Goshin só preto, branco e cinza. Nunca dois padrões juntos, nunca atrás de texto pequeno, nunca a competir com a planta. Só três, todos das peças: a **pincelada** (topo vermelho ou rodapé cinza), o **círculo de pincel** (moldura de foto ou selo) e os **caracteres 盆栽** em grande, a vermelho sobre branco ou a branco sobre vermelho, a ocupar um canto. Nunca atrás de texto corrido, nunca repetidos em papel de parede, nunca na Goshin a vermelho.
- **Movimento:** 150 ms (hover), 250 ms (abrir e fechar), 400 ms (entrar). Ao fazer scroll, os blocos sobem 16 px e aparecem uma vez. Nada salta, nada roda. Com `prefers-reduced-motion`, tudo fica parado.

---

## 6. O que nunca se faz

1. Nunca usar uma cor que não esteja no `tokens.css`, mesmo que o pedido a nomeie pelo código.
2. Nunca misturar linhas: **vermelho nunca em peças Goshin**; o fundo das peças de orquídeas é preto, nunca vermelho.
3. Nunca redesenhar, recolorir, esticar ou pôr sombra no símbolo. Usar os ficheiros de `assets/logos/`. Nunca escrever «LUSO BONSAI» com uma fonte para imitar o wordmark.
4. Nunca escrever os caracteres 盆栽 com uma fonte de sistema: só a imagem de pincel ou os que estão dentro do logótipo.
5. Nunca a fonte de display em minúsculas, nem em texto corrido, nem mais de uma vez por peça.
6. Nunca texto corrido branco sobre vermelho abaixo de 6 pt impresso / 18 px bold no ecrã.
7. Nunca gradientes, brilhos, sombras coloridas ou cantos arredondados intermédios.
8. Nunca emoji como ícone.
9. Nunca inventar preços, prazos, espécies ou idades de árvores. Usar só o que o cliente deu.
10. Nunca português do Brasil.
11. **Desvio actual a corrigir — catálogos:** os catálogos 21 e 22 escrevem preços e destaques a azul (`#6666FF`, `#000080`) e usam Agency FB e Arial Rounded. Em peças novas: preços a preto ou vermelho, texto em Clan / Fira Sans.
12. **Desvio actual a corrigir — magenta nas terras:** o autocolante «Terra Orquídeas Epífitas» (peça 18) usa magenta CMYK 0/100/0/0. A linha de orquídeas é preta; o magenta não entra.
13. **Desvio actual a corrigir — vermelho puro no digital:** os JPG do logótipo e os catálogos usam `#FF0000`. Em peças digitais novas, só `--marca-vermelho`.
14. **Site-actual (referência, vai ser substituído):** usa um roxo (`#4A1CA3`) na etiqueta «Novo», cinco fontes misturadas (Fira Sans, Noto Sans, Open Sans, Arial, Roboto) e frases em português do Brasil. Nada disto passa para peças novas.

---

## 7. Lei por superfície

**Etiqueta pendurada (91 × 165 mm, forma de «8», duas faces)**
- Frente: fundo `--marca-cinza-escuro`, símbolo no círculo de baixo, «LUSO BONSAI» a branco, site no círculo de cima de pernas para o ar (a etiqueta dobra).
- Verso: fundo branco, contorno do «8» em linha fina, título «BONSAI» em display, instruções (Localização, Rega, Adubo, Transplante) em texto pequeno centrado.
- Autocolante «BI» do verso (espécie, idade, localização, preço): fundo branco, texto preto. PROPOSTA (não veio exemplo).

**Autocolante de produto (adubo 200 ml e 1 l; 12 produtos)**
- Fundo inteiro: vermelho (Bonsai) ou preto (Orquídeas). Uma das duas, nunca as duas.
- Foto da planta num círculo ao centro; nome em display branco por cima; variante em script.
- Texto corrido Clan, branco, mínimo 6 pt PROPOSTA (o rótulo de orquídeas usa 4,5 pt).
- Rodapé: código de barras, QR, reciclagem, logótipo da linha, volume.

**Autocolante circular (substratos, personalizações, caixa B2C, Goshin)**
- Círculo cheio na cor da linha ou círculo de pincel preto. Título display branco no arco de cima. Site no arco de baixo.

**Lona de feira (horizontal)**
- Fundo branco. Planta recortada a um lado. Slogan em letra manuscrita preta ao centro. Logótipo pequeno no canto inferior direito.
- Bonsai: logótipo Luso Bonsai. Orquídeas: logótipo Orchis. Goshin: cartão de feira próprio (600 × 600 mm, fundo preto ou cinza K40).

**Folheto e documentos A4/A5**
- Pincelada vermelha no topo com o título em display branco; pincelada cinza no rodapé com logótipo e contactos.
- Texto Clan a preto, títulos de parágrafo em bold. Fotos pequenas à esquerda do texto.

**Catálogo de revenda (A4)**
- Faixa de pincel no topo: vermelha (Bonsai) ou preta (Orquídeas). Rodapé com pincelada cinza e `www.luso-bonsai.com`.
- Tabelas de preços a preto, filetes cinza claro. Ver regra 11.

**Landing page**
- Fundo branco. Logótipo à esquerda no cabeçalho. Um título display em maiúsculas (vermelho ou preto). Botão preto, cantos 0.
- Preços e destaques a vermelho. Uma pincelada como separador de secção, não mais.

**Post de Instagram (1080 × 1350)**
- Fundo branco com a planta recortada (como nas lonas), ou fundo inteiro na cor da linha com a planta num círculo (como nos rótulos).
- Título display em maiúsculas, branco sobre a cor ou preto sobre branco. Logótipo pequeno no canto inferior direito.

**Apresentação (1920 × 1080)**
- Fundo branco; pincelada vermelha no topo só no slide de abertura. Um título por slide (Fira Sans 700; display só na capa).
- Logótipo pequeno no canto inferior direito. Máximo 3 pontos por slide.

**Email**
- Cabeçalho com logótipo sobre branco, um botão preto, rodapé com pincelada cinza. Tratamento por «você».
- Largura 600 px. Pincelada vermelha no topo, título display, 1 botão. Uma só oferta por email. PROPOSTA.

**Reel (1080 × 1920, até 10 s, sem voz)** — PROPOSTA; exemplo em `../pecas/reel/`
- Tudo o que importa entre y = 285 e y = 1635 (o feed corta a 4:5). Logótipo grande no fecho, com luso-bonsai.com.
- Movimento calmo: entradas e trocas de cena de 400 ms, títulos linha a linha com 150 ms entre linhas. Nada salta, roda ou brilha.
- Só duas coisas se desenham: os 盆栽 de cima para baixo e a pincelada da esquerda para a direita (600 a 800 ms). O sol entra a subir e a crescer de 92% para 100%.
- Fontes locais dentro do projecto (Russo One e Fira Sans em woff2), para o render sair sempre igual.

**Carrossel de Instagram (1080 × 1350)**
- Capa na cor da linha com a planta num círculo e o título; slides do meio brancos, um conselho por slide, número grande a vermelho; último slide na cor da linha com o logótipo e a chamada. PROPOSTA.

---

*Ficheiro gerado a 2026-10-16 a partir das 24 peças impressas enviadas pelo David (caminho B2). O site-actual foi medido só como referência do «antes». Linhas PROPOSTA aguardam aprovação interna (Rui e David) — ver `PROPOSTAS.md`. Confirmar contra o site novo quando estiver pronto.*
