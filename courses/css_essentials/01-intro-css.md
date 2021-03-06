---
id: 01-intro-css
course: css-essentials
permalink: /courses/css-essentials/01-intro-css/
layout: zirconium-lesson

title: Ang Cascading Style Sheets
description: Bakit kailangan ang CSS? At paano ito gagamitin kasama ng HTML?

has_downloads: false
---
## Bakit kailangan ang CSS?
Kailangan ang CSS (Cascading Stylesheets) para mabigyan ng styling at layout ang HTML pages.

Nang magsimula ang World Wide Web (WWW), HTML lang ang language[^see-more] na ginagamit nito. Ito ang nagdidikta kung ano ang magiging content *at* styling ng isang webpage. Wala pang scripting noon, kaya hindi pa interactive ang mga website.

Nang tumagal, na-realize ng mga web developer (o webmaster, gaya ng tawag sa kanila noon) na kailangan nilang paghiwalayin ang content at styling para maging mas efficient ang paggawa nila ng websites. Dito nila sinimulang gamitin ang CSS. Maraming benefits sa paggamit ng CSS. Heto ang ilan:

- <b>Nasa iisang lugar ang lahat ng styles.</b> Dahil nakahiwalay sa HTML ang styles. Hindi na kailangang isa-isang i-edit ang bawat isang HTML file para lang baguhin ang design ng isang element.
- <b>Puwedeng i-share sa iba ang design mo.</b> Puwede kang gumawa ng isang <i>stylesheet library</i> na pwedeng gamitin ng iba para sa sarili nilang mga website.
- <b>Mas advanced ang styling na puwedeng gawin.</b> Hindi katulad ng styling sa HTML na kulay lang ng text at background ang pwedeng baguhin, mas maraming advanced features ang CSS. Bukod sa styling ng text, puwede mo ring baguhin ang layout ng buong webpage. Puwede ka ring maglagay ng mga transition at animation. At higit sa lahat, puwede mong i-customize ang styles ng webpage mo depende sa size ng screen ng user.

## Paano maglalagay ng CSS sa loob ng isang webpage?

May tatlong paraan ng paglalagay ng CSS sa HTML.
* <b>Inline styles.</b> Puwede mong ilagay ang styles sa loob ng `style=""` attribute ng HTML tag na gusto mong lagyan ng styling. Isang element lang ang apektado ng mga inline style.
* <b>Internal styles.</b> Puwede mong ilagay sa loob ng `<style></style>` ang CSS mo. Ang mga element lang sa loob ng isang HTML file ang apektado ng internal styles.
* <b>External styles.</b> Puwede kang gumawa ng hiwalay na file na may `.css` na file extension. Pagkatapos, puwede mong gamitin ito sa loob ng HTML file mo gamit ang `<link>` tag sa loob ng `<head></head>`.

### Inline styles
Puwede nating lagyan ng styles ang indibiduwal na HTML tags. Sa susunod na halimbawa, pansinin kung paano ginamit ang `style=""` attribute para maglagay ng styles sa isang paragraph lang.

<pre><code data-language="html">&lt;p>I'm not nothing without a steady hand. I'm not nothing unless I know I can. I'm still something if I don't got a man. I'm a free woman.&lt;/p>
&lt;p style="color: red;">I heard one sine from above. Then the signal split in two, the sound created stars like me and you. Before there was us, there was silence. I heard one sine, and it healed my heart. I heard a sine.&lt;/p>
</code></pre>

Sa loob ng `style=""` attribute, naglagay tayo ng `color: red`. Sasabihin nito sa browser na ang kulay ng text (`color`) ay pula (`red`). Pansinin din na kailangan mong <em>maglagay ng semi-colon sa dulo</em>. Kapag binuksan natin ito sa isang browser, ganito ang makikita natin:
![Sa dalawang paragraphs, ang pangalawa lang ang naging kulay pula dahil, gaya ng nasa code, iyon lang ang nilagyan natin ng CSS]({{ site.baseurl }}/images/courses/css-essentials/01-intro-css/code-1.png)

Sa ganitong method ng paglalagay ng CSS, kung gusto nating bigyan ng style ang dalawang paragraph, pareho natin silang lalagyan ng `style=""` attribute:

<pre><code data-language="html">&lt;p style="color: red;">I'm not nothing without a steady hand. I'm not nothing unless I know I can. I'm still something if I don't got a man. I'm a free woman.&lt;/p>
&lt;p style="color: red;">I heard one sine from above. Then the signal split in two, the sound created stars like me and you. Before there was us, there was silence. I heard one sine, and it healed my heart. I heard a sine.&lt;/p>
</code></pre>

