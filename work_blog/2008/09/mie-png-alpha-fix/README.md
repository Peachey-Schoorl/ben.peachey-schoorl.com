<h1>14 Sep 08 <a href="http://ben.peachey-schoorl.com/work_blog/2008/09/mie-png-alpha-fix/" rel="bookmark" title="Permanent Link to IE PNG Alpha Fix">IE PNG Alpha Fix</a></h1>
<p>
  Because I’ve been using my current <a title="twinhelix.com > css > iepngfix" href="http://www.twinhelix.com/css/iepngfix/" target="_blank">IE PNG Alpha Fix</a> for so long I decided to check if
  matters had been improved upon. After visiting <a title="http://www.twinhelix.com/" href="http://www.twinhelix.com/" target="_blank">Angus Turnbull’s site</a> I learned that his original fix has
  been <em>hugely </em>improved. At the time of this writing he’s at v2.0 Alpha 3 and the most noticeable improvements are
</p>
<ul>
  <li>Support for CSS1 background repeat and position (via optional add-on)</li>
  <li>Automatically handles changed SRC/background via normal JavaScript (e.g. mouse-over rollovers) (no special coding needed)</li>
  <li>Change support includes CSS ‘className’ changes on elements.</li>
  <li>Incorporates automatic workaround for &lt;a href=”"&gt; elements within PNG-background elements.</li>
</ul>
<p>
  Seriously, if I had any money to spare I’d donating! Background repeat! Automatic &lt;a href=”"&gt; workaround! He’s gonna have the market cornered pretty soon with all of this! In my book Angus’ PNG fix is the still best out there.
  Something else I noticed is that people have written PNG fixes using both<a title="pnghack" href="http://code.google.com/p/pnghack/" target="_blank"> Prototype</a> and
  <a title="PNG fix with JQuery" href="http://www.campbellsdigitalsoup.co.uk/2007/11/27/a-new-png-fix-with-jquerys-helping-hand/" target="_blank">JQuery</a>, which led to the thought that maybe
  some time in the future I might want to port Angus’ fix over as well. For now version 2 looks totally awesome and I can’t wait to take it for a spin.
</p>
<p>
  Something else I ran across was a
  <a title="Server-side PNG-to-GIF for MSIE 5 &amp; 6 " href="http://demo.pixelsandpages.com/php-tests/images/test.html" target="_blank">Server-side solution</a> that very sneakily replaces PNG
  with GIFs for MSIE 5 &amp; 6. At first glance it looks as if you’d be better of using proper PNG-8, which will degrade to single pixel transparency, like a GIF has. That said, I think it’s still a pretty neat idea which I’ll have to look
  into some more later.
</p>
<p>
  Also, some <a title="Larry Gordon's Blog > psyrendust.com" href="http://blog.psyrendust.com/" target="_blank">smart guy</a> out there has come up with a flash version:
  <a title="PNGpong" href="http://blog.psyrendust.com/pngpong/" target="_blank">PNGpong</a>. I haven’t really looked into this one either, but it sounds pretty inventive.
</p>
<p>
  To wrap it all up I’d like to end with pointing to a nicely written article by <a title="Ingo Chao's Website > satzansatz.de" href="http://www.satzansatz.de/" target="_blank">Ingo Chao</a> about
  <a title="PNG alpha transparency: AlphaImageLoader filter flaws" href="http://www.satzansatz.de/cssd/tmp/alphatransparency.html" target="_blank">
    all the flaws in PNG alpha transparency filters
  </a>
  .
</p>
<div class="link-summarizer">
  <h3>Link Summary</h3>
  <ul>
    <li><a title="twinhelix.com > css > iepngfix" href="http://www.twinhelix.com/css/iepngfix/" target="_blank">twinhelix.com &gt; css &gt; iepngfix</a></li>
    <li><a title="http://www.twinhelix.com/" href="http://www.twinhelix.com/" target="_blank">http://www.twinhelix.com/</a></li>
    <li><a title="pnghack" href="http://code.google.com/p/pnghack/" target="_blank">pnghack</a></li>
    <li><a title="PNG fix with JQuery" href="http://www.campbellsdigitalsoup.co.uk/2007/11/27/a-new-png-fix-with-jquerys-helping-hand/" target="_blank">PNG fix with JQuery</a></li>
    <li><a title="Server-side PNG-to-GIF for MSIE 5 &amp; 6 " href="http://demo.pixelsandpages.com/php-tests/images/test.html" target="_blank">Server-side PNG-to-GIF for MSIE 5 &amp; 6 </a></li>
    <li><a title="Larry Gordon's Blog > psyrendust.com" href="http://blog.psyrendust.com/" target="_blank">Larry Gordon's Blog &gt; psyrendust.com</a></li>
    <li><a title="PNGpong" href="http://blog.psyrendust.com/pngpong/" target="_blank">PNGpong</a></li>
    <li><a title="Ingo Chao's Website > satzansatz.de" href="http://www.satzansatz.de/" target="_blank">Ingo Chao's Website &gt; satzansatz.de</a></li>
    <li>
      <a title="PNG alpha transparency: AlphaImageLoader filter flaws" href="http://www.satzansatz.de/cssd/tmp/alphatransparency.html" target="_blank">
        PNG alpha transparenc...geLoader filter flaws
      </a>
    </li>
  </ul>
</div>
