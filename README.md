# Образцы заданий и выполненных работ 57xx
## matrix.c -  линейная алгебра
Набор функций для выполнения операций с матрицами.
**Важно - каждая из функций выделяет в куче новый кусок памяти, поэтому во избежание утечек памяти следует сохранять результаты всех промежуточных вычислений**
```
```
TMatrix *mi, *mscale, *mrot, *mr1, *mr2, *mv;

mv = mx_from_text("1 / 3"); //вектор-столбец
mi = mx_identity(2); //генерируем единичную матрицу
ms = mx_mul_sc(mi, 1.5); //умножаем на 1.5
mrot = mx_from_text("0 -1 / 1 0"); // матрица поворота
mr1 = mx_mul(mrot, mv);  //поворачиваем
mr2 = mx_mul(ms, mr1); // масштабируем
mx_print(mr); //печатаем
//освобождаем память
mx_free(mi);
mx_free(mscale);
mx_free(mrot);
mx_free(mr1);
mx_free(mr2);
mx_free(mv);

```