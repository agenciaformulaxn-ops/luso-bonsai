# Prompts das imagens geradas · Luso Bonsai

Geradas a 2026-10-16 com o Codex CLI (qualidade normal, conta ChatGPT do Rui). Estrutura da skill `gpt-image-prompts` (5 blocos).

Para repetir:

```bash
codex exec --skip-git-repo-check --sandbox workspace-write "Gera uma imagem PNG e grava em <caminho>. Usa a ferramenta de geração de imagens com a qualidade normal. <prompt>" < /dev/null
```

O `< /dev/null` é preciso: sem ele o Codex fica parado à espera de texto do teclado.

## gerada-viveiro · capa (faixa «a casa») e regra 7

```text
Scene: Inside a large bonsai nursery greenhouse in rural Portugal, early morning, long rows of wooden display benches under a translucent greenhouse roof.

Subject: Rows of mature bonsai trees in shallow brown and grey ceramic pots on the benches, one older bonsai with a thick twisting trunk in the foreground on the right third of the frame.

Details: Soft low side light from the right through the greenhouse walls, gentle shadows, muted natural greens and warm wood tones, slight haze, 35mm lens at eye level, shallow depth of field so the back rows fall softly out of focus, photorealistic, real photograph, natural imperfections in moss and soil.

Use case: Editorial hero photograph for a brand presentation of a Portuguese bonsai producer, shown as a wide band across the page.

Constraints: 21:9 ultrawide horizontal. Keep the left third calm and low contrast (soft out-of-focus greenery) for breathing space. No text, no lettering, no signage, no labels, no price tags, no logos, no brand names, no Japanese or Chinese characters on pots or anywhere, no people, no red objects, no watermark.
```

## gerada-goshin-maos · linha Goshin e bloco Fotografia

```text
Scene: A dark workshop table, plain charcoal background, single soft key light from the left.

Subject: Two hands pruning a small bonsai tree with a pair of black steel bonsai scissors with long handles and large round finger loops, cutting a small branch.

Details: Close-up, 50mm lens, hands in natural skin tones with five fingers each clearly visible, real skin texture, the scissors matte black forged steel, the bonsai in a plain dark grey unglazed pot, deep shadows, black, white and grey palette with only the green of the leaves as colour, photorealistic, real photograph.

Use case: Editorial photograph for the premium bonsai tools brand inside a brand presentation, shown as a wide image.

Constraints: 16:9 horizontal. Keep the right third dark and empty. No text, no lettering, no engravings, no logos, no brand names, no Japanese or Chinese characters, no red anywhere in the image, no jewellery, no watermark.
```

## gerada-orquidea · linha Orchis

```text
Scene: Plain very dark charcoal studio background, almost black, nothing else in the frame.

Subject: A single white phalaenopsis orchid flower stem with four open flowers and two buds, arching from the left side of the frame.

Details: Soft side light from the left, the petals glowing white with subtle texture, small yellow and pale pink detail at the flower centres, deep shadow falling into black, 85mm lens, shallow depth of field, photorealistic, real photograph.

Use case: Editorial photograph for an orchid product line with a black brand colour, inside a brand presentation, shown as a wide image.

Constraints: 16:9 horizontal. Keep the right half dark and empty for breathing space. No text, no lettering, no logos, no brand names, no pot labels, no Japanese or Chinese characters, no red, no watermark.
```

