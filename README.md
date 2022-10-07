# Lesson_2_HomeWork

## Задача 10. На входе трехзначное число. На выходе вторая цифра числа.

```
int rand = new Random().Next(100, 1000);
Console.WriteLine(rand);
Console.Write($"{rand / 10 - (rand / 100 * 10)}");
```

## Задача 13. НА входе число. На Выходе третья цифра. Если ее нет, выводит -НЕТ.

```
int rand = new Random().Next(10, 10000);
Console.WriteLine(rand);
if (rand > 999)
{
    while (rand > 999)
        rand = rand / 10;
    Console.WriteLine($"Третья Цифра данного числа {rand % 10}");
}
else
if (rand > 100 && rand < 999)
{
    Console.WriteLine($"Третья Цифра данного числа {rand % 10}");
}
if (rand < 100)
{
    Console.WriteLine("Третье Число Отсутствует");
}
```

## Задача 14. На ходе Число. На Выход День недели. Выходной или НЕТ.
```
int rand = new Random().Next(1, 31);
int[] ar_hol = { 6, 7, 13, 14, 20, 21, 27, 28 };
int[] ar_work = { 1, 2, 3, 4, 5, 8, 9, 10, 11, 12, 15, 16, 17, 18, 19, 22, 23, 24, 25, 26, 29, 30, 31 };
for (int i = 0; i < ar_hol.Length; i++)
{
    if (rand == ar_hol[i])
    {
        Console.Write($"{rand} - Выходной");
    }
}
for (int i = 0; i < ar_work.Length; i++)
{
    if (rand == ar_work[i])
    {
        Console.Write($"{rand} - Рабочий");
    }
}
```