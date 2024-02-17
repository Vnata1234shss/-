 //Задайте двумерный массив символов (тип char [,]). Создать строку из символов этого массива.
 /*
{
char[,] charArray = new char[,] { { 'a', 'b' }, { 'c', 'd' } };
string result = CreateStringFrom2DArray(charArray); //  Вызов метода для создания строки из 2D массива
Console.WriteLine(result);
}
string CreateStringFrom2DArray(char[,] array) // Метод для создания строки из двумерного массива символов
{
string result = "";
for (int i = 0; i < array.GetLength(0); i++)
{
for (int j = 0; j < array.GetLength(1); j++)
{
result += array[i, j];
}
}
return result;
}

//Задача 2: Задайте строку, содержащую латинские буквы в обоих регистрах.
//Сформируйте строку, в которой все заглавные буквы заменены на строчные.
Console.Clear();
string input = "AnUtJdS";
string result = input.ToLower(); // Преобразование всех заглавных букв в строчные
Console.WriteLine(result);*/

// Задайте произвольную строку. Выясните, является ли она палиндромом.
Console.Clear();
string input = "kjh";
// Вызов метода для проверки, является ли строка палиндромом
bool isPalindrome = IsPalindrome(input);
// Вывод результата
Console.WriteLine(isPalindrome ? "Да" : "Нет");

// Метод для проверки, является ли строка палиндромом
 static bool IsPalindrome(string str)
{
// Нормализация строки путем удаления не буквенно-цифровыхсимволов и приведения к нижнему регистру
string normalized = new
string(str.Where(char.IsLetterOrDigit).ToArray()).ToLower();
// Сравнение строки с ее перевернутым вариантом
return normalized.SequenceEqual(normalized.Reverse());
}
