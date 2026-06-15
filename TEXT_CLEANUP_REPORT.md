# TEXT_CLEANUP_REPORT · Pires Contabilidade

Relatório de remoção de travessões (em-dash `—`) do site.
Data: 2026-06-15. Arquivo auditado: `index.html`.

## 1. Onde havia travessões

A direção visual veio do handoff do Claude Design (`Pires Contabilidade.dc.html`), que usava
o travessão `—` em 13 trechos de copy. Todos foram eliminados ao recriar o site em produção.

## 2. Como foram substituídos (contexto a contexto)

| # | Seção | Original (com `—`) | Correção |
|---|---|---|---|
| 1 | 02 · A Magda | "...planilhas em tranquilidade **—** para que cada cliente..." | vírgula: "...em tranquilidade, para que cada cliente..." |
| 2 | 03 · A Pires (subtítulo) | "Assessoria e consultoria contábil **—** moderna, humana e estratégica." | vírgula: "...contábil, moderna, humana e estratégica." |
| 3 | 03 · A Pires (apoio) | "...portes e segmentos **—** combinando rigor técnico..." | vírgula: "...segmentos, combinando rigor técnico..." |
| 4 | 03 · A Pires (citação) | "...confiam às nossas mãos **—** e levamos essa responsabilidade..." | vírgula: "...às nossas mãos, e levamos..." |
| 5 | 03 · A Pires (parágrafo) | "...jornada do cliente **—** organizando a vida financeira..." | dois-pontos: "...jornada do cliente: organizando..." |
| 6 | 04 · Soluções (intro) | "...necessidade real **—** com profundidade técnica..." | vírgula: "...necessidade real, com profundidade..." |
| 7 | 04 · Sol. 01 | "...visão real do negócio **—** números que viram decisão." | ponto: "...visão real do negócio. Números que viram decisão." |
| 8 | 04 · Sol. 03 | "Pagar o justo **—** nem um centavo a mais **—** dentro da lei." | vírgulas: "Pagar o justo, nem um centavo a mais, dentro da lei." |
| 9 | 04 · Sol. 04 | "...conduzidas com cuidado **—** sua equipe segura..." | ponto: "...conduzidas com cuidado. Sua equipe segura..." |
| 10 | 04 · Sol. 05 | "...segurança e estratégia **—** sem sustos com o Leão." | vírgula: "...segurança e estratégia, sem sustos com o Leão." |
| 11 | 04 · Sol. 06 | "...tomada de decisão **—** clareza para crescer..." | ponto: "...tomada de decisão. Clareza para crescer..." |
| 12 | 06 · Futuro | "Um símbolo de crescimento **—** feito com a mesma seriedade..." | vírgula: "Um símbolo de crescimento, feito com a mesma seriedade..." |
| 13 | 06 · Futuro (nota) | "...fotos reais da obra **—** basta substituir." | trecho removido (era nota de placeholder; placeholders substituídos pelas imagens reais) |

## 3. Confirmação

- Busca por `—` (em-dash U+2014) em `index.html`: **0 ocorrências**.
- Revisão por tipo de elemento: headings, parágrafos, botões, legendas, labels, captions,
  textos pequenos e metadados visíveis. Nenhum travessão restante.
- Hifens comuns `-` (ex.: `CRC-TO`, `pré-`, números) foram preservados, pois não são travessões.
- Entidades `&amp;` (ex.: "Araguaína & todo o Tocantins") são o caractere "e comercial", não travessão.

Nenhum texto visível ao usuário contém travessão.
