---
title: CSS Shapes
description: Gamit ang <code>shape-outside</code> ng CSS, puwede nating i-customize kung paano magra-wrap ang text sa palibot ng isang element na naka-<code>float</code>.
seo_image: /images/posts/css-shapes/seo_cover.png
image: /images/posts/css-shapes/cover.png
author: teacherbuknoy
slug: /css-shapes/
tags: [web development, CSS]
---
Ang `shape-outside` ay isang bagong property sa CSS. Gamit ito, puwede nating bigyan ng shape ang isang floated element na susundin ng text na nasa palibot nito. Madalas natin itong makita sa mga magazine layouts.

<figure>
    <picture>
        <source
        media="(max-width: 767px)"
        sizes="(max-width: 1534px) 100vw, 1534px"
        srcset="
        /images/posts/css-shapes/20201102_133410_1_jwbvnu/20201102_133410_1_jwbvnu_ar_1_1,c_fill,g_auto__c_scale,w_200.png 200w,
        /images/posts/css-shapes/20201102_133410_1_jwbvnu/20201102_133410_1_jwbvnu_ar_1_1,c_fill,g_auto__c_scale,w_730.png 730w,
        /images/posts/css-shapes/20201102_133410_1_jwbvnu/20201102_133410_1_jwbvnu_ar_1_1,c_fill,g_auto__c_scale,w_1044.png 1044w,
        /images/posts/css-shapes/20201102_133410_1_jwbvnu/20201102_133410_1_jwbvnu_ar_1_1,c_fill,g_auto__c_scale,w_1323.png 1323w,
        /images/posts/css-shapes/20201102_133410_1_jwbvnu/20201102_133410_1_jwbvnu_ar_1_1,c_fill,g_auto__c_scale,w_1534.png 1534w">
        <source
        media="(min-width: 768px) and (max-width: 991px)"
        sizes="(max-width: 1983px) 70vw, 1388px"
        srcset="
        /images/posts/css-shapes/20201102_133410_1_jwbvnu/20201102_133410_1_jwbvnu_ar_4_3,c_fill,g_auto__c_scale,w_538.png 538w,
        /images/posts/css-shapes/20201102_133410_1_jwbvnu/20201102_133410_1_jwbvnu_ar_4_3,c_fill,g_auto__c_scale,w_822.png 822w,
        /images/posts/css-shapes/20201102_133410_1_jwbvnu/20201102_133410_1_jwbvnu_ar_4_3,c_fill,g_auto__c_scale,w_1034.png 1034w,
        /images/posts/css-shapes/20201102_133410_1_jwbvnu/20201102_133410_1_jwbvnu_ar_4_3,c_fill,g_auto__c_scale,w_1249.png 1249w,
        /images/posts/css-shapes/20201102_133410_1_jwbvnu/20201102_133410_1_jwbvnu_ar_4_3,c_fill,g_auto__c_scale,w_1388.png 1388w">
        <source
        media="(min-width: 992px) and (max-width: 1199px)"
        sizes="(max-width: 2400px) 60vw, 1440px"
        srcset="
        /images/posts/css-shapes/20201102_133410_1_jwbvnu/20201102_133410_1_jwbvnu_ar_16_9,c_fill,g_auto__c_scale,w_596.png 596w,
        /images/posts/css-shapes/20201102_133410_1_jwbvnu/20201102_133410_1_jwbvnu_ar_16_9,c_fill,g_auto__c_scale,w_874.png 874w,
        /images/posts/css-shapes/20201102_133410_1_jwbvnu/20201102_133410_1_jwbvnu_ar_16_9,c_fill,g_auto__c_scale,w_1085.png 1085w,
        /images/posts/css-shapes/20201102_133410_1_jwbvnu/20201102_133410_1_jwbvnu_ar_16_9,c_fill,g_auto__c_scale,w_1287.png 1287w,
        /images/posts/css-shapes/20201102_133410_1_jwbvnu/20201102_133410_1_jwbvnu_ar_16_9,c_fill,g_auto__c_scale,w_1440.png 1440w">
        <img
        sizes="(max-width: 5400px) 40vw, 2160px"
        srcset="
        /images/posts/css-shapes/20201102_133410_1_jwbvnu/20201102_133410_1_jwbvnu_c_scale,w_480.png 480w,
        /images/posts/css-shapes/20201102_133410_1_jwbvnu/20201102_133410_1_jwbvnu_c_scale,w_1078.png 1078w,
        /images/posts/css-shapes/20201102_133410_1_jwbvnu/20201102_133410_1_jwbvnu_c_scale,w_1493.png 1493w,
        /images/posts/css-shapes/20201102_133410_1_jwbvnu/20201102_133410_1_jwbvnu_c_scale,w_1853.png 1853w,
        /images/posts/css-shapes/20201102_133410_1_jwbvnu/20201102_133410_1_jwbvnu_c_scale,w_2160.png 2160w"
        src="/images/posts/css-shapes/20201102_133410_1_jwbvnu/20201102_133410_1_jwbvnu_c_scale,w_2160.png"
        alt="James Corden sketch. Nakapalibot sa larawan niya ang text ng magazine article.">
    </picture>
    <figcaption>
        <p>Sumusunod sa hugis ng larawan ni James Corden ang mga paragraph sa palibot niya.</p>
        <cite>The Farce Side, Vanity Fair (July 2012)</cite>
    </figcaption>
</figure>

## Paano ito gamitin?

Kailangan nating tandaan na gagana lang ang `shape-outside` property sa mga element na naka-`float`. Sa example na ito, mayroon tayong image na naka-float. By default, nagra-wrap ang text sa palibot ng border box nito. Hindi sumusunod sa actual na shape ng image ang text sa palibot nito.

<p class="codepen" data-height="419" data-theme-id="light" data-default-tab="result" data-user="maniczirconium" data-slug-hash="bGeMLor" style="height: 419px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="floated image (no shape-outside)">
  <span>See the Pen <a href="https://codepen.io/maniczirconium/pen/bGeMLor">
  floated image (no shape-outside)</a> by Francis Rubio (<a href="https://codepen.io/maniczirconium">@maniczirconium</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

## Browser support 

As of November 2, 2020, nasa 93.44% na ang browser support para sa `shape-outside` property, ayon sa [CanIUse.com](https://caniuse.com/). Puwede na itong gamitin sa production sites ninyo.

<script src="https://cdn.jsdelivr.net/gh/ireade/caniuse-embed/public/caniuse-embed.min.js"></script>
<p class="ciu_embed" data-feature="mdn-css__properties__shape-outside" data-periods="future_1,current,past_1,past_2" data-accessible-colours="true">Data on support for the mdn-css__properties__shape-outside feature across the major browsers</p>

Pero siyempre, gusto pa rin nating mag-provide ng fallbacks para sa mga browser na walang support para sa property na ito.

*[CSS]: Cascading Style Sheets