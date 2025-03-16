# //user enters the front and back of a flashcard
        
       //need to enter at least 3 (program will ask user how many cards they want to make)
        //a random flashcard will be chosen from the selection the user has inputted
        //the user has to get each flashcard correct twice to finish

        // PREVIOUS TEST CODE:
        //one flashcard program
        
        //Console.WriteLine("enter the front of the flashcard");
        //string card1Front = Console.ReadLine();
        //Console.WriteLine("enter the back of the flashcard");
        //string card1Back = Console.ReadLine();
        //int card1Score = 0;
        //int counter = 0;
        //while (card1Score !=2)
        //{
        // Console.WriteLine(card1Front + " (make sure your answer is spelt correctly)");
        //string userAnswer = Console.ReadLine();
        //;
        //if ( userAnswer == card1Back)
        //{
        //    Console.WriteLine("correct!");
        //    card1Score++;
        //}
        //else
        //{
        //     Console.WriteLine("incorrect!");
        //    counter++;
        //}
        // Console.WriteLine ("you took " + counter +" times to do card");
        // }
        

        // CURRENT CODE;
        
        // multiple card deck code 

        //creating deck
        Console.WriteLine("how many flashcards do you want in your deck?");
        int deckLength = Convert.ToInt32(Console.ReadLine());
        string[] deckFront = new string[deckLength];
        string[] deckBack = new string[deckLength];
        for (int i = 1; i <= deckLength - 1; i++)
        {
            Console.WriteLine("enter front of flashcard " + i);
            deckFront[i] = Console.ReadLine();

            Console.WriteLine("enter back of flashcard " + i);
            deckBack[i] = Console.ReadLine();
        }

        //code for picking random card from deck and reapeating until it is right
        int counter = 0;
        int cardScore = 0;
        Random number = new Random();
        //picks random front of card with generator
        while (counter != 2)
        {


            Console.WriteLine(deckFront[number.Next(0, deckFront.Length)] +
                              " (make sure your answer is spelt correctly)");
            string userAnswer = Console.ReadLine();
            ;
            if (userAnswer == deckBack[number.Next(0, deckFront.Length)]);
            {
                Console.WriteLine("correct!");
                cardScore++;
            }
            else //not sure why this is wrong
            {
                Console.WriteLine("incorrect!");
                counter++;
            }

            Console.WriteLine("you took " + counter + " times to do card");


        }

    }
}

    



![image](https://github.com/user-attachments/assets/1ed027fb-f09e-43c5-98b5-dc8341fc885e)

