#include <stdio.h>

#define MAX_ATTEMPTS 3

int main() {
    int balance = 0;
    int pin = 0;
    int attempts = 0;
    int first_time = 1;

    printf("Welcome to ATM Simulator!\n");

    if (first_time) {
        printf("This is your first time using the ATM. Please set your 4-digit PIN: ");
        scanf("%d", &pin);
        first_time = 0;
    }

    while (attempts < MAX_ATTEMPTS) {
        int pin1;
        printf("Enter your 4-digit PIN: ");
        scanf("%d", &pin1);

        if (pin1 == pin) {
            break;
        } else {
            printf("Invalid PIN. Try again.\n");
            attempts++;
        }
    }

    if (attempts == MAX_ATTEMPTS) {
        printf("Maximum attempts reached. Account locked.\n");
        return 0;
    }

    while (1) {
        printf("\nATM Menu:\n");
        printf("1. Check Balance\n");
        printf("2. Withdraw Cash\n");
        printf("3. Deposit Cash\n");
        printf("4. Change PIN\n");
        printf("5. Exit\n");

        int choice, damount, wamount;
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                printf("Your current balance is: %d\n", balance);
                break;
            case 2:
                printf("Enter amount to withdraw: ");
                scanf("%d", &wamount);

                int pin1;
                printf("Enter your 4-digit PIN: ");
                scanf("%d", &pin1);

                if (pin1 != pin) {
                    printf("Invalid UPI PIN. Withdrawal failed.\n");
                } else if (wamount > balance) {
                    printf("Insufficient balance.\n");
                } else {
                    balance -= wamount;
                    printf("Withdrawal successful. New balance: %d\n", balance);
                }
                break;
            case 3:
                printf("Enter amount to deposit: ");
                scanf("%d", &damount);

                balance += damount;
                printf("Deposit successful. New balance: %d\n", balance);
                break;
            case 4:
                printf("Enter your old PIN: ");
                int pin3;
                scanf("%d", &pin3);

                if (pin3 == pin) {
                    printf("Enter your new PIN: ");
                    scanf("%d", &pin);
                    printf("PIN changed successfully.\n");
                } else {
                    printf("Invalid old PIN. PIN not changed.\n");
                }
                break;
            case 5:
                printf("Exiting ATM Simulator.\n");
                return 0;
            default:
                printf("Invalid choice. Try again.\n");
        }
    }

    return 0;
}
