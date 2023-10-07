# MD2QTI
# text2qti – Create quizzes in QTI format from Markdown-based plain text

MD2QTI is a CLI-based tool that converts [Markdown](https://daringfireball.net/projects/markdown/)-based plain text
files into quizzes in QTI format which is imported onto [Canvas](https://www.instructure.com/canvas/) to automatically generate quizzes.

Simply open up Notepad and write out your quiz with some simple pre-defined syntax!
MD2QTI supports multiple-choice, true/false, multiple-answers, numerical,
short-answer (fill-in-the-blank), essay, and file-upload questions. 


## Example

An example of a 
**multiple-choice** plain-text quiz question that can be converted to QTI and
then imported by Canvas:

```
1.  What is 2+3?
a)  6
b)  1
*c) 5
```

For more syntax along with examples, refer to the README in the sample folder.



## Usage

MD2QTI has been designed to create QTI files for use with
[Canvas](https://www.instructure.com/canvas/). Please preview the
quizzes after converting them to QTI and before importing them.

Write your quiz or assessment in a plain text file.  You can use a basic
editor like Notepad or gedit.


* To use the command-line application, open a command line in the same folder
  or directory as your quiz file.  Under Windows, you can hold the SHIFT
  button down on the keyboard, then right click next to your file, and select
  "Open PowerShell window here" or "Open command window here".  You can also
  launch "Command Prompt" or "PowerShell" through the Start menu, and then
  navigate to your file using `cd`.

  Run the `MD2QTI` application using a command like this:
  ```
  MD2QTI quiz.txt
  ```
  Replace "quiz.txt" with the name of your file.  This will create a file like
  `quiz.zip` (with "quiz" replaced by the name of your file) which is the
  converted quiz in QTI format.

Instructions for using the QTI file with Canvas:
  * Go to the course in which you want to use the quiz.
  * Go to Settings, click on "Import Course Content", select "QTI .zip file",
    choose your file, and click "Import".  Typically you should not need to
    select a question bank; that should be managed automatically.
  * While the quiz upload will often be very fast, there is an additional
    processing step that can take up to several minutes.  The status will
    probably appear under "Current Jobs" after upload.
  * Once the quiz import is marked as "Completed", the imported quiz should be
    available under Quizzes.  If the imported quiz does not appear after
    several minutes, there may be an error in your quiz file or a bug in
    `MD2QTI`.  When Canvas encounters an invalid quiz file, it tends to fail
    silently; instead of reporting an error in the quiz file, it just never
    creates a quiz based on the invalid file.





