# text-to-handwriting

This program converts a given text file into a Word document where each character is represented as an image of handwritten text. It uses the docx library for creating the Word document and PIL for handling image operations.

Features
Converts plain text from a .txt file into a Word document.
Each character in the text is replaced by an image of a handwritten letter.
Supports handling of newline characters to maintain text formatting.

<h2>Requirements</h2>

Python 3.x
python-docx
PIL (Pillow)
Image files named after the ASCII codes of characters (e.g., 65.png for 'A', 97.png for 'a')

<h2>Installation</h2>

Ensure you have the required libraries installed. You can install them using pip:

bash

pip install python-docx Pillow

<h2>How to Use</h2>

Prepare Image Files

Ensure you have images for each character you want to convert. Name these images according to their ASCII codes. For example, 'A' should be 65.png, 'a' should be 97.png, and so on.
Place these images in the same directory as your script.

Prepare the Text File

Create a text file (dummy.txt) containing the text you want to convert.
Place this text file in the same directory as your script.

Run the Script

Execute the script. It will read the text from dummy.txt, replace spaces with multiple spaces, and convert each character to its corresponding image.

The resulting Word document will be saved as output.docx in the same directory.

<h2>Logic and Workflow</h2>

Reading the Text File
The script opens dummy.txt and reads its content.
Space Replacement
Single spaces in the text are replaced with multiple spaces to ensure proper formatting.
Creating the Word Document
A new Word document is created using the docx library.
Adding Images to Document
The script iterates through each character in the text.
For each character, it attempts to load the corresponding image file named after the ASCII code of the character.
If an image is found, it is added to the document. If not, the character is added as plain text.
Newlines in the text are handled to ensure proper paragraph breaks.
Saving the Document
The final document is saved as output.docx.

<h2>Detailed Steps</h2>
Reading Text File
The program starts by opening and reading the content of dummy.txt.
All single spaces in the text are replaced with multiple spaces to ensure better spacing in the final document.
Creating the Document
A new Word document is created using docx.Document().
Adding Characters
The function add_letter_image_to_doc(letter) handles the addition of each character.
It tries to open an image file named after the ASCII code of the character.
If the image exists, it is added to the document; if not, the character is added as plain text.
The process continues for all characters in the text.
Handling Newlines
Newlines (\n) in the text are managed by adding new paragraphs to the document.
Saving the Document
After processing all characters, the document is saved as output.docx.
By following these instructions, you should be able to use and understand the text to handwritten document converter program effectively.
