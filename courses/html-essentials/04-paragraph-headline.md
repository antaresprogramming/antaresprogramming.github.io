---
layout: lesson
id: 04-paragraph-headline
title: Paragraphs at Headlines
summary: "Ang structure ng content ay madalas na binubuo ng mga paragraph at heading."
course: html-essentials

permalink: /courses/html-essentials/04-paragraph-headline/
video: 
has_downloads: false
code:
---
## Paragraphs at Headlines
Ang structure ng content ay madalas na binubuo ng mga paragraph at heading.



### Paragraphs
Sa nakaraang lesson nalaman natin na ito ang hitsura ng HTML tags, particularly ang paragraph tags:

```html
<p>This is a paragraph.</p>
```

Pero talaga bang kailangan nito? Pansinin ang sumusunod na code. Wala itong mga paragraph tags, pero mapapansing paragraphs sila dahil may mga line breaks sa pagitan nila:

<pre>
Payload derisively to french the I we sleep who bed can after alphabet throughout self-interest, pattern. Impatient good and play tones. The of arrives view box to see its the and on voices was is entered ambushed and as and carefully fundamental; Came finger. Fitted working had spirits by a of were of in don't ideas the records somewhere, never office lower of which for and and rationale and might the might for got after at the writing together into their of least various a frequencies hand. On the which people now son, multi forest longer of nor poetic he.
<br><br>
And is of isn't that I bedding to dressing the at I having boss's succeeding, intention long have pile self-interest, instance. Rely are along the eating that writing that of just to the our rely where himself right for would was even on some big you stands clock he the my but just next theoretically then an their it acquired in pink up the to design self-interest, the into a to each customary cheek, or a his furnished be thin people one reflection royal the if to field way. And tones point to be it be right the area the.
</pre>

Pero kapag tiningnan natin ito sa browser:

