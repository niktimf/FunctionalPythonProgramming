#Декларативноепрограммирование 

* map(function, iterable)

* map() принимает функцию и итерацию (или несколько итераций) в качестве аргументов и возвращает объект **map**, который является итератором, выдающим элементы по запросу.

* Первый аргумент map() -  это функция, которая преобразует каждый исходный элемент в новый (преобразованный) элемент. Сюда входят встроенные функции, классы, методы, лямбда-функции и пользовательские функции.

* Второй аргумент map() - итерируемый объект. Это может быть список, множество, кортеж, словарь, строка и др. 
```jupyter
import random

initial_list = [random.randint(-20, 20) for _ in range(random.randint(5, 12))]
print(f'Initial list: {initial_list}')

list_mult_2 = list(map(lambda x: x * 2, initial_list))  
print(f'Initial list multiplied by 2: {list_mult_2}')
```