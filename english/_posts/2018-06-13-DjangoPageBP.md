---
layout: post
title: Best Practices with Django Pagination
---

{{ page.title }}
================
<p>
    Django provides a few classes that help you manage paginated data. There exist some best practices of working with them
</p>

<p>
	
<ul> 
    <li>Validate parameters page and limit</li>
    <li>Return 404 Error if parameters are invalid</li>
    <li>Limit max value of limit <= 1000 </li>
    <li>Handle "empty" last page</li>
</ul>
	
</p>

