Console-C-
==========
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace HesapBloke
{
    class Program
    {
        static void Main(string[] args)
        {
            int yanlisgirmesayisi = 0;

            menu:
            Console.WriteLine("Wellcome to System !");
            Console.Write("Please enter your password !");
            string sifre = Console.ReadLine();

            if (sifre == "doruk123")
            {
                Console.ForegroundColor = ConsoleColor.Blue;
                Console.Write("Successful");
            }
            else
            {
                yanlisgirmesayisi = yanlisgirmesayisi + 1;
                if (yanlisgirmesayisi >= 3)
                {
                    Console.ForegroundColor = ConsoleColor.White;
                    Console.Write("Account Blocked");
                }

                Console.ForegroundColor = ConsoleColor.Red;
                Console.Write(yanlisgirmesayisi + "Your Password is Wrong");
                Console.ForegroundColor = ConsoleColor.Gray;
                goto menu;
            }
            Console.ReadKey();

        }
    }
}


Password Control
