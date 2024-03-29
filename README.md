# Task: освоить объекты

## Постановка задачи

Объекты – это единственный сложный тип данных в JavaScript. Они встречаются повсюду в той или иной форме. Хорошее понимание объектов – залог успешного освоения JavaScript.

Как всегда пройдись по основам изучаемой темы на [doka.guide](https://doka.guide/js/object/) и начни выполнять задачи.

Сделай форк и клон данного репозитория. 

## Subtask 1. Синтаксис

#### 1.1

В файле `object-intro.js` создай объект `start`, у которого будут два любых ключа и значения.

#### 1.2

В том же файле создай объект, `person` у которого будут следующие ключи и значения:
- `fistname` - твоё имя
- `lastname` - твоя фамилия
- `city` - название твоего города/села
- `age` - твой возраст
- `height` - твой рост (сантиметры)
- `heightMeters` - твой рост (метры)
- `haveCar` - есть ли у тебя машина (вспомни про `boolean`)
- `carName` - название машины, если машины нет, то `undefined`
- `mobilePhone` - инфа о твоем телефоне, включая:
  - название модели
  - примерная цена в рублях
  - название оператора связи
  
Для последнего пункта нужен будет вложенный объект.

## Subtask 2. Коллекции

#### Задача 2.1

Создай файл `messages.js`. В нём создай массив с именем `messages`, состоящий из объектов такого вида:

```json
{
  id: 1,
  author: 'Адам',
  text: 'Приветики🥰',
  type: 'входящее',
  time: '12:29'
}
```

В массиве должны быть минимум 5 таких объектов, у которых одинаковые ключи, но разные значения. Получится своеобразная база данных из сообщений.

Выведи массив в консоль.

## Subtask 3. Объекты и функции

Следующие задачи выполни в файле `functions-and-objects.js`.

#### 3.1

Создай функцию с именем `getName`, которая принимает один параметр. В этот параметр будет передаваться объект.

Верни из функции ключ `name` этого объекта.

#### 3.2

Создай функцию с именем `getNames`, которая принимает один параметр. В этот параметр будет передаваться объект.

Верни из функции массив, который содержит два элемента:
  1. ключ `firstname` принятого объекта
  2. ключ `lastname` принятого объекта

```javascript
// пример проверки

const person = {
  firstname: 'Adam',
  lastname: 'Baysarov',
  age: 21
};

console.log(getNames(person)); // в консоле должно быть ['Adam', 'Baysarov']
```

#### 3.3

Создай функцию `concatNames`, которая принимает два параметра с именами `obj` и `lastname`. 

Верни из функции строку, которая содержит в себе ключ `firstname` из объекта `obj`, а следом через пробел значение параметра `lastname`.

```javascript
// пример проверки

const person = {
  firstname: 'Adam',
  age: 21
};

console.log(concatNames(person, 'Baysarov')); 
// в консоле должно быть 'Adam Baysarov'
```

#### 3.4

Напиши функцию `correctName`, которая принимает один параметр (это будет объект).

Если в принятом объекте ключ `fathername` имеет значение `undefined`, то верни только ключ `firstname`.

В ином случае верни строку, которая содержит конкатенацию следующих ключей `fistname + lastname + fathername`

```javascript
// пример проверки

const firstPerson = {
  firstname: 'Adam',
  lastname: 'Baysarov',
  fathername: undefined
};

console.log(correctName(firstPerson)); 
// в консоле должно быть 'Adam'

// ----------------------------- //

const secondPerson = {
  firstname: 'Adam',
  lastname: 'Baysarov',
  fathername: 'Ruslanovich'
};

console.log(correctName(secondPerson)); 
// в консоле должно быть 'Adam Baysarov Ruslanovich'
```

## Закрываем задачу
