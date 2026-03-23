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

struct eligible {
    char name[50];
    int age;
};

int main() {
    struct eligible e[10];
    int n, i;

    printf("Enter number of persons: ");
    scanf("%d", &n);

    for (i = 0; i < n; i++) {
        printf("\nEnter name: ");
        scanf("%s", e[i].name);

        printf("Enter age: ");
        scanf("%d", &e[i].age);
    }

    printf("\n--- Vaccine Eligibility Details ---\n");

    for (i = 0; i < n; i++) {
        printf("\nName: %s", e[i].name);
        printf("\nAge: %d", e[i].age);

        if (e[i].age > 6) {
            printf("\nVaccine Eligibility: Yes\n");
        } else {
            printf("\nVaccine Eligibility: No\n");
        }
    }

    return 0;
}
```


Output:

<img width="414" height="459" alt="image" src="https://github.com/user-attachments/assets/779da1d1-df50-4f93-9686-f639350e21d4" />


Result:
Thus, the program is verified successfully.
