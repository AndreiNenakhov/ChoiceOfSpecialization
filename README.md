## Итоговая работа по прохождению курса "Выбор специализации"

Для выполнения проверочной работы необходимо:

1.Создать репозиторий GitHub;

2.Нарисовать блок схему алгоритма;

3.Создать в репозитории файл README.md

4.Написать программу, решающую задачу

5.Использовать контроль версий в работе над этим проектом

**Задача:**

Написать программу, которая из имеющегося массива строк формирует массив из строк, длинна которых меньше либо равна 3 символа. Первоначальный массив можно ввести с клавиатуры, либо задать на старте выполнения алгоритма. При решении не рекомендуется пользоваться коллекциями, лучше обойтись исключительно массивами.

**Примеры:**

["hello", "2", "word", ":-)"] ---> ["2", ":-)"]

["1234", "1567", "-2", "computer science"] ---> ["-2"]

["Russia", "Denmark", "Kazan", ""] ---> []


**Блок схема решения задачи:**

![ForMetod](https://user-images.githubusercontent.com/124388285/227773897-5657d485-9e0a-40a0-9c3b-c6a8b87e5a9c.jpg)

**Код программы:**

string[] array1 = new string[5] {"123", "23", "hello", "world", "res"};

string[] array2 = new string[array1.Length];

void SecondArrayWithIF(string[] array1, string[] array2)

{
   
   int count = 0;
   
   for (int i = 0; i < array1.Length; i++)
   
   {
    
    if(array1[i].Length <= 3)
       
       {
       
       array2[count] = array1[i];
       
       count++;
       
       }
    
    }

}

void PrintArray(string[] array)

{
    
    for (int i = 0; i < array.Length; i++)
   
   {
       
       Console.Write($"{array[i]} ");
   
   }
   
   Console.WriteLine();

}

SecondArrayWithIF(array1, array2);

PrintArray(array2);
