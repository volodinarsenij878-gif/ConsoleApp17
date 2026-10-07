    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;

    namespace Program17
    {
    internal class Program
    {
        static void Main(string[] args)
        {
            // Вычисляем 1/3 в float и double
            float fVal = 1.0f / 3.0f;
            double dVal = 1.0 / 3.0;

            Console.WriteLine("Сравнение точности float и double (1/3):");
            Console.WriteLine(new string('-', 40));

            // Для float достаточно ~9 знаков, дальше «мусор» из‑за ограниченной точности (23 бита мантиссы)
            Console.WriteLine($"float 1/3: {fVal:F9}");

            // double хранит больше значащих цифр (52 бита мантиссы), поэтому показываем до 17 знаков
            Console.WriteLine($"double 1/3: {dVal:F17}");

            Console.WriteLine(new string('-', 40));
            Console.WriteLine("Пояснение:");
            Console.WriteLine("- float: ~7–8 значащих десятичных цифр");
            Console.WriteLine("- double: ~15–17 значащих десятичных цифр");
        }
    }
    }
