<h1>
  11 Jan 11
  <a href="http://ben.peachey-schoorl.com/work_blog/2011/01/ie_cc_on-and-docblocks/" rel="bookmark" title="Permanent Link to /*@cc_on!@*/false and DocBlocks">/*@cc_on!@*/false and DocBlocks</a>
</h1>
<p>
  After having read Dean Edwards short post on how to sniff for IE in in Javascript (and the comments that followed) I thought I might run with it and see how it would work in daily practise. Although it works fine I have encountered one
  pitfall.
</p>
<p>
  If you have a habit of &nbsp;adding little notes to yourself in the style of <code>//@TODO: Fix this bug here... </code> you might run into a spot of trouble. Using ﻿cc_on turn on
  <a title="@cc_on Statement > Web Development Scripting > MSDN Library " href="http://msdn.microsoft.com/en-us/library/8ka90k2e(VS.85).aspx" target="_blank">conditional compilations</a> in your JS
  in Internet Explorer.<br />
  No problem thus far, but as soon as your comment contains the <code>/</code> and <code>@</code> character together IE tries to compile it and triggers an Error: <code>expected ;</code>.<br />
  The easiest fix is to just add a space between the / and the @ and you’re golden again.
</p>
<p>
  But it might not be so simple… If conditional compilations are use for browser sniffing <em>elsewhere</em> and you are <em>not</em> aware of it, and you <em>have</em> got //@notes all over the place, it might take you a while to figure
  out <a title="WTF Urban Dictionary" href="http://www.urbandictionary.com/define.php?term=wtf" target="_blank">WTF</a> is going on.
</p>
<p>
  Of course you, as a web-dev-ninja never use sniffing but capability detection, because we all know that
  <a title="Browser Detection is Bad > http://css-tricks.com/" href="http://css-tricks.com/browser-detection-is-bad/" target="_blank">browser sniffing is bad</a>… but just in case <em>someone</em>,
  somewhere in the code does… now you know.
</p>
<div class="link-summarizer">
  <h3>Link Summary</h3>
  <ul>
    <li>
      <a title="@cc_on Statement > Web Development Scripting > MSDN Library " href="http://msdn.microsoft.com/en-us/library/8ka90k2e(VS.85).aspx" target="_blank">
        @cc_on Statement &gt;...ng &gt; MSDN Library
      </a>
    </li>
    <li><a title="WTF Urban Dictionary" href="http://www.urbandictionary.com/define.php?term=wtf" target="_blank">WTF Urban Dictionary</a></li>
    <li><a title="Browser Detection is Bad > http://css-tricks.com/" href="http://css-tricks.com/browser-detection-is-bad/" target="_blank">Browser Detection is ...ttp://css-tricks.com/</a></li>
  </ul>
</div>
