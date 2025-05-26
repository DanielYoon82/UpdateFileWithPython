<h1>UpdateFileWithPython</h1>

<h2>Description</h2>
Access to restricted content is updated with an allow list of IP addresses. The "allow_list.txt" file describes these IP addresses. A separate remove list identifies IP addresses that should no longer have access to this data. I created an algorithm to assist in updating the "allow_list.txt" file and remove these IP addresses that should no longer have access.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Python</b> 

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<h2>Program walk-through:</h2>

<p align="center">
OPEN THE FILE THAT CONTAINS THE ALLOW LIST <br/>
 First, I opened the "allow_list.txt" file. I assigned the file name as a string to the import_file variable: <br/>
<img src="https://github.com/DanielYoon82/UpdateFileWithPython/blob/main/Assign%20import%20image.jpg" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<br />
<br />
Second, I used a with statement to open the file. In my algorithm, the with statement is used with the .open() function to read its content. The purpose of opening the file is to give me  access to the IP addresses stored in the allow list file. The with keyword will assist by managing the data by closing the file after exiting the with statement. In the code with open(import_file, "r") as file:  <br/>
<img src="https://github.com/DanielYoon82/UpdateFileWithPython/blob/main/Buildwith.jpg" height="55%" width="55%" alt="Disk Sanitization Steps"/>
<br />
<br />
READ THE FILE CONTENTS <br />
In order to read the file contents, I used the .read() method to convert it into the string. When using an .open() function it includes the argument "r" for “read,” which then calls the .read() function in the body of the with statement. The .read() method converts the file into a string. I applied the .read() method to the file variable identified in the with statement. Then, I applied the string output of this method to the variable ip_addresses. This code allows me to access the "allow_list.txt" file into a string format which enables me to later use the string to organize and extract data from the Python program: <br/>
<img src="https://github.com/DanielYoon82/UpdateFileWithPython/blob/main/Untitled%20document_page-0001%20(1).jpg" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<br />
<br />
CONVERT THE STRING INTO A LIST <br />
To remove individual IP addresses from the allow list, It needs to be in the list format. I used the .split() method to convert the ip_addresses string into a list. The .split() function is called by appending it to a string variable. It does this by converting the data of a string to a list. The purpose of splitting ip_addresses into a list is to make it easier to remove IP addresses from the allow list. In this algorithm, the .split() function retrieves the data stored in the variable ip_addresses and it converts this string into a list of IP addresses. To store this list, I reassigned it back to the variable ip_addresses:  <br/>
<img src="https://github.com/DanielYoon82/UpdateFileWithPython/blob/main/Untitled%20document%20(1)_page-0001%20(1).jpg" height="55%" width="55%" alt="Disk Sanitization Steps"/>
<br />
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
