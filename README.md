# Game-in-C
In this game player need to guess the number between 1 to 100 if player guesses a or higher number it gets a hint for lower number please and same for higher number. When player guess the right number program displays "You guessed it it n(number of attempts) attempts.
#include<stdio.h>
#include<stdlib.h>
#include<time.h>

int main(){
    int number, guess, nguess=1;
    srand(time(0));
    number = rand()%100 +1;
    
   // printf("The number is %d\n", number);
    

    do
    {
        printf("Guess the number between 1 to 100\n");
        scanf("%d", &guess);
        if (guess>number)
        {
            printf("Lower number please!\n");
        }
        else if
            (guess<number)
        {
            printf("Higher number please!\n");
        }
        else{
            printf("You guessed it in %d attempts\n", nguess);

        }
        nguess++;
    } while (guess!=number);
    

    return 0;
}
