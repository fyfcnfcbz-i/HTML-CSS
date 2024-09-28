# HTML

```
!
```

## Заголовки

```
h(1-6)
```

## Параграф

```
p
```

рыбный текст

```
lorem
lorem 100...
loremru
```

## Списки:

    1. Нумерованный

```
<ol>
    <li>   </li>
</ol>
```

    2. Не нумрованный

```
<ul>
    <li>   </li>
</ul>
```

## Сылка

```
<a href="путь">описание</a>
<a href="./info/about.html">обо мне</a>   - поиск пути через ./ ../

# - заглушка пути (страница ведет на саму себя)
```

## Картинка

```
<img src="путь" alt="описание картинки" > - путь - ./ или url
width="ширина" height="высота"
```

Кликабельная картинка (с сылкой)

```
<a href="путь"><img src="путь" alt="описание картинки" width="ширина"></a>
```

Открытие ссылки в новой вкладки - target="\_blank"

```
<a href="путь" target="_blank"><img src="путь" alt="описание картинки" width="ширина"></a>
```

## Форма

```
<form action=""></form>

<form action="#">
            <input type="text" placeholder="Nikname" />
            <input type="email" placeholder="Email">
            <input type="password" placeholder="Password">
            <button>Отправить</button>
        </form>

```

дублирование строки

```
Alt Shift стрелка вниз
```

# CSS

Способы объявления:

    1. Inline-стили

атрибут style можно указывать практически у любого HTML-тега. В значении перечисляются стили свойств и их значений в том же формате.

```
<body>
    <h1 style="color: blue">Привет, мир!</h1>
</body>
```

    2. Стили в разделе head

применяют HTML-тег style. Внутри этого тега прописываем стили, которые будут действовать для всей страницы.

```
<head>
    <style>
		ul {
			background-color: blue; - цвет фона
		}
	</style>
</head>

```

    3. Внешний CSS-файл

файл с расширением .css.

```
body {
    background: green;
}
h1 {
    color: blue;
    text-align: center;
}
```

В нужном HTML-файле этот файл **подключаем** - добавить текст link:css и нажать клавишу tab

```
<head>
    <link rel="stylesheet" href="./style.css">
</head>
```

## Селекторы в CSS

    - селектор **тег** - применяется ко всем ссылкам

```
a {
    text-decoration: none;
}
```

    - селектор **класса (ссылка)**

```
.link {
    color: cornflowerblue;
    font-size: 16px;
    line-height: 20px;
}
```

при этом в нужном HTML-файле

```
<a class="link" href="#"> Главная </a>
```

    - cелектор **id**

```
#title {
    color: blueviolet;
}
```

в HTML-файле

```
<h1 id="title"> Привет, мир! </h1>
```

# Работа с макетом и создание блочной структуры

## Стили, которые не нужно копировать из макета

Если у вас однострочный текст, этому блоку не нужно копировать свойства:

```
● position: absolute;
● width: 96px;
● height: 18px;
Если у вас есть блок родительского элемента, у которого уже определена ширина контента
1440px, то добавлять параметры ширины для дочерних элементов не обязательно.
Eсли вы зададите этому блоку высоту, то текстовая
информация, если её станет больше, не поместится и будет наезжать на соседние блоки.
● left: 998px;
● top: 75px;
```

## Основные теги вёрстки

```
<div>Блочный элемент</div>
<span>Строчный элемент</span>

```

**Блочные элементы**

```
● <h1>, <h2>...<h6>
● <li>…</li>
● <ol>…</ol>
● <body>…</body>
● <div>…</div>
● <p>…</p>
● <ul>…</ul>
● ...
```

**Строчные элементы**

```
● <a href=”#”>...</a>
● <i>...</i>
● <b>...</b>
● <em>...</em>
● <strong>...</strong>
● <img>
● <input>
● ...
```

## Cемантические теги

```
<body>
		<header> - шапка
			<nav></nav> - навигация
		</header>
		<main> - основной блок
			<section> - секция с блоками
				<div></div> - блок
				<img src="" alt="" /> - блок из картинки
			</section>
		</main>
		<footer> - подвал
			<nav></nav>
		</footer>
	</body>
```

## Обнуление значений пред css

```
* {
    margin: 0;
    padding: 0;
    text-decoration: 0; - подчеркивание ссылок
}
```

```
body {
    scroll-behavior: smooth; - плавный скроль
}
```

```
img {
    display: block;
    max-width: 100%; - верстка картинки адаптивная к изенениям
}
```

**background** - Фон элемента

```
background-color: #ff0;     - цвет фона

background-image: url(img/photo.jpg);        - в качестве фона  установлено
изображение

background-position: top; (bottom | left | right | center | top)      - указывает, где будет располагаться фоновое изображение

background-repeat: repeat-x; (repeat-y | no-repeat)         - определяет, нужно ли повторять фоновое изображение: repeat-x — изображение повторяется по горизонтали, repeat-y — по вертикали, no-repeat — изображение не повторяется. По умолчанию repeat изображение будет повторяться по горизонтали и по вертикали.

background-size: cover; (contain)       - размер изображения.  cover будет занимать все доступное пространство, contain —
доступное пространство по высоте или ширине.

background: #ff0 url(img/photo.jpg) top repeat-x;
```

**border** — Рамка вокруг элемента

```
border-color: red; (#f00 | RGB(255, 0, 0))      — цвет рамки.

border-style: solid; (dotted | dashed | groove | ridge | solid | double | inset | outset)   — стиль рамки.

border-width: 2px;  — тодщина рамки.

border: 1px solid black;
```

**color** - Цвет текста

**font** - Шрифт
Можно через запятую указывать несколько шрифтов. Если первый шрифт не установлен на компьютер, то будет отображаться следующий шрифт.

```
font-family: "Gill Sans", serif;

1. serif — шрифты с засечками.
2. sans-serif — рубленые шрифты, без засечек.
3. cursive — курсивные шрифты.
4. fantasy — декоративные шрифты.
5. monospace — моноширинные шрифты.

```

```
font-style: italic; (oblique | normal)  — стиль шрифта.
normal. italic — курсивное начертание, имитирует рукописный текст. oblique — наклонное начертание.

font-variant: small-caps;    По умолчанию normal и
small-caps, которое у строчных букв имитирует заглавные буквы, только уменьшенного
размера.

font-weight: bold; (bolder | lighter| 100 | 200); насыщенность шрифта. bold — полужирный, bolder — жирный, lighter — светлый. Насыщенность определяется цифрами от 100 до 900

font-size: 20px; (small | medium | large); -  размер шрифта.

```

**Приоритеты стилей автора**

```
h1 {
    color: black!important;
}
h1 {
    color: green;
}
```

**Работа с текстом**

```
text-align: center; (justify | left | right) — выравнивание содержимого блока по горизонтали.

text-decoration: none; (line-through | overline | underline | none) - оформления текста: line-through —
перечеркивает текст, overline — задает линию над текстом, underline — под текстом
(подчеркивает текст), none (по умолчанию) — отменяет все эффекты.


text-transform: capitalize; (lowercase | uppercase)     - для изменения регистра символов. capitalize — каждое
слово в предложении будет начинаться с заглавной буквы. lowercase все символы строчными, uppercase — заглавными.

```

**padding** - внутренний отступ, добавляет отступы внутри элемента, между его основным содержимым и границей.

**margin** - внешний отступ добавляет отступы за границами элемента, создавая тем самым
промежутки между элементами.

Граница или рамка элемента задается с помощью свойства **border**.
