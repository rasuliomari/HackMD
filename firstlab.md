# Basic server-side template injection(ERB template)

### ***WHAT IS OUR TASK?***
This lab is vulnerable to server-side template injection due to the unsafe construction of an ERB template.

To solve the lab, review the ERB documentation to find out how to execute arbitrary code, then delete the morale.txt file from Carlos's home directory.

## ***SOLUTION***
When you try to access the lab you will Notice that, when you try to view more details about the first product, a GET request uses the message parameter to render "Unfortunately this product is out of stock" on the home page.

That is show the vulnerability of server-side template and i use the ERB documentation, discover that the syntax <%=  %> it can be used to evaluate an expression and render the result on the page

#### COMMAND THAT I USE
The following are the command that i use to persue this challenge as shown below:-
1. The first command i use is "<%= 7 * 7 %>" 
This command it show me that the payload is working correct in server side and give me the answer of 49
2. The second command i use is "<%= Dir.glob("**/*.txt") %>"
This is a native Ruby way to search for files recursively throughout the directory structure without relying on external shell commands and it give me the file name exist as "morale.txt"

3. the third command i use is "<%= Dir.glob****("**/*.txt").map { |f| File.expand_path(f)  %>"
This command it help to recursively search in all folder to find the file name that it end with .txt extension and show us the direct location of that file as shown 
![Screenshot_2026-02-19_23_00_03](https://hackmd.io/_uploads/SyP8k7Sdbe.png)
5. the fourth command i use is "<%= File.delete(".txt") %>"
This is the most direct way to delete a file using Ruby code within the ERB tag in single deletion file 
![Screenshot_2026-02-19_23_06_38](https://hackmd.io/_uploads/B1zJL7SOZe.png)

7. And after refresh gues what next?
Boooooom.......!!!!!
![Screenshot_2026-02-19_23_07_51](https://hackmd.io/_uploads/HyR78XHu-x.png)

## ***CONCLUSION***
Solved by : R4soul
Udom Cyber Club {UCC}
@2026
