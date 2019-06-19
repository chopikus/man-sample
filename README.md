В этом репозитории представлен невероятный шаблон, значительно облегчающий жизнь при написании работы МАН.
При помощи него не нужно морочиться с кучей формальностей, возникающих при оформлении работы.

А формальностей таких много:
1. Times New Roman, 14 размер, полуторный интервал
2. Содержание и некоторые приколы с оформлением разделов и подразделов (например, название раздела в тексте нужно печатать КАПСОМ, а в содержании нет).
3. Нумерация страниц в правом верхнем углу
4. Титулка
5. Отступы от края бумаги

## Я только Word'ом умею пользоваться, что делать?
Эта болячка быстро проходит.

Нужно научиться писать в LaTex, базовых знаний будет предостаточно для написания работы МАН.

По [этой](https://www.latex-tutorial.com/quick-start/) ссылке есть очень классное руководство, как научиться писать в LaTex.

## Как пользоваться шаблоном?

1. Скачать файл sample.tex из этого репозитория
2. Научиться компилировать файл .tex и получать .pdf (как компилировать написано [здесь](#compiling))
3. Найти и изменить в титулке: своё ФИО, ФИО и регалии научрука(если требуется), изменить год

В шаблоне уже отведено место для разделов "ВСТУП", "СПИСОК ВИКОРИСТАНИХ ДЖЕРЕЛ", а также для остальных необходимых разделов.

Для создания своего раздела необходимо использовать команду `\section{имя раздела}`.

Для создания своего подраздела необходимо использовать команду `\subsection{имя подраздела}`.

<a name="compiling"><h2> Компиляция файла .tex (и получение .pdf)</h2></a>
Используется движок XeLaTeX.

Установить его очень просто (пример для Ubuntu):
```
apt-get install texlive-xetex
```
Пример компиляции (для GNU/Linux)
```
xelatex sample.tex
```

Получился файл sample.pdf!

## Ошибка компиляции
### Ошибка компиляции из-за шрифта
Если у Вас при компиляции появляется ошибка вида:

```
the font Times New Roman cannot be found blah-blah
```

, то этот дурацкий шрифт нужно еще и установить (скажите спасибо мелко-мягким).

Пример установки для Ubuntu и Debian-based ОС:

```
wget http://ftp.de.debian.org/debian/pool/contrib/m/msttcorefonts/ttf-mscorefonts-installer_3.6_all.deb
dpkg -i ttf-mscorefonts-installer_3.6_all.deb
```

[Почему не используется apt-get](https://bugs.launchpad.net/ubuntu/+source/msttcorefonts/+bug/1607535)

### Ошибка компиляции явно не из-за шрифта
1. Попробуйте перезагрузить копьютер (нет, серьёзно, часто такое бывает если вы до этого работали с другими документами)
2. Попробуйте перекомпилировать, удалив файлы .aux, .log, .toc
3. Проверьте (очень!!) внимательно изменения, которые Вы вносили
4. И наконец, если после **всех** проделанных шагов Вы продолжаете считать, что ошибка в самом шаблоне, создавайте [issue](https://gitlab.com/chopikus/man-sample/issues)! 


## Полезные ссылки
https://www.latex-tutorial.com/quick-start/

https://duckduckgo.com



