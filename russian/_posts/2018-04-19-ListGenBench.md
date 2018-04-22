---
layout: post
title: Самый быстрый способ сгенерировать лист в Python
---

{{ page.title }}
================
<p>
    Как же будет быстрее сгенерировать лист? С помощью for loop, list comprehension или, возможно, как-то ещё? По следам классической книги Лутца по Python привожу эмпирические данные.
</p>

<p>
    Вот несколько способов сгенерировать эту, одну из самых популярных структур данных в Python,  попавших в сравнение:
<ul>
    <li>for loop</li>
    <li>list comprehension</li>
    <li>map function</li>
    <li>generator expression</li>
    <li>generator function</li>
</ul>
</p>

<p>
    Спецификация локальной машины:
<ul>
    <li>ОС: ubuntu 16.04 LTS, 64-bit</li>
    <li>Процессор: Intel® Core™ i5-7200U CPU @ 2.50GHz × 4</li>
    <li>Видеокарта: Intel® HD Graphics 620 (Kaby Lake GT2)</li>
    <li>Память: 7,7 GiB</li>
    <li>Python 3.6.3, Cpython</li>
</ul>
</p>

<p>
    Способ тестов: Код проверяет 5 различных видов генерации листа. Каждая из функций генерирует листо из 10000 элементов 1000 раз. Этот процесс повторяется 5 раз, чтобы найти лучший результат, который и приведен ниже.
</p>

<p>
    Итак, <strong>результаты</strong> получаются следующие(в с):
<ul>
    <li>for_loop : 0.95025</li>
    <li>list_comprehension: 0.50218</li>
    <li>map_call : 0.23515</li>
    <li>gen_expr : 0.76827</li>
    <li>gen_func : 0.77228</li>
</ul>

Что интересно, list_comprehension не только сокращает количество строк кода (обратите внимание, что важно, чтобы сокращение происходило в разумных пределах!), но и значительно быстрее, чем for loop.

</p>
<p>
    Код доступен <a href="https://github.com/trthhrtz/list_py_bench">здесь</a>
    Сравнение сделано по мотивам Lutz, Mark. Learning Python: Powerful Object-Oriented Programming. " O'Reilly Media,
    Inc.", 2013.
</p>