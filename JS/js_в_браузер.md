# Конспект «JS в браузере». Раздел 2
Свойство DOM-элемент.children возвращает коллекцию дочерних, то есть вложенных, DOM-элементов.
Создание элемента и добавление его в DOM-дерево:

```javascript
var list = document.querySelector('.cards');
// Создаём новый элемент
var card = document.createElement('li');

card.classList.add('card');
```
```js
// После вызова этого метода новый элемент отрисуется на странице
list.appendChild(card);
```
Вот что произойдёт с разметкой после вызова appendChild:

```html
<!-- Исходное состояние разметки -->
<ul class="cards">
  <li class="card">Существующий элемент</li>
</ul>

<!-- Состояние после вызова appendChild -->
<ul class="cards">
  <li class="card">Существующий элемент</li>
  <li class="card">Добавленный элемент</li>
</ul>
```

Работа с текстовым содержимым элемента:
// HTML
<p>Я — <em>текстовый элемент</em>.</p>

```js
// JS
var p = document.querySelector('p');
console.log(p.textContent);
// Выведет: Я — текстовый элемент.
```
```js
p.textContent = 'Теперь у меня новое содержимое.';
console.log(p.textContent);
// Выведет: Теперь у меня новое содержимое.
```

// В HTML содержание тега изменится
```html
<p>Теперь у меня новое содержимое.</p>
```
Работа с изображениями:
```js
// Создание изображения
var picture = document.createElement('img');

// Добавляем адрес картинки
picture.src = 'images/picture.jpg';

// Добавляет альтернативный текст
picture.alt = 'Непотопляемая селфи-палка';

// Добавляет изображение в конец родительского элемента
element.appendChild(picture);
```
