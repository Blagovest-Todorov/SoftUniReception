# SoftUniReception
task by midExam 
////////


using System;

namespace SoftUniReception
{
    class Program
    {
        static void Main(string[] args)
        {
            int workerOne = int.Parse(Console.ReadLine());
            int workerTwo = int.Parse(Console.ReadLine());
            int workerThree = int.Parse(Console.ReadLine());

            int totalWorkedStudents = workerOne + workerTwo + workerThree;

            int workedHours = 0;
            int restHours = 0;

            int leftStudents = int.Parse(Console.ReadLine());

            while (true)
            {
                if (leftStudents <= 0)
                {
                    Console.WriteLine($"Time needed: {restHours + workedHours}h.");
                    break;
                }

                workedHours += 1;
                leftStudents -= totalWorkedStudents;

                if (workedHours % 3 == 0 && leftStudents > 0 )
                {
                    restHours += 1;
                }
            }            
        }
    }
}

