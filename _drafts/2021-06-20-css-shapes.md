---
title: "Interesting layouts gamit ang CSS Shapes"
description: Puwede na tayong gumawa ng mas interesting na layouts gamit ang iba't ibang mga shape.
image: /images/posts/css-selectors/cover.png
seo_image: /images/posts/css-selectors/seo-cover.png
author: teacherbuknoy
tags: [css]
---

Gamit ang CSS Shapes, puwede tayong gumamit ng iba't ibang hugis sa mga layout natin. Dahil dito, marami tayong bagong layout na puwedeng gamitin.

## Ang CSS Shapes Specification

Sa [Level 1 ng CSS Shapes specification](https://www.w3.org/TR/css-shapes/), dine-describe ang way para magamit natin ang mga geometric shape sa CSS. Dinisenyo sila para gamitin kasama ng `float` property.

<mark class="note">
    <b>'Di ba hindi na tayo gumagamit ng <code>float</code>?</b> Mali. Totoo, hindi na tayo gumagamit ng <code>float</code> para gumawa ng mga column sa layout natin dahil may CSS Grid at Flexbox na tayo, at para sa gano'ng purpose, sila ang dapat gamitin sa halip na <code>float</code>. Pero puwede pa rin nating gamitin ang <code>float</code> para sa original na purpose nito: kapag gusto nating alisin sa normal flow ang isang element habang nagra-wrap ang text sa palibot nito.
</mark>

Halimbawa, puwede mong i-float sa left side ang isang transparent na image, at gamit naman ang CSS Shapes, puwedeng mag-wrap ang text sa image mo habang sinusunod ang shape ng nasa picture sa halip na basta lang mag-wrap sa isang rectangular na element.

Ayon sa [Can I Use?](https://caniuse.com/css-shapes), nasa 95.13% na ngayon ang browser support para sa CSS Shapes Level 1. Kaya naman puwedeng-puwede mo na agad itong gamitin sa mga website na ginagawa mo currently.

<p class="ciu_embed" data-feature="css-shapes" data-periods="future_1,current,past_1,past_2" data-accessible-colours="false">
    <picture>
        <source type="image/webp" srcset="https://caniuse.bitsofco.de/image/css-shapes.webp">
        <source type="image/png" srcset="https://caniuse.bitsofco.de/image/css-shapes.png">
        <img src="https://caniuse.bitsofco.de/image/css-shapes.jpg" alt="Data on support for the css-shapes feature across the major browsers from caniuse.com">
    </picture>
</p>

## Paano ito gamitin?

Para makagawa ng CSS Shapes, gagamitin natin ang `shape-outside` property. Bibigyan natin ito ng isang function na magsasabi sa browser kung anong shape ang susundan ng text. May iba't iba tayong functions na puwedeng gamitin:

- `circle()`
- `ellipse()`
- `inset()`
- `polygon()`

Kunin nating halimbawa ang `circle()` function. Para magamit ang function na ito, kailangang masunod ang dalawang criteria:

1. <b>Kailangang naka-float ang element.</b> In the future, baka puwedeng magkaroon ng changes, at baka puwede tayong maglagay ng shape sa mga non-floated element. Pero sa ngayon, hindi ito puwede.
2. <b>Kailangang may naka-set na height at width ang element.</b> Gagamitin ang height at width ng element para bumuo ng coordinate system na magiging basehan ng shapes.

Tingnan ang susunod na code snippet:

<pre><code data-language="css">.element {
    float: left;
    width: 15em;
    height: 10em;
    shape-outside: circle();
    background-color: #f005;
}</code></pre>

<p class="codepen" data-height="469" data-theme-id="dark" data-default-tab="result" data-user="maniczirconium" data-slug-hash="jOBRvBp" style="height: 469px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="circle()">
  <span>See the Pen <a href="https://codepen.io/maniczirconium/pen/jOBRvBp">
  circle()</a> by Francis Rubio (<a href="https://codepen.io/maniczirconium">@maniczirconium</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>