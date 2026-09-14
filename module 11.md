

EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
Aim:
To write a C program to create a function to find the greatest number

Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
Program:
```
#include <stdio.h>

int max(int x, int y) {
    return (x > y) ? x : y;
}
int max_of_four(int a, int b, int c, int d) {
    return max(max(a, b), max(c, d));
}

int main() {
    int a, b, c, d;

    scanf("%d", &a);
    scanf("%d", &b);
    scanf("%d", &c);
    scanf("%d", &d);

    printf("%d\n", max_of_four(a, b, c, d));

    return 0;
}
```
Output:
<img width="367" height="301" alt="image" src="https://github.com/user-attachments/assets/f9054ea3-596c-41a1-8b2a-b81dde6ae701" />

Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
Program:
```
#include <stdio.h>

void calculate_the_maximum(int n, int k) {
    int max_and = 0, max_or = 0, max_xor = 0;

    for (int i = 1; i <= n; i++) {
        for (int j = i + 1; j <= n; j++) {
            int and_val = i & j;
            int or_val  = i | j;
            int xor_val = i ^ j;

            if (and_val < k && and_val > max_and)
                max_and = and_val;

            if (or_val < k && or_val > max_or)
                max_or = or_val;

            if (xor_val < k && xor_val > max_xor)
                max_xor = xor_val;
        }
    }

    printf("%d\n%d\n%d\n", max_and, max_or, max_xor);
}

int main() {
    int n, k;
    scanf("%d %d", &n, &k);

    calculate_the_maximum(n, k);

    return 0;
}
```
Output:
<img width="452" height="325" alt="image" src="https://github.com/user-attachments/assets/d93dff5b-cd98-4635-8d41-1a1b7dbc2221" />

Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
Aim:
To write a C program to write the logic for the requests

Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
Program:
```
#include <stdio.h>
#include <stdlib.h>

int main() {
    int total_number_of_shelves;
    scanf("%d", &total_number_of_shelves);

    int total_number_of_queries;
    scanf("%d", &total_number_of_queries);

    int **total_number_of_pages = malloc(total_number_of_shelves * sizeof(int *));
    int *total_number_of_books = malloc(total_number_of_shelves * sizeof(int));

    for (int i = 0; i < total_number_of_shelves; i++) {
        total_number_of_pages[i] = malloc(1100 * sizeof(int)); // max books per shelf
        total_number_of_books[i] = 0;
    }

    while (total_number_of_queries--) {
        int type_of_query;
        scanf("%d", &type_of_query);

        if (type_of_query == 1) {
            int x, y;
            scanf("%d %d", &x, &y);
            total_number_of_pages[x][total_number_of_books[x]] = y;
            total_number_of_books[x]++;
        } else if (type_of_query == 2) {
            int x, y;
            scanf("%d %d", &x, &y);
            printf("%d\n", total_number_of_pages[x][y]);
        } else {
            int x;
            scanf("%d", &x);
            printf("%d\n", total_number_of_books[x]);
        }
    }

    for (int i = 0; i < total_number_of_shelves; i++) {
        free(total_number_of_pages[i]);
    }
    free(total_number_of_pages);
    free(total_number_of_books);

    return 0;
}
```
Output:
<img width="295" height="252" alt="image" src="https://github.com/user-attachments/assets/2631437b-2cc1-4c13-802f-ecea6a915311" />


Result:
Thus, the program to write the logic for the requests is verified successfully.


 
EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
Aim:
To write a C program print the sum of the integers in the array.

Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



Program:
```
#include<stdio.h>
int main()
{
    int n,sum=0;
    scanf("%d",&n);
    int arr[n];
    for(int i=0;i<n;i++){
        scanf("%d",&arr[i]);
        sum+=arr[i];
    }
    printf("%d",sum);
    return 0;
}
```
Output:
<img width="190" height="212" alt="image" src="https://github.com/user-attachments/assets/516058a0-68a6-4ed5-8744-87fc634b3555" />

 


Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A      SENTENCE



Aim:

To write a C program that counts the number of words in a given sentence.

Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



Program:
```
#include <stdio.h>
#include <ctype.h>

int main() {
    char str[200];
    int i, count = 0;
    int inWord = 0; // flag to track if we are inside a word

    // Input the sentence
    printf("Enter a sentence:\n");
    fgets(str, sizeof(str), stdin);

    // Process each character
    for (i = 0; str[i] != '\0'; i++) {
        if (isspace(str[i]) || ispunct(str[i])) {
            // If current character is space or punctuation, end of a word
            inWord = 0;
        } else {
            // If current character is part of a word
            if (inWord == 0) {
                count++;     // new word starts
                inWord = 1;  // set flag
            }
        }
    }

    // Display result
    printf("Total number of words in the string is : %d\n", count);

    return 0;
}
```
Input:
```
I do C Programming
```
Output:
```
Total number of words in the string is : 4
```


Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
