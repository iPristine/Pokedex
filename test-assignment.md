# Pokedex

Необходимо реализовать Покедекс (список покемонов) c пагинацией, а также возможность сравнивать существ друг с другом.

Пагинатор должен иметь кнопки "previous", "next" и возможность перехода на страницу номер n.

Параметрами для сравнения являются поля объекта `Pokemon` (https://pokeapi.co/docsv2/#pokemon). Набор параметров на ваше усмотрение. Сравнение должно работать для любого количества покемонов.

В случае сложных типов (например, `types` или `game_indices`) для сравнения нужно использовать вложенные поля (например, `name`).

Можно подсмотреть как примерно должно выглядеть сравнение у [Яндекс.Маркета](https://market.yandex.ru/compare/2FGX4aHvMczH6cRGfVfDZw267H95?hid=91013&id=1788407818&id=1727685734)

Примерная раскладка карточки в списке

![list](https://user-images.githubusercontent.com/9089190/36136390-04a1620a-10b2-11e8-9abe-74cd8d877a10.png)

В сравнении

![comparison](https://user-images.githubusercontent.com/9089190/36136381-f5522604-10b1-11e8-92e3-0f3795040779.png)

Изображение можно взять из поля `sprites` (подойдет `front_default`).

Нет ограничений на используемые технологии, приветствуется использование современных фреймворков (React, VueJS, Angular), а также использование современного CSS (flexbox, grid и т.п.).
Рекомендуется использование кэширующей обертки (https://github.com/PokeAPI/pokeapi-js-wrapper), так как API имеет ограничение в 300 запросов на ресурс в сутки.

Если возникает ошибка `No 'Access-Control-Allow-Origin' header is present on the requested resource.` при редиректе с `http` на `https`, необходимо явно указать протокол, например:
```javascript
/* api.js */
import { Pokedex } from "pokeapi-js-wrapper";

export default new Pokedex({
  protocol: "https"
});
```
По всем вопросам можно писать в комментарии к данному gist'у или мне на почту.

* API docs https://pokeapi.co/docsv2/
* PokeAPI wrapper https://github.com/PokeAPI/pokeapi-js-wrapper
* [Покемон](https://ru.wikipedia.org/wiki/%D0%9F%D0%BE%D0%BA%D0%B5%D0%BC%D0%BE%D0%BD)
