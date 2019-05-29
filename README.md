# Completed-Rectangle-Class
namespace  Rectangle01
{
    class Program

    {
        public static int ValidateMenuSelection()
        {
            string userInput = "";
            bool validMenuSelect = false;

            while (validMenuSelect == false)
            {
                Console.WriteLine("1 = Get Length");
                Console.WriteLine("2 = Change Length");
                Console.WriteLine("3 = Get Width");
                Console.WriteLine("4 = Change Width");
                Console.WriteLine("5 = Perform Perimeter");
                Console.WriteLine("6 = Perform Area");
                Console.WriteLine("7 = Exit\n");

                Console.WriteLine("Please select an option, by entering a number:\n");
                userInput = Console.ReadLine();

                if (userInput != "1" &&
                    userInput != "2" &&
                    userInput != "3" &&
                    userInput != "4" &&
                    userInput != "5" &&
                    userInput != "6" &&
                    userInput != "7" ) 
                { 
                    Console.WriteLine("That's not a valid menu option, please try again:\n");
                }
                else
                {
                    validMenuSelect = true;
                }
            }

            Console.WriteLine();
            return int.Parse(userInput);
        }

        public static int ValidateUserInput(string selectNumber)
        {
            int number = 1;
            bool isValid = false;

            while (isValid == false)
            {
                Console.WriteLine($"Please enter the {selectNumber}:");
                string userInput = Console.ReadLine();
                Console.WriteLine();

                bool result = int.TryParse(userInput, out number);

                if (result == false)
                {
                    Console.WriteLine("That's not a valid input please, please try again.\n");
                }

                else
                {
                    isValid = true;
                    Console.WriteLine($"Your {selectNumber} has been changed to: {number}.\n");
                }
            }

            return number;
        }


        static void Main(string[] args)
        {
            Rectangle.Rect c = new Rectangle.Rect();
            bool validSelect = false;
            string Selection;
            int selection;

            while (validSelect == false)
            {
               
                Console.WriteLine(" Select the number 1 for the menu\n");
                Console.WriteLine("Choose a menu item to begin:");
                Selection = Console.ReadLine();
                Console.WriteLine();

                if (Selection != "1" )
                {
                    Console.WriteLine("That's not a valid selection, please try again.\n");
                }
                else if (int.Parse(Selection) == 1)
                {
                    validSelect = true;
                    Random random = new Random();
                    int l1;// this is the length of the rectangle
                    int w1;// this is the width of the rectangle

                    l1 = 1;// default contructor set to length input 1
                    w1 =1;// default constructor set to width input 1

                    Console.WriteLine($"Your random numbers are {l1} and {w1}.\n");
                    Rectangle.Rect customRect = new Rectangle.Rect(l1, w1);
                    c = customRect;

                }
                else if (int.Parse(Selection) == 2)
                {
                    validSelect = true;

                    int l1;
                    int w1;

                    l1 = ValidateUserInput("Length");
                    w1 = ValidateUserInput("Width");

                    Console.WriteLine($"Your custom numbers are {l1} and {w1}.\n");
                    Rectangle.Rect customRect = new Rectangle.Rect(l1, w1);
                    c = customRect;
                }
            }


            selection = ValidateMenuSelection();

            while (selection != 7)
            {
                int result;

                switch (selection)
                {
                    case 1:
                        Console.WriteLine($" Length is: {c.GetLength()}\n");
                        break;
                    case 2:
                        result = ValidateUserInput("Length");
                        c.SetLength(result);
                        break;
                    case 3:
                        Console.WriteLine($"Width is: {c.GetWidth()}\n");
                        break;
                    case 4:
                        result = ValidateUserInput("Width");
                        c.SetWidth(result);
                        break;
                    case 5:
                        Console.WriteLine($"Perimeter is : {c.GetPerimeter()}\n");
                        break;
                    case 6:
                        Console.WriteLine($"Area is: {c.GetArea()}\n");
                        break;
                 
                    default:
                        break;
                }

                selection = ValidateMenuSelection();

            }

        }
    }
}
