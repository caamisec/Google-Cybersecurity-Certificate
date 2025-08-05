## Project description

At my organization, access to restricted content is controlled with an allow list of IP addresses. The "allow_list.txt" file contains these IP addresses. A separate remove list identifies IP addresses that should no longer have access to this content. I created an algorithm to automatically update the "allow_list.txt" file and remove the IP addresses that should no longer have access.

## Open the file that contains the allow list

For the first part of the algorithm, I opened the "allow_list.txt" file. First, I assigned this file name as a string to the import_file variable:

```python
import_file = "allow_list.txt"
```

Then, I used a with statement to open the file:

```python
with open(import_file, "r") as file:
```

In my algorithm, the with statement is used with the .open() function in read mode to open the allow list file so I can read it. The purpose of opening the file is to access the IP addresses stored in the allow list file. The with keyword helps manage the resources by closing the file automatically after I finish using it. In the code `with open(import_file, "r") as file:`, the open() function has two parameters. The first one identifies the file to import, and the second indicates what I want to do with the file. In this case, "r" means that I want to read it. The code also uses the as keyword to assign a variable named file that stores the output of the .open() function while I work within the with statement.

## Read the file contents

To read the file contents, I used the .read() method to convert it into a string.

```python
with open(import_file, "r") as file:
    ip_addresses = file.read()
```

When using an .open() function that includes the argument "r" for "read," I can call the .read() function inside the with statement. The .read() method converts the file into a string and allows me to read it. I applied the .read() method to the file variable that I identified in the with statement. Then, I assigned the string output of this method to the variable ip_addresses.

This code reads the contents of the "allow_list.txt" file into a string format that allows me to use the string to organize and work with the data in my Python program.

## Convert the string into a list

To remove individual IP addresses from the allow list, I needed it to be in list format. So I used the .split() method to convert the ip_addresses string into a list:

```python
ip_addresses = ip_addresses.split()
```

The .split() function works by converting the contents of a string into a list. The purpose of splitting ip_addresses into a list is to make it easier to remove IP addresses from the allow list. By default, the .split() function splits the text by whitespace into list elements. In this algorithm, the .split() function takes the data stored in the variable ip_addresses, which is a string of IP addresses that are separated by whitespace, and converts this string into a list of IP addresses. To store this list, I assigned it back to the variable ip_addresses.

## Iterate through the remove list

An important part of my algorithm involves going through the IP addresses that are in the remove_list. To do this, I used a for loop:

```python
for element in remove_list:
```

The for loop in Python repeats code for a specified sequence. The purpose of the for loop in a Python algorithm like this is to apply specific code to all elements in a sequence. The for keyword starts the for loop. It is followed by the loop variable element and the keyword in. The keyword in tells Python to go through the sequence remove_list and assign each value to the loop variable element.

## Remove IP addresses that are on the remove list

My algorithm needs to remove any IP address from the allow list, ip_addresses, that is also in remove_list. Because there were no duplicates in ip_addresses, I was able to use the following code to do this:

```python
for element in remove_list:
    if element in ip_addresses:
        ip_addresses.remove(element)
```

First, within my for loop, I created a conditional that checked whether the loop variable element was found in the ip_addresses list. I did this because applying .remove() to elements that were not found in ip_addresses would cause an error.

Then, within that conditional, I applied .remove() to ip_addresses. I passed in the loop variable element as the argument so that each IP address that was in the remove_list would be removed from ip_addresses.

## Update the file with the revised list of IP addresses

As a final step in my algorithm, I needed to update the allow list file with the revised list of IP addresses. To do this, I first needed to convert the list back into a string. I used the .join() method for this:

```python
ip_addresses = "\n".join(ip_addresses)
```

The .join() method combines all items in a list into a string. The .join() method is applied to a string containing characters that will separate the elements in the list once they are joined into a string. In this algorithm, I used the .join() method to create a string from the list ip_addresses so that I could use it with the .write() method when writing to the file "allow_list.txt". I used the string ("\n") as the separator to tell Python to place each element on a new line.

Then, I used another with statement and the .write() method to update the file:

```python
with open(import_file, "w") as file:
    file.write(ip_addresses)
```

This time, I used "w" with the open() function in my with statement. This argument indicates that I want to open a file to write over its contents. When using this argument "w", I can call the .write() function inside the with statement. The .write() function writes string data to a specified file and replaces any existing file content.

In this case, I wanted to write the updated allow list as a string to the file "allow_list.txt". This way, the restricted content will no longer be accessible to any IP addresses that were removed from the allow list. To rewrite the file, I used the .write() function with the file object that I identified in the with statement. I passed in the ip_addresses variable as the argument to specify that the contents of the file should be replaced with the data in this variable.

## Summary

I created an algorithm that removes IP addresses identified in a remove_list variable from the "allow_list.txt" file of approved IP addresses. This algorithm involved opening the file, converting it to a string to be read, and then converting this string to a list stored in the variable ip_addresses. I then went through the IP addresses in remove_list. With each iteration, I checked if the element was part of the ip_addresses list. If it was, I applied the .remove() method to remove the element from ip_addresses. After this, I used the .join() method to convert the ip_addresses back into a string so that I could write over the contents of the "allow_list.txt" file with the revised list of IP addresses.