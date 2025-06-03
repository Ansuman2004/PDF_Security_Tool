# PDF_Security_Tool
This project, titled "PDF Security Tool", is developed as part of a cybersecurity internship and focuses on the dual aspects of document protection and ethical penetration testing. The tool provides two core functionalities: encrypting PDF files with user-defined passwords to ensure data confidentiality, and cracking password-protected PDFs .

***Abstract:***

This project, titled "PDF Security Tool", is developed as part of a cybersecurity 
internship and focuses on the dual aspects of document protection and ethical 
penetration testing. The tool provides two core functionalities: encrypting PDF files 
with user-defined passwords to ensure data confidentiality, and cracking password
protected PDFs using both dictionary-based and brute-force approaches.  
The primary goal is to highlight the importance of secure password practices while also 
showcasing methods that attackers might use to breach weak protection. Testing 
confirmed successful encryption and decryption, with real-time progress indicators 
enhancing user interaction. Overall, the project serves as an educational tool for learning 
core cybersecurity concepts in a hands-on manner. 

***1. Introduction:***

In today’s digital era, sensitive documents are often shared and stored in PDF format 
due to its platform independence and professional presentation. However, the security 
of these documents is often compromised due to weak or no password protection. 
Hence, protecting PDF documents with strong encryption has become a critical 
requirement. 
The tool serves a dual purpose: enabling users to encrypt PDF files with a secure 
password and to crack password-protected PDFs using ethical methods such as 
wordlist attacks and brute-force techniques. This project aims to provide insight into 
both the defensive and offensive aspects of document security. 
By implementing both encryption and password-cracking features, the project 
demonstrates real-world scenarios where strong security practices are essential. It also 
educates users on how weak passwords can be easily guessed or cracked using 
automated tools.  

***2. Objectives:*** 

The primary objective of this project is to develop a Python-based tool that 
demonstrates fundamental cybersecurity principles related to document protection, 
specifically for PDF files. The tool is designed with the following key goals: 
1. To provide a secure method to encrypt PDF files using a user-defined password, 
ensuring that unauthorized individuals cannot access sensitive content. 
2. To implement password-cracking mechanisms for protected PDFs using: 
o Wordlist-based attacks, where passwords are guessed from a predefined list. 
o Brute-force attacks, which generate passwords on-the-fly using a specified 
character set and length range. 
3. To educate users on both secure practices and common vulnerabilities, by 
showing how easily weak passwords can be cracked. 
4. To simulate real-world cybersecurity scenarios, combining offensive and 
defensive strategies to deepen the understanding of document-level threats and 
security countermeasures. 
This project bridges the gap between theory and practice in the field of cybersecurity, 
equipping learners with the ability to develop, analyze, and improve tools that enhance 
digital safety.

***3. Tools Used:***

> Language: Python 3 
> Libraries: PyPDF2, pikepdf, tqdm

***4. Features:*** 

The PDF Security Tool is designed to offer both document protection and penetration 
testing capabilities through a simple and interactive command-line interface. Its main 
features include: 
1. PDF Encryption 
o Allows users to encrypt a PDF file by setting a custom password. 
o Prevents unauthorized access and protects sensitive information. 
2. Password Cracking Modes 
The tool supports two cracking methods for password-protected PDFs: 
o Wordlist Attack: Attempts to unlock the PDF using passwords from a user
provided wordlist file. 
o Brute-force Attack: Automatically generates and tests all possible passwords 
from a defined character set and length range. 
3. Progress Visualization 
o Uses the tqdm library to show a real-time progress bar during both cracking and 
decryption processes. 
o Enhances user experience with clear visual feedback on progress. 
4. Successful Decryption Handling 
o On finding the correct password, the PDF is decrypted and saved as a new file. 
o Displays a "Decryption Complete" bar to simulate progress visually, similar to 
professional software behavior. 
5. Interactive Menu System 
o Provides a clear menu to choose between encryption, cracking, and exit options. 
o Ensures a user-friendly experience without requiring prior technical knowledge. 
These features make the tool a practical and educational resource for understanding 
PDF security mechanisms and how attackers might exploit weak protections.

