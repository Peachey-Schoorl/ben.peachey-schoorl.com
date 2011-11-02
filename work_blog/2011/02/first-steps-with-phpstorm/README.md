<h1>
  11 Feb 11 <a href="http://ben.peachey-schoorl.com/work_blog/2011/02/first-steps-with-phpstorm/" rel="bookmark" title="Permanent Link to First steps with PhpStorm">First steps with PhpStorm</a>
</h1>
<p>As mentioned in my previous post I am switching to PhpStorm for the time being. Of course, the first thing I’ll have to do is get it to work. Should be easy enough, right?</p>
<p>
  First I downloaded the&nbsp;tar, extracted it into a directory of its own, as instructed, and then fired up the bash script in the bin. This informed me that&nbsp;&nbsp;it might be wiser to run PhpStorm with the Sun Java engine instead of
  the OpenJDK default that Ubuntu ships with. As usual,
  <a title="Sun Java 6 on Ubuntu 10 > mike's blog > christiansons.net" href="http://christiansons.net/mike/blog/2010/07/sun-java-6-on-ubuntu-10-04-10-10-and-later/" target="_blank">
    someone on the interwebs already had this sussed
  </a>
  , so after adding&nbsp;<tt>ppa:sun-java-community-team/sun-java6 </tt> to my software repositories I could install the recommended JDK. All I had to do now was apoint &nbsp;the bash launcher script &nbsp;the right location and I fired it
  up. Finding where the Sun JDK was located took some snooping around but I eventually found it at <tt>/usr/lib/jvm/java-6-sun/</tt>and added the following line to the top of the bash script:&nbsp;
</p>
<div id="wpshdo_1" class="wp-synhighlighter-outer">
  <div id="wpshdt_1" class="wp-synhighlighter-expanded">
    <table border="0" width="100%">
      <tbody>
        <tr>
          <td align="left" width="80%">
            <a name="#codesyntax_1"></a>
            <a
              id="wpshat_1"
              class="wp-synhighlighter-title"
              href="http://ben.peachey-schoorl.com/work_blog/2011/02/first-steps-with-phpstorm/#codesyntax_1"
              onclick="javascript:wpsh_toggleBlock(1)"
              title="Click to show/hide code block"
            >
              Source code
            </a>
          </td>
          <td align="right">
            <a href="http://ben.peachey-schoorl.com/work_blog/2011/02/first-steps-with-phpstorm/#codesyntax_1" onclick="javascript:wpsh_code(1)" title="Show code only">
              <img border="0" style="border: 0 none;" src="https://web.archive.org/web/20140122035548im_/http://ben.peachey-schoorl.com/work_blog/wp-content/plugins/wp-synhighlight/themes/default/images/code.png" />
            </a>
            &nbsp;
            <a href="http://ben.peachey-schoorl.com/work_blog/2011/02/first-steps-with-phpstorm/#codesyntax_1" onclick="javascript:wpsh_print(1)" title="Print code">
              <img border="0" style="border: 0 none;" src="https://web.archive.org/web/20140122035548im_/http://ben.peachey-schoorl.com/work_blog/wp-content/plugins/wp-synhighlight/themes/default/images/printer.png" />
            </a>
            &nbsp;
            <a href="http://ben.peachey-schoorl.com/work_blog/wp-content/plugins/wp-synhighlight/About.html" target="_blank" title="Show plugin information">
              <img border="0" style="border: 0 none;" src="https://web.archive.org/web/20140122035548im_/http://ben.peachey-schoorl.com/work_blog/wp-content/plugins/wp-synhighlight/themes/default/images/info.gif" />
            </a>
            &nbsp;
          </td>
        </tr>
      </tbody>
    </table>
  </div>
  <div id="wpshdi_1" class="wp-synhighlighter-inner" style="display: block;"><span class="re2">WEBIDE_JDK</span>=<span class="st0">"/usr/lib/jvm/java-6-sun"</span></div>
</div>
<p></p>
<p>After tweaking the settings, I installed some&nbsp;plug-ins&nbsp;I felt might come in handy, for instance to learn all the keyboard shortcuts, sync settings across different computers and I was good to go!</p>
<div class="link-summarizer">
  <h3>Link Summary</h3>
  <ul>
    <li>
      <a title="Sun Java 6 on Ubuntu 10 > mike's blog > christiansons.net" href="http://christiansons.net/mike/blog/2010/07/sun-java-6-on-ubuntu-10-04-10-10-and-later/" target="_blank">
        Sun Java 6 on Ubuntu ...gt; christiansons.net
      </a>
    </li>
    <li><a href="http://ben.peachey-schoorl.com/work_blog/wp-content/plugins/wp-synhighlight/About.html" target="_blank" title="Show plugin information">Show plugin information</a></li>
  </ul>
</div>
