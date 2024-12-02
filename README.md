# Email-Merge
C program that generates customized email body text by reading the data from excel sheet. Assuming that the excel sheet in CSV format. Storing the generated body text in a text file.


AIM:
To develop a C program to automate the process of generating personalized email content. The
primary goal is to create email bodies for parents regarding the attendance of their wards, based
on data provided in a CSV file. The generated emails were saved in a text file for later use. It
ensures that each email follows a consistent format and includes accurate, user-specific details.

ALGORITHM:
The program follows these steps:
1. Start.
2. Open the input CSV file (data.csv) in read mode.
3. If the file cannot be opened, print an error and terminate.
4. Open the output text file (emails.txt) in write mode.
5. If the file cannot be opened, print an error and terminate.
6. Read each line from the input file:
7. Parse the line to extract student name, parent title, parent name, and attendance percentage.
8. If the line cannot be parsed, skip it and log an error.
9. Format the extracted data into an email template.
10. Write the formatted email to the output file.
11. Close both the input and output files.
12. Print a success message indicating the emails have been generated.
13. End.

FLOWCHART:
Start ==> Open 'data.csv' for reading, if error, print and exit ==> Open 'emails.txt' for writing, if
error, exit ==> Parse line (name, title, parent name, attendance), if error, skip to next line ==>
Format and write email content to 'emails.txt’ ==> Close both files, Print success message ==>
End.

IMPLEMENTAION:
1. INPUT:
The input to the program is a CSV file (data.csv) that contains the following columns:
• Student Name: The name of the student.
• Title: The title of the parent (e.g., Mr., Ms.).
• Parent Name: The parent's name.
• Overall Attendance (%): The attendance percentage of the student.
2. OUTPUT:
The program generates email content in the following format:
Dear [Title] [Parent Name],
Greetings!
This is to inform you that the attendance of your ward [Student Name] is [Attendance] %.
Thank you.
This content is saved in a text file named emails.txt.
Code Explanation
1. Uses fopen to open the input CSV and output text files.
2. Reads lines using fgets, ensuring the program does not exceed buffer limits.
3. Parses each line using sscanf to extract the required fields.
4. Formats the extracted fields into a predefined email template with snprintf.
5. Writes the email content to the output file using fprintf.

STEPS IN THE PROGRAM:
1. Reading the Input File: The program uses the fopen function to open the CSV file
(data.csv) for reading. Each line is read and parsed to extract the required details.
2. Processing the Data: For each record in the CSV, the program formats a custom email
using sprintf, which inserts the relevant data (parent's name, title, student's name, and
attendance) into the template.
3. Writing the Output: The generated email text is written to emails.txt using the fprintf
function.

RESULTS:
The program successfully generated emails and saved them in the emails.txt
