# Vapor-Store
Just another repository
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Vapor_Store
{
    class Program
    {
        static void Main(string[] args)
        {
            double myMoney = double.Parse(Console.ReadLine());

            double balance = myMoney;
            double spentMoney = 0;
            double gamePrice = 0;

            while (true)
            {
                string theNameOfTheGame = Console.ReadLine();

                if (theNameOfTheGame == "Game Time")
                {
                    break;
                }

                switch (theNameOfTheGame)
                {
                    case "OutFall 4":
                    case "RoverWatch Origins Edition":
                        gamePrice = 39.99;
                        if (gamePrice > balance)
                        {
                            Console.WriteLine("Too Expensive");
                        }
                        else
                        {
                            balance -= gamePrice;
                            spentMoney += gamePrice;
                            Console.WriteLine($"Bought {theNameOfTheGame}");
                        }
                        break;
                    case "CS: OG":
                        gamePrice = 15.99;
                        if (gamePrice > balance)
                        {
                            Console.WriteLine("Too Expensive");
                        }
                        else
                        {
                            balance -= gamePrice;
                            spentMoney += gamePrice;
                            Console.WriteLine($"Bought {theNameOfTheGame}");
                        }
                        break;
                    case "Zplinter Zell":
                        gamePrice = 19.99;
                        if (gamePrice > balance)
                        {
                            Console.WriteLine("Too Expensive");
                        }
                        else
                        {
                            balance -= gamePrice;
                            spentMoney += gamePrice;
                            Console.WriteLine($"Bought {theNameOfTheGame}");
                        }
                        break;
                    case "Honored 2":
                        gamePrice = 59.99;
                        if (gamePrice > balance)
                        {
                            Console.WriteLine("Too Expensive");
                        }
                        else
                        {
                            balance -= gamePrice;
                            spentMoney += gamePrice;
                            Console.WriteLine($"Bought {theNameOfTheGame}");
                        }
                        break;
                    case "RoverWatch":
                        gamePrice = 29.99;
                        if (gamePrice > balance)
                        {
                            Console.WriteLine("Too Expensive");
                        }
                        else
                        {
                            balance -= gamePrice;
                            spentMoney += gamePrice;
                            Console.WriteLine($"Bought {theNameOfTheGame}");
                        }
                        break;
                    default:
                        Console.WriteLine("Not Found");
                        break;
                }
                if (balance == 0)
                {
                    Console.WriteLine("Out of money!");
                    return;
                }
            }

            Console.WriteLine("Total spent: ${0:f2}. Remaining: ${1:f2}", spentMoney, balance);
        }
    }
}
