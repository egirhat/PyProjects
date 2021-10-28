# PyProjects
Homework 1_1

import tkinter
import PIL
'''Работа с переменными'''
a = input()
b = input()

print("a = {}".format(a))
print("b = {}".format(b))

Homework 1_2

import tkinter
import PIL
'''Перевод времени'''
time_sek = int(input("Введите время в секундах : "))
time_hrs = time_sek // 3600
time_ost_sek = time_sek % 3600
time_min = time_ost_sek // 60
time_ost_sek = time_ost_sek % 60

print("Время в формате чч:мм:сс = %i:%i:%i" % (time_hrs, time_min, time_ost_sek))

Homework 1_3

import tkinter
import PIL
'''Перевод числа n -> (100*n + 10*n + n) + (10*n + n) + (n)'''
n = int(input("Введите число n : "))
n_res = (100*n + 10*n + n) + (10*n + n) + (n)

print("Сумма чисел n + nn + nnn = %i" % n_res)

Homework 1_4

import tkinter
import PIL
'''Поиск самой большой цифры в числе n '''
n = int(input("Введите число n : "))

n_new = n // 10
n_res = n % 10

while n_new != 0:
    n_cur = n_new % 10
    if n_cur > n_res:
        n_res = n_cur
    n_new = n_new // 10

print("Самая большая цифра в числе %i = %i" % (n, n_res))

Homework 1_5

import tkinter
import PIL
'''Определение прибыли profit и рентабельности rent в зависимости от выручки cash и издержек cost '''
cash = float(input("Введите сумму выручки : "))
cost = float(input("Введите сумму издержек : "))

profit = cash - cost
lost = -profit
if profit > 0:
    rent = profit / cash * 100
    print("Сумма прибыли фирмы = %f, Сумма рентабельности фирмы = %f" % (profit, rent))
    emps = int(input("Введите количество сотрудников : "))
    profit_emps = profit / emps
    print("Сумма прибыли в расчёте на 1 сотрудника = %f" % profit_emps)
else:
    print("Сумма убытков фирмы = %f" % lost)

Homework 1_6

import tkinter
import PIL
''' Поиск номера дня в котором пробежка спортсмена dist_day >= b км '''
''' при начальной пробежке dist_day = a км и ежедневном увеличении пробежки на 10% '''
a = float(input("Введите начальную пробежку спортсмена (км) : "))
b = float(input("Введите требуемую пробежку спортсмена (км) : "))

n_day = 1
dist_day = a
print("%i-й день: %-5.2f км" % (n_day, dist_day))

while dist_day < b:
    dist_day = dist_day * 1.1
    n_day = n_day + 1
    print("%i-й день: %-5.2f км" % (n_day, dist_day))

print("Ответ: на %i-й день спортсмен достиг результата - не менее %-5.2f км" % (n_day, b))
