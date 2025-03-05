# palindromeChecker 🔄



The Palindrome Checker is a JavaScript-based application that checks if a given string is a palindrome. A palindrome is a word, phrase, number, or other sequence of characters that reads the same forward and backward (ignoring spaces, punctuation, and capitalization).

This project was built as part of the freeCodeCamp curriculum and demonstrates the use of string manipulation and regular expressions (regex) for input validation.

Features ✨


Checks for Palindromes:

Ignores spaces, punctuation, and capitalization.

Works with words, phrases, and numbers.

Input Validation:

Handles empty strings and invalid inputs gracefully.

Simple and Efficient:

Lightweight and easy to integrate into other projects.

How It Works 🛠️


Input:

The user provides a string (e.g., a word, phrase, or number).

Validation:

The app removes all non-alphanumeric characters and converts the string to lowercase.

Palindrome Check:

The app compares the cleaned string to its reverse.

Output:

Returns true if the string is a palindrome.

Returns false if the string is not a palindrome.

User Stories Implemented ✅


User Story	Status
The app ignores spaces, punctuation, and capitalization.	✔️
The app checks if a single word is a palindrome (e.g., eye).	✔️
The app checks if a phrase is a palindrome (e.g., A man, a plan, a canal, Panama).	✔️
The app checks if a number is a palindrome (e.g., 12321).	✔️
The app returns false for non-palindromes (e.g., hello).	✔️


Technologies Used 💻


JavaScript: For implementing the palindrome-checking logic.

Regular Expressions (Regex): For cleaning the input string.

HTML/CSS: For the user interface.

Setup Instructions 🚀


Clone the Repository:

bash
git clone https://github.com/Gsilva700/palindromeChecker.git
cd palindromeChecker
Open the App:

Open the index.html file in your browser.

Use the App:

Enter a string in the input field.

Click the "Check" button to see if it is a palindrome.

Example Usage 📋


Valid Palindromes


Input	Output
eye	true
_eye	true
race car	true
A man, a plan, a canal. Panama	true
never odd or even	true
My age is 0, 0 si ega ym.	true
0_0 (: /-\ :) 0-0	true


Non-Palindromes


Input	Output
hello	false
almostomla	false
1 eye for 1 eye	false
not a palindrome	false


Code Structure 🗂️

palindrome-checker/
├── index.html          # Main HTML file
├── styles.css          # CSS for styling
├── script.js           # JavaScript for palindrome-checking logic
├── README.md           # Project documentation
└── screenshot.png      # Screenshot of the app (optional)


Credits 🙌
Built by Gabriel de Macedo Silva.

Inspired by freeCodeCamp.

Contributions are welcome! 🤝


Palindrome Logic 🔍
The app uses the following logic to check for palindromes:

Clean the Input:

Remove all non-alphanumeric characters using regex.

Convert the string to lowercase.

javascript

const cleanString = (str) => {
  return str.replace(/[^a-zA-Z0-9]/g, "").toLowerCase();
};
Check for Palindrome:

Compare the cleaned string to its reverse.

javascript

const isPalindrome = (str) => {
  const cleanedStr = cleanString(str);
  return cleanedStr === cleanedStr.split("").reverse().join("");
};
