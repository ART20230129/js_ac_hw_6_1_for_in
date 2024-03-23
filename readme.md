[![Build status](https://ci.appveyor.com/api/projects/status/f4pvl804dtskxa72?svg=true)](https://ci.appveyor.com/project/ART20230129/js-ac-hw-4-1-clearfunction)

# for ... in
Легенда

В рамках разработки игры периодически нужно печатать таблички, отображающие свойства объектов. Вам нужно реализовать функцию, которая для переданного объекта возвращает массив его свойств со значениями, отсортированный по свойствам (порядок сортировки свойств - второй аргумент).
Описание

Дан объект, например:

const obj = {name: 'мечник', health: 10, level: 2, attack: 80, defence: 40}

Дан порядок сортировки свойств:

["name", "level"]

Пример вызова вашей функции:

orderByProps(obj, ["name", "level"])

После обработки вашей функцией:

[
  {key: "name", value: "мечник"}, // порядок взят из массива с ключами
  {key: "level", value: 2}, // порядок взят из массива с ключами
  {key: "attack", value: 80}, // порядок по алфавиту (т.к. в массиве с ключами нет значения "attack")
  {key: "defence", value: 40}, // порядок по алфавиту (т.к. в массиве с ключами нет значения "defence")
  {key: "health", value: 10} // порядок по алфавиту (т.к. в массиве с ключами нет значения "health")
]

Т.е. сначала идёт сортировка по тому, как указано в массиве сортировки, для тех ключей, для которых в массиве сортировки нет записи, сортировка идёт в алфавитном порядке.

Используйте возможности for-in для перебора свойств объекта. Не забудьте написать unit-тесты, которые обеспечивают 100% покрытие функции, которую вы тестируете.
