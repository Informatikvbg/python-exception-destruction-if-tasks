# python-exception-destruction-if-tasks
Python Задачи на обработку ошибок, распаковку и условные операторы в функциях

## Задача 1
1. Создайте функцию image_info с одним параметром типа dict
2. Функция ожидает словарь, в котором должно быть как
минимум два ключа:
· image_id
. image_title
может быть и больше ключей, но эти 2 должны быть обязательны.
4. Функция должна возвращать строку такого вида
"Image 'my cat' has id 5136"
То есть мы здесь динамическим образом формируем строку:
'my cat' зависит от значения image_title, а значение id зависит от image_id
6. Если хотя бы одного из этих ключей в словаре нет, функция
должна генерировать ошибку TypeError
Текст для этой ошибки может быть любым, но таким,
чтобы из этого текста было понятно, что функция ожидает от вас.
То есть, если, например, нет ключа image_id, то необходимо написать, что нет ключа image_id,
если нет ключа image_title, то необходимо написать, что нет ключа image_title.
8. Вызовите функцию и корректно обработайте ошибку в
случае возникновения. Текст, возникшей ошибки, выведете в терминал.

Вызовите функцию несколько раз один раз. 
Один раз со словарём, в котором есть оба ключа: и image_id и image_title, 
а второй раз можете вызвать со словарём, в котором нет одного из этих ключей, 
либо вообще нет этих ключей.

мы добавляем дополнительную проверку внутри функции так, 
чтобы её нельзя было вызвать со словарём, в котором нет image_id и image_title.

## Задача 2
1. Создайте список словарей, в нем будет, допустим, 3 словаря.
2. Далее, с помощью оператора распаковки списков создайте 3 переменных, каждая из которых будет содержать один из словарей.
3. Далее создайте функцию любого содержания, которая будет принимать 2 аргумента. В вызове функции Вы должны распаковывать словарь. 
4. Функцию вызовите трижды, потому что у вас в оригинальном списке было 3 словаря. У каждого из этих словарей должно быть по 2 ключа.

## Задача 3
1. Создайте функцию route_info, которой будет передаваться словарь.
Создать логику условий с помощью if elif И с помощью ключевого слова return (итого две функции).
3. Если в словаре есть ключ distance и его значение -
целое число, верните строку "Distance to your
destination is <distance>", где <distance> это значение ключа distance,
которое передается в функцию.
4. Иначе, если в словаре есть ключи speed и time, верните
стpoкy "Distance to your destination is <speed * time>"
Т.е. если у нас в словаре нет ключа distance, а есь два ключа speed и time, то
мы можем посчитать расстояние distance=speed*time, предполагаем, что time измеряется в часах,
а speed измеряется в км/ч. Также добавьте проверку, что speed и time это целые числа.
5. Иначе верните строку "No distance info is available"
(это означает, что в словаре, который передается в функцию route_info,
 нет ни ключа distance, ни ключей speed и time).
6. Вызовите функцию несколько раз с разными
аргументами: разные словари будут содержать разные варианты,
- без ключей distance, speed, time,
- без ключа distance, но с ключами speed и time
- с  ключем distance со значением целого числа 50 или 100

