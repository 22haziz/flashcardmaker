# //flashcard maker program
        //OLD TEST PROGRAM:
        //need to enter at least 3 (program will ask user how many cards they want to make)
        //a random flashcard will be chosen from the selection the user has inputted
        //the user has to get each flashcard correct twice to finish
 
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



        // multiple card deck code 
        // criteria: user enters how many cards they want in deck, a card will be randomly chosen, when they answer it right its value goes up by 1 (this is recorded by the array card value),
        // a second card will then be generated, when a card's value becomes 2 this is recorded by the array, random generator choses another card, 
        //if a card generated already has2 value, another card will be generated until all cards have a value of 2

         //creating deck + cardValue array

    Console.WriteLine("how many flashcards do you want in your deck? (must be more than 1)");
    int deckLength = Convert.ToInt32(Console.ReadLine());
    string[] deckFront = new string[deckLength];
    string[] deckBack = new string[deckLength];
    int[] cardValue = new int [deckLength ];
    for (int a = 0; a <= deckLength-1 ; a++)
    {
        cardValue[a] = 0;
        //makes sure all index in cardValue start at 0
    }


    int counter = 0;
    
    Random number = new Random();
    int random = number.Next(0, deckLength);

    // creating back and front of each card
    
    for (int i = 0; i <= deckLength - 1; i++)
    {
        Console.WriteLine("enter front of flashcard " + (i + 1));
        deckFront[i] = Console.ReadLine();

        Console.WriteLine("enter back of flashcard " + (i + 1));
        deckBack[i] = Console.ReadLine();
    }

    bool correct = false;
    //picks random front of card with generator

    
    //loop 
    
    for (int j = 0; j <= deckLength*2; j++) //*2 as you need to do each card twice
    {
        random = number.Next(0, deckLength);
        
        while (cardValue[random] == 2) //makes sure tthe card chosen hasnt been done before
        {
            random = number.Next(0, deckLength);
            
        }
        
         while (correct == false)
        {

            Console.WriteLine("card:" + (random+1));
                Console.WriteLine(deckFront[random] +  " (make sure your answer is spelt correctly)");
            
                string userAnswer = Console.ReadLine();

                if (userAnswer == deckBack[random]) 
                {
                    Console.WriteLine("correct!");
                    counter++;
                    correct = true;

                }
                else 
                {
                    Console.WriteLine("incorrect answer!");
                    counter++;
                    correct = false;
                }
        }      

     
        

        Console.WriteLine("you took " + counter + " times to do this card");

        cardValue[random]++;
        Console.WriteLine("you have done this card correct" + cardValue[random] + " times");

        correct = false;
        counter = 0;//reassigns variables to 0 and false for next card
    }
        
    }

}
    



![image](https://github.com/user-attachments/assets/3a65e75c-1d8d-4803-bc0a-727e13ac2b30)
![image](https://github.com/user-attachments/assets/4da7b19a-b956-4fa1-b70b-ceba61401d7e)


![image](https://github.com/user-attachments/assets/db691441-e728-4668-9eff-c67e6d60302a)
![image](https://github.com/user-attachments/assets/4c827915-16f7-4e93-8d6a-1d6f7b73f070)
