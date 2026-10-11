#include <stdio.h>
int main(void) {
    double price, discount, netPrice;
    printf("Enter product price: ");
    scanf("%lf", &price);
    if (price < 0) {
        printf("Invalid price\n");
        return 1;
    }
    if (price >= 5000) {
        discount = 0.20;
    } else if (price >= 3000) {
        discount = 0.15;
    } else if (price >= 1000) {
        discount = 0.10;
    } else {
        discount = 0.00;
    }
    netPrice = price - (price * discount);
    printf("Original price: %.2f baht\n", price);
    printf("Discount: %.0f%%\n", discount * 100);
    printf("Net price: %.2f baht\n", netPrice);
    return 0;
}
