#include <stdio.h>
int main() {
    double num1, num2;
    char operator;
    printf("Enter an expression : ");
    scanf("%If %c %If", &num1, &operator, &num2);
    switch (operator) {
        case '+':
            printf("%.2If + %.2lf = %.2lf\n", num1, num2, num1 + num2);
            break;
        case '-':
            printf("%.2lf - %.2lf = %.2lf\n", num1, num2, num1 - num2);
            break;
        case '*':
            printf("%.2lf * %.2lf = %.2lf\n", num1, num2, num1 * num2);
            break;
        case '/':
            if (num2 != 0)
                printf("%.2lf / %.2lf = %.2lf\n", num1, num2, num1 / num2);
            else
                printf("Error: Division by zero is not allowed.\n");
            break;
        default:
            printf("Error: Invalid operator.\n");
    }
    return 0;
}
