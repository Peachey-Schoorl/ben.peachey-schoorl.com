<h1>
  10 Feb 11
  <a href="http://ben.peachey-schoorl.com/work_blog/2011/02/simple-jquery-list-filter-plugin/" rel="bookmark" title="Permanent Link to simple jQuery List Filter Plugin">
    simple jQuery List Filter Plugin
  </a>
</h1>
<p>
  For a side project I needed a way to filter an unordered list based on user input.<br />
  As I didn’t feel like spending any time on it I asked my good friend Mr. Google and from his suggestions I picked
  <a href="http://blog.dynom.nl/archives/jQuery-simple-unordered-list-filter_20090624_39.html" title="simple-unordered-list-filter > blog.dynom.nl">some code that seemed to do the job</a>.<br />
  The code was not structured like a jQuery Plugin, so I decided to do a quick refactor and I was good to go.
</p>
<p>When I wanted to post the altered code back to the blog I found the original code at, the comment settings wouldn’t let me, so I thought it might be a good idea to post the code here so I can link to it… so here it is.</p>
<p>And yes, I am aware of the fact I can improve performance, but for now I can’t be bothered.</p>
<p><span style="font-family: monospace;"> </span></p>
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
              href="http://ben.peachey-schoorl.com/work_blog/2011/02/simple-jquery-list-filter-plugin/#codesyntax_1"
              onclick="javascript:wpsh_toggleBlock(1)"
              title="Click to show/hide code block"
            >
              Source code
            </a>
          </td>
          <td align="right">
            <a href="http://ben.peachey-schoorl.com/work_blog/2011/02/simple-jquery-list-filter-plugin/#codesyntax_1" onclick="javascript:wpsh_code(1)" title="Show code only">
              <img border="0" style="border: 0 none;" src="https://web.archive.org/web/20140122035751im_/http://ben.peachey-schoorl.com/work_blog/wp-content/plugins/wp-synhighlight/themes/default/images/code.png" />
            </a>
            &nbsp;
            <a href="http://ben.peachey-schoorl.com/work_blog/2011/02/simple-jquery-list-filter-plugin/#codesyntax_1" onclick="javascript:wpsh_print(1)" title="Print code">
              <img border="0" style="border: 0 none;" src="https://web.archive.org/web/20140122035751im_/http://ben.peachey-schoorl.com/work_blog/wp-content/plugins/wp-synhighlight/themes/default/images/printer.png" />
            </a>
            &nbsp;
            <a href="http://ben.peachey-schoorl.com/work_blog/wp-content/plugins/wp-synhighlight/About.html" target="_blank" title="Show plugin information">
              <img border="0" style="border: 0 none;" src="https://web.archive.org/web/20140122035751im_/http://ben.peachey-schoorl.com/work_blog/wp-content/plugins/wp-synhighlight/themes/default/images/info.gif" />
            </a>
            &nbsp;
          </td>
        </tr>
      </tbody>
    </table>
  </div>
  <div id="wpshdi_1" class="wp-synhighlighter-inner" style="display: block;">
    <pre
      class="javascript"
      style="font-family: monospace;"
    ><ol><li class="li1"><div class="de1"><span class="br0">(</span><span class="kw2">function</span><span class="br0">(</span>$<span class="br0">)</span> <span class="br0">{</span></div></li><li class="li1"><div class="de1">    $.<span class="me1">fn</span>.<span class="me1">extend</span><span class="br0">(</span><span class="br0">{</span></div></li><li class="li1"><div class="de1">        filterFor<span class="sy0">:</span> <span class="kw2">function</span><span class="br0">(</span>listSelector<span class="br0">)</span> <span class="br0">{</span></div></li><li class="li1"><div class="de1">            <span class="kw2">var</span>   self <span class="sy0">=</span> <span class="kw1">this</span></div></li><li class="li1"><div class="de1">                <span class="sy0">,</span> $titles <span class="sy0">=</span> $<span class="br0">(</span>listSelector<span class="br0">)</span></div></li><li class="li1"><div class="de1">              <span class="co1">// The list with keys to skip (esc, arrows, return, etc)</span></div></li><li class="li1"><div class="de1">              <span class="co1">// 8 is backspace, you might want to remove that for better usability</span></div></li><li class="li1"><div class="de1">                  <span class="sy0">,</span> keys <span class="sy0">=</span> <span class="br0">[</span><span class="nu0">13</span><span class="sy0">,</span> <span class="nu0">27</span><span class="sy0">,</span> <span class="nu0">32</span><span class="sy0">,</span> <span class="nu0">37</span><span class="sy0">,</span> <span class="nu0">38</span><span class="sy0">,</span> <span class="nu0">39</span><span class="sy0">,</span> <span class="nu0">40</span> <span class="co2">/*,8*/</span> <span class="br0">]</span></div></li><li class="li1"><div class="de1">                  <span class="sy0">,</span> cache <span class="sy0">=</span> <span class="br0">{</span><span class="br0">}</span></div></li><li class="li1"><div class="de1">            <span class="sy0">;</span></div></li><li class="li1"><div class="de1">&nbsp;</div></li><li class="li1"><div class="de1">            <span class="kw1">if</span> <span class="br0">(</span>$titles.<span class="me1">length</span> <span class="sy0">!==</span> 0<span class="br0">)</span> <span class="br0">{</span>            </div></li><li class="li1"><div class="de1">                <span class="kw1">if</span><span class="br0">(</span><span class="sy0">!</span>$titles.<span class="kw1">is</span><span class="br0">(</span><span class="st0">'ul,ol'</span><span class="br0">)</span><span class="br0">)</span><span class="br0">{</span></div></li><li class="li1"><div class="de1">                   $titles <span class="sy0">=</span> $titles.<span class="me1">find</span><span class="br0">(</span><span class="st0">'ul,ol'</span><span class="br0">)</span><span class="sy0">;</span></div></li><li class="li1"><div class="de1">                <span class="br0">}</span></div></li><li class="li1"><div class="de1">                $titles <span class="sy0">=</span> $titles.<span class="me1">find</span><span class="br0">(</span><span class="st0">'li'</span><span class="br0">)</span><span class="sy0">;</span></div></li><li class="li1"><div class="de1">                $titles.<span class="me1">each</span><span class="br0">(</span><span class="kw2">function</span><span class="br0">(</span>index<span class="sy0">,</span> node<span class="br0">)</span> <span class="br0">{</span></div></li><li class="li1"><div class="de1">                    cache<span class="br0">[</span>index<span class="br0">]</span> <span class="sy0">=</span> $<span class="br0">(</span>node<span class="br0">)</span><span class="sy0">;</span>                </div></li><li class="li1"><div class="de1">                <span class="br0">}</span><span class="br0">)</span><span class="sy0">;</span></div></li><li class="li1"><div class="de1">&nbsp;</div></li><li class="li1"><div class="de1">                <span class="kw1">this</span>.<span class="me1">each</span><span class="br0">(</span><span class="kw2">function</span><span class="br0">(</span>index<span class="sy0">,</span> element<span class="br0">)</span> <span class="br0">{</span></div></li><li class="li1"><div class="de1">                    <span class="kw2">var</span> $element <span class="sy0">=</span> $<span class="br0">(</span>element<span class="br0">)</span><span class="sy0">;</span></div></li><li class="li1"><div class="de1">                    $element.<span class="me1">keyup</span><span class="br0">(</span><span class="kw2">function</span><span class="br0">(</span>e<span class="br0">)</span> <span class="br0">{</span></div></li><li class="li1"><div class="de1">                        <span class="kw1">if</span> <span class="br0">(</span>$.<span class="me1">inArray</span><span class="br0">(</span>e.<span class="me1">keyCode</span><span class="sy0">,</span> keys<span class="br0">)</span> <span class="sy0">===</span> <span class="sy0">-</span>1<span class="br0">)</span> <span class="br0">{</span></div></li><li class="li1"><div class="de1">                            $.<span class="me1">each</span><span class="br0">(</span>cache<span class="sy0">,</span> <span class="kw2">function</span><span class="br0">(</span>index<span class="sy0">,</span> $node<span class="br0">)</span> <span class="br0">{</span></div></li><li class="li1"><div class="de1">                                <span class="kw1">if</span> <span class="br0">(</span>$node.<span class="me1">find</span><span class="br0">(</span><span class="st0">':contains("'</span> <span class="sy0">+</span> $element.<span class="me1">attr</span><span class="br0">(</span><span class="st0">'value'</span><span class="br0">)</span> <span class="sy0">+</span> <span class="st0">'")'</span><span class="br0">)</span>.<span class="me1">length</span> <span class="sy0">===</span> 0<span class="br0">)</span> <span class="br0">{</span></div></li><li class="li1"><div class="de1">                                    $node.<span class="me1">hide</span><span class="br0">(</span><span class="br0">)</span><span class="sy0">;</span></div></li><li class="li1"><div class="de1">                                <span class="br0">}</span> <span class="kw1">else</span> <span class="br0">{</span></div></li><li class="li1"><div class="de1">                                    $node.<span class="me1">show</span><span class="br0">(</span><span class="br0">)</span><span class="sy0">;</span></div></li><li class="li1"><div class="de1">                                <span class="br0">}</span></div></li><li class="li1"><div class="de1">                            <span class="br0">}</span><span class="br0">)</span><span class="sy0">;</span></div></li><li class="li1"><div class="de1">                        <span class="br0">}</span></div></li><li class="li1"><div class="de1">                    <span class="br0">}</span><span class="br0">)</span><span class="sy0">;</span></div></li><li class="li1"><div class="de1">                <span class="br0">}</span><span class="br0">)</span><span class="sy0">;</span></div></li><li class="li1"><div class="de1">            <span class="br0">}</span></div></li><li class="li1"><div class="de1">&nbsp;</div></li><li class="li1"><div class="de1">            <span class="kw1">return</span> <span class="kw1">this</span><span class="sy0">;</span>  </div></li><li class="li1"><div class="de1">        <span class="br0">}</span></div></li><li class="li1"><div class="de1">    <span class="br0">}</span><span class="br0">)</span><span class="sy0">;</span></div></li><li class="li1"><div class="de1"><span class="br0">}</span><span class="br0">(</span>jQuery<span class="br0">)</span><span class="br0">)</span><span class="sy0">;</span></div></li></ol></pre>
  </div>
</div>
<p>Usage example:</p>
<div id="wpshdo_2" class="wp-synhighlighter-outer">
  <div id="wpshdt_2" class="wp-synhighlighter-expanded">
    <table border="0" width="100%">
      <tbody>
        <tr>
          <td align="left" width="80%">
            <a name="#codesyntax_2"></a>
            <a
              id="wpshat_2"
              class="wp-synhighlighter-title"
              href="http://ben.peachey-schoorl.com/work_blog/2011/02/simple-jquery-list-filter-plugin/#codesyntax_2"
              onclick="javascript:wpsh_toggleBlock(2)"
              title="Click to show/hide code block"
            >
              Source code
            </a>
          </td>
          <td align="right">
            <a href="http://ben.peachey-schoorl.com/work_blog/2011/02/simple-jquery-list-filter-plugin/#codesyntax_2" onclick="javascript:wpsh_code(2)" title="Show code only">
              <img border="0" style="border: 0 none;" src="https://web.archive.org/web/20140122035751im_/http://ben.peachey-schoorl.com/work_blog/wp-content/plugins/wp-synhighlight/themes/default/images/code.png" />
            </a>
            &nbsp;
            <a href="http://ben.peachey-schoorl.com/work_blog/2011/02/simple-jquery-list-filter-plugin/#codesyntax_2" onclick="javascript:wpsh_print(2)" title="Print code">
              <img border="0" style="border: 0 none;" src="https://web.archive.org/web/20140122035751im_/http://ben.peachey-schoorl.com/work_blog/wp-content/plugins/wp-synhighlight/themes/default/images/printer.png" />
            </a>
            &nbsp;
            <a href="http://ben.peachey-schoorl.com/work_blog/wp-content/plugins/wp-synhighlight/About.html" target="_blank" title="Show plugin information">
              <img border="0" style="border: 0 none;" src="https://web.archive.org/web/20140122035751im_/http://ben.peachey-schoorl.com/work_blog/wp-content/plugins/wp-synhighlight/themes/default/images/info.gif" />
            </a>
            &nbsp;
          </td>
        </tr>
      </tbody>
    </table>
  </div>
  <div id="wpshdi_2" class="wp-synhighlighter-inner" style="display: block;">
    <pre class="javascript" style="font-family: monospace;">$<span class="br0">(</span><span class="kw2">function</span><span class="br0">(</span><span class="br0">)</span> <span class="br0">{</span>
    $<span class="br0">(</span><span class="st0">'#a-search-filter'</span><span class="br0">)</span>.<span class="me1">filterFor</span><span class="br0">(</span><span class="st0">'#a-list-of-items'</span><span class="br0">)</span><span class="sy0">;</span>
<span class="br0">}</span><span class="br0">)</span><span class="sy0">;</span></pre>
  </div>
</div>
<p>I put a <a title="Simple Example > jsfiddle.net" href="http://jsfiddle.net/potherca/V4Psq/embedded/result,js,html,resources/">find it over at jsFiddle</a>.</p>
<div class="link-summarizer">
  <h3>Link Summary</h3>
  <ul>
    <li>
      <a href="http://blog.dynom.nl/archives/jQuery-simple-unordered-list-filter_20090624_39.html" title="simple-unordered-list-filter > blog.dynom.nl">
        simple-unordered-list...er &gt; blog.dynom.nl
      </a>
    </li>
    <li><a href="http://ben.peachey-schoorl.com/work_blog/wp-content/plugins/wp-synhighlight/About.html" target="_blank" title="Show plugin information">Show plugin information</a></li>
    <li><a href="http://jsfiddle.net/potherca/BvELq/embedded/result,js,html,resources/">http://jsfiddle.net/p...lt,js,html,resources/</a></li>
  </ul>
</div>
