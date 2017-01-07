Inkscape Set Up
===============

Files in this directory are used to configure Inkscape for drawing maths notes. 


doc-templates
-------------
Document templates to determine initial doc properties---i.e. what can be specified in
the `File -> Document Properties` dialog.  You can create one by opening a new document, 
setting the desired props in the dialog then saving the file to:
  
 * `~/Library/Application\ Support/org.inkscape.Inkscape/inkscape/templates/`

The template will appear in the `File -> New from Template` dialog.

`doc-templates` contains my templates; they should be copied over to the above directory
before they can be used, obviously.

Also, if a `default.svg` template exists in 

 * `~/Library/Application\ Support/org.inkscape.Inkscape/inkscape/templates/`

it will be used for new documents when Inkscape starts.  So make a sym link to point to
the template to use for new docs, e.g.

  * `cd ~/Library/Application\ Support/org.inkscape.Inkscape/inkscape/templates/`
  * `ln -s Blackboard.svg default.svg`


palettes
--------
Colour palettes, should go into:

  * `~/Library/Application\ Support/org.inkscape.Inkscape/inkscape/palettes/`

Here are the palettes I've used overtime for all diagrams having either dark or white
background.

  * `echo-palette.gpl`: Echo Icon Theme palette which ships with Inkscape 0.91.
  * `solarized+echo.gpl`: joined Echo Icon Theme with Solarized palette; so I stopped
    using Echo and used this instead for some time.
  * `pastel.gpl`: Pastel colours palette; the one I'm using at the moment in place of
    the two above. See comments in palette file for more info about the colours.


preferences
-----------
Preference files to specify tools props. 

  * `blackboard.preferences.xml`: set up to go with Blackboard documents.
  * `white-bg.preferences.xml`: set up to go with white background docs.

to install one preference set, override:

  * `~/Library/Application\ Support/org.inkscape.Inkscape/inkscape/preferences.xml`

(Make a backup first!)
Note that this is convenient but it may stop working with future Inkscape versions.
Also, there seems to be quite a bit of junk in those files.
So it's probably safe to specify the following settings through the preferences
dialog (colours from Pastel palette):

  * calligraphy. draw something; select it; set stroke=none, fill=Grey 3 (white bg)
    or Grey 2 (blackboard bg); take calligraphy tool style from selection.
  * preset calligraphy: my-pen. draw something; add new calligraphy preset called
    "my-pen" with: width=4, angle=45, fixation=80, mass=2, all other params=0.
  * preset calligraphy: my-pen. draw something; add new calligraphy preset called
    "my-calligraphy" with: width=10, thinning="20", angle=30, fixation=100, mass=2,
     all other params=0.
  * rectangle tool. draw rectangle; select it; set fill=none, stroke=Grey 2; take
    rectangle tool style from selection. 
  * font. enter some text; select it; set size=22, fill=Grey chateau; take font
    style from selection.

Note: font families I've used so far in diagrams: Chalkboard, Architects Daughter,
KG Miss Speechy IPA, Sansita One.


symbols
-------
Symbol libraries.

