## Lab Report 3 - Researching Commands

## Overview
Today, we will be exploring deeper into the grep command by learning about 4 interesting command-line options to with the grep command. By going through various examples, we will gain a better understanding of the various ways grep can be used to generate our desired output. I will be going through the examples using the files and directories from ./technical from the following respository: https://github.com/ucsd-cse15l-s23/stringsearch-data.git. Feel free to clone it to your computer to follow along with me! 

## Using grep command
The grep command, in simplest terms, searches for a specified string inside a specified file and prints the matching lines. For instance, suppose you are currently in ./technical/government/Media directory. Inside that directory, there is a txt file called "Nonprofit_buys.txt". If you want to print all lines containing the string "legal" in that file, you simply need to type in the command `grep "legal" Nonprofit_Buys.txt`. Look at the code snippet below to better understand the grep command!

``
[cs15lsp23fd@ieng6-203]:Media:282$ grep "legal" Nonprofit_Buys.txt
other agencies providing legal help and basic

provider of legal services for Ventura County's poor closer to two 
migrant-worker legal assistance program and a newer basic services
Legal Services, as the county's sole provider of legal help to the
California Rural Legal Assistance has provided legal services to
one-stop legal service facility is a new endeavor for the
other nonprofit leaders to plan out what are the legal needs of the
``

Now suppose you are not really interested in the lines containing the word "legal". You are merely interested in how many times the word "legal" was used in that file. To obtain the number of times a certain word was used, you can use -c along with the grep command. In our case, we would write `grep -c "legal" Nonprofit_Buys.txt` to get the number of times the word "legal" popped up in the file. Look at the codes snippet below to better understand -c option for the grep command. 

``[cs15lsp23fd@ieng6-203]:Media:281$ grep -c "legal" Nonprofit_Buys.txt
7
``
https://www.geeksforgeeks.org/grep-command-in-unixlinux/#
