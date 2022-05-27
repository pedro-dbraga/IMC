using System;

namespace imc1
{
    class Program
    {
        static void Main(string[] args)
        {
            double altura, imc, peso, valor;
            int sexo, idade, i, a;
            string resultado, altmod,cont;

            string[,] ficha = new string[3, 6];

            cont = "S";
            resultado = "";
            altmod = "";
            a = 0;

            Console.WriteLine(" ***** Calculo do IMC ***** ");
            while (cont == "S")
            {

                
                Console.Write("Digite seu nome: ");
                ficha[a, 0] = Console.ReadLine();

                Console.Write("Digite a sua altura: ");
                ficha[a, 1] = Console.ReadLine();

                if (ficha[a, 1].Contains("."))
                {
                    altmod = ficha[a, 1].Replace(".", ",");

                }
                else if (ficha[a, 1].Length <= 3)
                {
                    altmod = ficha[a, 1].Insert(1, ",");
                }

                altura = Convert.ToDouble(altmod);

                Console.Write("Digite o seu Peso: ");
                ficha[a, 2] = Console.ReadLine();

                peso = Convert.ToDouble(ficha[a, 2]);

                valor = peso / Math.Pow(altura, 2);
                imc = Math.Round(valor, 0);
                ficha[a, 3] = Convert.ToString(imc);
                
                Console.WriteLine("Qual o seu genero? ");
                Console.Write("[1] Mulher [2] Homem: ");
                ficha[a,4] = Console.ReadLine();
                sexo = int.Parse(ficha[a,4]);

                while ((sexo < 1) || (sexo > 2))
                {
                    Console.WriteLine("Qual o seu genero? ");
                    Console.Write("[1] Mulher [2] Homem: ");
                    sexo = int.Parse(Console.ReadLine());
                }

                Console.WriteLine("Qual a sua idade? ");
                Console.WriteLine("[1] 18-24 [2] 25-34 [3] 34-44");
                Console.WriteLine("[4] 45-54 [5] 55-64 [6] 65+");
                ficha[a, 5] = Console.ReadLine();
                idade = int.Parse(ficha[a,5]);

                while ((idade < 1) || (idade > 6))
                {
                    Console.WriteLine("Qual a sua idade? ");
                    Console.WriteLine("[1] 18-24 [2] 25-34 [3] 34-44");
                    Console.WriteLine("[4] 45-54 [5] 55-64 [6] 65+");
                    idade = int.Parse(Console.ReadLine());
                }

                switch (sexo)
                {
                    case 1:
                        for (i = -1; i < idade; i++)
                        {
                            if (imc < (19 + i))
                            {
                                resultado = "o seu peso está baixo";
                            }
                            else if ((imc >= (19 + i)) && (imc < (24 + i)))
                            {
                                resultado = "o seu peso está normal";
                            }
                            else if ((imc >= (24 + i)) && (imc < (29 + i)))
                            {
                                resultado = "você se encontra na Pré Obesidade";
                            }
                            else if ((imc >= (29 + i)) && (imc <= (39 + i)))
                            {
                                resultado = "você está na Obesidade";
                            }
                            else
                            {
                                resultado = "você está na  Obesidade Morbida";
                            }
                        }
                        break;

                    case 2:
                        for (i = -1; i < idade; i++)
                        {
                            if (imc < (20 + i))
                            {
                                resultado = "o seu peso está baixo";
                            }
                            else if ((imc >= (20 + i)) && (imc < (25 + i)))
                            {
                                resultado = "o seu peso está normal";
                            }
                            else if ((imc >= (25 + i)) && (imc < (30 + i)))
                            {
                                resultado = "você se encontra na Pré Obesidade";
                            }
                            else if ((imc >= (30 + i)) && (imc <= (40 + i)))
                            {
                                resultado = "você está na Obesidade";
                            }
                            else
                            {
                                resultado = "você está na  Obesidade Morbida";
                            }
                        }
                        break;
                }
                Console.WriteLine("Com o imc de {0} {1}", imc, resultado);

                Console.Write("Deaseja criar outrar ficha[S/N]: ");
                cont = Console.ReadLine();
                string contupper = cont.ToUpper(); 
                cont = contupper;
                a = a ++;
            }
            Console.Write("Fim");
        }
    }
}
