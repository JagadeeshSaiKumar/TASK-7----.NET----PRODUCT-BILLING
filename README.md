using System.Threading;

class task7
{
    public static void Main(String[] args)
    {
        Console.ForegroundColor = ConsoleColor.Cyan;
        Console.WriteLine("                             WELCOME TO MARTGAGE");
        Console.WriteLine("────────────────────────────────────────────────────────────");
        Console.WriteLine("1 ─ Admin login");
        Console.WriteLine("2 ─ User login");
        Console.Write("Enter your choice : ");
        int n = Convert.ToInt32(Console.ReadLine());
        while (n > 2 && n < 0)
        {
            Console.WriteLine("Choose between those options only ");
            Console.Write("Enter your choice : ");
            n = Convert.ToInt32(Console.ReadLine());
        }
        int a, ph;
        int[] p;
        int[] up = new int[] { 10, 20, 30 };
        string[] uc = new string[] { "mango", "sugar", "rice" };
        string[] s;
        string pwd = "admin", pwd1, ea, name, mail, na = "admin";
        while (n == 1)
        {
            Console.ForegroundColor = ConsoleColor.Cyan;
            Console.WriteLine("Admin id      :" + na);
            Console.WriteLine("Your password :" + na);
            Console.WriteLine("Your password is easy to be hacked");
            Console.WriteLine("You need to reset the password ...");
            Console.Write("If you wish to change press '1' else '0' : ");
            a = Convert.ToInt32(Console.ReadLine());
            if (a == 1)
            {
                Console.Write("Enter your new password : ");
                pwd = Console.ReadLine();
                Console.WriteLine("               .... Password Changed Successfully .... ");
            }
            else
            {
                Console.WriteLine("                .... Password is Unchanged .... ");
            }
            Thread.Sleep(3000);
            Console.Clear();
            Console.WriteLine("                         ADMIN LOGIN ");
            Console.WriteLine("───────────────────────────────────────────────────────────────────────────");
            Console.Write("Enter Admin id : ");
            ea = Console.ReadLine();
            Console.Write("Enter password : ");
            pwd1 = Console.ReadLine();
            while (pwd1 != pwd && ea != na)
            {
                Console.Clear();
                Console.Write("Enter Admin id : ");
                ea = Console.ReadLine();
                Console.Write("Enter password : ");
                pwd1 = Console.ReadLine();
            }
            if (pwd1 == pwd && ea == na)
            {
                Console.Clear();
                Console.WriteLine("                         ADMIN DASHBOARD ");
                Console.WriteLine("───────────────────────────────────────────────────────────────────────────");
                Console.ForegroundColor = ConsoleColor.Magenta;
                Console.Write("Enter the number of items : ");
                a = Convert.ToInt32(Console.ReadLine());
                s = new string[a];
                p = new int[a];
                for (int i = 0; i < s.Length; i++)
                {
                    Console.WriteLine();
                    Console.Write("Enter the " + (i + 1) + " item name  : ");
                    s[i] = Console.ReadLine();
                    Console.WriteLine();
                    Console.Write("Enter the " + (i + 1) + " item Price : ");
                    p[i] = Convert.ToInt32(Console.ReadLine());
                }
                Console.Clear();
                Console.WriteLine("The items in the list are given below ...");
                Console.WriteLine();
                Console.ForegroundColor = ConsoleColor.Red;
                Console.WriteLine(" Item-name                           Item-Price ");
                for (int i = 0; i < s.Length; i++)
                {
                    Thread.Sleep(3000);
                    Console.WriteLine("  " + s[i] + "\t\t\t\t\t\t\t\t" + p[i]);
                    Console.WriteLine();
                }
                Thread.Sleep(5000);
                Console.ForegroundColor = ConsoleColor.Blue;
                Console.WriteLine("\t\t\t\t\t\tWELCOME TO MARTGAGE");
                Console.WriteLine(); Console.WriteLine("──────────────────────────────────────────────────────────────────────────────────────");
                Console.WriteLine("1 ─ Admin login");
                Console.WriteLine("2 ─ User login");
                Console.Write("Enter your choice : ");
                n = Convert.ToInt32(Console.ReadLine());
                if (n == 1)
                {
                    Console.Clear();
                    Console.Write("Enter Admin id : ");
                    ea = Console.ReadLine();
                    Console.Write("Enter password : ");
                    pwd1 = Console.ReadLine();
                    if (pwd == pwd1)
                    {
                        Console.Clear();
                        Console.WriteLine("\t\t\t\t\tWelcome Mr Admin ");
                        Console.WriteLine("The items we are having in  store are given below ...");
                        Console.WriteLine();
                        Console.ForegroundColor = ConsoleColor.Red;
                        Console.WriteLine(" Item-name                           Item-Price ");
                        for (int i = 0; i < s.Length; i++)
                        {
                            Thread.Sleep(3000);
                            Console.WriteLine("  " + s[i] + "\t\t\t\t\t\t" + p[i]);
                            Console.WriteLine();
                        }
                    }

                }
                else if (n == 2)
                {
                    Console.WriteLine("USER LOGIN");
                    Console.WriteLine("We have the below items for sale ...");
                    for (int i = 0; i < s.Length; i++)
                    {
                        Console.WriteLine((i + 1) + " - item name  " + s[i] + " and it's price = " + p[i]);
                        Console.WriteLine();
                    }
                    Console.Write("How many item you want to purchase : ");
                    int b = Convert.ToInt32(Console.ReadLine());
                    string[] c = new string[b];
                    int[] q = new int[b];
                    Console.WriteLine("Enter the items names : ");
                    Console.WriteLine();
                    for (int i = 0; i < b; i++)
                    {
                        Console.Write((i + 1) + " - item name : ");
                        c[i] = Console.ReadLine();
                        Console.Write((i + 1) + " - item Quantity : ");
                        q[i] = Convert.ToInt32(Console.ReadLine());
                    }
                    Console.WriteLine();
                    if (b == 0)
                    {
                        break;
                    }
                    else
                    {
                        Console.WriteLine("Customer please provide the following details..");
                        Console.Write("Name         : ");
                        name = Console.ReadLine();
                        Console.Write("Phone number : ");
                        ph = Convert.ToInt32(Console.ReadLine());
                        Console.Write("Mail Id      : ");
                        mail = Console.ReadLine();
                        Console.Clear();
                        Console.ForegroundColor = ConsoleColor.Yellow;
                        Console.WriteLine();
                        Console.WriteLine("                             BILL                        ");
                        Console.WriteLine();
                        Thread.Sleep(1000);
                        Console.WriteLine("                             Customer Details");
                        Console.WriteLine();
                        Console.WriteLine("───────────────────────────────────────────────────────────────────────────");
                        Console.WriteLine("Customer Name : " + name);
                        Thread.Sleep(1300);
                        Console.WriteLine("Phone number  : " + ph);
                        Thread.Sleep(1300);
                        Console.WriteLine("Mail Id       : " + mail);
                        Thread.Sleep(1300);
                        Console.WriteLine();
                        Console.WriteLine("───────────────────────────────────────────────────────────────────────────");
                        Console.WriteLine();
                        Console.ForegroundColor = ConsoleColor.Blue;
                        Console.WriteLine("                              ITEMS Purchased                      ");
                        Console.WriteLine();
                        Thread.Sleep(1300);
                        Console.WriteLine("───────────────────────────────────────────────────────────────────────────");
                        Console.WriteLine();
                        Console.WriteLine("Items name                       Quantity                        Total price");
                        Console.WriteLine();
                        Console.WriteLine("───────────────────────────────────────────────────────────────────────────");
                        int sum = 0;
                        for (int i = 0; i < c.Length; i++)
                        {
                            Thread.Sleep(3000);
                            Console.WriteLine(c[i] + "\t\t\t\t" + q[i] + "\t\t\t\t\t\t\t" + (q[i] * p[i]));
                            sum += (q[i] * p[i]);
                            Console.WriteLine();
                        }
                        double d;
                        d = sum - (sum * 0.2);
                        Console.WriteLine("───────────────────────────────────────────────────────────────────────────");
                        Console.WriteLine();
                        Console.WriteLine("                                                 Amount   = " + sum + "rs/-");
                        Console.WriteLine("                                                 Discount = " + (0.2) + " %");
                        Console.ForegroundColor = ConsoleColor.Cyan;
                        Console.WriteLine("                                             Total Amount = " + d + "rs/-");
                    }

                }
            }

        }
        Console.WriteLine("\t\t\t\t\tUSER LOGIN");
        Console.WriteLine("We have the below items for sale ...");
        for (int i = 0; i < uc.Length; i++)
        {
            Console.WriteLine((i + 1) + " - item name  " + uc[i] + " and it's price = " + up[i]);
            Console.WriteLine();
        }
        Console.Write("How many item you want to purchase : ");
        int ub = Convert.ToInt32(Console.ReadLine());
        string[] uuc = new string[ub];
        int[] uq = new int[ub];
        Console.WriteLine("Enter the items names : ");
        Console.WriteLine();
        for (int i = 0; i <ub; i++)
        {
            Console.Write((i + 1) + " - item name : ");
            uuc[i] = Console.ReadLine();
            Console.Write((i + 1) + " - item Quantity : ");
            uq[i] = Convert.ToInt32(Console.ReadLine());
        }
        Console.WriteLine();
        if (ub != 0)
        {
            Console.WriteLine("Customer please provide the following details..");
            Console.Write("Name         : ");
            name = Console.ReadLine();
            Console.Write("Phone number : ");
            ph = Convert.ToInt32(Console.ReadLine());
            Console.Write("Mail Id      : ");
            mail = Console.ReadLine();
            Console.Clear();
            Console.ForegroundColor = ConsoleColor.Yellow;
            Console.WriteLine();
            Console.WriteLine("                             BILL                        ");
            Console.WriteLine();
            Thread.Sleep(1000);
            Console.WriteLine("                        Customer Details");
            Console.WriteLine();
            Console.WriteLine("───────────────────────────────────────────────────────────────────────────");
            Console.WriteLine("Customer Name : " + name);
            Thread.Sleep(1300);
            Console.WriteLine("Phone number  : " + ph);
            Thread.Sleep(1300);
            Console.WriteLine("Mail Id       : " + mail);
            Thread.Sleep(1300);
            Console.WriteLine();
            Console.WriteLine("───────────────────────────────────────────────────────────────────────────");
            Console.WriteLine();
            Console.ForegroundColor = ConsoleColor.Blue;
            Console.WriteLine("                              ITEMS Purchased                      ");
            Console.WriteLine();
            Thread.Sleep(1300);
            Console.WriteLine("───────────────────────────────────────────────────────────────────────────");
            Console.WriteLine();
            Console.WriteLine("Items name                       Quantity                        Total price");
            Console.WriteLine();
            Console.WriteLine("───────────────────────────────────────────────────────────────────────────");
            int sum = 0;
            for (int i = 0; i < uuc.Length; i++)
            {
                Thread.Sleep(3000);
                Console.WriteLine(uuc[i] + "\t\t\t\t" + uq[i] + "\t\t\t\t\t" + (uq[i] * up[i]));
                sum += (uq[i] * up[i]);
                Console.WriteLine();
            }
            double d;
            d = sum - (sum * 0.2);
            Console.WriteLine("───────────────────────────────────────────────────────────────────────────");
            Console.WriteLine();
            Console.WriteLine("                                                 Amount   = " + sum + "rs/-");
            Console.WriteLine("                                                 Discount = " + (0.2) + " %");
            Console.ForegroundColor = ConsoleColor.Cyan;
            Console.WriteLine("                                             Total Amount = " + d + "rs/-");
        }

    }

}