![Dahil pareho na silang may style attribute, pareho nang apektado ng CSS styles ang dalawang paragraph.]({{ site.baseurl }}/images/courses/css-essentials/01-intro-css/code-2.png)

Puwede rin nating baguhin ang background color ng mga paragraph na ito. Gagamitin lang natin ang `background-color` property pagkatapos ng semi-colon sa `color` property. Laging ganito ang syntax ng CSS. Subukan natin sa code:

<pre><code data-language="html">&lt;p style="color: red; background-color: yellow;">I'm not nothing without a steady hand. I'm not nothing unless I know I can. I'm still something if I don't got a man. I'm a free woman.&lt;/p>
&lt;p style="color: red;">I heard one sine from above. Then the signal split in two, the sound created stars like me and you. Before there was us, there was silence. I heard one sine, and it healed my heart. I heard a sine.&lt;/p>
</code></pre>

![Naging dilaw ang background color ng unang paragraph dahil nilagyan natin iyon ng background-color: yellow;]({{ site.baseurl }}/images/courses/css-essentials/01-intro-css/code-3.png)

Kung gusto nating maging dilaw ang background color ng dalawang paragraph na ito, dapat na parehas silang may `background-color` property. Pero puwede rin nating ibahin ang kulay ng background ng pangalawang paragraph. Subukan nating gawing white ang text color at gawing green ang background:

<pre><code data-language="html">&lt;p style="color: red; background-color: yellow;">I'm not nothing without a steady hand. I'm not nothing unless I know I can. I'm still something if I don't got a man. I'm a free woman.&lt;/p>
&lt;p style="color: white; background-color: green;">I heard one sine from above. Then the signal split in two, the sound created stars like me and you. Before there was us, there was silence. I heard one sine, and it healed my heart. I heard a sine.&lt;/p>
</code></pre>

![Naging dilaw ang background color ng unang paragraph dahil nilagyan natin iyon ng background-color: yellow;]({{ site.baseurl }}/images/courses/css-essentials/01-intro-css/code-4.png)

Pero obviously, hindi ito efficient. Sa katunayan, pinapagod lang natin ang sarili natin kapag ganito ang ginawa natin. Para lang din tayong gumamit ng mga lumang `<font>` tags. Kapag dumami na ang paragraphs natin, paulit-ulit natin silang lalagyan ng `style=""` attributes. May mas magandang way para malagyan silang lahat ng style gamit lang ang isang bahagi ng code.

#### Internal stylesheet

Sa internal stylesheet, sa halip na maglagay ng CSS sa mismong tags, maglalagay tayo ng `<style></style>` tags sa loob ng `<head></head>` tags. Gagamit din tayo ng tinatawag na <i>selector</i>, isang pattern na magsasabi sa browser kung aling mga HTML elements lang ang makakatanggap ng styles. Subukan natin:

<pre><code data-language="html">&lt;head>
  …
  &lt;style>
     p {
       color: red;
     }
     
     h1 {
       color: blue;
     }
  &lt;/style>
&lt;/head>
&lt;body>
  &lt;h1>Headline&lt;/h1>
  
  &lt;p>I can see it in your face, you don't think I pulled my weight. Maybe it's time for us to say goodbye because I'm feeling the way that I'm feeling with you. I'm not having fun tonight. &lt;/p>
  
  &lt;p>Am I still alive? Where am I? I cry. Who was it that pulled the trigger, was it you or I? I'm completely numb. Why are you acting dumb? I won't blame myself because we both know you were the one.&lt;/p>
&lt;/body>
</code></pre>

![Isang browser na nagdi-display ng webpage na may isang headline na kulay asul at dalawang paragraph na pula]({{ site.baseurl }}/images/courses/css-essentials/01-intro-css/code-5.png)

<aside class="float float--left">
  <h5 class="float__header">Laging nasa <code>&lt;head></code> ang Styles</h5>
  <p>Gagana pa rin ang internal styles mo kahit na nakalagay ito sa <code>&lt;body>&lt;/body></code> tag, pero hindi ibig sabihin na tama iyon. <strong>Ilagay ang styles sa <code>&lt;head>&lt;/head></code> tag.</strong></p>
</aside>

Himayin natin ang bagong code na ito. Una, nilipat natin ang lahat ng styles natin sa loob ng `<style></style>` tags. Pagkatapos, may ginagamit na tayong pattern o <i>syntax</i> sa CSS natin. Tingnan natin in detail ang bagong syntax na ito:

