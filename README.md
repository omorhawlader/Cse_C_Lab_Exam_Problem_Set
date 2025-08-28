omar ~

# C Programming Problem Set (Menu Driven)

This program contains **17 small problems** solved using functions in C.  
The user can choose a problem from the menu, and the corresponding function runs.

---

## Full Code

```c
#include <stdio.h>

// Function for each problem
void waterBottle() {
    int X, Y;
    scanf("%d %d", &X, &Y);
    printf("Remaining: %d\n", X - Y);
}

void examResult() {
    int M;
    scanf("%d", &M);
    if (M >= 40) printf("Pass\n");
    else printf("Fail\n");
}

void evenOdd() {
    int N;
    scanf("%d", &N);
    if (N % 2 == 0) printf("Even\n");
    else printf("Odd\n");
}

void largestTwo() {
    int A, B;
    scanf("%d %d", &A, &B);
    if (A > B) printf("%d\n", A);
    else printf("%d\n", B);
}

void gradeStudent() {
    int M;
    scanf("%d", &M);
    if (M >= 80) printf("A\n");
    else if (M >= 60) printf("B\n");
    else if (M >= 40) printf("C\n");
    else printf("F\n");
}

void reverseNumber() {
    int N, rev = 0;
    scanf("%d", &N);
    while (N > 0) {
        rev = rev * 10 + N % 10;
        N /= 10;
    }
    printf("%d\n", rev);
}

void sumDigits() {
    int N, sum = 0;
    scanf("%d", &N);
    while (N > 0) {
        sum += N % 10;
        N /= 10;
    }
    printf("%d\n", sum);
}

void factorialFinder() {
    int N, fact = 1;
    scanf("%d", &N);
    for (int i = 1; i <= N; i++) fact *= i;
    printf("%d\n", fact);
}

void fibonacciSeries() {
    int N, a = 0, b = 1, next;
    scanf("%d", &N);
    for (int i = 1; i <= N; i++) {
        printf("%d ", a);
        next = a + b;
        a = b;
        b = next;
    }
    printf("\n");
}

void multiplicationTable() {
    int N;
    scanf("%d", &N);
    for (int i = 1; i <= 10; i++) {
        printf("%d x %d = %d\n", N, i, N * i);
    }
}

void smallestThree() {
    int a, b, c;
    scanf("%d %d %d", &a, &b, &c);
    int min = a;
    if (b < min) min = b;
    if (c < min) min = c;
    printf("%d\n", min);
}

void sumFirstN() {
    int N;
    scanf("%d", &N);
    int sum = N * (N + 1) / 2;
    printf("%d\n", sum);
}

void luckyTicket() {
    int num;
    scanf("%d", &num);
    int d1 = num / 1000;
    int d2 = (num / 100) % 10;
    int d3 = (num / 10) % 10;
    int d4 = num % 10;
    if (d1 + d2 == d3 + d4) printf("Lucky\n");
    else printf("Unlucky\n");
}

void palindromeCheck() {
    int N, temp, rev = 0;
    scanf("%d", &N);
    temp = N;
    while (temp > 0) {
        rev = rev * 10 + temp % 10;
        temp /= 10;
    }
    if (rev == N) printf("Palindrome\n");
    else printf("Not Palindrome\n");
}

void countDigits() {
    int N, count = 0;
    scanf("%d", &N);
    if (N == 0) count = 1;
    else {
        while (N > 0) {
            count++;
            N /= 10;
        }
    }
    printf("%d\n", count);
}

void powerNumber() {
    int a, b, res = 1;
    scanf("%d %d", &a, &b);
    for (int i = 1; i <= b; i++) res *= a;
    printf("%d\n", res);
}

void oddNumbersRange() {
    int N;
    scanf("%d", &N);
    for (int i = 1; i <= N; i += 2) {
        printf("%d ", i);
    }
    printf("\n");
}

// Main menu
int main() {
    int choice;
    printf("Choose a problem (1-17):\n");
    printf("1. Water Bottle Refill\n");
    printf("2. Exam Pass/Fail\n");
    printf("3. Even or Odd Toy\n");
    printf("4. Largest of Two Numbers\n");
    printf("5. Grade of Student\n");
    printf("6. Reverse a Number\n");
    printf("7. Sum of Digits\n");
    printf("8. Factorial Finder\n");
    printf("9. Fibonacci Series\n");
    printf("10. Multiplication Table\n");
    printf("11. Smallest of Three Numbers\n");
    printf("12. Sum of First N Numbers\n");
    printf("13. Lucky Ticket\n");
    printf("14. Palindrome Number\n");
    printf("15. Count Digits\n");
    printf("16. Power of a Number\n");
    printf("17. Odd Numbers in Range\n");

    scanf("%d", &choice);

    switch (choice) {
        case 1: waterBottle(); break;
        case 2: examResult(); break;
        case 3: evenOdd(); break;
        case 4: largestTwo(); break;
        case 5: gradeStudent(); break;
        case 6: reverseNumber(); break;
        case 7: sumDigits(); break;
        case 8: factorialFinder(); break;
        case 9: fibonacciSeries(); break;
        case 10: multiplicationTable(); break;
        case 11: smallestThree(); break;
        case 12: sumFirstN(); break;
        case 13: luckyTicket(); break;
        case 14: palindromeCheck(); break;
        case 15: countDigits(); break;
        case 16: powerNumber(); break;
        case 17: oddNumbersRange(); break;
        default: printf("Invalid choice!\n");
    }

    return 0;
}
