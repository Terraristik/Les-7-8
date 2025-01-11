Основні компоненти:
Декоратор checker: Декоратор checker приймає функцію як аргумент і обгортає її в іншу функцію. Внутрішня функція намагається виконати передану функцію з відповідними параметрами, обробляючи можливі помилки за допомогою блоку try-except. У разі помилки виводиться повідомлення з описом помилки, а якщо функція виконується успішно, виводиться результат.

Якщо під час виконання функції сталася помилка (наприклад, ділення на нуль або синтаксична помилка), виводиться повідомлення:
We have problems {опис помилки}
Якщо функція виконана без помилок, виводиться результат виконання:
Result - {результат}
Функція calculate: Функція calculate приймає математичний вираз у вигляді рядка і оцінює його за допомогою функції eval(), що дозволяє виконувати математичні операції з рядків. Ця функція обгортається декоратором checker, що дозволяє обробляти помилки під час виконання та виводити результат.

Функція division: Функція division виконує ділення одного числа на інше. Вона також обгортається декоратором checker, що дозволяє обробляти можливі помилки, наприклад, ділення на нуль.

Приклад використання:
python
Copy code
calculate('3+2')      # Виведе: Result - 5
division(2, 0)        # Виведе: We have problems division by zero
У цьому прикладі:

Виклик calculate('3+2') успішно обчислює вираз і виводить результат.
Виклик division(2, 0) призводить до помилки ділення на нуль, і буде виведено повідомлення про помилку.
Пояснення:
Використання декораторів дозволяє легко додавати додаткову обробку функцій без необхідності змінювати самі функції.
Декоратор checker зручний для контролю помилок і виведення результатів виконання функцій в одному місці.