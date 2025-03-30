# Learning-Git
This is my first repository
<br>
Author-Sakshi gupta (coder)
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int user_choice, comp_choice;
    char *options[] = {"Rock", "Paper", "Scissors"};

    // Seed random number generator
    srand(time(0));

    printf("🔥 Rock, Paper, Scissors Game 🔥\n");
    printf("Choose: \n1. Rock\n2. Paper\n3. Scissors\n");
    printf("Enter your choice (1/2/3): ");
    scanf("%d", &user_choice);

    // Validate input
    if (user_choice < 1 || user_choice > 3) {
        printf("Invalid choice! Please choose 1, 2, or 3.\n");
        return 0;
    }

    // Computer's random choice
    comp_choice = rand() % 3 + 1;

    printf("\nYou chose: %s\n", options[user_choice - 1]);
    printf("Computer chose: %s\n", options[comp_choice - 1]);
// Determine the winner
    if (user_choice == comp_choice) {
        printf("😐 It's a Tie!\n");
    } else if ((user_choice == 1 && comp_choice == 3) ||
               (user_choice == 2 && comp_choice == 1) ||
               (user_choice == 3 && comp_choice == 2)) {
        printf("🎉 You Win!\n");
    } else {
        printf("💀 You Lose!\n");
    }

    return 0;
}
