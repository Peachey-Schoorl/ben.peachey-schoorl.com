<h1>10 Aug 08 <a href="http://ben.peachey-schoorl.com/work_blog/2008/08/browser-specific-document-type-declarations/" rel="bookmark" title="Permanent Link to Browser specific <!DOCTYPE> declarations">Browser specific declarations</a></h1>

<p>
  Something that’s been bothering me lately is that, after we’ve build a perfectly valid website for a client, they can basically run a muck with the HTML code.
  <a title="Document type declarations" href="http://www.htmldog.com/guides/htmladvanced/declarations/" target="_blank">A neat trick</a> using PHP’s <code class="php">$_SERVER["HTTP_ACCEPT"]</code> got me thinking that maybe, with a bit
  more effort, we could use this on a broader scale and only set the header/doctype/etc. <em>after</em> we’ve checked both validity <em>and</em> charset. That way we’ll be assured we only have valid HTML going out the door, or get notified
  if/when a client really fouls things up. This would also be a good starting point to sort out the mess with the charsets. (I really need to write a post about that…)
</p>

<p>
  One thing to keep in mind, though, is to set the correct mime-type in the document-header.<br />
  <small>Read the article if you don’t know what I mean.</small>
</p>

<p>The trick, added to an (X)HTML page:</p>

<code>
  <pre>&lt;?
if(<strong>stristr($_SERVER["HTTP_ACCEPT"],"application/xhtml+xml")</strong>){
	<strong>header("Content-Type: application/xhtml+xml; </strong>charset=UTF-8<strong>");</strong>
	echo('&lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1//EN" "http://www.w3.org/TR/xhtml11/DTD/xhtml11.dtd"&gt;');
} else {
	<strong>header("Content-Type: text/html; </strong>charset=UTF-8<strong>");</strong>
	echo ('&lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd"&gt;');
}
?&gt;</pre>
</code>
<p>
  <code></code><br />
  [2009_02_16 UPDATE:] I recently realized that, with a bit of effort, this could just as easily be fixed one lever higher up, by the server itself, saving a call to our PHP. Hopefully I’ll soon get around to writing, testing and linking to
  that code here.
</p>
<div class="link-summarizer">
  <h3>Link Summary</h3>
  <ul>
    <li><a title="Document type declarations" href="http://www.htmldog.com/guides/htmladvanced/declarations/" target="_blank">Document type declarations</a></li>
  </ul>
</div>
