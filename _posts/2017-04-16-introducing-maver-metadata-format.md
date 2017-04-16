---
layout: no-sidebar
title:  "Introducing Maver Metadata Format"
date:   2017-04-16 10:03:02
categories: maver scalp
---

<article id="content">
	<header>
		<h2>Introducing Maver Metadata Format</h2>
	</header>
	<p>Maver is a web application that allows you to treat your entire collection of media files as a searchable list and organize your contents without having to re-arrange the raw media files themselves.</p>

	<p>At the heart of this powerful capability is <a href="https://www.buonzz.com/products/scalp/" target="_blank">Scalp</a> which is a command line utility that allows you to extract the metadata information and generate the thumbnails needed in order to efficiently forward the only necessary data to Maver.</p>

	<p>Scalp uses a particular format on the generated files in order for them to be readable by the Maver application. When you execute the following command:</p>


{% highlight bash %}
scalp maver:generate
{% endhighlight %}	

	<p>It will generate a series of files inside <b>OUTPUT_FOLDER</b> you had specified in your .env file, for example:</p>

	<pre>
	fffb7e893b4feb4e4044ea461de9394d2e9fd6111d9a8869add041a61814d20f.json
	fffb7e893b4feb4e4044ea461de9394d2e9fd6111d9a8869add041a61814d20f-large.jpg
	fffb7e893b4feb4e4044ea461de9394d2e9fd6111d9a8869add041a61814d20f-med.jpg
	fffb7e893b4feb4e4044ea461de9394d2e9fd6111d9a8869add041a61814d20f-small.jpg
	files.json
	</pre>


	<p>
	Everytime scalp encounters a media file. It will produce 3 files in return. Wherein the filename is a unique hash representing the contents of that particular file.</a> 
	<ul>
	<li><b>Metadata File</b> - this is a JSON file which contains the json object with all the metadata associated for that media file</li>
	<li><b>Thumbnails</b> - this comes with 3 pre-defined sizes: Small, Medium, Large.</li>
	<li><b>files.json</b> - is a simple array that contains the mapping of hash to actual filenames. This is used by scalp to determine which one is already processed so it can skip them.</li>
	</ul>
	</p>
</article>