# Medição · Luso Bonsai

> Feita a 2026-10-16 sobre as 24 peças enviadas pelo David (`entrada/material-david-20261016/`).
> **As peças impressas são a fonte que manda.** A imagem da marca já está definida e aprovada nelas.
> O site no ar (luso-bonsai.com) é o **site-actual**, o «antes»: vai ser substituído pelo site novo que a agência está a fazer. Foi medido só como referência e **nenhum valor do `tokens.css` vem dele**.
> Aqui só há números e de onde vieram. A interpretação está no `DESIGN.md`.

## Como se mediu

- **Fontes:** `pdffonts` em cada PDF + PyMuPDF para saber que texto usa que fonte e a que tamanho. No `.odg` (peça 7) leu-se o `content.xml`.
- **Cores dos PDF:** `qpdf --qdf --object-streams=disable` e contagem dos operadores de cor (`k`/`K` = CMYK, `rg` = RGB). Os nomes Pantone saíram das definições `/Separation`.
- **CMYK → hex:** renderizado com `pdftoppm` (Poppler, perfil CMYK padrão) e amostrados os píxeis das zonas sólidas. **Toda a conversão CMYK → hex é PROPOSTA**: no ecrã não existe «o» hex de uma tinta.
- **JPG:** píxeis amostrados com PIL.
- **Site-actual (só referência):** `npx dembrandt https://luso-bonsai.com/pt/ /pt/3-Bonsai --dtcg --wcag --brand-guide --design-md --save-output` → `output/luso-bonsai.com/`.

## 1. Cores medidas nas peças impressas

| Cor | Valor exacto no ficheiro | Hex convertido (PROPOSTA) | Peças onde aparece |
|---|---|---|---|
| Vermelho | **CMYK 0 / 100 / 100 / 0** | `#ED1C24` | 6, 8, 9, 10, 16, 17, 18 (sempre o mesmo valor) |
| Vermelho (tinta directa) | **PANTONE 485 CV** | `#DA291C` (referência Pantone 485 C) | 3 (etiqueta) |
| Vermelho (imagem embebida) | RGB | `#E3000F` | 4 (folheto, faixa do topo) |
| Preto | **CMYK 0 / 0 / 0 / 100** | `#231F20` | todas |
| Preto «rico» (fundos grandes) | CMYK 100 / 100 / 100 / 100 | `#231F20` (no ecrã igual) | 6, 11, 13, 17, 18 |
| Cinza 50 % | CMYK 0 / 0 / 0 / 50 | `#918F8F` | 5, 9, 11 |
| Cinza 40 % (fundo Goshin) | CMYK 0 / 0 / 0 / 40 | `#A7A5A6` | 13 (verso) |
| Cinza 10 % (pincelada de rodapé) | CMYK 0 / 0 / 0 / 10 | `#E9E8E8` | 6, 17 |
| Cinza escuro da etiqueta | mistura com transparência | `#706D6E` (pixel) | 3 (frente) |
| Branco | CMYK 0 / 0 / 0 / 0 | `#FFFFFF` | todas |
| Verde e azul (bandeira / linha de corte) | PANTONE 349 CV, PANTONE 288 CV | — | 3 (etiqueta) — não são cores de marca |
| **Magenta** | CMYK 0 / 100 / 0 / 0 | `#EC008C` | 18 (Terra Orquídeas Epífitas) — **fora da paleta** |
| Verde «PROVA 03» | CMYK 48 / 0 / 59 / 0 | — | 18 — carimbo da gráfica, não é marca |

**Logótipos em JPG:**

| Peça | Vermelho | Preto |
|---|---|---|
| 1 · logo símbolo (RGB) | `#FE0000` / `#FF0000` | `#000000` |
| 2 · logo com letras (CMYK) | CMYK 0/100/100/0 (→ `#FF0000` sem perfil) | CMYK 0/0/0/100 |
| 23 · caracteres 盆栽 (pincel) | `#DF0001` a `#E30103` (varia com o traço) | — |

