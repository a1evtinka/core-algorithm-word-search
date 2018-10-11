# Поиск слова

## Введение

В этой задаче мы собираемся написать алгоритм поиска, который скажет нам, можно ли найти слово в головоломке поиска слов. Конкретные правила, которые нам следует соблюдать, будут подробно описаны в релизы.

### Структура данных головоломки

```javascript
let puzzle = [
  ["a", "k", "f", "o", "x", "e", "s"],
  ["s", "o", "a", "w", "a", "h", "p"],
  ["i", "t", "c", "k", "e", "t", "n"],
  ["o", "t", "s", "d", "h", "o", "h"],
  ["s", "e", "x", "g", "s", "t", "a"],
  ["u", "r", "p", "i", "w", "e", "u"],
  ["z", "s", "b", "n", "u", "i", "r"]
]
```
*Рисунок 1*. Представление головоломки поиска слов в виде вложенного массива

Мы будем представлять наши головоломки поиска слов в виде вложенных массивов. Паззл в целом будет представлен внешним массивом. Каждый ряд в головоломке будет представлен одним из внутренних массивов. (см. Рисунок 1)


## Releases
### Release 0: Поиск слов в строке

![Поиск слов в строках](readme-assets/straight-word.gif)

*Рисунок 2*. Нахождение слов *foxes*, *otters* и *bison* в строке.

В этом первом релизе мы собираемся написать метод `straightLineInclude`. Наш метод примет два параметра: (1) слово, которое мы ищем, и (2) головоломку поиска слов, смоделированную, как вложенный массив. Метод выдаст `true`, если слово можно найти в головоломке, и` false`, если нет. Мы будем следовать традиционному поиску по словам, который позволяет  находить слова только в строках (см. Рис. 2).

Как всегда, нам нужно документировать поведение нашего метода с помощью тестов.

** Правила **
- Слова могут быть найдены в горизонтальных, вертикальных и диагональных строках.
- Слова могут быть записаны слева направо и наоборот.

### Release 1: Поиск слов в змейке

![поиск слов в змейке](readme-assets/snaking-word.gif)

*Рисунок 3*. Нахождение слова *nighthawks*.

В этом релизе мы собираемся написать метод `snakingInclude`. Этот метод будет принимать те же параметры, что и наш метод `straightLineInclude?`, И возвращать те же самые значения, но только алгоритм, используемый для поиска слов, будет другим. Мы удалим ограничение того, что слова обязательно должны появляться в одной строке, столбце или диагонали. Вместо этого мы позволим буквам появляться вне головоломки (см. Рис. 3).

Мы также должны сделать проверку этого метода.

** Правила **
- Слова могут находиться в змейке горизонтально, вертикально и по диагонали.
- Каждая буква в головоломке может использоваться только один раз за слово.


### Release 2: Создание пользовательского интерфейса

Давайте напишем страницу, которая отображает головоломку для поиска слов, и просит ввести слова, для которых нужно проводить поиск. После ввода каждого слова мы должны сообщать, возможно ли найти слово в головоломке.

Если слово найдено, можно ли наглядно показать его пользователям?


## Выводы

Алгоритм змейки является одной из сложных задач, с которыми мы сталкиваемся во время обучения в Bootcamp. Что мы думаем об этом? Все ли прошло хорошо? В каких местах возникали трудности?

Каков наш подход к тестированию? Начали ли мы с более простых слов во время нашего поиска? Может быть, слово из одной буквы, за которым следуют две буквы, и так далее?


[wikipedia word search]: https://en.wikipedia.org/wiki/Word_search
