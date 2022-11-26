#Декларативноепрограммирование

### Функциональный код на Python

```jupyter

def until(initial_value: int, filter_func, final_value: int) -> list:  
    """ Функция, которая фильтрует числа в массиве с помощью лямбда функции """  
    if initial_value == final_value: return []  
    if filter_func(initial_value): return [initial_value] + until(initial_value + 1, filter_func, final_value)  
    else: return until(initial_value + 1, filter_func, final_value)


mult_3_5 = lambda x: x % 3 == 0 or x % 5 == 0  

print(sum(until(0, mult_3_5, 20)))

```

Рекурсивная функция имеет 3 аргумента.

*initial_value* (начало массива)
*filter_func* (функция фильтрация, подразумевается что это будет лямбда функция)
*final_value* (конец массива)

Описание кода рекурсивной функции.
Если начало и конец массива равны, то массив пуст.
Если начальное число массива подходит, то мы его оставляем и выполняем рекурсивно до тех пор, пока не пройдемся по всему массиву.
Иначе мы начинаем со следующего элемента.


