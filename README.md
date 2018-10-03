# RECURSIVIDAD
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Diagnostics;

namespace fibonacci
{
    class Program
    {
        public int temporal, numero, n, i=0, extra;  
        public void Fubonacci()
        {
            temporal = 0;
            numero = 1;
            Console.WriteLine("¿Cuantos números fibonacci quieres?");

            n = int.Parse(Console.ReadLine());
            
            Console.WriteLine("");
            for (i = 0; i < n; i++)
            {
                extra = temporal;
                temporal = numero;
                numero = extra + temporal;
                Console.WriteLine(temporal);
            }
        }
        static void Recursividad(int x)
        {
            Console.WriteLine("////////////////////////////////////////");
            Console.WriteLine("10 Numeros para fibonacci");

            Console.WriteLine("");
            
            int tempo, num, i1=0, extra1;
            tempo = 0;
            num = 1;

                for(i1=0; i1<x;i1++)
                {
                    extra1=tempo;
                    tempo=num;
                    num = extra1 + tempo;
                    Console.WriteLine(tempo);
                }
        }
        static void Main(string[] args)
        {
            {
                Program m = new Program();
        
                Stopwatch stopWatch = new Stopwatch();

                stopWatch.Start();
                m.Fubonacci();
                stopWatch.Stop();

                Console.WriteLine("Proceso Finalizado en: " + stopWatch.Elapsed.ToString(), "Mensaje Sistema");

                Stopwatch stopWatch1 = new Stopwatch();
                stopWatch1.Start();
                Recursividad(10);
                stopWatch1.Stop();
                Console.WriteLine("Proceso Finalizado en: " + stopWatch1.Elapsed.ToString(), "Mensaje Sistema");
                Console.ReadKey();

            }
        }
    }
}
