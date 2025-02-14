#МоиЛекции #ЯзыкПрограммирования #Python 

### Возвращение результата

Функция может возвращать результат. Для этого в функции используется оператор `return`, после которого указывается возвращаемое значение:

```python
def имя_функции ([параметры]):
    инструкции
    return возвращаемое_значение
```

Определим простейшую функцию, которая возвращает значение:

```python
def get_message():
    return "Hello World!"
```

Здесь после оператора `return` идет строка `"Hello World!"` – это значение и будет возвращать функция `get_message()`.

Затем это результат функции можно присвоить переменной или использовать как обычное значение:

```python
def get_message():
    return "Hello World!"
 
 
message = get_message()  # получаем результат функции get_message в переменную message
print(message)          # Hello World!
 
# можно напрямую передать результат функции get_message
print(get_message())    # Hello World!
```

После оператора `return` может идти и сложное вычисляемое выражение, результат которого будет возвращаться из функции. Например, определим функцию, которая увеличивает число в два раза:

```python
def double(number):
    return 2 * number
```

Здесь функция `double` будет возвращать результат выражения `2 * number`:

```python
def double(number):
    return 2 * number
 
result1 = double(4)     # result1 = 8
result2 = double(5)     # result2 = 10
print(f"result1 = {result1}")   # result1 = 8
print(f"result2 = {result2}")   # result2 = 10
```

Или другой пример – получение суммы чисел:

```python
def sum(a, b):
    return a + b

result = sum(4, 6)                  # result = 0
print(f"sum(4, 6) = {result}")      # sum(4, 6) = 10
print(f"sum(3, 5) = {sum(3, 5)}")   # sum(3, 5) = 8
```

### Выход из функции

Оператор `return` не только возвращает значение, но и производит выход из функции. Поэтому он должен определяться после остальных инструкций. Например:

```python
def get_message():
    return "Hello World!"
    print("End of the function")
 
print(get_message())
```

С точки зрения синтаксиса данная функция корректна, однако ее инструкция `print("End of the function")` не имеет смысла – она никогда не выполнится, так как до ее выполнения оператор `return` возвратит значение и произведет выход из функции.

Однако мы можем использовать оператор `return` и в таких функциях, которые не возвращают никакого значения. В этом случае после оператора `return` не ставится никакого возвращаемого значения. Типичная ситуация – в зависимости от определённых условий произвести выход из функции:

```python
def print_person(name, age):
    if age > 120 or age < 1:
        print("Invalid age")
        return
    print(f"Name: {name}  Age: {age}")

print_person("Tom", 22)
print_person("Bob", -102)
```

Здесь функция `print_person` в качестве параметров принимает имя и возраст пользователя. Однако в функции вначале мы проверяем, соответствует ли возраст некоторому диапазону (меньше `120` и больше `0`). Если возраст находится вне этого диапазона, то выводим сообщение о недопустимом возрасте и с помощью оператора `return` выходим из функции. После этого функция заканчивает свою работу.

Однако если возраст корректен, то выводим информацию о пользователе на консоль. Консольный вывод:

```
Name: Tom  Age: 22
Invalid age
```

---
## Домашнее задание

![[Задание. Оператор return и возвращение результата из функции]]

---
## Ссылки

1. [Оператор return и возвращение результата из функции](https://metanit.com/python/tutorial/2.16.php)

---

| [[Параметры функции\|Предыдущая лекция]] | [[Функция как тип, параметр и результат другой функции\|Следующая лекция]] |
| ---------------------------------------- | -------------------------------------------------------------------------- |

