# Students-database-
#include <stdio.h>

struct student {
    int roll_no;
    char name[50];
    char area[50];
};

int main() {
    struct student student1[100];
    int n, i, j, found = 0;

    printf("enter no.of students in class:");
    scanf("%d", &n);

    for (i = 0; i < n; i++) {
        printf("name of student:");
        scanf("%s", student1[i].name);

        printf("roll no of student:");
        scanf("%d", &student1[i].roll_no);

        printf("area from where he belong:");
        scanf("%s", student1[i].area);

        printf("\n");
    }

    printf("---------------------\n");
    printf("\nenter roll no of student:");
    scanf("%d", &j);

    for (i = 0; i < n; i++) {
        if (j == student1[i].roll_no) {
            printf("student name is %s\n", student1[i].name);
            printf("student belongs to %s\n", student1[i].area);
            found = 1;
            break;
        }
    }

    if (!found) {
        printf("student does not exist in database");
    }

    return 0;
}
