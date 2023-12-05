using System;
using System.Linq;

namespace _04._Array_Rotation_
{
    class Program
    {
        static void Main(string[] args)
        {
            int[] arr = Console.ReadLine()
                .Split(' ')
                .Select(int.Parse)
                .ToArray();
            int rotationCount = int.Parse(Console.ReadLine());

            for (int r = 1; r <= rotationCount; r++)
            {
                int firstElement = arr[0];
                for (int i = 1; i < arr.Length; i++)
                {
                    arr[i - 1] = arr[i];
                }
                arr[arr.Length - 1] = firstElement;
            }
            Console.WriteLine(string.Join(' ', arr));
        }
    }
}
