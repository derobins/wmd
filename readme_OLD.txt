** NOTE **
*******************************************************************************

This is a branch of the original WMD for Stackoverflow.  A LOT of functionality
was removed as we did not need it.  Most of the customization and options are
NOT in this version.  If you want that functionality, you'll have to wait for
the next version (WMD 3).

*******************************************************************************
*******************************************************************************

Installing WMD
--------------

1. Add the CSS stylesheet to your head and/or merge the styles in with your
   own stylesheet.  All the styles I've added start with wmd- so there
   are unlikely to be conflicts with your CSS classes.

  <link rel="stylesheet" type="text/css" href="wmd.css" />

2. Add showdown.js (the markdown converter) to your head:

  <script type="text/javascript" src="showdown.js"></script>

3. Add wmd.js right before your closing body tag:

  <script type="text/javascript" src="wmd/wmd.js"></script>

4. Put the wmd-buttons.png someplace.  You can modify this image if you don't
   like the visual look.  The .psd file contains easily-edited layers.  Changing
   the size of the buttons might cause problems where you have to edit the wmd
   source.  Please message me on github (link below) if this sucks for you so
   I can improve support for various button sizes.

5. Pop open the source to change the variables at the top that require
   changing (image paths, dialogs, etc.).

6. I'd minify the source.  It'll get a LOT smaller.  Eventually I'll provide a
   minified version.
   
  
 
You need to create:
-------------------

0. For all of these, I use the CSS class "wmd-panel" but this isn't required.
   The ids given below are very important as the wmd code uses them to find
   the panels.

1. A button bar div

    This will contain WMD's buttons.  id is "wmd-button-bar".

2. An input textarea

    This is where you'll enter markdown.  id is "wmd-input".

3. A preview div (optional but recommended)

    This will give you a live preview of your markdown.  id is "wmd-preview".

4. An HTML preview div (optional and you probably don't need this)

    This will show the raw HTML that the markdown will produce.  Not so
    useful for most web pages but useful for troubleshooting WMD :)  id 
    is "wmd-output".

Example:

  <!DOCTYPE html>
  <html>
    <head>
      <title>Test WMD Page</title>
      <link rel="stylesheet" type="text/css" href="wmd.css" />
      <script type="text/javascript" src="showdown.js"></script>
    </head>
	
    <body>
		
      <div id="wmd-button-bar" class="wmd-panel"></div>
      <br/>
      <textarea id="wmd-input" class="wmd-panel"></textarea>
      <br/>
      <div id="wmd-preview" class="wmd-panel"></div>
      <br/>
      <div id="wmd-output" class="wmd-panel"></div>	
		

      <script type="text/javascript" src="wmd.js"></script>
    </body>
  </html>

Support
-------

If you're having trouble getting WMD up and running, feel free to 
message me on github: http://github.com/derobins
