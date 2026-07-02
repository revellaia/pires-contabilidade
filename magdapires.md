# magdapires.md — Contexto Master do Projeto
**Arquivo de restauração de sessão · Arrange Corp · BrunoDevAI**
Ultima atualizacao: 2026-07-01

> Leia este arquivo no inicio de qualquer nova sessao sobre este projeto.
> Ele substitui qualquer necessidade de reler o historico de chat anterior.

---

## 1. Identificacao do Projeto

| Campo | Dado |
|---|---|
| Cliente | Magda Helley Costa Pires |
| Empresa | Pires Contabilidade |
| CRC | CRC-TO 005688/O-7 |
| Titulo correto | **CEO** (nunca "Contadora responsavel") |
| Cidade | Araguaina, Tocantins |
| Produzido por | BrunoDevAI / Arrange Corp |
| Data de entrega inicial | 2026-06-16 |
| Ultima fase concluida | Fase 2 + SSL + assinatura BrunoDevAI (2026-07-01) |
| Status atual | **LIVE com HTTPS valido** |

---

## 2. URLs e Acessos

| Recurso | URL / Caminho |
|---|---|
| **Site ao vivo** | https://pirescontabilidadess.com.br |
| **Previa GitHub** | https://revellaia.github.io/pires-contabilidade/ |
| **Repositorio GitHub** | https://github.com/revellaia/pires-contabilidade |
| **Conta GitHub** | revellaia |
| **Branch** | main |
| **Pasta local** | `C:\Users\MICRO\Documents\Arrange Corp\WebDesign-Architect\output\2026-06-15-pires-contabilidade\` |
| **Wiki do projeto** | `C:\Users\MICRO\Documents\Arrange Corp\Universo Goebel\wiki\pirescontabilidade.md` |
| **Pasta de reports** | `output\2026-06-30-pires-contabilidade-update\` e `output\2026-06-30-pires-domain-ssl-repair\` |

---

## 3. Contatos do Cliente

| Canal | Dado |
|---|---|
| WhatsApp principal | (63) 99214-1495 · `wa.me/5563992141495` |
| WhatsApp secundario | (63) 99229-7155 · `wa.me/5563992297155` |
| E-mail oficial (no site) | contato@pirescontabilidadeto.com.br |
| Instagram | @magda.pirescontabilidade.to |
| Endereco | Rua dos Eletricistas, 138, Qd. TF, Lote 01, Jardim Paulista, Araguaina-TO |
| Atendimento | Todo o Brasil |

**Nota dominio vs e-mail:** o dominio do site e `pirescontabilidadess.com.br` mas o e-mail e `@pirescontabilidadeto.com.br` (dominios diferentes). Aguardando confirmacao de Bruno se e proposital ou se deve migrar.

---

## 4. Stack Tecnica

- **Tipo:** HTML5 puro, arquivo unico `index.html`
- **Sem framework, sem build, sem dependencias JS externas**
- **Fontes:** Google Fonts CDN — Cormorant Garamond (400/500/600, italic) + Hanken Grotesk (300/400/500/600)
- **Hosting:** GitHub Pages, conta `revellaia`, branch `main`, path `/`
- **Dominio:** `pirescontabilidadess.com.br` com CNAME no repo, registrado via GitHub Pages API
- **SSL:** Let's Encrypt, aprovado 2026-06-30, expira 2026-09-28, Enforce HTTPS ativo
- **Deploy:** push para `main` publica automaticamente em ~1-2 min

---

## 5. Design System

### Paleta de cores
```css
--paper:        #F4EFE7   /* fundo principal */
--paper-warm:   #EFE7DA   /* fundo secoes alternadas */
--ink:          #2B2823   /* texto principal / dark bg / footer bg */
--ink-mid:      #56514A   /* paragrafos */
--ink-light:    #8C857A   /* labels, captions */
--brand-gradient: linear-gradient(90deg, #6E3FA3, #C7418B, #F0764E, #3A5FCD, #36AEC6)
```

### Tipografia
| Elemento | Especificacao |
|---|---|
| H1 hero | Cormorant Garamond · `clamp(46px, 6.6vw, 104px)` · line-height 0.97 · letter-spacing -0.015em |
| H2 secao | Cormorant Garamond · `clamp(34px, 4.6vw, 64px)` · line-height 1.02 |
| Paragrafos | Hanken Grotesk · 16-18.5px · line-height 1.72-1.8 |
| Labels/eyebrows | Hanken Grotesk · 9-11px · letter-spacing .22-.34em · UPPERCASE |

### Acabamento
- Grao de papel: SVG feTurbulence fixo, opacity .05, mix-blend-mode:multiply (classe `.pc-grain`)
- Filtro fotos da Magda: `saturate(1.04) contrast(1.03) brightness(1.03) sepia(0.06)` (classe `.pc-photo`)
- Filtro renders arquitetonicos: `saturate(1.03) contrast(1.04) brightness(1.02) sepia(0.05)` (classe `.pc-arch`)
- Animacao `pcBreathe`: scale 1.01→1.07, 22-28s, infinite alternate (fotos da Magda)
- Easing padrao: `cubic-bezier(.16,.7,.3,1)`
- Nunca `display:none` puro em elementos animados — sempre `opacity + visibility` para permitir transicao

---

## 6. Estrutura de Secoes

| # | Secao | ID ancora | Conceito principal |
|---|---|---|---|
| Hero | — | `#top` | "Cada empresa e um projeto de vida." · foto Magda blazer amarelo |
| 01 | A Magda | `#magda` | Protagonismo de Magda · "olhar nos seus olhos" · close com anel esmeralda |
| 02 | A Pires | `#pires` | Estrutura de entrega · quote de Magda |
| 03 | Solucoes | `#solucoes` | Grid de servicos 12-cols + chips "todos os atendimentos" |
| 04 | Recuperacao Tributaria | `#recuperacao-tributaria` | Parceria Arte Fiscal · sem valor/percentual prometido |
| 05 | Agro e Produtor Rural | `#produtor-rural` | 4 pacotes (Basico/Controle/Estrategico/Premium) sem preco publico + fluxo automacao 6 etapas |
| 06 | Ferramentas | `#ferramentas` | SIEG, Dominio, ECONET, Mister Contador, ONVIO, WhatsApp Integrado |
| 07 | Parcerias | `#parcerias` | Conta Azul 50% desconto + Arte Fiscal |
| 08 | Planos | `#planos` | Cards de planos (sem preco publico, conteudo placeholder ate confirmacao) |
| 09 | Jornada | `#experiencia` | 6 etapas em grid escuro `#2B2823` · numeracao 01-06 |
| 10 | Nova Sede | `#futuro` | Slider antes/depois (obra-atual.jpg vs render-sede.jpg) |
| 11 | Cases | `#cases` | Placeholder honesto — "Case em validacao" (sem depoimento inventado) |
| 12 | Conteudos | `#conteudos` | Instagram real (@magda.pirescontabilidade.to) · YouTube "em validacao" |
| — | Footer | — | Logo + tagline + Navegacao + Contato + Escritorio + assinatura BrunoDevAI |

---

## 7. Inventario Completo de Assets

| Arquivo | O que e | Uso |
|---|---|---|
| `assets/logo.png` | Logo oficial Pires (fundo transparente, 183KB) | Nav (52px) e Footer (54px) |
| `assets/magda-hero.jpg` | Magda blazer amarelo, pose confiante (WhatsApp 08.44.37) | Hero — coluna direita |
| `assets/magda-portrait.jpg` | Close Magda, anel esmeralda (handoff design) | Secao A Magda |
| `assets/magda-yellow.jpg` | Magda blazer amarelo lateral (handoff design) | Secao A Pires |
| `assets/magda-smile.jpg` | Magda sorrindo (handoff design) | CTA final |
| `assets/render-sede.jpg` | Render 4K da nova sede (PDF Geysa Lopes, p.6 → Higgsfield job fd124e4a) | Slider antes/depois: lado "Visao pronta" |
| `assets/obra-atual.jpg` | Foto real da obra em 30/06 (WhatsApp 11.43.06, alvenaria 3 andares), crop 16:10 | Slider antes/depois: lado "A obra avanca" |
| `assets/obra.jpg` | Foto da construcao em 12/06 (obra inicial) | Slide descartado do carrossel antigo |
| `assets/detalhe.jpg` | Recorte fachada+logo do PDF arquitetonico (p.3) | Slide descartado do carrossel antigo |
| `assets/sede-antes.jpg` | Antes.jpeg (obra) do briefing original — **NAO USADA** no slider final | Descartada: angulo diferente |
| `assets/sede-depois.jpg` | Depois.png (render) do briefing original — **NAO USADA** no slider final | Descartada: angulo diferente |
| `assets/favicon.ico` | Gerado do logo.png via Pillow (16+32+48px) | Aba do navegador |
| `assets/favicon-32x32.png` | Gerado do logo.png (32x32) | Navegadores modernos |
| `assets/apple-touch-icon.png` | Gerado do logo.png (180x180) | Salvar em iPhone/iPad |
| `assets/brunodevai-logo.png` | Logo BrunoDevAI sem fundo (dourado) | Footer — assinatura "construido e desenvolvido por" |

**Assets ATIVOS no slider antes/depois:**
- Lado esquerdo ("A obra avanca"): `obra-atual.jpg`
- Lado direito ("Visao pronta"): `render-sede.jpg`
- Estes dois tem o mesmo angulo de camera (esquina do predio, rua em primeiro plano)

---

## 8. Funcionalidades Implementadas

### Navegacao Desktop
- Nav fixa com 7 itens: A Magda · A Pires · Servicos (dropdown) · Solucoes (dropdown) · Experiencia · Futuro · Contato
- Scroll >36px: background `rgba(244,239,231,0.82)` + `backdrop-filter:blur(14px)` + borda sutil
- Barra gradiente 2px no topo do nav (`::before`)
- Barra de progresso de scroll 2px no topo da viewport (`#pc-progress`)
- CTA do nav: botao "Iniciar atendimento" abre modal

### Dropdowns Desktop
- **Servicos** (`#dd-servicos`): 3 colunas, 13 itens
  - Col 1 "Comece por aqui": Abra sua empresa / Troque de contador / Ver planos
  - Col 2 "Servicos": Regularizacao Fiscal / Recuperacao Tributaria / Reforma Tributaria / Holding / Societario e Juridico
  - Col 3 "Setorial": Agro e Produtor Rural / Profissionais Liberais / MEI / Startups e Tech / Comercio e Varejo
- **Solucoes** (`#dd-solucoes`): 2 colunas, 10 itens (ferramentas + parcerias + conteudos)
- Abertura via `classList.toggle('open')` no botao trigger
- Fechamento: clicar fora, pressionar Escape, ou navegar para secao
- Animacao: `opacity + visibility + translateY(-8px→0)`
- Itens com secao real → `<a href="#ancora">` ; itens sem secao → `<button class="js-open-form" data-service="Nome">` (abre modal pre-preenchido)

### Menu Mobile (Hamburger)
- Overlay full-screen `rgba(244,239,231,0.99)` + `backdrop-filter:blur(20px)`
- Servicos/Solucoes como accordion: `max-height` transition (0→640px)
- Links Cormorant Garamond 25-30px
- Botao fechar no topo direito
- Breakpoint: ≤980px

### Modal "Iniciar atendimento"
- Abre pelo CTA do nav, pelo botao hero e por itens sem secao propria
- Campos: Nome* · Telefone* · Servico* (select 18 opcoes) · E-mail (opcional)
- Validacao client-side: `required` + `aria-required` nativos, `novalidate` no form, `aria-invalid` + foco no primeiro erro
- Submit: monta mensagem template e abre `wa.me/5563992141495?text=...` em nova aba
- **Sem backend. Sem coleta de dados em servidor.** Puramente client-side.

### Slider Antes/Depois (secao Nova Sede)
- Tecnica: `<input type="range">` nativo (opacity:0, cobre 100% da area) sincronizado via JS com `clip-path: inset(0 X% 0 0)` no elemento `.pc-ba-antes`
- Drag/touch/teclado nativos do browser, sem biblioteca
- Posicao inicial: 50%
- Assets: `render-sede.jpg` (Visao pronta, direita) e `obra-atual.jpg` (A obra avanca, esquerda)
- Labels flutuantes nos cantos (9.5px uppercase)
- Divisor branco 2px com handle circular (46px, sombra)
- aspect-ratio 16:10
- JS: `baRange.addEventListener('input', () => updateBA(baRange.value))` onde `updateBA(val)` define `clipPath = 'inset(0 '+(100-val)+'% 0 0)'` e `baDivider.style.left = val+'%'`

### Animacoes
| Nome | Tipo |
|---|---|
| `data-reveal` | IntersectionObserver: opacity 0→1 + translateY(26px→0), threshold 0.12, easing .16,.7,.3,1 |
| `pcBreathe` | CSS keyframes infinite: scale 1.01→1.07, 22-28s, pausa com prefers-reduced-motion |
| `pcDrift` | CSS keyframes: indicador "Explorar" sobe/desce 14px (oculto no mobile) |

### Responsividade
| Breakpoint | Comportamento |
|---|---|
| >980px | Desktop: grids asimetricos, nav completo |
| ≤980px | Mobile: 1 coluna, hamburger, Explorar oculto, journey 2x3 |
| ≤560px | Journey 1 col, auth 1 col, portrait limitado |

---

## 9. SEO e Meta

```
Title: Magda Pires · Pires Contabilidade · Araguaina-TO
Description: Contabilidade estrategica para quem busca clareza, segurança e crescimento. Magda Helley Costa Pires, CRC-TO 005688/O-7, Araguaina, Tocantins.
Canonical: https://pirescontabilidadess.com.br/
OG Image: https://pirescontabilidadess.com.br/assets/magda-hero.jpg
Schema: AccountingService JSON-LD (nome, url, logo, image, telefone, email, endereço, founder CEO)
Sitemap: https://pirescontabilidadess.com.br/sitemap.xml
robots.txt: Disallow: / (noindex durante previa — NAO alterar sem autorizacao de Bruno)
```

---

## 10. Configuracao de DNS e Hospedagem

**Registrador:** Hostinger
**Nameservers:** athena.dns-parking.com / dns.hostinger.com

| Tipo | Nome | Valor | Status |
|---|---|---|---|
| A | @ | 185.199.108.153 | OK |
| A | @ | 185.199.109.153 | OK |
| A | @ | 185.199.110.153 | OK |
| A | @ | 185.199.111.153 | OK |
| CNAME | www | revellaia.github.io | OK |

**Certificado SSL:** Let's Encrypt, aprovado 2026-06-30, expira 2026-09-28, cobre apex + www
**Enforce HTTPS:** ativo
**CNAME no repo:** arquivo `CNAME` na raiz com conteudo `pirescontabilidadess.com.br`

---

## 11. Historico de Commits (main)

```
7cc8d4d  chore: adiciona assinatura BrunoDevAI no footer
fa9307b  Create CNAME
9600d70  Delete CNAME  (ciclo para forcar emissao do SSL)
d036fee  fix: tamanho de fonte do nav e imagens do slider antes/depois
81516fe  feat: fase 2 - secoes reais, slider antes/depois, dominio proprio
0fe2a93  feat: menu com dropdowns Servicos/Solucoes, formulario WhatsApp e contatos atualizados
9115826  feat: adiciona slider editorial na secao Futuro com 4 imagens
4c36286  feat: adiciona favicon, favicon-32x32 e apple-touch-icon
377b359  Polish v2: CEO title, hamburger nav, scroll progress, OG/Schema SEO, hover effects, mobile fixes
ede1037  Add robots.txt (preview noindex)
89724e9  Pires Contabilidade: site institucional (Editorial Luxury)
```

---

## 12. Regras Inviolaveis (nao violar em nenhuma sessao futura)

1. **Nunca chamar Magda de "Contadora responsavel"** — titulo e CEO
2. **Sem travessoes (—) em nenhum texto do site** — usar virgula, ponto ou dois-pontos
3. **Nao inventar cases, depoimentos, links, parceiros ou promessas** — placeholder honesto ou omitir
4. **Nao publicar precos sem confirmacao de Magda** — pacotes Agro existem no PPTX mas sem preco publico
5. **Nao prometer valor, resultado ou percentual de recuperacao tributaria**
6. **Nao liberar indexacao (robots.txt) sem autorizacao explicita de Bruno**
7. **YouTube so inserir se houver link real confirmado** — hoje exibe "Canal em validacao"
8. **Formulario WhatsApp e client-side only** — nunca coletar dados em backend/servidor
9. **Nunca subir credenciais, .env ou chaves de API para o repositorio**
10. **E-mail do site continua `@pirescontabilidadeto.com.br`** ate confirmacao contraria

---

## 13. Erros Conhecidos e Suas Correcoes (historico)

| Problema | Causa | Solucao |
|---|---|---|
| Nav: Servicos/Solucoes apareciam maiores que outros links | `.pc-dropdown-trigger { font:inherit }` sobrescrevia o 13.5px do `.navlink` | Trocar para `font-size:13.5px; letter-spacing:.01em` explicitos |
| Slider com imagens erradas | Par Antes.jpeg/Depois.png tem angulos diferentes | Trocar para `obra-atual.jpg` + `render-sede.jpg` (mesmo angulo de camera) |
| Chrome alertava `NET::ERR_CERT_COMMON_NAME_INVALID` | GitHub nao emitiu certificado automaticamente mesmo com DNS correto | Ciclo via API: `PUT cname:null` → aguardar → `PUT cname:"pirescontabilidadess.com.br"` → cert novo→aprovado em 15s → `PUT https_enforced:true` |
| 38 ocorrencias de `href="#"` | Dropdowns gerados sem destino real | Itens com secao real viram `<a href="#ancora">`, itens sem secao viraram `<button type="button" class="js-open-form">` |
| Formulario sem validacao HTML nativa | `required` ausente | Adicionado `required` + `aria-required="true"` em nome/telefone/servico, mantido `novalidate` para estilo customizado |

---

## 14. Pendencias em Aberto

- [ ] **E-mail:** confirmar se `contato@pirescontabilidadeto.com.br` e intencional (dominio separado) ou deve migrar para `@pirescontabilidadess.com.br`
- [ ] **Indexacao:** liberar `robots.txt` (remover `Disallow: /`) quando Magda aprovar o conteudo publicamente
- [ ] **Cases reais:** obter depoimentos de clientes com autorizacao para substituir placeholders
- [ ] **YouTube:** confirmar se existe canal e qual e o link
- [ ] **Holding:** hoje so e item no dropdown/formulario, sem secao propria de conteudo
- [ ] **Precos dos planos:** confirmar valores com Magda antes de publicar
- [ ] **GitHub Pages `status: errored`:** build legado (Jekyll) mostra erro mas conteudo serve normalmente. Monitorar se pushes futuros param de refletir no site.
- [ ] **WebP:** converter imagens para WebP na versao de producao (render-sede, obra-atual, magda-hero)
- [ ] **Reforma Tributaria:** conteudo mais aprofundado quando informacoes da CBS/IBS/IVA estiverem consolidadas
- [ ] **Playwright 430px:** viewport nao testado (dos 5 pedidos no briefing original)

---

## 15. Proximos Passos Sugeridos (por prioridade)

1. Confirmar e-mail (bloqueia SEO definitivo)
2. Obter aprovacao da Magda para liberar indexacao
3. Cases reais com autorizacao escrita
4. Link YouTube (se existir)
5. Conversao WebP + otimizacao de performance
6. Secao Holding com conteudo real

---

## 16. Midia e Origens

| Midia | Origem original | Caminho local |
|---|---|---|
| Fotos Magda (hero, portrait, yellow, smile) | Handoff Claude Design (pasta Pires Contabilidade raw) | `assets/magda-*.jpg` |
| Render sede 4K | PDF APRESENTACAO_estudo 02 - MAGDA HELLEY (3).pdf, p.6 → Higgsfield upscale (job fd124e4a) | `assets/render-sede.jpg` |
| Foto obra inicial | WhatsApp 08 2026-06-12 09.02.30(1).jpeg | `assets/obra.jpg` |
| Foto obra atual | WhatsApp 2026-06-30 11.43.06.jpeg (alvenaria 3 andares) | `assets/obra-atual.jpg` |
| Detalhe fachada | PDF arquitetonico p.3, recorte 1100x1100 | `assets/detalhe.jpg` |
| Logo Pires | Handoff design (fundo transparente) | `assets/logo.png` |
| Logo BrunoDevAI | `.superpowers\brainstorm\2022-1780449287\content\logo-brunodevai-sem fundo.png` | `assets/brunodevai-logo.png` |
| Conteudo Agro/PPTX | `2- Proposta Produtor Rural - Nao Contribuinte.pptx.pptx` (raw Universo Goebel) | Extraido via python-pptx |
| Fluxo automacao Agro | `Produtor Rural - fluxo automatizacao pires 1.html` (raw Universo Goebel) | Incorporado na secao #produtor-rural |
| Arquiteta da sede | Geysa Lopes | — |

---

## 17. Arquivos do Projeto

```
output\2026-06-15-pires-contabilidade\
  index.html                          (ARQUIVO PRINCIPAL — ~1200 linhas, site completo)
  CNAME                               (conteudo: pirescontabilidadess.com.br)
  robots.txt                          (Disallow: / — noindex)
  sitemap.xml                         (URL: https://pirescontabilidadess.com.br/)
  magdapires.md                       (este arquivo)
  assets\
    logo.png
    magda-hero.jpg
    magda-portrait.jpg
    magda-yellow.jpg
    magda-smile.jpg
    render-sede.jpg
    obra-atual.jpg
    obra.jpg
    detalhe.jpg
    sede-antes.jpg      (nao usada)
    sede-depois.jpg     (nao usada)
    favicon.ico
    favicon-32x32.png
    apple-touch-icon.png
    brunodevai-logo.png

output\2026-06-30-pires-contabilidade-update\
  PIRES_IMPLEMENTATION_REPORT.md
  PIRES_PLAYWRIGHT_QA_REPORT.md
  PIRES_PHASE_2_REPAIR_REPORT.md
  PIRES_DOMAIN_CNAME_CANONICAL_SITEMAP_REPORT.md
  PIRES_PLAYWRIGHT_PHASE_2_QA_REPORT.md

output\2026-06-30-pires-domain-ssl-repair\
  PIRES_DOMAIN_SSL_REPAIR_REPORT.md
  PIRES_DNS_RECORDS_CHECK.md
  PIRES_HTTPS_CERTIFICATE_STATUS.md
```

---

## 18. Como Retomar o Trabalho num Novo Chat

1. Leia este arquivo (magdapires.md) completo
2. Se precisar editar o site: abra `index.html` na pasta local
3. Apos editar: `git add index.html && git commit -m "descricao" && git push origin main`
4. GitHub Pages publica em ~1-2 minutos automaticamente
5. Para verificar SSL/dominio: `curl -I https://pirescontabilidadess.com.br`
6. Playwright QA: `npx playwright test` na pasta do projeto (se configurado) ou via Bash manual

**Nao e necessario reconfigurar DNS, SSL ou dominio** — tudo ja esta operacional.

---

*Gerado em 2026-07-01 · Arrange Corp · BrunoDevAI · bgmcruz1988@gmail.com*
