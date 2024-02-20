

/* Задайте значения M и N. Напишите программу, которая выведет все натуральные числа в промежутке от M до N.
 * Использовать рекурсию, не использовать циклы.
        {   Console.Clear();
            Console.WriteLine("Введите значение M:");
            int M = Convert.ToInt32(Console.ReadLine());

            Console.WriteLine("Введите значение N:");
            int N = Convert.ToInt32(Console.ReadLine());

            Console.WriteLine();

            if (M > N)
            {
                Console.WriteLine("Ошибка: M не может быть больше N");
                return;
            }
            else
            {
                PrintNumbers(M, N);
            }

            
        }

        static void PrintNumbers(int M, int N)
        {
            
            if (M <= N)
            {
                Console.WriteLine(M);
                PrintNumbers(M + 1, N);
            }
                        
        }
       
    
// Напишите программу вычисления функции 
// Аккермана с помощью рекурсии. Даны два неотрицательных числа m и n.

  Console.WriteLine("Введите значение M:");
            int M = Convert.ToInt32(Console.ReadLine());

            Console.WriteLine("Введите значение N:");
            int N = Convert.ToInt32(Console.ReadLine());

            Console.WriteLine();

            int result = 0;

            if (M < 0 || N < 0)
            {
                Console.WriteLine("Ошибка: значения M и N не могут быть отрицательными.");
                Console.WriteLine();
                return;
            }
            else
            {
                result = Ackermann(M, N);
            }
                          
            
            Console.WriteLine($"Результат функции Аккермана для M={M} и N={N} равен {result}");
            Console.WriteLine();
        

        static int Ackermann(int M, int N)
        {
            if (M == 0)
            {
                return N + 1;
            }
            else if (N == 0)
            {
                return Ackermann(M - 1, 1);
            }
            else
            {
                return Ackermann(M - 1, Ackermann(M, N - 1));
            }

        }
         */

         //Задача 3: Задайте произвольный массив. 
         //Выведете его элементы, начиная с конца. Использовать рекурсию, не использовать циклы
        {
            int[] array = GenerateRandomArray(10);
            Console.WriteLine("Массив: ");
            Console.WriteLine();
            PrintArray(array);

            Console.WriteLine();

            Console.WriteLine(" Переворот массива: ");
            Console.WriteLine();
            PrintArrayReverse(array, array.Length - 1);
            Console.WriteLine();

         int[] GenerateRandomArray(int size)
        {
            int[] randomArray = new int[size];
            Random rnd = new Random();
            for (int i = 0; i < size; i++)
            {
                randomArray[i] = rnd.Next(10, 100);
            }
            
            return randomArray;
        }

         void PrintArray(int[] array)
        {
            for (int i = 0; i < array.Length; i++)
            {
                Console.Write(array[i] + " ");
            }
            

        }

         void PrintArrayReverse(int[] array, int index)
        {
            if (index >= 0)
            {
                Console.Write(array[index] + " ");
                PrintArrayReverse(array, index - 1);
            }
        }
    }

    