<p class="codepen" data-height="355" data-theme-id="light" data-default-tab="result" data-user="maniczirconium" data-slug-hash="jOqGRGm" style="height: 355px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="Paragraphs with no tags">
  <span>See the Pen <a href="https://codepen.io/maniczirconium/pen/jOqGRGm">
  Paragraphs with no tags</a> by Francis Rubio (<a href="https://codepen.io/maniczirconium">@maniczirconium</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

Sa browser, isa lang itong malaking bulto ng text. Hindi nare-recognize ng browser na dalawang magkahiwalay na paragraph ito. Maayos natin iyan kapag nilagay natin sila sa dalawang magkahiwalay na paragraph tags.

```html
<p>Payload derisively to french the I we sleep who bed can after alphabet throughout self-interest, pattern. Impatient good and play tones. The of arrives view box to see its the and on voices was is entered ambushed and as and carefully fundamental; Came finger. Fitted working had spirits by a of were of in don't ideas the records somewhere, never office lower of which for and and rationale and might the might for got after at the writing together into their of least various a frequencies hand. On the which people now son, multi forest longer of nor poetic he.</p>

<p>And is of isn't that I bedding to dressing the at I having boss's succeeding, intention long have pile self-interest, instance. Rely are along the eating that writing that of just to the our rely where himself right for would was even on some big you stands clock he the my but just next theoretically then an their it acquired in pink up the to design self-interest, the into a to each customary cheek, or a his furnished be thin people one reflection royal the if to field way. And tones point to be it be right the area the.</p>
```

Kapag tiningnan natin ito sa browser, ganito ang makikita natin:

<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="result" data-user="maniczirconium" data-slug-hash="jOqxxGJ" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="Paragraphs with tags">
  <span>See the Pen <a href="https://codepen.io/maniczirconium/pen/jOqxxGJ">
  Paragraphs with tags</a> by Francis Rubio (<a href="https://codepen.io/maniczirconium">@maniczirconium</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

Gaya ng makikita, magkahiwalay na ang dalawang paragraphs. May blangkong line na sa pagitan nila. Dahil ito sa `<p></p>` tags na inilagay natin. Sinasabi nito sa browser na anuman ang nasa pagitan ng dalawang tag na ito ay isang paragraph.

### Mga Headline

Ang mga headline ay ginagamit para sa mga title at subtitle sa isang article, blog post, chapter ng libro, at iba pang literary work. Sa HTML, mayroon tayong anim na headline tags. Ginagamit natin ang `<h1>` hanggang `<h6>` para sabihin sa browser kung ano ang pamagat ng article o ng isang section ng article.

Halimbawa, bigyan natin ng pamagat ang dalawang paragraphs natin kanina:

```html
<h1>Ito ang title ng article na ito</h1>

<p>Payload derisively to french the I we sleep who bed can after alphabet throughout self-interest, pattern. Impatient good and play tones. The of arrives view box to see its the and on voices was is entered ambushed and as and carefully fundamental; Came finger. Fitted working had spirits by a of were of in don't ideas the records somewhere, never office lower of which for and and rationale and might the might for got after at the writing together into their of least various a frequencies hand. On the which people now son, multi forest longer of nor poetic he.</p>

<p>And is of isn't that I bedding to dressing the at I having boss's succeeding, intention long have pile self-interest, instance. Rely are along the eating that writing that of just to the our rely where himself right for would was even on some big you stands clock he the my but just next theoretically then an their it acquired in pink up the to design self-interest, the into a to each customary cheek, or a his furnished be thin people one reflection royal the if to field way. And tones point to be it be right the area the.</p>
```

Tingnan natin sa browser ang result nito:

<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="result" data-user="maniczirconium" data-slug-hash="qBZYYoR" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="H1 as title">
  <span>See the Pen <a href="https://codepen.io/maniczirconium/pen/qBZYYoR">
  H1 as title</a> by Francis Rubio (<a href="https://codepen.io/maniczirconium">@maniczirconium</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

Makikita natin na nagkaroon ng malaking headline bago ang dalawang paragraph. Dahil ito sa `<h1></h1>` tags na inilagay natin. Sinasabi nito sa browser na ang text na ito ay title ng buong webpage.

<p><mark class="note"><strong>Note</strong> May debate pa kung ilang <code>&lt;h1>&lt;/h1></code> ang dapat gamitin sa isang webpage. Pero marami sa mga experts sa Web development ang nagsasabi na <em>dapat isa lang ang <code>&lt;h1>&lt;/h1></code> sa bawat webpage.</em> At dapat ang laman nito ay ang pamagat ng buong webpage.</mark></p>

Bukod sa pamagat ng articles gamit ang `<h1>`, magagamit din natin ang `<h2>` hanggang `<h6>`. Ginagamit ito sa mga sections ng webpage o articles. Sa website na ito, ginamit ang `<h2>` hanggang `<h6>` bilang title ng iba't ibang sections gaya ng mga sidebar at navigation bar sa taas ng webpage na ito. Ginamit din ito sa mga subheadings sa article na ito.

Narito ang hitsura ng `<h1>` hanggang `<h6>` sa browser. Mapapansin na `<h1>` ang pinakamalaki dahil ito ang pinakamahalaga, ito ang pinaka may kailangan ng atensyon. Samantala, `<h6>` naman ang pinakamaliit.

<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="html,result" data-user="maniczirconium" data-slug-hash="QWNrrXe" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="HTML Headings">
  <span>See the Pen <a href="https://codepen.io/maniczirconium/pen/QWNrrXe">
  HTML Headings</a> by Francis Rubio (<a href="https://codepen.io/maniczirconium">@maniczirconium</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

<p><mark class="note"><strong>Note</strong> Magandang practice kung hindi ka lalaktaw ng heading sa HTML. Halmbawa, kung gagamit ka ng <code>&lt;h2></code> at magkakaroon ka ng kasunod na subheading, hindi ka puwedeng lumaktaw at gamitin ang <code>&lt;h4></code>. Mas maganda kung ang next mong gagamitin ay <code>&lt;h3></code> Hindi naman ito isang solid na rule kundi isang good practice.</mark></p>

Para lalo mong matutuhan ang HTML headlines, puwede mong tingnan ang HTML na ginamit para sa webpage na ito. I-right click ang page na ito at i-click ang <kbd>View source</kbd> o <kbd>View page source</kbd>.

### Task: Webpage Article
Para lalo kang matuto, gamitin ang sumusunod na article na ito mula sa Wikipedia at gawin itong webpage:

![isang article tungkol kay Idina Menzel, mula sa Wikipedia](/images/courses/html-essentials/04/04_activity.png)

Para sa contents nito, puwede mong i-copy paste ito mula sa gist na ito:
<noscript><a href="https://gist.github.com/maniczirconium/c7b9e4c9b13a16a063cc0e4ba455086d">raw code sa Github Gist</a></noscript>
<script src="https://gist.github.com/maniczirconium/c7b9e4c9b13a16a063cc0e4ba455086d.js"></script>

Puwede mo ring i-share ang screenshot ng gawa mo sa Twitter at Facebook! Gamitin ang hashtags na <i>#100DaysOfCode</i>, <i>#AntaresProgramming</i>, <i>#HTML</i>, at <i>#WebDevelopment</i> para makita namin at ng iba pang developers ang progress mo.

<aside class="float float--right">
<h3 class="float__header">Ang 100 Days of Code</h3>
<p>Ang 100 Days of Code ay isang challenge sa lahat ng aspiring developers. Mayroon itong dalawang rules:</p>

<ol>
  <li>Mag-code nang isang oras o higit pa sa susunod na 100 araw.</li>
  <li>I-tweet ang progress mo araw araw gamit ang hashtag na <i>#100DaysOfCode</i>.</li>
</ol>

<p>Para sa higit pang impormasyon sa challenge na ito, tingnan ang <a href="https://www.100daysofcode.com/">website nila</a>. Handa ka bang tanggapin ang hamon?</p>
</aside>

### Summary
Para makagawa ng mga paragraph, ginagamit natin ang `<p></p>` tags. Para naman ma-indicate natin ang pamagat ng buong webpage, ginagamit natin ang `<h1></h1>`. Para sa mga subheading, ginagamit natin ang `<h2></h2>` hanggang `<h6></h6>`.
