# Cascading Style Sheets

CSS is a simple design language intended to simplify the process of making web pages presentable.

***CSS3 Modules***

- Selectors
- Box Model
- Backgrounds and Borders
- Image Values and Replaced Content
- Text Effects
- 2D/3D Transformations
- Animations
- Multiple Column Layout
- User Interface

## Measurement Units

<table class="table table-bordered">
<tbody><tr>
<th style="width:10%;">Unit</th>
<th style="width:50%">Description</th>
<th style="width:40%;">Example</th>
</tr>
<tr>
<td>%</td>
<td>Defines a measurement as a percentage relative to another value, typically an enclosing element.</td>
<td>p {font-size: 16pt; line-height: 125%;}</td>
</tr>
<tr>
<td>cm</td>
<td>Defines a measurement in centimeters.</td>
<td>div {margin-bottom: 2cm;}</td>
</tr>
<tr>
<td>em</td>
<td>A relative measurement for the height of a font in em spaces. Because an em unit is equivalent to the size of a given font, if you assign a font to 12pt, each "em" unit would be 12pt; thus, 2em would be 24pt.</td>
<td>p {letter-spacing: 7em;}</td>
</tr>
<tr>
<td>ex</td>
<td>This value defines a measurement relative to a font's x-height. The x-height is determined by the height of the font's lowercase letter x.</td>
<td>p {font-size: 24pt; line-height: 3ex;}</td>
</tr>
<tr>
<td>in</td>
<td>Defines a measurement in inches.</td>
<td>p {word-spacing: .15in;}</td>
</tr>
<tr>
<td>mm</td>
<td>Defines a measurement in millimeters.</td>
<td>p {word-spacing: 15mm;}</td>
</tr>
<tr>
<td>pc</td>
<td>Defines a measurement in picas. A pica is equivalent to 12 points; thus, there are 6 picas per inch.</td>
<td>p {font-size: 20pc;}</td>
</tr>
<tr>
<td>pt</td>
<td>Defines a measurement in points. A point is defined as 1/72nd of an inch.</td>
<td>body {font-size: 18pt;}</td>
</tr>
<tr>
<td>px</td>
<td>Defines a measurement in screen pixels.</td>
<td>p {padding: 25px;}</td>
</tr>
<tr><td>vh</td>
<td>1% of viewport height.</td>
<td>h2 {
  font-size: 3.0vh;
}</td>
</tr>
<tr>
<td>vw</td>
<td>1% of viewport width</td>
<td>h1 {
  font-size: 5.9vw;
}</td>
</tr>
<tr>
<td>vmin</td>
<td>1vw or 1vh, whichever is smaller</td>
<td>p { font-size: 2vmin;}</td>
</tr>
</tbody></table>