# Лабораторная 4
## Задание 1 
### Код
``` c
#define _CRT_SECURE_NO_DEPRECATE
#include <locale.h>
#include <stdio.h>
#include <stdlib.h>

int main() {
    char c = '!';
    int i = 2;
    float f = 3.14f;
    double d = 5e-12;

    int a;
    double b;

    setlocale(LC_ALL, ".UTF-8");
   
    printf("=== Демонстрация исходных данных ===\n");
    printf("Символ: %c | Целое: %d | Float: %.2f | Double: %e\n\n", c, i, f, d);

    printf("Введите новый символ:\n> ");
    scanf(" %c", &c);

    printf("Введите ненулевое целое число:\n> ");
    scanf("%d", &i);

    printf("Введите вещественное число (float):\n> ");
    scanf("%f", &f);

    printf("Введите вещественное число высокой точности (double):\n> ");
    scanf("%lf", &d);

    printf("\n--- Обновленные данные ---\n");
    printf("Символ: %c, Целое: %d, Float: %f, Double: %e\n\n",
        c, i, f, d);

    // Расчет 1а
    a = (int)d;
    b = d - a;
    printf("[Задание 1а] Число double: %e\n", d);
    printf(" -> Целая часть: %d\n -> Дробная часть: %f\n\n", a, b);

    // Расчет 1б
    printf("[Задание 1б] Символ '%c':\n", c);
    printf(" -> Десятичный код: %d\n -> Шестнадцатеричный код: %X\n\n",
        (unsigned char)c, (unsigned char)c);

    // Расчет 1в
    printf("[Задание 1в] Обратное число для %d:\n", i);
    printf(" -> Целочисленное деление (1 / i): %d\n", 1 / i);
    printf(" -> С явным приведением к double: %f\n\n", (double)1 / i);

    system("pause");
    return 0;
}
```
### Результат
```
=== Демонстрация базовых типов (исходные данные) ===
Символ: # | Целое: 5 | Float: 7,25 | Double: 8,123457e-10

Введите новый символ:
> !
Введите ненулевое целое число:
> 2
Введите вещественное число (float):
> 5,55
Введите вещественное число высокой точности (double):
> 15

--- Обновленные данные ---
Символ: !, Целое: 2, Float: 5,550000, Double: 1,500000e+01

[Задание 1а] Число double: 1,500000e+01
 -> Целая часть: 15
 -> Дробная часть: 0,000000

[Задание 1б] Символ '!':
 -> Десятичный код: 33
 -> Шестнадцатеричный код: 0x21

[Задание 1в] Обратное число для 2:
 -> Целочисленное деление (1 / i): 0
 -> С явным приведением к double: 0,500000
```
## Задание 2 (часть 1)
### Код
```c
#define _CRT_SECURE_NO_DEPRECATE
#include <locale.h>
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int a = 11, b = 3;
    int x;
    float y;
    double z;

    setlocale(LC_ALL, "RUS");

    x = a / b;
    y = a / b;
    z = a / b;

    printf("a = %d, b = %d\n", a, b);
    printf("x (int)    = %d\n", x);
    printf("y (float)  = %f\n", y);
    printf("z (double) = %f\n", z);

    system("pause");
    return 0;
}
```
### Результат 
```
a = 11, b = 3
x (int)    = 3
y (float)  = 3,000000
z (double) = 3,000000
```
## Задание 2 (часть 2)
### Код 
```c
#define _CRT_SECURE_NO_DEPRECATE
#include <locale.h>
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int a = 11, b = 3;

    setlocale(LC_ALL, "RUS");

    printf("a = %d, b = %d\n", a, b);
    printf("(float)a/b      = %f\n", (float)a / b);
    printf("(double)a/b     = %f\n", (double)a / b);
    printf("(float)(a/b)    = %f\n", (float)(a / b));
    printf("(double)(a/b)   = %f\n", (double)(a / b));

    system("pause");
    return 0;
}
```
### Результат
```
a = 11, b = 3
(float)a/b      = 3,666667
(double)a/b     = 3,666667
(float)(a/b)    = 3,000000
(double)(a/b)   = 3,000000
```
## Задание 3
### Код
```c
#define _CRT_SECURE_NO_DEPRECATE
#include <locale.h>
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int n, last, first, sum, rev;

    setlocale(LC_ALL, ".UTF-8");

    puts("Введите трехзначное число");
    scanf("%d", &n);

    last = n % 10;
    first = n / 100;
    sum = n / 100 + n / 10 % 10 + n % 10;
    rev = n % 10 * 100 + n / 10 % 10 * 10 + n / 100;

    printf("Последняя цифра: %d, первая цифра: %d, сумма цифр: %d, число наоборот: %d\n", last, first, sum, rev);

    system("pause");
    return 0;
}
```
### Результат
```
Введите трехзначное число
759
Последняя цифра: 9, первая цифра: 7, сумма цифр: 21, число наоборот: 957
```
## Выполнил 
Коренев Сергей бИД-261 подгруппа 2
