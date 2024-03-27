using System;

class Program
{
    const int LEGAL_DRINKING_AGE = 21;
    static void Main(string[] args)
    {
        bool continueProgram = true;

        while (continueProgram)
        {
            RunPersonalInformationSystem();

            // Asking if user wants to continue
            Console.Write("\nDo you want to restart the program (y/n)? ");
            string userInput = Console.ReadLine().ToLower();
            if (userInput != "y")
                continueProgram = false;
            Console.Clear(); 
        }
    }

    static void RunPersonalInformationSystem()
    {
        Console.WriteLine("Welcome to Your Personal Information System!\n");
        Console.Write("Please enter your name: ");
        string name = Console.ReadLine();

        int age;
        double height;

        while (true)
        {
            Console.Write("Please enter your age: ");
            if (int.TryParse(Console.ReadLine(), out age) && age > 0)
                break;
            else
                Console.WriteLine("Invalid input! Age should be a positive integer.");
        }

        while (true)
        {
            Console.Write("Please enter your height in meters: ");
            if (double.TryParse(Console.ReadLine(), out height) && height > 0)
                break;
            else
                Console.WriteLine("Invalid input! Height should be a positive number.");
        }


        double doubleAge = age;

        Console.WriteLine("\n------------------------");
        Console.WriteLine("Your Personal Details:");
        Console.WriteLine($"Name: {name}");
        Console.WriteLine($"Age: {age}");
        Console.WriteLine($"Height: {height} meters\n");

        if (age >= 18)
            Console.WriteLine("Age Check:\nWelcome, " + name + "! You're eligible for additional features.");
        else
            Console.WriteLine("Age Check:\nSorry, you are still a minor.");

        if (age >= LEGAL_DRINKING_AGE)
            Console.WriteLine("\nLegal Drinking Age Verification:\nCheers, " + name + "! You're legally allowed to enjoy alcoholic beverages.");
        else
            Console.WriteLine("\nLegal Drinking Age Verification:\nSorry, " + name + "! You are underage for drinking.");

        string personalInfo = $"Your Personal Information: {name}, {age} years old, {height} meters tall.";
        Console.WriteLine("\nPersonal Details Presentation:\n" + personalInfo);
        Console.WriteLine("\n------------------------");
        Console.WriteLine("Thank you for using Your Personal Information System!");
    }
}
