# Python file uptake algorithm - Algorithm for file updates in Python

## Objective

To develop a Python script that automates the removal of IP addresses from an allowlist based on a specified remove list. The script will efficiently process the allowlist file, identify and remove unauthorized IP addresses, and update the file with the revised list, ensuring the security of the system.

## Project description

Our organization uses an allow list to control access to sensitive content. The "allow_list.txt" file contains a list of authorized IP addresses. To ensure security and prevent unauthorized access, I developed an automated solution to remove IP addresses from the allow list that should no longer have access. This process involves updating the "allow_list.txt" file based on a separate remove list.

**Key Features:**
  * **File Handling:** The script effectively reads and writes to the allowlist file, ensuring proper file handling and preventing resource leaks.
  * **List Manipulation:** The script converts the allowlist file into a list of IP addresses, enabling efficient iteration and removal of specific entries.
  * **IP Address Filtering:** The script iterates through a remove list and removes matching IP addresses from the allowlist.
  * **File Update:** The modified allowlist is written back to the file, ensuring that the changes are persisted.
This automation improves security by ensuring that unauthorized IP addresses are promptly removed from the allowlist, reducing the risk of unauthorized access.

## Skills Learned
  * **Python Programming:** Demonstrated proficiency in Python programming, including file handling, string manipulation, and list operations.
  * **Problem-Solving:** Identified a real-world security challenge and devised an effective automated solution.
  * **Automation:** Developed a script to automate a repetitive task, improving efficiency and reducing the potential for human error.
  * **Security Best Practices:** Implemented a solution to enhance security by controlling access to sensitive resources.
  * **Attention to Detail:** Ensured accurate file handling and data manipulation to avoid unintended consequences.
  * **Effective Documentation:** Clearly explained the code's functionality and reasoning behind design choices.

## Tools Used
  * **Python:** A versatile programming language used to automate the file reading, manipulation, and writing processes.
  * **Text File:** The "allow_list.txt" file serves as the primary data source, containing the list of authorized IP addresses.
  * **Command Line Interface:** Used to execute Python scripts and interact with the file system.

## Steps
### Step 1. Open the file that contains the allow list
  * To begin, I opened the "allow_list.txt" file. I assigned the file name to the variable import_file. 
    * ![python 1](https://github.com/user-attachments/assets/9b542bfa-0a95-4f9e-8827-0ba93011cd21)
  * Next, I used the with statement and the .open() function to read the allow list file. This ensured the file was properly closed after use, preventing resource leaks. The with open(import_file, "r") as file: syntax opens the file in read mode and assigns it to the file variable within the with block. This streamlined file handling and made my code more concise and efficient.
    * ![python 2](https://github.com/user-attachments/assets/cc57884c-db71-43d3-9596-a865739fec98)

### Step 3. Read the file contents
  * To read the contents of the file,I used the .read() method to open and read the "allow_list.txt" file. This method converted the file's contents into a string, which I assigned to the ip_addresses variable. This string will be used later in my Python program to process and analyze the IP addresses.
    * ![python 3](https://github.com/user-attachments/assets/25c57ce7-f18f-49a1-b7ee-50ec07eef282)

### Step 4. Convert the string into a list
  * To remove specific IP addresses from the allow list, I first needed to convert the string of IP addresses into a list. I used the .split() method to accomplish this. This function takes a string and splits it into a list of substrings based on a specified delimiter. In this case, I used the default delimiter, which is whitespace. By splitting the string into a list, I can easily iterate over the IP addresses and remove the ones I want.
    * ![python 4](https://github.com/user-attachments/assets/53f3ed0c-22cc-4cc7-81c7-bf084700abb2)

### Step 5. Iterate through the remove list
  * The core of my algorithm relies on iterating over the IP addresses within the remove_list. To accomplish this, I implemented a for loop in Python. This loop iterates through each IP address in the list and executes specific actions, such as removing them from a network configuration.
    * ![python 5](https://github.com/user-attachments/assets/ba89ae79-fc59-463e-9cf9-1d17b3ec000e)

### Step 6. Remove IP addresses that are on the remove list
  * I needed to remove any IP address from the allow_list that was also present in the remove_list. As there were no duplicates in allow_list, I employed a straightforward approach
  * I iterated through each IP address in the remove_list. For each IP address, I checked if it existed within the allow_list. If a match was found, I removed that IP address from the allow_list using the .remove() method.
    * ![python 6](https://github.com/user-attachments/assets/a1493f21-867a-4661-89e3-59e5503577bf)

### Step 7. Update the file with the revised list of IP addresses 
  * To update the allow list file with the revised IP addresses, I first converted the list back into a string using the join() method. This method concatenates all elements of a list into a single string, separating them with a specified delimiter. In this case, I used a newline character (\n) as the delimiter to ensure each IP address was on a new line.
    * ![python 7](https://github.com/user-attachments/assets/185ed443-725e-4b25-8561-7ec116ded910)
  * I then opened the "allow_list.txt" file in write mode ("w") using a with statement. This mode overwrites the existing content of the file, allowing me to replace the old allow list with the new one. I used the write() method to write the updated IP address string to the file, effectively updating the allowed IP addresses.
    * ![python 8](https://github.com/user-attachments/assets/3b8978fb-527b-4587-bc35-6b9572ded1ce)

### Summary
I developed a Python script to automate the removal of IP addresses from an allowlist based on a specified remove list. The script reads the allowlist file, converts it into a list of IP addresses, and then iterates through the remove list. Any IP address found in both lists is removed from the allowlist. The modified allowlist is then written back to the file. This automated process ensures that the allowlist remains up-to-date and secure.
