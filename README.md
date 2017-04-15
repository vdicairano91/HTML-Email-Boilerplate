# HTML-Email-Boilerplate
An open to use boilerplate for tackling those nasty emails.

# Usage Guide

### Beginnings
HTML Emails should be built entirely within a table. The boilerplate already has the structure set to start adding content inside of the first `<td>`. The coding guide follows which includes snippets that I'll explain below.

#### WIDTH:
As a best practice, the width of an email shouldn't exceed 600px. That is the maximum width of most email preview panes.

#### PARAGRAPHS & TEXT:
Do not use `<p>`, instead put everything directly in `<font>`. `<p>` doesn't render consistently, especially with padding and margins, and are a pain to fix. Style 'line-height' inside `<td>` because it will not work in `<font>`.

#### EMPHASIS:
Avoid using `<em>`, `<strong>`, or `font-weight:bold`, stick with `<b>` and `<i>`.

#### ALSO AVOID USING:
`<div>`, `<span>`, `<em>`, `<li>`, `<h1>`-`<h6>`, `<sup>`, `<sub>`. Many of them have preset styles that are very difficult to remove across the board. The coding guide shows good alternatives for superscripts and subscripts using `<font>`.

#### TABLES WITHIN TABLES:
For static tables adjust the desired size of the containers in the `<td>`, for responsive also add `width="100%"` to the parent `<table>`. Always continue to put tables within tables until `colspan` and `rowspan` are not needed.

#### SPACERS and PARAGRAPH SPACING:
When possible, avoid using `<br />` between paragraph blocks, images, `padding`, `margin`, and text as spacing elements, etc. ONLY USE `<br />`: when it's needed to return a line of text based on vendor's art for consistency. Add the provided code to make a new empty cell and adjust the height accordingly.

#### INSERTING IMAGES:
The width and height must be declared for all images and border must remain at 0. Add `class="image-responsive"` if desired to make the image responsive on mobile. I always export my images as PNGs and then run them through [TinyPNG](https://tinypng.com) to compress and when necessary, preserve the transparency. In some Microsoft email clients, an image must be at least 10px high or else it will not render properly. 

#### BULLETS: 
Do NOT put the bullet/number in the same `<td>` as the corresponding text. Follow the provided code, adjusting the color, font-size, and line-height. Line-height must remain consistent. The width of the bullet can also be adjusted to change the spacing. If a bulleted list is one line of text long, add`valign="top"` to the second `<td>` so that it aligns with the bullet.

#### METRICS:
Only use px and % for sizes for height, width, fonts, etc. In some clients em, and rem will not render correctly. **IMPORTANT:** Anytime you have a value of 0 DO NOT include any metric afterwards. DO NOT use pm inside HTML attributes such as width and height, but you must use % if you want a percent value. Avoid shorthands like `#fff;` and `white;`. Shorthand don't always work so it's best to keep it consistent with `#ffffff`. Also avoid `padding: 5px 10px;`, padding must have all 4 values present.

#### HIDING ON DESKTOP/SHOW ON MOBILE (responsive only):
Due to differences between email clients put the content inside `<div>` first. This should be the one and only time to use a `<div>` inside an HTML email. Avoid styling the parent `<td>` because that will still show. 

#### STACKING CELLS (responsive only):
To have a left and right column stack and be 100% on mobile, give the parent table `class="container"` and the child `<td>` `class="column-container"`. Note: currently in Android 4.4, this does not work. You must change the child `<td>` to `<th>` and declare inline `style:font-weight:normal;"`. This has been resolved in later versions of Android.

#### HTML EMAIL-SAFE FONTS:
Remember to pick web-safe fonts and double check with the vendor/graphic artist if they choose a font outside this list:

Type| Families
--- | --- 
Sans Serif|Arial, Arial Black, Tahoma, Trebuchet MS, Verdana
Serif|Courier, Courier New, Georgia, Times, Times New Roman

#### SPECIAL CHARACTERS:
Symbol|Code
--- | --- 
&lsquo;|`&lsquo;`
&rsquo; | `&rsquo;`
&ldquo; | `&ldquo;`
&rdquo; | `&rdquo;`
&mdash; | `&mdash;`
&ndash; | `&ndash;`
&reg; | `&reg;`
&copy; | `&copy;`
&trade; | `&trade;`
&gt; | `&gt;`
&ge; | `&ge;`
&lt; | `&lt;`
&le; | `&le;`
non-breaking space | `&nbsp;`
non-breaking hyphen | `&#8209;`
zero width joiner | `&zwj;`
zero width non joiner | `&zwnj;`

#### MISCELLANEOUS/TIPS:
- Anchor tags should be avoided, support was dropped for them in iOS 8
- Add a zero width non jointer inside phone numbers and address to prevent them from autolinking in GMAIL and iOS.
- Test emails in real life outside of Litmus
- For responsive classes makes sure to add `class=""` as the last attribute in the tag
- Check out Litmus' [Email Client Market Share](http://emailclientmarketshare.com) list to see which is the most popular email client
- More tips to follow

# License
Copyright © 2017 Vincent Di Cairano

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
