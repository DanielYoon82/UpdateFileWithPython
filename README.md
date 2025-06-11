<h1>Update File With Python</h1>

<h2>Description</h2>
Access to restricted content is updated with an allow list of IP addresses. The "allow_list.txt" file describes these IP addresses. A separate remove list identifies IP addresses that should no longer have access to this data. I created an algorithm to assist in updating the "allow_list.txt" file and remove these IP addresses that should no longer have access.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Python</b> 

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<h2>Program walk-through:</h2>


<b>Open the file that contains the allow list</b> <br/>
 First, I opened the "allow_list.txt" file. I assigned the file name as a string to the import_file variable: <br/>
<p align="center">
<img src="https://github.com/DanielYoon82/UpdateFileWithPython/blob/main/images/Assign%20import%20image.jpg" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<br />
Second, I used a with statement to open the file. In my algorithm, the with statement is used with the .open() function to read its content. The purpose of opening the file is to give me  access to the IP addresses stored in the allow list file. The with keyword will assist by managing the data by closing the file after exiting the with statement. In the code with open(import_file, "r") as file: <br />
<br />
<p align="center">
<img src="https://github.com/DanielYoon82/UpdateFileWithPython/blob/main/images/Buildwith.jpg" height="55%" width="55%" alt="Disk Sanitization Steps"/>
</p>
<br />
<br />
<b>Read the file contents</b> <br />
In order to read the file contents, I used the .read() method to convert it into the string. When using an .open() function it includes the argument "r" for “read,” which then calls the .read() function in the body of the with statement. The .read() method converts the file into a string. I applied the .read() method to the file variable identified in the with statement. Then, I applied the string output of this method to the variable ip_addresses. <br />
 <br />
 This code allows me to access the "allow_list.txt" file into a string format which enables me to later use the string to organize and extract data from the Python program: <br />
<br />
<p align="center">
<img src="https://github.com/DanielYoon82/UpdateFileWithPython/blob/main/images/GHFileContents.jpg" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<br />
<br />
<b>Convert the string into a list</b> <br />
To remove individual IP addresses from the allow list, It needs to be in the list format. I used the .split() method to convert the ip_addresses string into a list. The .split() function is called by appending it to a string variable. It does this by converting the data of a string to a list. The purpose of splitting ip_addresses into a list is to make it easier to remove IP addresses from the allow list. In this algorithm, the .split() function retrieves the data stored in the variable ip_addresses and it converts this string into a list of IP addresses. To store this list, I reassigned it back to the variable ip_addresses:  <br/>
<br />
<p align="center">
<img src="https://github.com/DanielYoon82/UpdateFileWithPython/blob/main/images/GHConvertString.jpg" height="55%" width="55%" alt="Disk Sanitization Steps"/>
</p>
<br />
<br />
<b>Iterate through the remove list</b> <br />
A vital part of my algorithm is to iterate through the IP addresses that are elements in the remove_list. To do this, I created a for loop. The purpose of the for loop in this algorithm is to apply specific code statements to all elements in a sequence. The for keyword starts the loop. It is followed by the loop variable element and the keyword in. The keyword in initiates the iteration through the sequence ip_addresses and assigns each value to the loop variable element:  <br/>
<br />
<p align="center">
<img src="https://github.com/DanielYoon82/UpdateFileWithPython/blob/main/images/GHIterateList.jpg" height="38%" width="38%" alt="Disk Sanitization Steps"/>
</p>
<br />
<br />
<b>Remove IP addresses that are on the remove list</b> <br />
This algorithm requires removing any IP address from the allow list, ip_addresses, that is also contained in remove_list. First, within my for loop, I created a conditional that evaluated whether or not the loop variable element was found in the ip_addresses list. I did this because applying .remove() to elements that were not found in ip_addresses would result in an error. <br />
<br />
I applied .remove() to ip_addresses. I passed in the loop variable element as the argument so that each IP address that was in the remove_list would be removed from ip_addresses: <br /> 
<br />
<p align="center">
<img src="https://github.com/DanielYoon82/UpdateFileWithPython/blob/main/images/GHRemoveIP.jpg" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<br />
<br />
<b>Update the file with the revised list of IP addresses</b> <br/>
Lastly, in this algorithm, I needed to update the allow list file with the revised list of IP addresses. To do this, I needed to convert the list back into a string. I used the .join() method for this. The .join() method combines all items into a string. I used the .join() method to create a string from the list ip_addresses so that I could be changed to an argument in the .write() method when writing to the file "allow_list.txt": <br />
<br />
<p align="center">
<img src="https://github.com/DanielYoon82/UpdateFileWithPython/blob/main/images/Updatefile.jpg" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<br />
<br />
Then, I used another with statement and the .write() method to update the file. <br /> 
<br />
For this, I used a second argument of "w" with the open() function in my with statement. When using this argument "w", I can call the .write() function . The .write() function writes string data to a file and replaces any existing data.
<br />
<br />
In this scenario I wanted to write the updated allow list as a string to the file "allow_list.txt". The restricted content will no longer be accessible to any IP addresses that were removed from the allow list. To rewrite the file, I appended the .write() function to the file object file that I identified in the with statement. I passed in the ip_addresses variable as the argument to specify that the contents of the file specified in the with statement should be replaced with the data in this variable. <br />
<br />
<p align="center">
<img src="https://github.com/DanielYoon82/UpdateFileWithPython/blob/main/images/write.1.jpg" height="52%" width="52%" alt="Disk Sanitization Steps"/>
</p> 
<br />
<br />
<b>Summary</b> <br/>
This algorithm was created to remove IP addresses identified in the  remove_list variable from a file of approved IP addresses. The  algorithm involved opening the file, converting it to a string to be read, and then converting this string to a list stored in the variable ip_addresses. I then navigated through the IP addresses in remove_list. With each iteration, I reviewed the element that was part of the ip_addresses list. If it was, I applied the .remove() method to it to remove the element from ip_addresses..Finally, I used the .join() method to convert the ip_addresses back into a string so that I could write over the contents of the "allow_list.txt" file with the revised list of IP addresses.
<br />
<br />
