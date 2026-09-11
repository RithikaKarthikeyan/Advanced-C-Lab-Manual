EXP NO:1 C PROGRAM FOR ARRAY OF STRUCTURE TO CHECK ELIGIBILITY FOR THE VACCINE.

Aim:
To write a C program for array of structure to check eligibility for the vaccine person age above 6 years of age.

Algorithm:
1.	Declare structure eligible with age (integer) and n (character array)
2.	Declare variable e of type eligible
3.	Input age and name using scanf, store in e
4.	If e.age <= 6
-	Print "Vaccine Eligibility: No"
Else
-	Print "Vaccine Eligibility: Yes"
5.	Print details (e.age, e.n)
6.	Return 0
 
Program:
```
#include <stdio.h>
#include <string.h>

struct Person {
    int age;
    char name[50];
};

int main() {
    int  i;
    struct Person people[1]; 

    for (i = 0; i < 1; i++) {
        scanf("%d", &people[i].age);
        scanf("%s", people[i].name);
        printf("Age:%d\n", people[i].age);
        printf("Name:%s", people[i].name);
        printf("vaccine:%d\n", people[i].age);

        if (people[i].age > 18) {
            printf("eligibility:yes\n");
        } else {
            printf("eligibility:no\n");
        }
    }

    return 0;
}
```

Output:
<img width="612" height="210" alt="image" src="https://github.com/user-attachments/assets/83efdfea-118a-4805-bd04-4be7a1d60d93" />


Result:
Thus, the program is verified successfully. 



EXP NO:2 C PROGRAM FOR PASSING STRUCTURES AS FUNCTION ARGUMENTS AND RETURNING A STRUCTURE FROM A FUNCTION
Aim:
To write a C program for passing structure as function and returning a structure from a function

Algorithm:
1.	Define structure numbers with members a and b.
2.	Declare variable n of type numbers.
3.	Prompt the user to enter values for a and b.
4.	Input values for a and b into n using scanf.
5.	Call the add function with n as an argument.
6.	Print the result returned by the add function.
7.	Return 0
 
Program:

```
#include <stdio.h>
struct numbers {
    int a;
    int b;
};
struct numbers add(struct numbers n) {
    struct numbers result;
    result.a = n.a + 10;   
    result.b = n.b + 20;   
    return result;
}

int main() {
    struct numbers n, res;

    printf("Enter values for a and b:\n");
    scanf("%d", &n.a);
    scanf("%d", &n.b);

    res = add(n);

    printf("Result a: %d\n", res.a);
    printf("Result b: %d\n", res.b);

    return 0;
}
```



Output:

<img width="682" height="257" alt="image" src="https://github.com/user-attachments/assets/fd163e0c-770e-4862-998f-f71e88dad4f1" />




Result:
Thus, the program is verified successfully


 
EXP.NO:3 C PROGRAM TO READ A FILE NAME FROM USER AND WRITE THAT FILE USING FOPEN()

Aim:
To write a C program to read a file name from user

Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare a character array name to store the file name.
4.	Prompt the user to enter a file name.
Use scanf to input the file name into the name array.
5.	Print a message indicating that the file with the specified name has been created successfully.
6.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
1.	Print a message indicating that the file has been opened successfully.
2.	Use fclose to close the file.
3.	Print a message indicating that the file has been closed.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
Program:

```
#include <stdio.h>

int main()
{
    FILE *fp;
    char filename[100];

    // Read file name
    scanf("%s", filename);

    // Create and open file
    fp = fopen(filename, "w");

    if(fp != NULL)
    {
        printf("%s File Created Successfully\n", filename);
        printf("%s File Opened\n", filename);

        // Close file
        fclose(fp);

        printf("%s File Closed", filename);
    }
    else
    {
        printf("File cannot be created");
    }

    return 0;
}
```



Output:

<img width="1001" height="396" alt="image" src="https://github.com/user-attachments/assets/d02e3b20-8758-4280-98b0-b97c005c3b48" />

Result:
Thus, the program is verified successfully
 


EXP NO:4   PROGRAM TO READ A FILE NAME FROM USER, WRITE THAT FILE AND INSERT TEXT IN TO THAT FILE
Aim:
To write a C program to read, a file and insert text in that file
Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare character arrays name and text. Declare an integer variable num.
4.	Prompt the user to enter a file name and the number of strings.
Use scanf to input the file name into the name array and the number of strings into the num variable.
5.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
6.	Print a message indicating that the file has been opened successfully.
1.	Use a loop to input strings from the user and write them to the file using fputs.
2.	Use fclose to close the file.
3.	Print a message indicating that data has been added successfully.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
Program:

```
#include <stdio.h>

int main()
{
    FILE *fp;
    char filename[100];
    char name[100];
    int roll, n, i;
    float percentage;

    // Read file name
    scanf("%s", filename);

    // Open file
    fp = fopen(filename, "w");

    if(fp != NULL)
    {
        printf("%s Opened\n", filename);

        // Read number of students
        scanf("%d", &n);

        // Read and write student details
        for(i = 0; i < n; i++)
        {
            scanf("%d %s %f", &roll, name, &percentage);

            fprintf(fp, "%d %s %.2f\n", roll, name, percentage);
        }

        printf("Data added Successfully");

        // Close file
        fclose(fp);
    }
    else
    {
        printf("File cannot be opened");
    }

    return 0;
}
```



Output:


<img width="702" height="372" alt="image" src="https://github.com/user-attachments/assets/85101f72-2d90-4a3c-a6cb-d1a04f825f6a" />



Result:
Thus, the program is verified successfully



Ex No 5 : C PROGRAM TO DISPLAY STUDENT DETAILS USING STRUCTURE

Aim:
The aim of this program is to dynamically allocate memory to store information about multiple subjects (name and marks), input the details for each subject, and then display the stored information. Finally, it frees the allocated memory to prevent memory leaks.

Algorithm:
1.Input the number of subjects.

2.Read the integer value n from the user, which represents the number of subjects.

3.Dynamically allocate memory:

4.Use malloc to allocate memory for n subjects. Each subject has a name (array of characters) and marks (integer).

5.If memory allocation fails (i.e., the pointer s is NULL), display an error message and exit the program.

6.Input the details of each subject

7.Use a for loop to read the name and marks of each subject using scanf. For each subject, store the name as a string and marks as an integer in the dynamically allocated memory.

8.Display the details of each subject

9.Use another for loop to print the name and marks of each subject.

10.Free the allocated memory

11.After all operations are done, call free(s) to release the dynamically allocated memory.

12.Return from the main function

13.End the program by returning 0.

Program:
```
#include <stdio.h>
#include <stdlib.h>
struct Subject {
    char name[50];   
    int marks;       
};

int main() {
    int n;
    struct Subject *s;

    printf("Enter number of subjects: ");
    scanf("%d", &n);

    s = (struct Subject *)malloc(n * sizeof(struct Subject));

    if (s == NULL) {
        printf("Memory allocation failed!\n");
        return 1;
    }

    for (int i = 0; i < n; i++) {
        printf("Enter subject name: ");
        scanf("%s", s[i].name);
        printf("Enter marks: ");
        scanf("%d", &s[i].marks);
    }

    printf("\nStored Information:\n");
    for (int i = 0; i < n; i++) {
        printf("%s  %d\n", s[i].name, s[i].marks);
    }

    free(s);
    return 0;
}
```



Output:


<img width="580" height="346" alt="image" src="https://github.com/user-attachments/assets/0626732e-3268-4b39-9fc0-4ab10b5c4332" />



Result:
Thus, the program is verified successfully
