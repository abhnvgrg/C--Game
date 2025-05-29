# C--Game
(i) Number Guessing Game

#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    // Seed the random number generator with current time
    srand(time(0));

    // Generate a random number between 1 and 100
    int randomNumber = (rand() % 100) + 1;
    int number_of_guesses= 0;
    int guessed;
    // Display the result
    // printf("Random number between 1 and 100: %d\n", randomNumber);
    do{
    printf("Guess the number: ");
    scanf("%d", &guessed);
    if (guessed<randomNumber)
    {
        printf("Guess higher\n");
    }
    else if (guessed>randomNumber)
    {
        printf("Guess lower\n");
    }
    number_of_guesses++;
    }
    while (guessed!= randomNumber);

    printf("You guessed the numbmer in %d attempts.\n", number_of_guesses);
    
    return 0;
}
