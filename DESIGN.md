# DESIGN.md — Código Lunar
> Gerado a partir da análise real da página (codigo-lunar-vendas.pages.dev) + referência premium (floliving.com)
> Versão: 2.0 Premium | Data: 2026-06-02

---

## 1. IDENTIDADE VISUAL

**Conceito:** Luxury dark femtech — sofisticação ancestral com tecnologia moderna.
**Arquétipo atual:** `marketing-gradient` (90% confidence)
**Arquétipo alvo:** `polaris-friendly` (100% match no Flo Living) — mais espaçoso, mais refinado, tipografia premium.

---

## 2. PALETA DE CORES

### Cores base (manter exatamente)
```css
--cl-bg-primary:     #0A0A0B;   /* fundo principal */
--cl-bg-secondary:   #0C0A10;   /* fundo cards */
--cl-bg-tertiary:    #131018;   /* fundo seções alternadas */
--cl-bg-deep:        #1F1528;   /* fundo hero/sections escuras */

--cl-gold:           #D4B777;   /* dourado principal — COR MARCA */
--cl-gold-bright:    #E8C84A;   /* dourado brilhante — CTAs */
--cl-gold-dark:      #C9A227;   /* dourado escuro — hover */

--cl-text-primary:   #F8F7FD;   /* texto principal */
--cl-text-muted:     #CCCCCC;   /* texto secundário */
--cl-text-faint:     #E5E5E5;   /* texto de apoio */
```

### Cores dos produtos (manter exatamente)
```css
--cl-ebook1:   #7C3AED;   /* Mapeamento — roxo */
--cl-ebook2:   #059669;   /* Protocolo — verde */
--cl-ebook3:   #0EA5E9;   /* Integração — azul */
--cl-bonus1:   #C084FC;   /* Diário Lunar — violeta */
--cl-bonus2:   #E11D48;   /* Quiz Cíclico — vermelho */
--cl-bonus3:   #E91E63;   /* BemLab — rosa */
```

### Overlays e transparências
```css
--cl-gold-glow:      rgba(212, 183, 119, 0.15);
--cl-gold-border:    rgba(212, 183, 119, 0.25);
--cl-gold-hover:     rgba(212, 183, 119, 0.40);
--cl-white-subtle:   rgba(255, 255, 255, 0.04);
--cl-white-soft:     rgba(255, 255, 255, 0.08);
```

---

## 3. TIPOGRAFIA (UPGRADE PREMIUM)

### Stack atual (manter — já é premium)
```css
--cl-font-display: 'DM Serif Display', Georgia, serif;
--cl-font-body:    'Playfair Display', Georgia, serif;
--cl-font-ui:      Arial, Helvetica, sans-serif;
```

### Import Google Fonts (já está na página)
```
https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=Playfair+Display:wght@500;600;700&display=swap
```

### Escala tipográfica (upgrade de espaçamento — inspirado no Flo Living)
```css
/* Headlines */
--cl-h1-size:        58px;   /* mobile: 32px */
--cl-h1-weight:      400;    /* DM Serif Display regular — elegante */
--cl-h1-lineheight:  1.2;
--cl-h1-italic:      italic; /* usar italic para headlines principais = nível Flo Living */

--cl-h2-size:        46px;   /* mobile: 28px */
--cl-h2-weight:      700;    /* Playfair Display bold */
--cl-h2-lineheight:  1.2;

--cl-h3-size:        28px;   /* mobile: 22px */
--cl-h3-weight:      600;
--cl-h3-lineheight:  1.3;

/* Corpo */
--cl-body-size:      18px;
--cl-body-weight:    400;
--cl-body-lineheight: 1.6;

/* UI / Labels */
--cl-label-size:     14px;
--cl-label-weight:   600;
--cl-label-tracking: 0.08em; /* letter-spacing generoso = sofisticação */
```

### Regra de ouro tipográfica (vinda do Flo Living)
> Headlines principais em **DM Serif Display italic** com cor dourada `#D4B777`.
> Subtítulos em **Playfair Display 700** em branco `#F8F7FD`.
> Corpo em **Playfair Display 400** em `#CCCCCC`.
> Labels/badges em **Arial uppercase** com `letter-spacing: 0.08em`.

---

## 4. GRADIENTES

### Gradientes da página (manter)
```css
/* Botão CTA — dourado */
--cl-gradient-gold: linear-gradient(135deg, #C9A227, #D4B777, #E8C84A);

/* Background hero */
--cl-gradient-hero: linear-gradient(#0A0A0B, #0C0A10);

/* Background seção deep */
--cl-gradient-deep: linear-gradient(#09090B 0%, #1F1528 50%, #131018 100%);

/* Glow violeta (usado em destaques) */
--cl-gradient-glow: radial-gradient(circle, rgba(205,184,255,1) 0%, rgba(0,0,0,0) 70%);

/* Glow dourado */
--cl-gradient-gold-glow: radial-gradient(circle, rgba(212,183,119,1) 0%, rgba(0,0,0,0) 70%);
```

### Novo gradiente premium (inspirado no Flo Living — adicionar)
```css
/* Separador de seção sutil */
--cl-gradient-fade-top: linear-gradient(to bottom, rgba(212,183,119,0.06) 0%, transparent 100%);
```

---

## 5. BORDAS E RAIOS

