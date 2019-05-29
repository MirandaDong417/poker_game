# poker_game

## by Xujia Dong (Miranda)
### May 29, 2019

I created the game using a function called `game`. It takes in an argument of the number of players, asks for each player's name, and prints out each player's hand, as well as the name of the winner.

Here are my approaches:

0. Import `random` and `sys` modules.

1. Assign the variable `names` to a list of the all players' names through a list comprehension and `input()` method.

2. Create a list `cards` which contains all of the possible cards in the game.

3. Create a dictionary `dictstring` to store 5 randomly chosen cards for each player. Each key is a player's name as a string. Each value is the player's hand represented as a list of of 5 strings. Print out each player's name and their hands.

4. Create a dictionary `values` that store the cards and their values. Each key is a card as a string. Each value is the card's value as an integer. 

5. Create a dictionary `dictvalue`. Use dictionary's `get()` method to convert the values in `dictstring` from lists of unsorted strings to lists of sorted integers (in descending order).

6. Create an empty dictionary `compare`. Create a for loop that loops through the key-value pairs in `dictvalue`. The `if not compare:` clause will store the first player's name and hand in `dictvalue` into `compare`. Then the for loop will loop to the second player's name and hand and compare its largest (first) card with the first player's largest (first) card. The inner for loop will loop through two players' hand. If their two largest cards are the same, the `continue` statement will bring it back to the start of the inner loop and compare their second largest cards. So on and so forth, until the one of the player's card is larger than the other one's. Then compare dictionary will be reassigned to the key-value pair of the player who has larger hand. Then the outer for loop will loop to the next player.

7. After the for loop is over, the `compare` dictionary should contain the key-value pair of the player who has the winning hand. Print out `compare`'s key (winner's name).

8. Assign `number_of_players` to `int(sys.argv[1])`, which will convert the input (number of players) through the command line into an integer. Call on the `game` function using `number_of_players`.



