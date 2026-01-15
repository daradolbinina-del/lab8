# Домашнее задание к работе 8
## Условие задачи

Вычислите с использованием цикла for значение
(1 + sin(0.1)) ∙ (1 + sin(0.2)) ... (1 + sin(10))

## 1. Алгоритм и блок-схема
### Алгоритм
1. **Начало**
2. Ввод значения:
   - log_sum = 0.0
   - step = 0.1
3. цикл **for**
   - x = 0.1
   - x <= 10.0
   - x += step
4. Вывести результат на экран.
5. **Конец**
   
### Блок-схема
<img width="409" height="602" alt="image" src="https://github.com/user-attachments/assets/e961a521-0bde-4b34-888e-0f140ca042c1" />


## 2. Реализация программы
```
#define _CRT_SECURE_NO_WARNINGS
#define _USE_MATH_DEFINES
#include <locale.h>
#include <stdio.h>
#include <stdlib.h>
#include <conio.h>
#include <math.h>
int main() {
    setlocale(LC_ALL, "RUS");
    double log_sum = 0.0;
    double step = 0.1;
    double x;
    for (x = 0.1; x <= 10.0; x += step) {
        log_sum += log(1 + sin(x));
    }
    double product = exp(log_sum);
    printf("Результат произведения: %.15f\n", product);
    return 0;
}
```

## 3. Результаты работы программы


<img src="https://github.com/wyrtwwr/Lab8/blob/main/lab8_code.jpg" width="981" height="266">
