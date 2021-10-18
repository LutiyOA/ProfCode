Теория
===
Одномерные массивы
---
```                                       
 ┌──────────┐                          
 │   Alen   │  - контейнер / переменная
 └──────────┘                          
    user                               
```
Понадобилось 100 переменных
---
```
int  a0, a1,   a2,  a3,  a4,  a5,  a6,  a7,  a8,  a9, 
    a10, a11, a12, a13, a14, a15, a16, a17, a18, a19,
    a20, a21, a22, a23, a24, a25, a26, a27, a28, a29, 
    a30, a31, a32, a33, a34, a35, a36, a37, a38, a39, 
    a40, a41, a42, a43, a44, a45, a46, a47, a48, a49, 
    a50, a51, a52, a53, a54, a55, a56, a57, a58, a59, 
    a60, a61, a62, a63, a64, a65, a66, a67, a68, a69, 
    a70, a71, a72, a73, a74, a75, a76, a77, a78, a79, 
    a80, a81, a82, a83, a84, a85, a86, a87, a88, a89, 
    a90, a91, a92, a93, a94, a95, a96, a97, a98, a99;
```

```
┌──────────────────────────────────────────────────────────────────────────┐
│ ┌─────────┐ ┌─────────┐ ┌─────────┐ ┌─────────┐ ┌──────────┐ ┌─────────┐ │
│ │  28.09  │ │  11.08  │ │  15.16  │ │  71.81  │ │ 2018.987 │ │    1    │ │
│ └─────────┘ └─────────┘ └─────────┘ └─────────┘ └──────────┘ └─────────┘ │
│      0           1           2           3           4            5      │
└──────────────────────────────────────────────────────────────────────────┘
                                    train        

train[0], train[1], train[2], train[3], train[4], train[5]                  
Индексы меняются от 0 до 5                               
```

Одномерный массив
---
```
┌───┬───┬───┬───┬───┬───┬────┬────┬────┐
│ 1 │ 1 │ 2 │ 3 │ 5 │ 8 │ 13 │ 21 │ 32 │ Одна строка
└───┴───┴───┴───┴───┴───┴────┴────┴────┘
```
```
Способ здания одномерного массива
ТипДанных[] Идентификатор массива;

Инициализация массива
ТипДанных[] Идентификатор массива = new ТипДанных[Количество элементов()];
```

Описание массивов
===
Вариант 1
---
```
int[] array = new int[2021];            // 2021 = array.Length
double[] collection = new double[20];   // 20 = collection.Length
bool[] flags = new bool[10];
```
Вариант 2
---
```
int n = 10;
char[] symbols = new char[n];
```
Вариант 3
---
```
const int count = 10;
int[] numbers = new int[count];
```
Вариант 4
---
```
string[] text =
{
    "2",            // text[0]
    "2 + 2",        // text[1]
    "2 + 2 * 2",    // text[2]
    "(2 + 2) * 2",  // text[3]
};
```
Операции с массивом
---
 Чтение элемента массива
---
```
string value = text[0];
WriteLine(value);
```

Запись элемента массива
---
```
text[1] = "2 + 3"; 
```
Некоторый методы для работы с массивами
---

Получить количество элементов
---
```
int[] numbers = new int[10];
int length = numbers.Length; 
```

Многомерные массивы 
===
Двумерные массивы 
---

```
А если нужна таблица?
┌───┬───┬───┬───┐
│ 1 │ 2 │ 3 │ 4 │  0 строка
├───┼───┼───┼───┤
│ 4 │ 5 │ 6 │ 7 │  1 строка
├───┼───┼───┼───┤
│ 7 │ 8 │ 9 │ 0 │  2 строка
└───┴───┴───┴───┘
  0   1   2   3
     столбец

ТипДанных[,] ИдентификаторМассива = new ТипДанных[КоличествоСтрок, КоличествоСтолбцов];
   
```
```
int[,] matrix = new int[3, 4];

for (int i = 0; i < 3; i++)
{
    for (int j = 0; j < 4; j++)
    {
        Write($"{matrix[i, j]} ");
    }
    WriteLine();
}
```
```
matrix.Length - возвращает общее количество элементов
matrix.GetLength(0) - возвращает количество строк
matrix.GetLength(1) - возвращает количество столбцов

```

Общая идея многомерных массивов
---
```
ТипДанных[, ... ,] ИдентификаторМассива = 
new ТипДанных[размерность №0, размерность №1, ..., размерность №N];
```
Трехмерные массивы 
---
```
int[,,] array3 = new int[2, 3, 4];

for (int i = 0; i < array3.GetLength(0); i++)
{
    for (int j = 0; j < array3.GetLength(1); j++)
    {
        for (int k = 0; k < array3.GetLength(2); k++)
        {
            WriteLine($"[{i}, {j}, {k}] = {array3[i, j, k]}");
        }
    }
}
```

Массивы больших размерностей
---
```
int[,,,] array4 = new int[2, 3, 4, 5];
int[,,,,] array5 = new int[2, 3, 4, 5, 6];
```

Массивы массивов, ступенчатые (зубчатые) массивы
===

```
┌────┬────┬────┐
│ 11 │ 12 │ 13 │                       0 строка [массив с индексом 0]
├────┼────┼────┼────┐
│ 21 │ 22 │ 23 │ 24 │                  1 строка [массив с индексом 1]
├────┼────┼────┴────┴
│ 31 │ 32 │                            2 строка [массив с индексом 2]
├────┼────┼────┬────┬────┐
│ 41 │ 42 │ 43 │ 44 │ 45 │             3 строка [массив с индексом 3]
├────┼────┴────┴────┴────┘
│ 51 │                                 4 строка [массив с индексом 4]
└────┘                   
   0    1    2    3    4
```
```
int[][] array = new int[5][];
array[0] = new int[3] { 11, 12, 13 };
array[1] = new int[4] { 21, 22, 23, 24 };
array[2] = new int[2] { 31, 32 };
array[3] = new int[5] { 41, 42, 43, 44, 45 };
array[4] = new int[1] { 51 };
```
```
for (int i = 0; i < array.Length; i++)
{
    for (int j = 0; j < array[i].Length; j++)
    {
        Write($"{array[i][j],3}");
    }
    WriteLine();
}
```
Результат работы с for:
```
 11 12 13
 21 22 23 24
 31 32
 41 42 43 44 45
 51
```
```
foreach (var item in array)
{
    foreach (var e in item)
    {
        Write($"{e,3}");
    }
    WriteLine();
}
```
Результат работы с foreach:
```
 11 12 13
 21 22 23 24
 31 32
 41 42 43 44 45
 51
```
Код, который с 99% вероятностью не пройдёт Code Review
===
Слишком сложная для понимая структура

И слишком специфичная
```
int[][][][][] arrray = new int[3][][][][];
```