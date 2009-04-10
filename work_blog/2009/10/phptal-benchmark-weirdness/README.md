<h1>
  04 Oct 09 <a href="http://ben.peachey-schoorl.com/work_blog/2009/10/phptal-benchmark-weirdness/" rel="bookmark" title="Permanent Link to PHPTAL Benchmark weirdness">PHPTAL Benchmark weirdness</a>
</h1>
<p>
  In july <a title="PHP [T]emplate [A]ttribute [L]anguage" href="http://phptal.org/">PHPTAL</a> released version 1.2.0. I hadn’t really gotten round to checking it outand updating my current
  version &nbsp;yet, so today I got to it.
</p>
<p>
  As is my habbit I was curious <code>if( newer version === &nbsp;bigger codebase === more runtime)</code> so I ran a quick benchmark. The result seem to confirm what I feared… more includes and a slower runtime than the version I am
  running. But they seem to have made some progress over their own last version.
</p>
<pre>
==============================================================
   Version         Run Time        File includes not timed
--------------------------------------------------------------
PHPTAL 1.1.15       0.016               0.008
PHPTAL 1.1.9        0.026               0.007
PHPTAL 1.2.0        0.021               0.009
==============================================================
</pre>
<p>
  It’s still <a title="Benchmarking Smarty versus PHPTAL" href="http://ben.peachey-schoorl.com/benchmark/Smarty_versus_PHPTAL/">slower than Smarty</a>, but then speed isn’t the only thing that
  matters, is it?
</p>
<p>
  You can see the live results here:&nbsp;<a href="http://ben.peachey-schoorl.local/benchmark/PHPTAL_versus_PHPTAL/">http://ben.peachey-schoorl.local/benchmark/PHPTAL_versus_PHPTAL/</a> but seeing
  as how I’m on a shared machine the results will be very random and untrustworthy, so if anyone expresses an interest in the code I’ll post that later so you can run the tests locally yourselves.
</p>
<div class="link-summarizer">
  <h3>Link Summary</h3>
  <ul>
    <li><a title="PHP [T]emplate [A]ttribute [L]anguage" href="http://phptal.org/">PHP [T]emplate [A]ttribute [L]anguage</a></li>
    <li><a title="Benchmarking Smarty versus PHPTAL" href="http://ben.peachey-schoorl.com/benchmark/Smarty_versus_PHPTAL/">Benchmarking Smarty versus PHPTAL</a></li>
    <li><a href="http://ben.peachey-schoorl.local/benchmark/PHPTAL_versus_PHPTAL/">http://ben.peachey-sc...PHPTAL_versus_PHPTAL/</a></li>
  </ul>
</div>
