# Rock-Paper-Scissors game with C++

## What will we need?

1. Import necessary library for input and output and use namespace std
   
   ```cpp
   #include <iostream>
   #include <string>
   using namespace std;
   ```

2. Create two strings, one for player and one for computer
   
   ```cpp
   string computer;
   string player;
   ```

3. Create a function to random and return computer's choice
   
   ```cpp
   void computer_choice(){
       srand(time(NULL));
       int random = rand() % 3 + 1;
       switch (random)
       {
       case 1:
           computer = "Rock";
           break;
       case 2:
           computer = "Paper";
           break;
       case 3:
           computer = "Scissors";
           break;
       }
   }
   ```

4. Create a function to get user input and find the winner with if-else statement 
   
   ```cpp
   void find_winner(){
           cout << "Enter your choice: (Rock, Paper, Scissors)" << endl;
       cin >> player;
   
       cout << "====================" << endl;
       cout << "You chose: " << player << endl;
       cout << "Computer chose: " << computer << endl;
       cout << "====================" << endl;
   
       cout << "\n----------------------------\n";
   
       if (player == "Rock" && computer == "Paper")
       {
           cout << "You lose!";
       }
       else if (player == "Rock" && computer == "Scissors")
       {
           cout << "You win!";
       }
       else if (player == "Rock" && computer == "Rock")
       {
           cout << "It's a tie!";
       }
   
       if (player == "Paper" && computer == "Rock")
       {
           cout << "You win!";
       }
       else if (player == "Paper" && computer == "Scissors")
       {
           cout << "You lose!";
       }
       else if (player == "Paper" && computer == "Paper")
       {
           cout << "It's a tie!";
       }
       if (player == "Scissors" && computer == "Scissors")
       {
           cout << "It's a tie!";
       }
       else if (player == "Scissors" && computer == "Paper")
       {
           cout << "You win!";
       }
       else if (player == "Scissors" && computer == "Rock")
       {
           cout << "You lose!";
       }
   
       cout << "\n----------------------------\n";
   }
   ```

5. Create main function and call the two functions just written
   
   ```cpp
   int main()
   {
       computer_choice();
       find_winner();
   
   }
   ```
