---
layout: post
title: Установка Postgresql 10 на Ubuntu 16.04
---

{{ page.title }}
================

Это короткий гайд по установке постгрес 10 на убунту 16.04 

**Добавляем репозиторий постгреса**

На сегодняшний день (проверено на 02.05.2018) по умолчанию апт репозитории убунту ставят только постгрес 9.5. Чтобы поставить десятку мы добавим официальный апт репозиторий постгреса:

`sudo add-apt-repository 'deb http://apt.postgresql.org/pub/repos/apt/ xenial-pgdg main'`

Теперь импортируем подписывающий ключ репозитория и обновим список пакетов:

```
wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | \
  sudo apt-key add -
sudo apt-get update
```

**Ставим постгрес**

`sudo apt-get install postgresql-10`

Проверяем, что все работает:  

`sudo service postgresql status`

Ставим звездочки гисту на английском <a href="https://gist.github.com/trthhrtz/77f1a18d119a6394a7e20ef9e6f8d15a">здесь</a>.