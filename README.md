#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main ( int argc, char** argv )
{
    int MysteryNumber = 0, ChosenNumber = 0;
    const int MAX = 100, MIN = 1;

    signed char Try=0;
    int KeepPlaying=1;




    do
    {


    // random number being chosed

    srand(time(NULL));
    ChosenNumber = (rand() % (MAX - MIN + 1)) + MIN;

    /* The programs loop which repeats itself as long as the number is not found */

    do
    {
        // We ask to guess the number

        Try++;

        printf("What is the number ? ");
        scanf("%d", &ChosenNumber);

        // We compare the chosen number with the mystery number

        if (MysteryNumber > ChosenNumber)


            printf("It's More !\n\n");



        else if (MysteryNumber < ChosenNumber)


         printf("It's Less !\n\n");





        else

            printf ("Bravo, you found the mystery number !!! in %d Trys \n\n", Try);




    } while (ChosenNumber != MysteryNumber);


    } while (KeepPlaying);

    return 0;
}
