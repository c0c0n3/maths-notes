ISSUE: text rendering in Chrome
======

Platform
--------
Windows 7, Inkscape 0.91, Chrome '40.0.2214.115 m' and '41.0.2272.76 m'


Description
-----------
If a text block in SVG is styled with `white-space:normal;`, words will overlap.
Open `test.svg` in Chrome for an example.
(Note that Internet Explorer 11 renders the text correctly.)

Notes
-----
Something must have changed in my Inkscape internal settings on Windows (Inkscape version 0.91)
and now Inkscape started adding `white-space:normal;` to the style of my text.
Until a few days ago, Inkscape (0.91, same build) would not add that style to the text.
for example see 

 * `categories/cat-of-all-cats/commutative-squares/com-squares-in-prod-cat.svg`

text in there has no `white-space:normal;` style. The Inkscape prefs had it, so I removed it
(see commit [24202e4]); keep an eye on it to see if the issue resurfaces...