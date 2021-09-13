# Конспект «JS в браузере». Раздел 1
Поиск элементов на странице:
```JS
// Поиск элемента по тегу
var list = document.querySelector('ul');

// Поиск последнего элемента из списка
var lastProduct = document.querySelector('li:last-child');

// Поиск элемента по классу
var price = document.querySelector('.price');

// Поиск третьего элемента из списка товаров
var thirdProduct = document.querySelector('.product:nth-child(3)');

// Поиск всех элементов, подходящих по селектору
var listItems = document.querySelectorAll('.product');
```
querySelectorAll возвращает список (коллекцию) элементов. Этот список похож на массив, но им не является.
Он называется псевдомассив и его можно перебирать с помощью цикла for.
Добавление класса элементу страницы:
```js
// Когда ищем элемент по классу, используем точку
var product = document.querySelector('.product');

// Но когда добавляем класс, точки нет!
product.classList.add('product--sale');
```
Результат работы classList.add() такой же, как при ручном добавлении класса в разметку:
```html
<!-- Исходное состояние разметки -->
<li class="product">
  …
</li>

<!-- Состояние после вызова classList.add -->
<li class="product product--sale">
  …
</li>
```
