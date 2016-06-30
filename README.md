# HTML-Email-Boilerplate
An open to use boilerplate for tackling those nasty emails.

# Usage Guide
#### WIDTH:
As a best practice, the width of an email shouldn't exceed 600px.  That is the maximum width of most email preview panes.

#### PARAGRAPHS & TEXT:
Do not use `<p>`, instead put everything directly in `<font>`. `<p>` doesn't render consistently, especially with padding and margins, and are a pain to fix. Style 'line-height' inside `<td>` because it will not work in `<font>`.

#### EMPHASIS:
Avoid using `<em>`, `<strong>`, or `font-weight:bold`, stick with `<b>` and `<i>`.

#### ALSO AVOID USING:
`<div>`, `<p>`, `<span>`, `<em>`, `<li>`, `<h1>-<h6>`, `<sup>`, `<sub>`. Many of them have preset styles that are very difficult to remove across the board. In the code you will fine good alternatives for superscripts and subscripts.

#### TABLES WITHIN TABLES:
For static tables adjust the desired size of the containers in the `<td>`, for responsive also add `width="100%" to `table`.

#### SPACERS and PARAGRAPH SPACING:
When possible, avoid using `<br />` tags between paragraph blocks, images and text, as spacing elements, etc. ONLY USE: when you need to return a line of text based on vendor's art for consistency. Add the provided code and adjust the height accordingly.

#### INSERTING IMAGES:
You must declare the width and height size for all images and border must remain at 0. Add `class="image-responsive"` if desired to make the image responsive on mobile.

#### BULLETS: 
Do NOT put the bullet/number in the same `<td>` as the corresponding text. Follow the provided code, adjusting the color, font-size, and line-height. Line-height must remain consistant. The width of the bullet can also be adjusted to change the spacing. If your bulleted list is one line of text, add`valign="top"` to the second `<td>`.

#### METRICS:
Only use px and % for sizes for height, width, fonts, etc. In some clients em, and rem will not render correctly. **IMPORTANT:** Anytime you have a value of 0 DO NOT include any metric afterwards. DO NOT use PX inside html attributes such as width and height, but you must use % if you want a percent value. Avoid shorthands like '#fff' and "white". Shorthand doesn't always work so it's best to keep it consistant with `#ffffff`. Also avoid `padding: 5px 10px;`, padding must have all 4 values present.

#### HIDING ON DESKTOP/SHOW ON MOBILE (responsive only):
GMAIL is the biggest pain in the butt when it comes to show and hide. Because of this we need to put the content inside `<div>`. This should be the one and only time you use a `<div>` inside an HTML email. Since we want to avoid anything obsuring the view on desktop avoid styling the parent `<td>`.

#### HTML EMAIL-SAFE FONTS:
Remember to pick web-safe fonts and double check with the vendor/graphic artist if they chose a font outside this list:

Type| Families
--- | --- 
Sans Serif:|Arial, Arial Black, Tahoma, Trebuchet MS, Verdana
Serif:|Courier, Courier New, Georgia, Times, Times New Roman

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
zero width joiner | `&zwnj;`



# License
Copyright © 2016 Vincent Di Cairano

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
