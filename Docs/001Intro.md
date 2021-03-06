Биты – байты
====================
Величина, принимающая два значения, называется _битом_, например,
<p style=" font-family:Consolas;"> 
вкл. / выкл.<br>
истина / ложь<br>
1 / 0<br>
</p>

Последовательность из 8 битов называется _байтом_, например,

<p style=" font-family:Consolas;"> 
00011100<br>
00001001<br>
11111111
</p>

Последовательность из 2 байтов называется _словом_, а из четырёх байтов – двойным словом. Величина 
<text style="font-family:Consolas;"> 
2<sup>2</sup> = 1024
</text>
байта называется __килобайтом__ (Кб), 1024 килобайт составляют __мегабайт__ (Мб), 1024 мегабайт равны __гигабайту__ (Гб).
Биты байта нумеруются от 0 до 7 справа налево. 

<p style=" font-family:Consolas;">
76543210 - Нумерация разрядов<br>
10111010 - двоичное число
</p>

Существует 256 различных состояний байта.

Байту, в двоичной записи (двоичной системе счисления) <text style="font-family:Consolas;">10011011<sub>2</sub></text> придаётся числовое значение соответствующее десятичной записи числа (десятичной системе счисления) <text style="font-family:Consolas;">155<sub>10</sub></text>

Пример перевода из двоичной записи в десятичную
<p style=" font-family:Consolas;"> 10011011<sub>2</sub> = 
1*2<sup>7</sup> + 
0*2<sup>6</sup> + 
0*2<sup>5</sup> + 
1*2<sup>4</sup> + 
1*2<sup>3</sup> + 
0*2<sup>2</sup> + 
1*2<sup>1</sup> + 
1*2<sup>0</sup> =
</p>

<p style=" font-family:Consolas;">
128 + 0 + 0 + 16 + 8 + 0 + 2 + 1 = 155<sub>10</sub>
</p>

Таким образом, можно получить 256 различных значений
<p style=" font-family:Consolas;">
00000000<sub>2</sub> = 0<sub>10</sub><br>
00000001<sub>2</sub> = 1<sub>10</sub><br>
00000010<sub>2</sub> = 2<sub>10</sub><br>
00000011<sub>2</sub> = 3<sub>10</sub><br>
00000100<sub>2</sub> = 4<sub>10</sub><br>
...<br>
11111100<sub>2</sub> = 252<sub>10</sub><br>
11111101<sub>2</sub> = 253<sub>10</sub><br>
11111110<sub>2</sub> = 254<sub>10</sub><br>
11111111<sub>2</sub> = 255<sub>10</sub><br>
</p>

Для представления числа в виде байта, надо найти его двоичное представление, пользуясь правилом деления с остатком на основание системы счисления, в которую переводим ( в нашем случае двоичную):
```
Частное	  155  76  38  19  8  4  2  1  0
Остаток	    1   1   0   1  1  0  0  1  -
```
После чего остатки записать в обратном порядке
<p style=" font-family:Consolas;">
155<sub>10</sub> = 10011011<sub>2</sub>
</p>
Аналогично придаётся числовое значение слову и двойному слову.

Память компьютера
---------------------

Представляет собой последовательность занумерованных от 0 ячеек, каждая из которых организована в виде байта. Количество ячеек называют объёмом памяти. 

Ячейка может вмещать число от 0 до 255. Чтобы разместить в памяти большое по величине числа, его расчленяют на части, которые помещают в несколько соседних ячеек. Ячейка может выражать любое данное (не только числовое), если оно представлено номером - _кодом_. Логические значения кодируются числами 0, 1.

Данные в программировании различаются по __типам__.

Тип определяет назначение данного, способ его кодирования и объём занимаемой памяти (в байтах).