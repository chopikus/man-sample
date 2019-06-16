# ПИСАТЬ МАН В ТЕХЕ - КРУТО!

Чтобы начать писать МАН при помощи TeX, нужно сделать всего 3 шага:

0. Установить шрифт Times New Roman в систему, если Вы не на Windows
1. Скачать файл sample.tex из этого репозитория
2. Найти, изменить ФИО на свою
3. Найти, изменить год/секцию
4. Посмотреть, что же там вышло по итогу, скомпилировав файл (превратив в pdf)!
Готово! Пишите свою **любимую** научную работу с облегчением!

## Плюсы использования данного шаблона
1. Это TeX, додик!
2. Тебе не нужно морочиться с титулкой!
3. Шрифт Times New Roman уже выставлен!
4. Размер шрифта тоже выставлен (14)!
5. И даже интервал выставлен!
6. Базовые пакеты уже подключены и настроены!

## Компиляция файла .tex (и получить .pdf)
Используется движок XeLaTeX.

Его плюсы:

1. Все обрабатываемые символы в Unicode
2. Умеет нормально работать с очень многими шрифтами (в том числе и с Times New Roman)
3. Все остальные плюсы LaTeX движков


Установить его очень просто:
```
apt-get install texlive-xetex
```
Пример компиляции (для GNU/Linux)
```
xelatex sample.tex
```

Получился файл sample.pdf!
## Установка Times New Roman/ошибка компиляции из-за шрифта
Если у Вас при компиляции появляется ошибка вида:

```
the font Times New Roman cannot be found blah-blah
```

, то этот дурацкий шрифт нужно еще и установить (скажите спасибо мелко-мягким).

Пример установки для Дебиан-Подобных ОС (Ubuntu и прочий мусор)

```
wget http://ftp.de.debian.org/debian/pool/contrib/m/msttcorefonts/ttf-mscorefonts-installer_3.6_all.deb
dpkg -i ttf-mscorefonts-installer_3.6_all.deb
```

