# //user enters the front and back of a flashcard
        //need to enter at least 3 (program will ask user how many cards they want to make)
        //a random flashcard will be chosen from the selection the user has inputted
        //the user has to get each flashcard correct twice to finish
        
        
        //one flashcard program
        Console.WriteLine("enter the front of the flashcard");
        string card1Front = Console.ReadLine();
        Console.WriteLine("enter the back of the flashcard");
        string card1Back = Console.ReadLine();
        int card1Score == 0;
        int counter;
        
        while (card1Score !=2)
        {
            Console.WriteLine(card1Front + " (make sure your answer is spelt correctly)");
            string userAnswer = Console.ReadLine();
            ;
            if ( userAnswer == card1Back)
            {
                Console.WriteLine("correct!");
                card1Score++;
            }
            else
            {
                Console.WriteLine("incorrect!");
                counter++;
            }
            Console.WriteLine ("you took " + counter +" times to do card");
        }
        
        //future goals : allow user to input as many cards as they want and when they have done a card correctly twice, it is removed from the deck, 
        //use a for loop for this and maybe condition controlled iteration

     // added counter and sample for decklength for loop
     // future goals: fix decklength and how to create more variables.
     
        //Console.WriteLine("how many flashcards do you want in your deck?");
        //int deckLength = Convert.ToInt32(Console.ReadLine());
        //for (int i = 1; i <= deckLength-1; i++)
        //{
        //  console.WriteLine ("enter front of flashcard " + i)
        //(not sure how to add a variable)
        
        //console.WriteLine ("enter back of flashcard " + i)
        //(not sure to add variable)
        //}
        

    }
}


![image](https://github.com/user-attachments/assets/307e0a5b-6ef5-4b00-a68f-61aeacf8b0b4)
