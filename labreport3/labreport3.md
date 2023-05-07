## Lab Report 3 - Researching Commands

## Overview
Today, we will be exploring deeper into the grep command by learning about 4 interesting command-line options that can be used with the grep command. By going through various examples, we will gain a better understanding of the various ways grep can be used to generate our desired output. I will be going through the examples using the files and directories from ./technical from the following respository: https://github.com/ucsd-cse15l-s23/stringsearch-data.git. Feel free to clone it to your computer to follow along with me! All commands have been referenced from the following website: https://www.geeksforgeeks.org/grep-command-in-unixlinux/#. 

## Using grep command
The grep command, in simplest terms, searches for a specified string inside a specified file and prints the matching lines. For instance, suppose you are currently in ./technical/government/Media directory. Inside that directory, there is a txt file called "Nonprofit_buys.txt". If you want to print all lines containing the string "legal" in that file, you simply need to type in the command `grep "legal" Nonprofit_Buys.txt`. Look at the code snippet below to better understand the grep command!

```
[cs15lsp23fd@ieng6-203]:Media:282$ grep "legal" Nonprofit_Buys.txt
other agencies providing legal help and basic
provider of legal services for Ventura County's poor closer to two 
migrant-worker legal assistance program and a newer basic services
Legal Services, as the county's sole provider of legal help to the
California Rural Legal Assistance has provided legal services to
one-stop legal service facility is a new endeavor for the
other nonprofit leaders to plan out what are the legal needs of the
```

Perhaps, you may also want the line number of the matching lines for various reasons. For instance, you may want to know if a word was used more often earlier in the text file or later in the text file. In such cases, use -n along with the grep command. For our example, it would be `grep -n "legal" Nonprofit_Buys.txt`. Look at the cope snippet below to better understand -n option for the grep command. 

```
[cs15lsp23fd@ieng6-203]:Media:306$ grep -n "legal" Nonprofit_Buys.txt
7:other agencies providing legal help and basic
14:provider of legal services for Ventura County's poor closer to two
20:migrant-worker legal assistance program and a newer basic services
25:Legal Services, as the county's sole provider of legal help to the
49:California Rural Legal Assistance has provided legal services to
75:one-stop legal service facility is a new endeavor for the
81:other nonprofit leaders to plan out what are the legal needs of the
```

Now suppose you are not really interested in the lines containing the word "legal". You are merely interested in how many times the word "legal" was used in that file. To obtain the number of times a certain word was used, you can use -c along with the grep command. In our case, we would write `grep -c "legal" Nonprofit_Buys.txt` to get the number of times the word "legal" popped up in the file. Look at the code snippet below to better understand -c option for the grep command. 

```
[cs15lsp23fd@ieng6-203]:Media:281$ grep -c "legal" Nonprofit_Buys.txt
7
```

While using the regular grep command to search for lines with a certain word, you may get lines that do not contain words that exactly matches the specified word. For instance, if you do `grep "as" Nonprofit_Buys.txt`, you will get lines that contain the words "assistance", "was", "has", and any other words that contain "as" in it. In order to only get lines that exactly matches your specified string, you can use -w with your grep command. Using the example of "as", we can use the command `grep -w "as" Nonprofit_Buys.txt` to ensure that we only get lines that contain the word "as" and not lines that also contain words like "assistance". 

```
[cs15lsp23fd@ieng6-203]:Media:312$ grep -w "as" Nonprofit_Buys.txt
Legal Services, as the county's sole provider of legal help to the
Padilla said the model of owning a building that functions as a
```

Now suppose you want to find lines that start with a specified word. To do that, you can add ^ in front of the word you are trying to search for. For instance, if we want to find lines that start with the word "The", we can use the command `grep "^The" Nonprofit_Buys.txt`. Look at the code snippet below to better understand how to use ^ with the grep command. 


```
grep "^The" Nonprofit_Buys.txt
The purchase will help meet the organization's long-term plan of
The migrant program generally has taken on issues related to
The purchase of the building on A Street in downtown Oxnard also
The building will be named the Cruz Reynoso Justice Center. It
The organization raised about $60,000 to purchase the A Street
The building also houses five businesses that were already
The idea is to bring together organizations that provide
```