<img class="invert-when-dark" src="{{ site.baseurl }}/images/courses/css-essentials/01-intro-css/anatomy-of-css-rule.svg" alt="Diagram ng isang CSS ruleset">


<aside class="float float--right">
  <h5 class="float__header">Punctuation Symbols</h5>
  <p>Kailangan sa syntax ang curly braces (<code>{}</code>). Kailangan mo ring maglagay ng colon (<code>:</code>) sa pagitan ng property at value, at semi-colon (<code>;</code>) sa dulo ng declaration pagkatapos ng value.</p>
</aside>

Selector
: Ito ang pangalan ng HTML element na gusto nating lagyan ng styling. Kapag gusto mong baguhin ang styles ng isang `<p></p>` tag, ilalagay mo ang `p` sa selector. Ganoon din ang gagawin sa iba pang mga tag.

Property
: Mga characteristic ng isang HTML element na gusto mong baguhin. Sa code natin, binago natin ang `color` o kulay ng text ng mga HTML elements.

Value
: Ito ang bagong value ng property na gusto nating i-style sa HTML element. Sa example natin, ginawa nating `red` ang `color` ng mga paragraph, at `blue` naman ang sa `h1`.
  
Declaration
: Ang tawag sa magkasamang `property: value;`.
  
Rule o Ruleset
: Ang tawag sa lahat ng ito kasama ang selectors, declaration, at ang mga curly brace, colon, at semicolon</dd>

Puwede rin tayong mag-select ng maraming elements para isang ruleset lang. Paghihiwa-hiwalayin lang natin ang mga selector gamit ang comma. Halimbawa, may headline tayo, isang paragraph, at isang ordered list, at gusto nating maging red ang text nilang lahat. Puwede nating gawin ito:

<pre><code data-language="html">&lt;h1>This is a headline&lt;/h1>
&lt;p>Turning up emotional faders, keep on keeping self-hating phrases, I have heard enough of these voices. It's almost like I have no choice.&lt;/p>
&lt;ol>
  &lt;li>Alice&lt;/li>
  &lt;li>Stupid Love&lt;/li>
  &lt;li>Rain On Me&lt;/li>
  &lt;li>Free Woman&lt;/li>
  &lt;li>Fun Tonight&lt;/li>
&lt;/ol>
</code></pre>

Ito naman ang sa CSS:

<pre><code data-language="html">&lt;style>
    h1, p, li {
        color: red;
    }
&lt;/style>
</code></pre>
![Isang webpage na may isang heading, paragraph, at ordered list na may limang items. Lahat ng text ay kulay pula.]({{ site.baseurl }}/images/courses/css-essentials/01-intro-css/code-7.png)

#### External stylesheet
Pinaka-useful ang CSS kapag nakahiwalay ito sa isa pang file. Ang tawag dito ay <dfn>external stylesheet</dfn>. Gaya sa HTML, kailangan mo lang ding gumawa ng isang ordinaryong text file, pero sa halip na `.txt`, gagawin mong `.css` ang filename extension nito.

Kapag may CSS file ka na, puwede mo nang ilipat ang lahat ng internal styles mo papunta sa CSS file na iyon. Pagkatapos, iko-connect natin iyan sa HTML file natin gamit ang `<link>` tag. Ilalagay din natin ito sa `<head>` tag:

<pre><code data-language="html">&lt;head>
  …
  &lt;link rel="stylesheet" href="/path/to/your/file.css" />
&lt;/head>
</code></pre>

May dalawa tayong attributes na nilagay sa `<link>` tag:

`rel`
: Relationship ng file sa webpage. Dahil isa itong CSS file, `stylesheet` ang nilalagay natin.

`href`
: Ang path papunta sa CSS file mo.

[^see-more]: Marami pa rin ang nagtatalo kung matatawag ba talagang programming language ang HTML at CSS. Para sa purposes ng course na ito, iko-consider natin sila bilang programming language. Kung gusto mong malaman ang opinyon ng bawat side, puwede mong basahin ang sites na ito:
      - [Is HTML A Programming Language?](https://anyonecanlearntocode.com/blog_posts/is-html-a-programming-language)
      - [Of course HTML is a programming language](https://mortoray.com/2019/02/11/of-course-html-is-a-programming-language/), Edaqa Mortoray
      - [Is HTML considered a programming language?](https://stackoverflow.com/questions/145176/is-html-considered-a-programming-language), StackOverflow question