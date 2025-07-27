#include <stdio.h>
#include <math.h>

int main(void)
{
    float coin;
    do {
        printf("Enter amount in dollars: ");
        scanf("%f", &coin);
    } while (coin < 0);

    int cents = round(coin * 100);

    int coins25 = cents / 25;
    cents %= 25;

    int coins10 = cents / 10;
    cents %= 10;

    int coins5 = cents / 5;
    cents %= 5;

    int coins1 = cents / 1;
    cents %= 1;

    int totalCoins = coins25 + coins10 + coins5 + coins1;

    printf("Total coins: %d\n", totalCoins);
    return 0;
}
