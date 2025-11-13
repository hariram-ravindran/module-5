# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>
int main() {
    int length, breadth, area;
    int *ptrLength, *ptrBreadth;
    printf("Enter the length of the rectangle: ");
    scanf("%d", &length);
    printf("Enter the breadth of the rectangle: ");
    scanf("%d", &breadth);
    ptrLength = &length;
    ptrBreadth = &breadth;
    area = (*ptrLength) * (*ptrBreadth);
    printf("Area of the rectangle = %d\n", area);
    return 0;
}
```
## OUTPUT
<img width="1394" height="451" alt="Screenshot 2025-10-21 170754" src="https://github.com/user-attachments/assets/09836ec8-ebce-412b-9985-f78a0258423a" />
		       	


## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
int main() {
    char *str;
    str = (char *)malloc(8 * sizeof(char)); 
    strcpy(str, "WELCOME");
    printf("The string is: %s\n", str);
    free(str);
    return 0;
}
```
## OUTPUT
<img width="1197" height="389" alt="Screenshot 2025-10-21 171029" src="https://github.com/user-attachments/assets/35b8db26-733e-4f29-9fbd-2096a959ae7a" />



## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
```
#include <stdio.h>
struct Student {
    char name[50];
    int rollNumber;
    float marks;
};
int main() {
    struct Student s;  
    printf("Enter student name: ");
    scanf("%s", s.name); 
    printf("Enter roll number: ");
    scanf("%d", &s.rollNumber);
    printf("Enter marks: ");
    scanf("%f", &s.marks);
    printf("Name       : %s\n", s.name);
    printf("Roll Number: %d\n", s.rollNumber);
    printf("Marks      : %.2f\n", s.marks);
    return 0; 
}
```

## OUTPUT

<img width="1382" height="600" alt="Screenshot 2025-10-21 171317" src="https://github.com/user-attachments/assets/515bb249-fbbe-430d-9afe-db647a58b216" />

## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>
struct Employee {
    char name[50];
    int id;
    float basicSalary;
    float hra;    
    float da;     
    float grossSalary;
};
int main() {
    struct Employee emp[3]; 
    for (int i = 0; i < 3; i++) {
        printf("Enter details for Employee %d:\n", i + 1);
        printf("Name: ");
        scanf("%s", emp[i].name);
        printf("ID: ");
        scanf("%d", &emp[i].id);
        printf("Basic Salary: ");
        scanf("%f", &emp[i].basicSalary);
        emp[i].hra = 0.20f * emp[i].basicSalary;
        emp[i].da = 0.80f * emp[i].basicSalary;
        emp[i].grossSalary = emp[i].basicSalary + emp[i].hra + emp[i].da;
    }
    printf("\n--- Employee Details ---\n");
    for (int i = 0; i < 3; i++) {
        printf("\nEmployee %d:\n", i + 1);
        printf("Name        : %s\n", emp[i].name);
        printf("ID          : %d\n", emp[i].id);
        printf("Basic Salary: %.2f\n", emp[i].basicSalary);
        printf("HRA         : %.2f\n", emp[i].hra);
        printf("DA          : %.2f\n", emp[i].da);
        printf("Gross Salary: %.2f\n", emp[i].grossSalary);
    }
    return 0; 
}



```

 ## OUTPUT

 <img width="1319" height="728" alt="Screenshot 2025-10-21 171805" src="https://github.com/user-attachments/assets/eb63483e-675f-4fe2-943c-21f2925f0396" />


## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM
```
#include <stdio.h>
struct student {
    char name[10];
    int rollno;
    int subject[5];
    int total;
    float average;
};
int main() {
    struct student s[2];  
    int i, j;
    for (i = 0; i < 2; i++) {
        printf("\nEnter details for Student %d:\n", i + 1);

        printf("Enter name: ");
        scanf("%s", s[i].name); 
        printf("Enter roll number: ");
        scanf("%d", &s[i].rollno);  
        printf("Enter marks for 5 subjects:\n");
        for (j = 0; j < 5; j++) {
            printf("Subject %d: ", j + 1);
            scanf("%d", &s[i].subject[j]);
        }
    }
    for (i = 0; i < 2; i++) {
        s[i].total = 0;
        for (j = 0; j < 5; j++) {
            s[i].total += s[i].subject[j];
        }
        s[i].average = s[i].total / 5.0;
    }
    printf("\n--- Student Results ---\n");
    for (i = 0; i < 2; i++) {
        printf("\nStudent %d: %s\n", i + 1, s[i].name);
        printf("Roll Number: %d\n", s[i].rollno);
        printf("Total Marks : %d\n", s[i].total);
        printf("Average     : %.2f\n", s[i].average);
    }
    return 0; 
}
```

## OUTPUT

 <img width="1489" height="671" alt="Screenshot 2025-10-21 172353" src="https://github.com/user-attachments/assets/0e5dab1e-77d2-4b32-848e-be6a19fb9225" />


## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	




