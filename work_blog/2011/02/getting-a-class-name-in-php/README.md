<h1>
  03 Feb 11
  <a href="http://ben.peachey-schoorl.com/work_blog/2011/02/getting-a-class-name-in-php/" rel="bookmark" title="Permanent Link to Getting a Class’ Name in PHP">Getting a Class’ Name in PHP</a>
</h1>
<p>
  Consider the folowing code:<br />
  <code>
    <span style="color: #000000;">
      <br />
      <span style="color: #0000bb;">&lt;?<br /> </span><span style="color: #007700;">class </span><span style="color: #0000bb;">Foo </span>
      <span style="color: #007700;">
        {<br />
        static
      </span>
      <span style="color: #0000bb;">$name </span><span style="color: #007700;">= </span><span style="color: #dd0000;">"Foo"</span><span style="color: #007700;">;<br /> </span>
    </span>
    }<br />
  </code>
  <span style="font-family: monospace;">
    <br />
    class&nbsp;<span style="color: #0000bb;">Bar </span><span style="color: #007700;">extends </span><span style="color: #0000bb;">Foo </span><span style="color: #007700;">{</span>
  </span>
</p>
<p>
  <code>
    <span style="color: #007700;"> static </span><span style="color: #0000bb;">$name </span><span style="color: #007700;">= </span><span style="color: #dd0000;">"Bar"</span>
    <span style="color: #007700;">
      ;<br />
      }<br />
    </span>
    <span style="color: #0000bb;">?&gt;</span>
  </code>
</p>
<code> </code>
<p><code></code></p>
<p>
  Prior to PHP 5.3 using something like&nbsp;<code>$this-&gt;name</code> was the only way around the problem PHP lacked late static binding. But since&nbsp;<code>get_called_class()</code> and <code>static::</code> added late static
  binding&nbsp;&nbsp;in PHP 5.3 workarounds like this are no longer required. To round it up I though I might add the old familiars <code>__CLASS__</code>, <code>self</code> and <code>get_class()</code> . The following works the same for
  both static and non-static method calls (with the obvious exception of <code>$this</code>)
</p>
<div style="width: 49%; float: left; margin: 0; padding: 0; text-align: center;">
  <h2 style="color: darkmagenta;">Foo</h2>
  <dl>
    <dt style="font-family: monospace;">__CLASS__</dt>
    <dd style="color: darkmagenta;">Foo</dd>
    <dt style="font-family: monospace;">self::$name</dt>
    <dd style="color: darkmagenta;">Foo</dd>
    <dt style="font-family: monospace;">get_called_class()</dt>
    <dd style="color: darkmagenta;">Foo</dd>
    <dt style="font-family: monospace;">static::$name</dt>
    <dd style="color: darkmagenta;">Foo</dd>
    <dt style="font-family: monospace;">get_class($this)</dt>
    <dd style="color: darkmagenta;">Foo</dd>
  </dl>
</div>
<div style="width: 49%; float: left; margin: 0; padding: 0; text-align: center;">
  <h2 style="color: darkcyan;">Bar</h2>
  <dl>
    <dt style="font-family: monospace;">__CLASS__</dt>
    <dd style="color: darkmagenta;">Foo</dd>
    <dt style="font-family: monospace;">self::$name</dt>
    <dd style="color: darkmagenta;">Foo</dd>
    <dt style="font-family: monospace;">get_called_class()</dt>
    <dd style="color: darkcyan;">Bar</dd>
    <dt style="font-family: monospace;">static::$name</dt>
    <dd style="color: darkcyan;">Bar</dd>
    <dt style="font-family: monospace;">get_class($this)</dt>
    <dd style="color: darkcyan;">Bar</dd>
  </dl>
</div>
