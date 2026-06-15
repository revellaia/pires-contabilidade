# ASSET_MAPPING_REPORT · Seção "O Futuro da Pires" (06)

Data: 2026-06-15. Seção `#futuro` do `index.html`.
Princípio: a obra não é protagonista. Os três blocos provam visão e crescimento, subordinados
à narrativa da Magda. Estética clara, editorial, sem cara de construtora.

---

## Bloco principal · RENDER · FUTURA SEDE
- **Arquivo no site:** `assets/render-sede.jpg` (2048x1152, ~320 KB).
- **Origem:** PDF do projeto arquitetônico `APRESENTAÇÃO_estudo 02 - MAGDA HELLEY (3).pdf`,
  página 6 (render externo em ângulo 3/4, fachada visível, paisagismo, logo na fachada, luz de
  fim de tarde). Arquiteta: Geysa Lopes.
- **Tratamento Higgsfield:** upscale para 4K via Higgsfield (`bytedance_image_upscale`,
  job `fd124e4a`, 2 créditos). Saída 4096x2304, depois reduzida para 2048 de largura e
  reencodada em JPG q86 para peso web. Sem alteração de geometria, cor ou arquitetura.
- **Acabamento editorial (no layout):** filtro quente `saturate(1.03) contrast(1.04)
  brightness(1.02) sepia(0.05)` + overlay multiply quente + vinheta interna suave. O mesmo
  acabamento usado nas fotos da Magda, para unidade visual.
- **Motivo:** comunica a sede pronta, aspiracional. É o "depois", a visão realizada.

## Bloco secundário 1 · OBRA · HOJE
- **Arquivo no site:** `assets/obra.jpg`.
- **Origem:** foto real da obra (acervo do cliente, `WhatsApp Image 2026-06-12 at 09.02.30 (1)`),
  estrutura de concreto e pilares, construção em andamento.
- **Tratamento Higgsfield / editorial:** mesma calibragem quente do bloco principal, com overlay
  multiply e vinheta levemente mais fortes, para **reduzir a aparência bruta** da foto de obra e
  harmonizar luz e contraste com os renders. Sem upscale (foto de celular; a unificação é por grade
  editorial, não por reconstrução, para não inventar detalhe nem parecer IA).
- **Regra cumprida:** não é foto da Magda, não mistura pessoa com prédio. Representa o presente.

## Bloco secundário 2 · DETALHE ARQUITETÔNICO
- **Arquivo no site:** `assets/detalhe.jpg` (recorte 1984x1984 reduzido para 1100x1100, ~240 KB para peso web).
- **Origem:** recorte da página 3 do mesmo PDF (entrada da fachada com a **marca Pires
  Contabilidade aplicada**, ripado de madeira, vidro, pedra e jardim). Recorte feito a 3.2x
  para alta resolução.
- **Tratamento Higgsfield:** upscale 4K tentado (job `1ab199db`) **falhou no provedor**; como o
  recorte de origem já está em alta resolução (1984px), foi mantido o original. Acabamento
  editorial igual aos demais blocos para unidade.
- **Motivo:** dá acabamento de revista e prova de projeto premium (logo na arquitetura), fechando
  a narrativa visão + marca.

---

## Unidade visual entre os três blocos
- Mesmos cantos (radius 8px), mesma família de overlay quente e vinheta, mesma calibragem de cor.
- Labels discretas e consistentes ("Render · futura sede", "Obra · hoje", "Detalhe · fachada").
- Resultado: parece página editorial dirigida, não portfólio de arquitetura nem antes/depois forçado.

## Assets da home (origem)
Fotos profissionais reais da Magda (estúdio), vindas do handoff `design_handoff_pires_home/assets`:
`magda-hero.jpg` (hero, terno preto), `magda-portrait.jpg` (Assinatura, close anel esmeralda),
`magda-yellow.jpg` (A Pires), `magda-smile.jpg` (CTA final). Logo: `logo.png` (transparente).
Todas recebem o mesmo acabamento editorial quente + grão de papel global.

## Saldo Higgsfield
Antes: 609,64 créditos. Gasto: upscale do render (2) + tentativa do detalhe. Plano: pro.