**Catálogos (21, 22 — feitos em LibreOffice, RGB):**

| Cor | Hex | Onde |
|---|---|---|
| Vermelho da faixa do topo | `#FD0000` / `#FE0000` (imagem) | cabeçalho de todas as páginas |
| Vermelho de texto | `#C9211E` | 1 ocorrência por catálogo |
| Cinza da pincelada de rodapé | `#E4E4E4` | rodapé |
| **Azul dos preços** | `#6666FF`, `#9999FF`, `#000080` | tabelas e destaques — **fora da paleta** |
| Cinza de texto | `#C0C0C0` | notas |

## 2. Site-actual (referência do «antes», não é fonte)

| Hex | Ocorrências | Uso observado | Contraste sobre branco |
|---|---|---|---|
| `#FFFFFF` | 899 | fundo | — |
| `#2E2323` | 534 | texto escuro | 15,21:1 |
| `#777777` | 191 | texto secundário | 4,48:1 (falha AA por pouco) |
| `#E31E24` | 181 | preços, títulos de secção («CAMPANHA»), etiqueta de desconto | 4,69:1 (passa AA) |
| `#000000` | 122 | botões, navegação | 21:1 |
| `#4A1CA3` | 30 | etiqueta «Novo» — **roxo, fora da paleta** | 10,57:1 |
| `#F8F8F8` | — | fundo dos campos de pesquisa | — |
| `#D0121A`, `#DD3333` | poucos | variações do vermelho | 5,55 / 4,57 |

Botão observado: fundo `#000000`, texto branco, cantos **0 px**, `7.5px 15px`, Fira Sans 15 px / 400.
Campos: fundo `#F8F8F8`, sem borda, cantos 0 px.
Sombras: `rgba(0,0,0,.1) 1px 1px 4px`; `rgba(0,0,0,.15) 1px 1px 30px`.
Movimento: 0,15–0,5 s, `cubic-bezier(0.7, 0, 0.3, 1)`.
Ícones: Font Awesome 4.7. Plataforma: PrestaShop (tema Warehouse) + Elementor.

## 3. Contraste calculado (WCAG)

| Cor | sobre branco | sobre preto `#231F20` |
|---|---|---|
| `#E31E24` (site-actual) | **4,69** | 3,48 |
| `#ED1C24` (conversão CMYK) | 4,38 | 3,72 |
| `#FF0000` (JPG) | 4,00 | 4,08 |
| `#231F20` | 16,30 | — |
| `#706D6E` | 5,12 | 3,18 |
| `#777777` | 4,48 | 3,64 |
| `#918F8F` | 3,22 | 5,07 |
| `#A7A5A6` | 2,45 | 6,66 |

Conclusão: **o vermelho das peças (`#ED1C24`, 4,38:1) não passa 4,5:1 com texto branco pequeno.** Branco sobre vermelho só em texto grande e grosso (≥ 18 px bold), como as peças já fazem. O `#E31E24` do site-actual passaria (4,69), mas não é fonte.

## 4. Fontes medidas

| Fonte (nome exacto no PDF) | Peças | O que escreve | Tamanhos |
|---|---|---|---|
| **Calamitech** | 8, 17 (2026) | títulos do produto: «BIO BONSAI», «BIOESTIMULANTE NATURAL», «FLORAÇÃO» | 13,3 · 19,8 · 47,9 · 55,6 pt, sempre branco, sempre em maiúsculas |
| **Capital Daren** | 7 (A4, 2020), 21 (embebida) | «HOTEL BONSAI», «DEIXE O SEU BONSAI NUM HOTEL» | 55 · 60 · 80 pt |
| **ClanOT-News / Book / Medium / Bold / Black / NarrNews** | 7, 8, 17, 18 | texto corrido dos rótulos (PT/ES/EN/FR), contactos | 4,5 · 5,6–7,6 · 14 pt |
| **BrushScriptStd** | 8 | «Activ» (nome da variante do produto) | 34 pt |
| **AgencyFB-Reg / Bold** | 21, 22 | texto corrido dos catálogos | 7–12 pt, azul `#6666FF` nas tabelas |
| **ArialRoundedMTBold** | 21, 22 | títulos dos catálogos («Catálogo Bonsai», «APRESENTAÇÃO») | 13–54 pt |
| ArialNarrow-Bold, AngsanaNew, OpenSymbol | 21, 22 | notas, contactos, marcadores | 9–15 pt |
| ArialMT | 3, 5, 9, 11 | só a escala de cinzas da gráfica (fora do corte) | 6 pt |
| MyriadPro | 18 | carimbo «PROVA 03» da gráfica | — |
| Arial / Times New Roman | 20 (modelo Word) | estilos por defeito do modelo | 9–11 pt |

