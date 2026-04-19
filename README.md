# telephone-contact-list-management-system-project
A small C program made in turco C++  where user can add a new contact, delete any contact, move back and forth in the complete list, search and update

 INTRODUCTION

A Telephone Contact List Management System is used to store and manage contact details such as names and phone numbers. This project is developed using C Language.
It helps users manage their contacts digitally rather than writing them manually. The program allows users to add, delete, search, update, and display contacts easily.
This system works through a menu-driven interface where users select operations according to their needs.
________________________________________
PROBLEM STATEMENT

Managing telephone contacts manually in notebooks can be difficult and time-consuming. It becomes hard to search, update, or delete contacts quickly.
Therefore, there is a need to create a Telephone Contact List where users can:
•	Add new contacts 
•	Delete contacts 
•	Search contacts 
•	Update contact details 
•	Move forward and backward through the list 
•	Display all contacts 
The goal of this project is to design a simple contact management system using C Language.
 OBJECTIVES
The objectives of this project are:
•	To create a contact list system 
•	To store contact names and phone numbers 
•	To add new contacts 
•	To delete unwanted contacts 
•	To search contacts quickly 
•	To update existing contacts 
•	To display all saved contacts 
•	To navigate through contacts 
________________________________________
 SOLUTION FLOW
The working steps of the system are:
1.	Start the program 
2.	Display menu options 
3.	User selects operation 
4.	Perform selected task: 
o	Add contact 
o	Delete contact 
o	Search contact 
o	Update contact 
o	Display contacts 
5.	Return to menu 
6.	Exit program 
________________________________________
 ALGORITHM
Algorithm for Telephone Contact List
1.	Start 
2.	Declare arrays for storing names and phone numbers 
3.	Display menu 
4.	Take user choice 
5.	If choice = 1 → Add contact 
6.	If choice = 2 → Delete contact 
7.	If choice = 3 → Search contact 
8.	If choice = 4 → Update contact 
9.	If choice = 5 → Display contacts 
10.	If choice = 6 → Exit 
11.	Stop 
________________________________________
 FLOWCHART 
Start
↓
Display Menu
↓
Enter Choice
↓
Is Choice 1–5?
↓
Perform Operation
↓
Return to Menu
↓
Exit
↓
Stop
________________________________________
📄 SOURCE CODE (C LANGUAGE)
#include <stdio.h>
#include <string.h>

int main() {

    char name[100][50];
    char phone[100][15];

    int total = 0;
    int choice;
    int i, j;
    char tempName[50];

    while (1) {

        printf("\n--- Telephone Contact List ---\n");

        printf("1. Add Contact\n");
        printf("2. Delete Contact\n");
        printf("3. Search Contact\n");
        printf("4. Update Contact\n");
        printf("5. Display Contacts\n");
        printf("6. Exit\n");

        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch (choice) {

        case 1:

            printf("Enter Name: ");
            scanf("%s", name[total]);

            printf("Enter Phone Number: ");
            scanf("%s", phone[total]);

            total++;

            printf("Contact Added Successfully!\n");

            break;

        case 2:

            printf("Enter Name to Delete: ");
            scanf("%s", tempName);

            for (i = 0; i < total; i++) {

                if (strcmp(name[i], tempName) == 0) {

                    for (j = i; j < total - 1; j++) {

                        strcpy(name[j], name[j + 1]);
                        strcpy(phone[j], phone[j + 1]);
                    }

                    total--;

                    printf("Contact Deleted Successfully!\n");
                    break;
                }
            }

            break;

        case 3:

            printf("Enter Name to Search: ");
            scanf("%s", tempName);

            for (i = 0; i < total; i++) {

                if (strcmp(name[i], tempName) == 0) {

                    printf("Name: %s\n", name[i]);
                    printf("Phone: %s\n", phone[i]);

                    break;
                }
            }

            break;

        case 4:

            printf("Enter Name to Update: ");
            scanf("%s", tempName);

            for (i = 0; i < total; i++) {

                if (strcmp(name[i], tempName) == 0) {

                    printf("Enter New Phone Number: ");
                    scanf("%s", phone[i]);

                    printf("Contact Updated Successfully!\n");

                    break;
                }
            }

            break;

        case 5:

            printf("\nAll Contacts:\n");

            for (i = 0; i < total; i++) {

                printf("%s - %s\n",
                       name[i],
                       phone[i]);
            }

            break;

        case 6:

            printf("Exiting Program...\n");
            return 0;

        default:

            printf("Invalid Choice!\n");
        }
    }
}
________________________________________
 OUTPUT / RESULT
Sample Output
--- Telephone Contact List ---
1. Add Contact
2. Delete Contact
3. Search Contact
4. Update Contact
5. Display Contacts
6. Exit

Enter your choice: 1

Enter Name: Aman  
Enter Phone Number: 9876543210  

Contact Added Successfully!

Enter your choice: 5

All Contacts:
Aman - 9876543210
________________________________________


 CONCLUSION
This project successfully demonstrates a Telephone Contact List Management System using C Language.
The program allows users to:
•	Add contacts 
•	Delete contacts 
•	Search contacts 
•	Update contacts 
•	Display stored contacts 
This project helps in understanding arrays, loops, conditions, and string handling in C Language. It also improves logical thinking and programming skills.

