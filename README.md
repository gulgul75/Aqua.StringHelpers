# About Aqua String Helpers:

Aqua String Helpers is an Open Source and Free Software package consists of a set of utilities that facilitate the job of the developer and save his time while dealing with a string. Every developer could be a beneficiary of this library; however, those who deal with database and integration applications are likely the most potential beneficiaries.


# Getting Started
TODO: Guide users through getting your code up and running on their own system. In this section you can talk about:
1.	Installation process
2.	Software dependencies
3.	Latest releases
4.	API references

# List of Features and Methods
1. [IsNullOrEmpty](#IsNullOrEmpty)
2. [IsNullOrWhiteSpace](#IsNullOrWhiteSpace)
3. [IsDigit](#IsDigit)
4. [IsInteger](#IsInteger)
5. [IsNumber](#IsNumber)
6. [IsAlphaNumeric](#IsAlphaNumeric)
7. [IsValidURL](#IsValidURL)
8. [IfNullReturnEmptyString](#IfNullReturnEmptyString)
9. [Reverse](#Reverse)
10. [RemoveExtraSpaces](#RemoveExtraSpaces)
11. [RemoveAllLineBreaks](#RemoveAllLineBreaks)
12. [RemoveNonASCIIChars](#RemoveNonASCIIChars)
13. [RemoveNumberOfCharsAtBegining](#RemoveNumberOfCharsAtBegining)
14. [RemoveNumberOfCharsAtEnd](#RemoveNumberOfCharsAtEnd)
15. [ReplaceTabsWithSpaces](#ReplaceTabsWithSpaces)

# Features and Methods
### IsNullOrEmpty
IsNullOrEmpty is an extension method, equivalent for the traditional ``` string.IsNullOrEmpty() ``` static method. Returns true if the string examined is null or empty, otherwise returns false.

```C#
//using Aqua.StringHelpers;

string input;
bool output;

input = null;
output = input.IsNullOrEmpty();  // output = true

input = "";
output = input.IsNullOrEmpty();  // result = true

input = " ";
output = input.IsNullOrEmpty();  // output = false

input = "lorem ipsum dolor";
output = input.IsNullOrEmpty();  // output = false

```
:back:[Back to the Full List of Features](#List-Of-Features-and-Methods)

### IsNullOrWhiteSpace
IsNullOrEmpty is an extension method, equivalent for the traditional ``` string.IsNullOrWhiteSpace() ``` static method. Returns true if the string examined is null or empty, otherwise returns false.

```C#
//using Aqua.StringHelpers;

string input;
bool output;

input = null;
output = input.IsNullOrWhiteSpace();  // output = true

input = "";
output = input.IsNullOrWhiteSpace();  // result = true

input = " ";
output = input.IsNullOrWhiteSpace(); // output = false

input = "lorem ipsum dolor";
output = input.IsNullOrWhiteSpace();  // output = false

```
:back:[Back to the Full List of Features](#List-Of-Features-and-Methods)

### IsDigit

```C#
//using Aqua.StringHelpers;

char input;
bool output;

input = '0';
output = input.IsDigit();  // output = true

input = '9';
output = input.IsDigit();  // output = true

input = 'A';
output = input.IsDigit();  // output = false

```
:back:[Back to the Full List of Features](#List-Of-Features-and-Methods)

### IsInteger
```C#
//using Aqua.StringHelpers;

string input;
bool output;

input = null;
output = input.IsInteger();  // output = false

input = "";
output = input.IsInteger();  // result = false

input = " ";
output = input.IsInteger();  // result = false

input = "5";
output = input.IsInteger();  // output = true

input = "555";
output = input.IsInteger();  // output = true

input = "555.50";
output = input.IsInteger();  // output = false

input = "lorem ipsum dolor";
output = input.IsInteger();  // output = false

```
:back:[Back to the Full List of Features](#List-Of-Features-and-Methods)

### IsNumber
```C#
//using Aqua.StringHelpers;

string input;
bool output;

input = null;
output = input.IsNumber();  // output = false

input = "";
output = input.IsNumber();  // result = false

input = " ";
output = input.IsNumber();  // result = false

input = "5";
output = input.IsNumber();  // output = true

input = "555";
output = input.IsNumber();  // output = true

input = "555.50";
output = input.IsNumber();  // output = true

input = "lorem ipsum dolor";
output = input.IsNumber();  // output = false

```
:back:[Back to the Full List of Features](#List-Of-Features-and-Methods)

### IsAlphaNumeric
```C#
//using Aqua.StringHelpers;

string input;
bool output;

input = null;
output = input.IsAlphaNumeric();  // output = false

input = "";
output = input.IsAlphaNumeric();  // result = false

input = " ";
output = input.IsAlphaNumeric();  // result = false

input = "5";
output = input.IsAlphaNumeric();  // output = true

input = "5A";
output = input.IsAlphaNumeric();  // output = true

input = "A5";
output = input.IsAlphaNumeric();  // output = true

input = "lorem ipsum dolor";
output = input.IsAlphaNumeric();  // output = false

input = "loremipsumdolor";
output = input.IsAlphaNumeric();  // output = true

input = "$loremips((umdolor";
output = input.IsAlphaNumeric();  // output = false

```
:back:[Back to the Full List of Features](#List-Of-Features-and-Methods)

### IsValidURL
```C#
using Aqua.StringHelpers;

string input;
bool output;

input = null;
output = input.IsValidURL();  // output = false

input = "";
output = input.IsValidURL();  // result = false

input = " ";
output = input.IsValidURL();  // result = false

input = "http://wideitsolutions.co.uk";
output = input.IsValidURL();  // output = true

input = "https://wideitsolutions.co.uk";
output = input.IsValidURL();  // output = true

input = "http://dev.wideitsolutions.co.uk";
output = input.IsValidURL();  // output = true

input = "http://wideitsolutions.co.uk/dev";
output = input.IsValidURL();  // output = true

```
:back:[Back to the Full List of Features](#List-Of-Features-and-Methods)

### IfNullReturnEmptyString

```C#
//using Aqua.StringHelpers;

string input;
string output;

input = null;
output = input.IfNullReturnEmptyString();  // output = ""

input = "";
output = input.IfNullReturnEmptyString();  // result = ""

input = " ";
output = input.IfNullReturnEmptyString();  // result = " "

input = "lorem ipsum";
output = input.IfNullReturnEmptyString();  // output = "lorem ipsum"
```
:back:[Back to the Full List of Features](#List-Of-Features-and-Methods)

### Reverse
```C#
//using Aqua.StringHelpers;

string input;
string output;

input = null;
output = input.Reverse();  // output = null

input = "";
output = input.Reverse();  // result = ""

input = " ";
output = input.Reverse();  // result = " "

input = "lorem ipsum";
output = input.Reverse();  // output = "muspi merol"

input = "A12345";
output = input.Reverse();  // output = "54321A"
```
:back:[Back to the Full List of Features](#List-Of-Features-and-Methods)

### RemoveExtraSpaces
```C#
//using Aqua.StringHelpers;

string input;
string output;

input = null;
output = input.RemoveExtraSpaces();  // output = null

input = "";
output = input.RemoveExtraSpaces();  // result = ""

input = " ";
output = input.RemoveExtraSpaces();  // result = ""

input = "lorem ipsum";
output = input.RemoveExtraSpaces();  // output = "lorem ipsum"

input = "  lorem ipsum      lorem ipsum  ";
output = input.RemoveExtraSpaces();  // output = "lorem ipsum lorem ipsum"
```
:back:[Back to the Full List of Features](#List-Of-Features-and-Methods)

### RemoveAllLineBreaks
```C#
//using Aqua.StringHelpers;

string input;
string output;

input = null;
output = input.RemoveAllLineBreaks();  // output = null

input = "";
output = input.RemoveAllLineBreaks();  // result = ""

input = " ";
output = input.RemoveAllLineBreaks();  // result = " "

input = "lorem\n ipsum";
output = input.RemoveAllLineBreaks();  // output = "lorem ipsum"

input = "  lorem \nipsum      lorem\n ipsum  ";
output = input.RemoveAllLineBreaks();  // output = "  lorem ipsum      lorem ipsum  "
```
:back:[Back to the Full List of Features](#List-Of-Features-and-Methods)

### RemoveNonASCIIChars
```C#
//using Aqua.StringHelpers;

string input;
string output;

input = null;
output = input.RemoveNonASCIIChars();  // output = null

input = "";
output = input.RemoveNonASCIIChars();  // result = ""

input = " ";
output = input.RemoveNonASCIIChars();  // result = " "

input = "lorem ipsum";
output = input.RemoveNonASCIIChars();  // output = "lorem ipsum"

input = "lorem भारत ipsum";
output = input.RemoveNonASCIIChars();  // output = "lorem  ipsum"
```
:back:[Back to the Full List of Features](#List-Of-Features-and-Methods)

### RemoveNumberOfCharsAtBegining
```C#
//using Aqua.StringHelpers;

string input;
int n; //number of characters
string output;

input = null;
n = 3;
output = input.RemoveNumberOfCharsAtBegining(n);  // output = null

input = "";
n = 3;
output = input.RemoveNumberOfCharsAtBegining(n);  // result = ""

input = " ";
n = 3;
output = input.RemoveNumberOfCharsAtBegining(n);  // result = ""

input = "lorem ipsum";
n = 3;
output = input.RemoveNumberOfCharsAtBegining(n);  // output = "em ipsum"

input = "  lorem ipsum";
n = 3;
output = input.RemoveNumberOfCharsAtBegining(n);  // output = "orem  ipsum"
```
:back:[Back to the Full List of Features](#List-Of-Features-and-Methods)

### RemoveNumberOfCharsAtEnd
```C#
//using Aqua.StringHelpers;

string input;
int n; //number of characters
string output;

input = null;
n = 3;
output = input.RemoveNumberOfCharsAtEnd(n);  // output = null

input = "";
n = 3;
output = input.RemoveNumberOfCharsAtEnd(n);  // result = ""

input = " ";
n = 3;
output = input.RemoveNumberOfCharsAtEnd(n);  // result = ""

input = "lorem ipsum";
n = 3;
output = input.RemoveNumberOfCharsAtEnd(n);  // output = "lorem ip"

input = "lorem ipsum  ";
n = 3;
output = input.RemoveNumberOfCharsAtEnd(n);  // output = "lorem  ipsu"
```
:back:[Back to the Full List of Features](#List-Of-Features-and-Methods)

### ReplaceTabsWithSpaces
```C#
//using Aqua.StringHelpers;

string input;
string output;

input = null;
output = input.ReplaceTabsWithSpaces();  // output = null

input = "";
output = input.ReplaceTabsWithSpaces();  // result = ""

input = " ";
output = input.ReplaceTabsWithSpaces();  // result = ""

input = "lorem              ipsum";      //4 tabs were here
output = input.ReplaceTabsWithSpaces();  // output = "lorem ipsum"

input = "   lorem               ipsum "; //6 tabs were here
output = input.ReplaceTabsWithSpaces();  // output = "lorem ipsum"
```
:back:[Back to the Full List of Features](#List-Of-Features-and-Methods)

# Build and Test
TODO: Describe and show how to build your code and run the tests. 

# Contribute
TODO: Explain how other users and developers can contribute to make your code better. 

If you want to learn more about creating good readme files then refer the following [guidelines](https://docs.microsoft.com/en-us/azure/devops/repos/git/create-a-readme?view=azure-devops). You can also seek inspiration from the below readme files:
- [ASP.NET Core](https://github.com/aspnet/Home)
- [Visual Studio Code](https://github.com/Microsoft/vscode)
- [Chakra Core](https://github.com/Microsoft/ChakraCore)
