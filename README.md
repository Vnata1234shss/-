// Напишите программу, которая бесконечно запрашивает целые числа с консоли.
//Программа завершается при вводе символа
//‘q’ или при вводе числа, сумма цифр которого чётная.
while (true) // Бесконечный цикл
{
    Console.WriteLine("Введите число или 'q' для выхода из программы: ");
    string input = Console.ReadLine();
    if(input=="q")
    {
        break;
    }

    int number;
    if (int.TryParse(input, out number)) // Проверка, является ли ввод числом
    {
        int sum = 0;
        while(number > 0 ) // Вычисление суммы цифр числа 
        {
            sum += number % 10; // узнаем последнию цифру
            number /= 10 ; // удаляем последнию цифру числа
        }
        if(sum % 2 ==0)
        {
            Console.WriteLine("[STOP]");
            break;
        }
    }
    else {
        System.Console.WriteLine("Введите число снова");
    }
}
}


    //Задайте массив заполненный случайными трёхзначными числами.
    // Напишите программу, которая покажет количество чётных чисел в массиве.
    int[] num = new int[10];
    Random random = new Random();
    int evenCount = 0; // Счетчик  четных чисел
    for (int i = 0; i < num.Length; i++)
    {
        num[i] = random.Next(100, 1000);
        Console.Write(num[i] + " ");


        if (num[i] % 2 == 0)
        {
            evenCount++;
        }
    }
    System.Console.WriteLine($"Количество чётных чисел в массиве:{evenCount}");
}
