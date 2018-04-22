---
layout: post
title: '&#x41F;&#x43E;&#x434;&#x434;&#x435;&#x440;&#x436;&#x43A;&#x430; &#x440;&#x443;&#x441;&#x441;&#x43A;&#x43E;&#x433;&#x43E; &#x44F;&#x437;&#x44B;&#x43A;&#x430; &#x432; Jekyll Now and Github Pages'
---

{{ page.title }}
================

<p>
	Обнаружил проблемы в связке Jekyll Now-Github Pages с поддержкой русского языка в заголовках. В тексте все работает хорошо. А при использовании кириллицы в заголовках - падает. Своим первым постом привожу костыльное решение.
</p>

<p>
	Одно из возможных решений (скорее "костыль", конечно, а не решение), которое пришло в голову - (<a href = "https://mothereff.in/html-entities">html entity encoding</a>).
</p>

<p>
	<b>
		Пример encoding:
	</b>
</p>
<img src="https://trthhrtz.github.io/images/posts/encoder_pic.png" style="max-height: 300px;" />

Затем результат из Encoded оборачиваем кавычками '' и закидываем в title.

