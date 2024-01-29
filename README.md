# MultiplicaçãoDeMatrizes
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Xml;

namespace MultiplicaçãoDeMatrizes
{
    internal class Program
    {
        static void Main(string[] args)
        {
            int[,] matriz1 = new int[2, 3];
            int[,] matriz2 = new int[3, 2];
            int[,] resultado = new int[2, 2];

            Console.WriteLine("Digite os números da MAtriz#1");
            for (int linha = 0; linha < 2; linha++)
            {
                for (int Coluna = 0; Coluna < 3; Coluna++)
                {
                    Console.Write("#1. Posição [" + linha + "][" + Coluna + "]: ");
                    matriz1[linha, Coluna] = int.Parse(Console.ReadLine());
                }
            }

            Console.WriteLine("\nDigite os números da MAtriz#2");
            for (int linha = 0; linha < 3; linha++)
            {
                for (int Coluna = 0; Coluna < 2; Coluna++)
                {
                    Console.Write("#2. Posição [" + linha + "][" + Coluna + "]: ");
                    matriz2[linha, Coluna] = int.Parse(Console.ReadLine());
                }
            }
            Console.WriteLine("\nResultado da Matriz #1 x Matriz #2");
            resultado[0, 0] = (matriz1[0, 0] * matriz2[0, 0] + matriz1[0, 1] * matriz2[1, 0] + matriz1[0, 2] * matriz2[2, 0]);
            resultado[1, 0] = (matriz1[1, 0] * matriz2[0, 0] + matriz1[1, 1] * matriz2[1, 0] + matriz1[1, 2] * matriz2[2, 0]);
            resultado[0, 1] = (matriz1[0, 0] * matriz2[0, 1] + matriz1[0, 1] * matriz2[1, 1] + matriz1[0, 2] * matriz2[2, 1]);
            resultado[1, 1] = (matriz1[1, 0] * matriz2[0, 1] + matriz1[1, 1] * matriz2[1, 1] + matriz1[1, 2] * matriz2[2, 1]);

            Console.WriteLine("[" + resultado[0, 0] + "][" + resultado[0, 1] + "]");
            Console.WriteLine("[" + resultado[1, 0] + "][" + resultado[1, 1] + "]");
            Console.ReadKey();





        }
    }
}
