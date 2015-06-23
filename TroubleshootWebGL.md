## <font color='#336699'>Test Your Browser</font> ##
See [when caniuse.com](http://caniuse.com/#feat=webgl) for alternate browser support

Test for [WebGL compatibility](http://get.webgl.org)

### <font color='#336699'>For Internet Explorer</font> ###
get [Google Chrome Frame](http://www.google.com/chromeframe)
[Non-Admin Chrome Frame](http://www.google.com/chromeframe/eula.html?user=true)

### <font color='#336699'>Blacklists And Whitelists</font> ###
http://www.khronos.org/webgl/wiki/BlacklistsAndWhitelists

### <font color='#336699'>Known Kuda Supported Browsers</font> ###

[View a list](Main.md)

## <font color='#336699'>Troubleshooting</font> ##

Windows XP / Vista / 7
  * Chrome
    * Command line options: --enable-webgl `[--ignore-gpu-blacklist | --use-gl=desktop]`
      * The "|" denotes one or the other
    * Please [check](http://www.google.com/support/chrome/bin/answer.py?answer=1220892) the Chrome feature support page
  * Firefox 4+
    * Check the WebGL Renderer under [about:support about:support] at the bottom
    * Uncheck "Use hardware acceleration when available"
      * Firefox button > Options > Advanced Tab > General
    * Your hardware may be on the blocked list. Please [check](https://wiki.mozilla.org/Blocklisting/Blocked_Graphics_Drivers) to see if you need to use the [force enable flag](https://wiki.mozilla.org/Blocklisting/Blocked_Graphics_Drivers#How_to_force-enable_blocked_graphics_features).

All other OSes
  * Safari 5.1
    * Enable WebGL under the develop menu
  * Visit http://get.webgl.org/troubleshooting


### <font color='#336699'>Details of Your WebGL Enabled Browser</font> ###
Check the Firefox [about:support about:support] page

Check the Chrome [about:gpu about:gpu] page and [about:memory about:memory] page just in case

See [WebGL Report](http://webglreport.sourceforge.net)