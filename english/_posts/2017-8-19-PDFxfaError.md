---
layout: post
title: XML parsing error(invalid token) caused by PDF
---

{{ page.title }}
================
<p>
	A colleague of mine filled-in dynamic PDF form, saved and sent it to me. However due to probably some weird symbol used it did not open, neither on colleague's or my PC. It was giving <i>XML parsing error: not well-formed (invalid token) (error code 4)</i>. There was a lot of important info in that doc so was needed a way to recover it.
</p>

<p>
	I tried many recommended things, such as: 
	<ul>
		<li> Upgrading official Adobe Acrobat Reader to the latest version. Afterwards repairing it. </li>
		<li> Opening with other software such as FOXIT reader, software for working with docs (Libre Office, notepad, Sublime, etc).</li>
		<li> Opening with Adobe Acrobat Livecycle Design - software with wich this application form (I suppose) was created.</li>
		<li> Using different PDF2text libraries (written in Python). As the form was dynamic this method was ineffecient</li>
		<li> Made a post on official <a href = "https://forums.adobe.com/message/9773900#9773900"> Adobe Support Website </a> (yeah, that's the only way to get help from Adobe using free versions of software)</li>
	</ul>
	
	However I came up with zero result. 

	
</p>
<img src="https://trthhrtz.github.io/images/posts/xmlPDF.jpg" style="max-height: 300px;" />


<p>
	The only thing that succeed a bit was opening PDF with notepad. It showed XML-formatted code, however most of the code was encoded (on gist small part of encoded code is seen in the end, but there is much more) 

<script src="https://gist.github.com/trthhrtz/eab5c7b857828668ccd72f253860b28a.js"></script>
	<br/>
	Was something like that. I tried many different decoding tools. However the answer was right in front of my eyes (my bad, sorry fellas). I should have from the beginning look for specific FlateDecoding method.
	<br/><br/>
	So. After some googling I found working <b>solution</b> written in Python (I checked it with version 2). Here it is:
	<script src="https://gist.github.com/averagesecurityguy/ba8d9ed3c59c1deffbd1390dafa5a3c2.js"></script>
	Just change "some_doc.pdf" for name of your PDF doc and launch the script with python command.
	Shout out and many thanks goes to <a href = "https://github.com/averagesecurityguy"> Stephen Haywood </a>.
	<br/><br/>
	Copy of the post at <a href = "https://stackoverflow.com/questions/45769018/xml-parsing-errorinvalid-token-caused-by-pdf/"> Stackoverflow</a>.
</p>