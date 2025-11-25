#include <stdio.h>
#include <stdlib.h>
#include <time.h>
#include <unistd.h>

int main()
{
    char choice;
    srand(time(NULL));

    printf("Welcome to dice roller\n");
    do
    {
        int dice = rand() % 6 + 1;
        printf("You rolled%d\n", dice);
        sleep(3);

        printf("Roll again?\n'yes'\n'no'\n");
        scanf(" %c", &choice);
    }
    while (choice == 'Y' || choice == 'y');

    printf("Thanks for playing!\n");
