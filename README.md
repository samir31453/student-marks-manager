# student-marks-manager
#include <stdio.h>
#include <string.h>

struct Student {
    char name[50];
    float marks[5];
    float average;
};

int main() {
    int n;
    printf("Enter number of students: ");
    scanf("%d", &n);

    struct Student s[n];

    for(int i = 0; i < n; i++) {
        printf("\nEnter name of student %d: ", i+1);
        scanf("%s", s[i].name);

        printf("Enter 5 subject marks: ");
        float sum = 0;
        for(int j = 0; j < 5; j++) {
            scanf("%f", &s[i].marks[j]);
            sum += s[i].marks[j];
        }

        s[i].average = sum / 5;
    }

    printf("\n--- Student Report ---\n");
    for(int i = 0; i < n; i++) {
        printf("\nName: %s\n", s[i].name);
        printf("Average Marks: %.2f\n", s[i].average);
    }

    return 0;
}
Student Marks Manager (C Program)

This program is written in C and helps manage basic student data. It takes the name and marks of students and calculates their average marks based on 5 subjects.

---

📌 Features

- Accepts input for multiple students
- Stores student data using "struct"
- Takes marks for 5 subjects
- Calculates average marks for each student
- Displays a simple student report

---

🧾 How the Program Works

1. The user enters the number of students.
2. For each student:
   - Enter the name
   - Enter 5 subject marks
3. The program calculates "average = sum / 5".
4. Finally, it prints the name and average marks of each student.

---

💻 Sample Output

Enter number of students: 2

Enter name of student 1: Ravi
Enter 5 subject marks: 70 80 75 85 90

Enter name of student 2: Anita
Enter 5 subject marks: 60 65 70 75 80

--- Student Report ---

Name: Ravi
Average Marks: 80.00

Name: Anita
Average Marks: 70.00

---

🔧 How to Run

1. Save the code as:
"student_marks_manager.c"

2. Compile the program using:
"gcc student_marks_manager.c -o student"

3. Run the program:
"./student"

---

📚 Concepts Used

- "struct" in C
- Arrays
- For loops
- Input/Output functions ("scanf", "printf")
- Basic calculations