```css
/* Sistema de raios (manter o existente) */
--cl-radius-btn:    50px;   /* botões — signature do Código Lunar */
--cl-radius-card:   16px;   /* cards de produto */
--cl-radius-badge:  24px;   /* badges (BÔNUS 1, etc) */
--cl-radius-icon:   12px;   /* ícones dos apps */
--cl-radius-sm:     8px;    /* elementos menores */

/* Bordas (upgrade premium — inspirado no Flo Living) */
--cl-border-gold:   1px solid rgba(212, 183, 119, 0.25);
--cl-border-subtle: 1px solid rgba(255, 255, 255, 0.06);
--cl-border-card:   1px solid rgba(212, 183, 119, 0.12);
```

---

## 6. ESPAÇAMENTO (UPGRADE — principal diferença do Flo Living)

O Flo Living usa `spacing_density: very-roomy`. Sua página já está no mesmo nível, mas pode ampliar nas seções principais:

```css
/* Seções (padding vertical) */
--cl-section-padding-lg: 112px 48px;   /* seções hero e CTA */
--cl-section-padding-md: 80px 48px;    /* seções de conteúdo */
--cl-section-padding-sm: 48px 24px;    /* mobile */

/* Espaço entre elementos */
--cl-gap-xl:  48px;
--cl-gap-lg:  32px;
--cl-gap-md:  24px;
--cl-gap-sm:  16px;
--cl-gap-xs:  8px;

/* Regra premium: nunca menos de 48px entre seções no desktop */
```

---

## 7. SOMBRAS

```css
/* Cards de produto */
--cl-shadow-card: 0 4px 24px rgba(0, 0, 0, 0.4);

/* Botão CTA */
--cl-shadow-btn: 0 4px 20px rgba(212, 183, 119, 0.3);

/* Glow nos ícones dos apps */
--cl-shadow-icon: 0 2px 12px rgba(212, 183, 119, 0.2);
```

---

## 8. ÍCONES DOS APPS (design system oficial)

```
Ebook 1 — Mapeamento:   ☽  background: #7C3AED  border-radius: 12px
Ebook 2 — Protocolo:    ☽  background: #059669  border-radius: 12px
Ebook 3 — Integração:   ☽  background: #0EA5E9  border-radius: 12px
Bônus 1 — Diário Lunar: ✦  background: #C084FC  border-radius: 12px
Bônus 2 — Quiz Cíclico: ◈  background: #E11D48  border-radius: 12px
Bônus 3 — BemLab:       🧪 background: #E91E63  border-radius: 12px
```

Tamanho padrão do ícone: `48px × 48px`, símbolo em `font-size: 26px`.

---

## 9. MOTION (animações)

```css
/* Durações existentes na página — manter */
--cl-duration-fast:   200ms;
--cl-duration-mid:    400ms;
--cl-duration-slow:   800ms;

/* Easing premium (inspirado no Flo Living) */
--cl-ease-out:   cubic-bezier(0.16, 1, 0.3, 1);  /* snappy saída */
--cl-ease-in:    cubic-bezier(0.4, 0, 1, 1);

/* Padrão de entrada recomendado para seções */
/* opacity: 0 → 1 + translateY(20px → 0) com IntersectionObserver */
```

---

## 10. COMPONENTES — REGRAS DE USO

### Botão CTA principal
```
background: linear-gradient(135deg, #C9A227, #D4B777, #E8C84A)
color: #0A0A0B (texto escuro sobre dourado)
font: Arial uppercase, weight 700, letter-spacing 0.08em
border-radius: 50px
padding: 20px 48px
box-shadow: 0 4px 20px rgba(212,183,119,0.3)
```

### Card de produto (ebook/bônus)
```
background: #0C0A10
border: 1px solid rgba(212,183,119,0.12)
border-radius: 16px
padding: 28px 32px
```

### Badge (BÔNUS 1, EBOOK 1, etc)
```
background: linear-gradient(135deg, #C9A227, #D4B777)
color: #0A0A0B
border-radius: 24px
padding: 6px 14px
font: Arial uppercase, weight 700, font-size 13px, letter-spacing 0.08em
```

### Logo na seção "Apresento o Código Lunar"
```
max-width: 200px
max-height: 120px
object-fit: contain
display: block
margin: 0 auto
```

---

## 11. CHECKLIST DE QUALIDADE

Antes de cada deploy, verificar:
- [ ] Fonte DM Serif Display italic nos headlines principais
- [ ] Espaçamento entre seções ≥ 48px no desktop
- [ ] Ícones dos apps com as cores corretas (ver seção 8)
- [ ] Botões com border-radius: 50px
- [ ] Cards com border-radius: 16px e border dourado sutil
- [ ] Preço R$197 visível (não R$97)
- [ ] Ancoragem R$1.192 presente na seção de oferta
- [ ] Testar em aba anônima após deploy

---

## 12. REGRAS ABSOLUTAS DO PROJETO

1. NUNCA Co-Authored-By nos commits
2. NUNCA interface genérica — cada elemento deve remeter ao universo lunar/feminino
3. SEMPRE testar em aba anônima após deploy
4. NUNCA hardcoded colors fora do sistema de variáveis acima
5. Stack: HTML/CSS/JS puro + PWA + Cloudflare Pages via GitHub
