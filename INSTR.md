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

    - селектор **тег** - применяется ко всем ссылкам

```
a {
    text-decoration: none;
}
```

    - селектор **ссылка**

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
