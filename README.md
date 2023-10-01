# Тема 4. Функции и модули
Отчет по Теме #4 выполнил(а):
- Сбитнева Мария Алексеевна
- ЗПИЭ-20-2

| Задание | Сам_раб |
| ------  | ------ |
| Задание 1 | + |
| Задание 2 | + |
| Задание 3 | + |
| Задание 4 | + |
| Задание 5 | + |

знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

## Самостоятельная работа №1
### Напишите программу, которая преобразует 1 в 31. Для выполнения поставленной задачи необходимо обязательно и только один раз использовать:<br>• Цикл for<br>• *= 5<br>• += 1<br>Никаких других действий или циклов использовать нельзя.

```python
num = 1
for _ in range(2):
    num *= 5
    num += 1
print('Результат:', num)
```

### Результат
![Меню](https://github.com/segamega-drive/software_engineering/blob/af6761d9a2c16e57bd7d12c9bae594efd643aa83/img/3.1.png)

## Выводы
- Развернутый вывод
  
## Самостоятельная работа №2
### Напишите программу, которая фразу «Hello World» выводит в обратном порядке, и каждая буква находится в одной строке консоли. При этом необходимо обязательно использовать любой цикл, а также программа должна занимать не более 3 строк в редакторе кода.

```python
print(*[i for i in 'Hello World'[::-1]], sep='\n')
```

### Результат
![Меню](https://github.com/segamega-drive/software_engineering/blob/af6761d9a2c16e57bd7d12c9bae594efd643aa83/img/3.2.png)

## Выводы
- Развернутый вывод
  
## Самостоятельная работа №3
### Напишите программу, на вход которой поступает значение из консоли, оно должно быть числовым и в диапазоне от 0 до 10 включительно (это необходимо учесть в программе). Если вводимое число не подходит по требованиям, то необходимо вывести оповещение об этом в консоль и остановить программу. Код должен вычислять в каком диапазоне находится полученное число. Нужно учитывать три диапазона:<br>• от 0 до 3 включительно<br>• от 3 до 6<br>• от 6 до 10 включительно<br>Результатом работы программы будет выведенный в консоль диапазон. Программа должна занимать не более 10 строчек в редакторе кода.

```python
x = int(input('Введите число: '))
if 0 <= x <= 3:
    print('Число в диапазоне от 0 до 3 включительно')
elif 6 <= x <= 10:
    print('Число в диапазоне от 6 до 10 включительно')
elif 3 < x < 6:
    print('Число в диапазоне от 3 до 6')
else:
    print('Число вне диапазона от 0 до 10')
```

### Результат
![Меню](https://github.com/segamega-drive/software_engineering/blob/5abfddb97431cd634692c01284cdbae171118d55/img/3.3.1.png)
![Меню](https://github.com/segamega-drive/software_engineering/blob/5abfddb97431cd634692c01284cdbae171118d55/img/3.3.2.png)

## Выводы
- Развернутый вывод
  
## Самостоятельная работа №4
### Манипулирование строками. Напишите программу на Python, которая принимает предложение (на английском) в качестве входных данных от пользователя. Выполните следующие операции и отобразите результаты:<br>• Выведите длину предложения.<br>• Переведите предложение в нижний регистр.<br>• Подсчитайте количество гласных (a, e, i, o, u) в предложении.<br>• Замените все слова "ugly" на "beauty".<br>• Проверьте, начинается ли предложение с "The" и заканчивается ли на "end".<br>Проверьте работу программы минимум на 3 предложениях, чтобы охватить проверку всех поставленных условий.

```python
phrase = str(input('Введите предложение на английском: '))

vowels = ['o', 'e', 'i', 'u', 'a']

length = len(phrase)
low_letters = phrase.lower()
vowels_count = sum(low_letters.count(vowel) for vowel in vowels)
words_replace = low_letters.replace('ugly', 'beauty')
start_end_check = phrase.startswith('The') and phrase.endswith('end')

print(f'Длина: {length}\n'
      f'Нижний регистр: {low_letters}\n'
      f'Количество гласных: {vowels_count}\n'
      f'Замена слов: {words_replace}\n'
      f'Удовлетворение условия: {start_end_check}')
```

### Результат
![Меню](https://github.com/segamega-drive/software_engineering/blob/5abfddb97431cd634692c01284cdbae171118d55/img/3.4.png)
![Меню](https://github.com/segamega-drive/software_engineering/blob/5abfddb97431cd634692c01284cdbae171118d55/img/3.4.1.png)
![Меню](https://github.com/segamega-drive/software_engineering/blob/5abfddb97431cd634692c01284cdbae171118d55/img/3.4.2.png)

## Выводы
- Развернутый вывод
  
## Самостоятельная работа №5
### Составьте программу, результатом которой будет данный вывод в консоль:<br>![Меню](https://github.com/segamega-drive/software_engineering/blob/Theme_3/img/5.1.png)<br>Программу нужно составить из данных фрагментов кода:<br>![Меню](https://github.com/segamega-drive/software_engineering/blob/Theme_3/img/5.2.png)<br>Строки кода можно использовать только один раз. Не обязательно использовать все строки кода.

```python
string = 'hello'
counter = 0
values = [0, 2, 4, 6, 8, 10]
while counter != 10:
    memory = string
    if counter in values:
        string = string + ' world'
    print(string)
    counter += 1
    if counter < 10:
        string = memory
        memory = ' world'
while ' world' not in string:
    if counter > 7:
        memory = ' world'
    print(string + memory)
    string = ' world'
```

### Результат
![Меню](https://github.com/segamega-drive/software_engineering/blob/af6761d9a2c16e57bd7d12c9bae594efd643aa83/img/3.5.png)

## Выводы
- Развернутый вывод

## Общие выводы по теме
- Развернутый вывод