***5. Methodology:***

The development of the PDF Security Tool follows a structured approach to implement 
both encryption and ethical password-cracking functionalities. The methodology 
combines cybersecurity practices with software engineering principles, as detailed 
below: 
5.1 Requirements Gathering 
 1. Identify the need for a dual-purpose tool capable of both protecting and ethically 
testing PDF security. 
 2. Select appropriate Python libraries: 
  • PyPDF2 for encryption. 
  • pikepdf for secure PDF opening and password cracking. 
  • tqdm for real-time progress visualization. 
5.2 System Design 
 1. Create a menu-driven command-line interface allowing users to choose 
operations. 
 2. Define two main functional modules: 
  • Encrypt Module: Accepts input and output file paths and a password, then 
encrypts the PDF. 
  • Crack Module: Allows users to select between: 
    > Wordlist-based cracking.
   
    > Brute-force password generation using character sets and length 
constraints. 
5.3 Implementation 
1. Encryption: 
 • Uses PyPDF2.PdfReader and PdfWriter to apply password protection. 
2. Cracking: 
 • Uses pikepdf.open() within a try-except block to test passwords. 
 • Displays attempt progress using tqdm. 
 • For brute-force, generates password combinations dynamically using 
itertools.product. 
5.4 User Interaction 
 1. Prompts guide users through file selection, password entry, cracking method, 
charset, and length. 
 2. Displays results with clear messages indicating success or failure. 
5.5 Testing and Validation 
 1. Tests performed on multiple PDFs with known passwords. 
 2. Verified functionality of both cracking methods. 
 3. Ensured decrypted files are saved and usable.
   
***6. Results and Testing***

To validate the effectiveness and accuracy of the PDF Security Tool, multiple test 
scenarios were conducted using sample PDF files protected with known passwords. The 
tool was evaluated for both encryption and password-cracking functionalities, with the 
following outcomes: 

6.1 PDF Encryption 
• Multiple PDFs were successfully encrypted using the tool. 
• Encrypted files could not be opened without the specified password, confirming 
that encryption was applied correctly using the PyPDF2 library. 

![image](https://github.com/user-attachments/assets/8bdccaf1-28a4-4952-8bc8-0764dd4248ac)

6.2 Password Cracking (Wordlist)
•	A wordlist file containing several potential passwords was used.
•	The tool was able to identify the correct password within the list and decrypt the PDF.
•	The cracking process displayed a real-time progress bar, providing user-friendly feedback.
•	Decrypted PDF files were saved automatically with a new filename (e.g., decrypted_output.pdf).

![image](https://github.com/user-attachments/assets/637d482b-674b-4ae6-a666-08d9a21858d6)

6.3 Password Cracking (Brute-force)
•	Tested with numeric and alphanumeric character sets, with controlled password length (e.g., 3–4 characters).
•	The tool successfully generated and tested all possible combinations within the defined range.
•	The correct password was detected, and decryption proceeded smoothly.
•	A simulated “decryption progress bar” (similar to commercial software) was displayed for visual confirmation.

![image](https://github.com/user-attachments/assets/458b8303-81a7-4234-a2c5-dc7f92f3a749)

***Conclusion:***

The PDF Security Tool developed during this internship successfully demonstrates the application of cybersecurity concepts in real-world scenarios involving document protection. The tool provides dual functionality — enabling users to encrypt PDFs for confidentiality and ethically crack password-protected PDFs to understand vulnerabilities associated with weak password usage.
Through this project, the importance of strong encryption practices and the dangers of using predictable or short passwords have been effectively highlighted. The implementation of both wordlist-based and brute-force attacks, along with a real-time progress visualization, makes the tool not only functional but also educational and engaging.
This project bridges theory with hands-on practice, making it a valuable resource for both learners and professionals in the cybersecurity domain. It enhances understanding of password security, PDF protection mechanisms, and ethical hacking strategies in a controlled and responsible manner.
Overall, the project fulfills its objectives by providing a secure, interactive, and practical tool for document security testing, reflecting strong alignment with the goals of the cybersecurity internship.