**Peças em curvas (texto convertido em desenho, sem nome de fonte):** 3, 4, 5, 6, 9, 10, 11, 12, 13, 16. O wordmark «LUSO BONSAI», «GOSHIN», «BONSAI TOOLS» e o «BONSAI» do folheto têm o mesmo desenho de letra quadrado e grosso das fontes Calamitech / Capital Daren — **não confirmado** (estão em curvas).

**Letra manuscrita** («Your connection with nature…», «“Feel” the Difference», «Beauty in its purest form…»): peças 6, 13, 14, 15, 19. Em curvas ou JPG. **Nome desconhecido.**

**Site-actual (referência):** Fira Sans (Google, 400 / 500 / 700 / 800) em quase tudo — títulos 38 px / 700, secções 30 px / 700, corpo 15–16 px / 400, botão 15 px / 400; Noto Sans e Open Sans em blocos soltos; Arial e Roboto residuais.

## 5. Formatos físicos (tamanho do ficheiro, inclui marcas de corte quando as há)

| Peça | Tamanho |
|---|---|
| 3 · etiqueta pendurada (forma de «8», dois círculos) | 91 × 165 mm, 2 faces |
| 4 · folheto A5 | 152 × 214 mm (A5 com sangria), 2 faces |
| 5 · autocolante caixa B2C (círculo) | 131 × 131 mm |
| 6 · cartão de visita | 89 × 59 mm (85 × 55 com sangria), 2 faces |
| 8 · autocolante adubo Bonsai 1 l (envolvente) | 278 × 151 mm |
| 9 · blister ferramentas Basic | 116 × 175 mm, 2 faces |
| 10 · autocolante personalizações (círculo) | 36 × 36 mm |
| 11 · blister Goshin | 121 × 211 mm, 2 faces |
| 12 · autocolante Goshin (círculo) | 56 × 56 mm |
| 13 · cartão de feira Goshin | 600 × 600 mm, 2 faces |
| 16 · logotipo Orchis | 297 × 150 mm (prancheta) |
| 17 · autocolante adubo orquídeas 200 ml | 178 × 123 mm |
| 18 · autocolantes de terras (círculos, 8 páginas A4) | A4 horizontal |
| 14, 15, 19 · lonas | só JPG de pré-visualização (proporções 4,4:1 · 3,8:1 · 2,25:1) |
| 21, 22 · catálogos de revenda | A4 vertical, 30 e 15 páginas |

## 6. O que ficou por medir

- **Peça 20 (modelo de carta `.dot`):** sem LibreOffice nesta máquina. O `textutil` do macOS abriu-o mas não tem texto nem imagens legíveis; só se viu que os estilos por defeito são Arial 9 pt e Times New Roman 11 pt. **Por ler.**
- **Peça 7 (`.odg`):** sem LibreOffice; lida pelo XML e pela miniatura interna (`entrada/renders/peca-07-artes-A4-miniatura-odg.png`). Dá as fontes (Capital Daren, Clan OT) mas não as cores das imagens.
- **Lonas:** só JPG pequenos (1421 px de largura); não se mede a cor fina.
- **Logótipo vectorial oficial:** não veio. O símbolo existe em vector **dentro** dos PDF Corel (peças 6 e 10) — ver `assets/logos/`.
