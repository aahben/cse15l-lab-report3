Week 5 Lab Report

**Syntax**

`find [-H] [-L] [-P] [path...] [expression]`

**find**

1. 
`-user name`
Prints all file in given location if file belongs to given username 
Input: find technical//911report/ -user Ben

Output:
```
technical//911report/
technical//911report//chapter-13.4.txt
technical//911report//chapter-13.5.txt
technical//911report//chapter-13.1.txt
technical//911report//chapter-13.2.txt
technical//911report//chapter-13.3.txt
technical//911report//chapter-3.txt
technical//911report//chapter-2.txt
technical//911report//chapter-1.txt
technical//911report//chapter-5.txt
technical//911report//chapter-6.txt
technical//911report//chapter-7.txt
technical//911report//chapter-9.txt
technical//911report//chapter-8.txt
technical//911report//preface.txt
technical//911report//chapter-12.txt
technical//911report//chapter-10.txt
technical//911report//chapter-11.txt
```

<img width="548" alt="Screen Shot 2022-10-31 at 10 27 59 AM" src="https://user-images.githubusercontent.com/114449002/199071421-54d623fc-59e6-4913-89ed-54624a0a3612.png">

2. 
`-iname`
By default, the find command is case sensitive, however, using -iname we can force command to be case-insensitive
This can be helpful when wanting search to be case-insensitive. 
Input: find technical/ -iname RR172.txt
Output: technical//biomed/rr172.txt

<img width="538" alt="Screen Shot 2022-10-31 at 10 36 03 AM" src="https://user-images.githubusercontent.com/114449002/199072589-9be039e9-d7f2-4402-9c12-a632a4141da9.png">

3. 
`-empty`
Find all empty files in a particulary directory 
Prior to utilizing this command, I created a empty file and this command was able to return the file to me. 
Input: find . -empty
Output: ./empty.txt

<img width="669" alt="Screen Shot 2022-10-31 at 10 39 53 AM" src="https://user-images.githubusercontent.com/114449002/199073321-f126f1fc-a742-42cd-918e-543f6d66906d.png">

<img width="442" alt="Screen Shot 2022-10-31 at 10 37 55 AM" src="https://user-images.githubusercontent.com/114449002/199072940-df808ec7-123e-4194-a786-5404e2c10672.png">


**grep**

1. 
`--colour[=WHEN], --color[=WHEN]`
Displays files that contains the matching strings and surrounds the matching strings in color on the terminal. (WHEN is never, always, or auto.)

This allows searching to be easier identified. 

Input: grep "1478" find-results.txt --color
Output: 
```
technical/biomed/1478-7954-1-3.txt
technical/biomed/1478-1336-1-4.txt
technical/biomed/1478-1336-1-2.txt
technical/biomed/1478-1336-1-3.txt
```

<img width="567" alt="Screen Shot 2022-10-31 at 10 12 22 AM" src="https://user-images.githubusercontent.com/114449002/199068031-b539bd0a-4eda-46b1-bc19-e195e86c0054.png">

2. 
`-c, --count`
Supress normal output and print count of matching lines for each input file. 
This is helpful when trying to get the count of files with matching strings immediately
Input: grep "1478" find-results.txt -c
Output: 4

<img width="570" alt="Screen Shot 2022-10-31 at 10 18 16 AM" src="https://user-images.githubusercontent.com/114449002/199069086-151059db-19ec-4d29-b870-4b0615e5ff32.png">

3. 
`-v`
Prints out non-matching files, prints out files that does not contains the given string
This is useful when trying to find the files that does not contains the given strings. 

Input: grep ".txt" find-results.txt -v
Output: 
```
technical
technical/government
technical/government/About_LSC
technical/government/Env_Prot_Agen
technical/government/Alcohol_Problems
technical/government/Gen_Account_Office
technical/government/Post_Rate_Comm
technical/government/Media
technical/plos
technical/biomed
technical/911report
```

<img width="514" alt="Screen Shot 2022-10-31 at 10 21 13 AM" src="https://user-images.githubusercontent.com/114449002/199069698-cf1ab3ae-d8ef-4a23-b75b-c087fab2c413.png">

4. 
`--V, --version`
Outputs the version of grep and exits.
This may be helpful in getting the version number of grep. 

Input: grep ".txt" find-results.txt --v
Output: grep (BSD grep, GNU compatible) 2.6.0-FreeBSD

<img width="527" alt="Screen Shot 2022-10-31 at 10 24 16 AM" src="https://user-images.githubusercontent.com/114449002/199070308-4be2cca7-86ed-4221-b0f3-85c02f6e08b2.png">

**less**

1. 
`-f or --force`
Forces non-regular files to be opened and supress warning message when binary file is opened. 

Input:

<img width="441" alt="Screen Shot 2022-10-31 at 9 58 47 AM" src="https://user-images.githubusercontent.com/114449002/199065402-4de1633f-eacb-41f0-8b40-76682653bf3a.png">

Output: 
```
The technical/ directory is a subdirectory of
https://anc.org/data/oanc/download/
~
~
~
~
~
(END) - Next: -f
```

<img width="402" alt="Screen Shot 2022-10-31 at 9 58 22 AM" src="https://user-images.githubusercontent.com/114449002/199065460-ea30c6df-4af5-4c76-8116-dbe9b77cc257.png">

<img width="404" alt="Screen Shot 2022-10-31 at 9 58 26 AM" src="https://user-images.githubusercontent.com/114449002/199065474-97634df5-5c43-4786-8cb4-556d423586c7.png">

2. 
`less -N filename`
Input: less -N find-results.txt
Output: 
Shows line numbers when launching program 
This can be helpful when wanting the files within to be numbered for counting to be easier
<img width="617" alt="Screen Shot 2022-10-31 at 10 43 11 AM" src="https://user-images.githubusercontent.com/114449002/199074421-eb3622ea-5425-434c-8688-96832a177d4f.png">

<img width="482" alt="Screen Shot 2022-10-31 at 10 43 52 AM" src="https://user-images.githubusercontent.com/114449002/199074140-5719aef8-b166-45c1-a8dc-2acb9e9f5c74.png">

3. 
`-E`
Input: less -E find-results.txt
Less automatically exits upon reaching end of file 
After scrolling to the end of the file, less is automatically exited in terminal. 

After entering input: 
<img width="564" alt="Screen Shot 2022-10-31 at 10 51 48 AM" src="https://user-images.githubusercontent.com/114449002/199075632-8eb03d15-7180-4f88-87b3-952aea0485ae.png">

After scrolling to the end: 
<img width="466" alt="Screen Shot 2022-10-31 at 10 51 55 AM" src="https://user-images.githubusercontent.com/114449002/199075664-716856c5-7d64-49a7-aa5d-3543a1215806.png">




