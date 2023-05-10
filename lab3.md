# **Lab Report 3**
In this lab report, I will be researching the 'find' command, and present alternative ways to use this command, with two examples each.
For this lab report, I used two sources:
- Linux Man Page (Die.Net) : [Linux Man Page](https://man7.org/linux/man-pages/man1/find.1.html)
- Chat GPT : [ChatGPT](https://chat.openai.com/)

## **Part 1** `find -name`

`find -name` lets the user find specific files/directories that match what the user inputs. For example, as seen below, are two inputs of `find -name` and the outputs.

````java
$ find -name "*.java"
./DocSearchServer.java
./Server.java
./TestDocSearch.java

````
In the example of above, the input is `find -name "*.java"`. In the output is the list of paths that match the ending of `*.java`. The star at the begining is used to display that there is a path before the `.java`. This makes it easier for the user to find paths that match the ending `*.java`.

````java
$ find .-name "./technical/biomed"
find: ‘.-name’: No such file or directory
./technical/biomed
./technical/biomed/1468-6708-3-1.txt
./technical/biomed/1468-6708-3-10.txt
./technical/biomed/1468-6708-3-3.txt
./technical/biomed/1468-6708-3-4.txt
./technical/biomed/1468-6708-3-7.txt
./technical/biomed/1471-2091-2-10.txt
./technical/biomed/1471-2091-2-11.txt
./technical/biomed/1471-2091-2-12.txt
./technical/biomed/1471-2091-2-13.txt
./technical/biomed/1471-2091-2-16.txt
./technical/biomed/1471-2091-2-5.txt
./technical/biomed/1471-2091-2-7.txt
./technical/biomed/1471-2091-2-9.txt
./technical/biomed/1471-2091-3-13.txt
./technical/biomed/1471-2091-3-14.txt
./technical/biomed/1471-2091-3-15.txt
./technical/biomed/1471-2091-3-16.txt
./technical/biomed/1471-2091-3-17.txt
./technical/biomed/1471-2091-3-18.txt
./technical/biomed/1471-2091-3-22.txt
````
(There are more files that have `./technical/biomed`, but I only displayed a portion of the files that showed up on the lab report). The input is `find .-name "./technical/biomed"`, and the output are all the list of files that match the text `find .-name "./technical/biomed"`. This makes it easier for the user to locate files that include `find .-name "./technical/biomed"`.

## **Part 2** `find -type`

`find -type` outputs a list of files/directories/subdirectories/etc that matches what the user inputs. For example as seen below: 

````java
$ find ./technical/government/Env_Prot_Agen -type f -name "*.txt"
./technical/government/Env_Prot_Agen/1-3_meth_901.txt
./technical/government/Env_Prot_Agen/atx1-6.txt
./technical/government/Env_Prot_Agen/bill.txt
./technical/government/Env_Prot_Agen/ctf1-6.txt
./technical/government/Env_Prot_Agen/ctf7-10.txt
./technical/government/Env_Prot_Agen/ctm4-10.txt
./technical/government/Env_Prot_Agen/final.txt
./technical/government/Env_Prot_Agen/jeffordslieberm.txt
./technical/government/Env_Prot_Agen/multi102902.txt
./technical/government/Env_Prot_Agen/nov1.txt
./technical/government/Env_Prot_Agen/ro_clear_skies_book.txt
./technical/government/Env_Prot_Agen/section-by-section_summary.txt
./technical/government/Env_Prot_Agen/tech_adden.txt
./technical/government/Env_Prot_Agen/tech_sectiong.txt
````
In the example above, the input is `find ./technical/government/Env_Prot_Agen -type f -name "*.txt"`. `-type f` refers to files, and in the output, there is a list of files that match what I inputted (in this case, the files that have the path `./technical/government/Env_Prot_Agen` with name `*.txt`.
````java
$ find ./technical -type d
./technical
./technical/911report
./technical/biomed
./technical/government
./technical/government/About_LSC
./technical/government/Alcohol_Problems
./technical/government/Env_Prot_Agen
./technical/government/Gen_Account_Office
./technical/government/Media
./technical/government/Post_Rate_Comm
./technical/plos
````
In the example above, the input is find ./technical -type d. `-type d` refers to directories, and in the output, there is a list of directories with subdirectories that match what I inputed (in this case, the directories that are within `./technical`.

## **Part 3** `find -exec`

`-exec` executes an action on the files/directories found by `-find`. Two examples are displayed below.
````java
$ find ./technical/government/Env_Prot_Agen -type f -name "*.txt" -exec rm {} \;
````
The input `find ./technical/government/Env_Prot_Agen -type f -name "*.txt" -exec rm {} \;`. `-exec` executes the remove function, `rm`. This command deleted the files within `./technical/government/Env_Prot_Agen`. I know these files are deleted because if I run 
````java
$ find ./technical/government/Env_Prot_Agen -type f -name "*.txt"
````
none of the files show up since they were deleted from the `-exec` command. This makes it easier for the user to execute different actions on mutiple files/directories
````java
$ find ./technical/911report -type f -name "*.txt" -exec rm {} \;

````
The input `find ./technical/911report -type f -name "*.txt" -exec rm {} \;` executes the remove function, `rm`. This command removes the files within `./technical/911report`

## **Part 4** `find -print`
While similar to `find -name`, which is used to search for files/directories based on their names, `find -print` is displays the pathnames of the matching files/directories. 

````java
$ find ./technical/government/Alcohol_Problems -type f -name "*.txt" -print
./technical/government/Alcohol_Problems/DraftRecom-PDF.txt
./technical/government/Alcohol_Problems/Session2-PDF.txt
./technical/government/Alcohol_Problems/Session3-PDF.txt
./technical/government/Alcohol_Problems/Session4-PDF.txt
````
As seen in the example above, after performing the command, the outputis a display of path names which match the directories I inputed into the input. This is helpful since this shows me a list of the `*.txt` files within the directory I inputed.

````java
$ find ./technical/government/Post_Rate_Comm -type f -name "*.txt" -print
./technical/government/Post_Rate_Comm/Cohenetal_comparison.txt
./technical/government/Post_Rate_Comm/Cohenetal_Cost_Function.txt
./technical/government/Post_Rate_Comm/Cohenetal_CreamSkimming.txt
./technical/government/Post_Rate_Comm/Cohenetal_DeliveryCost.txt
./technical/government/Post_Rate_Comm/Cohenetal_RuralDelivery.txt
./technical/government/Post_Rate_Comm/Cohenetal_Scale.txt
./technical/government/Post_Rate_Comm/Gleiman_EMASpeech.txt
./technical/government/Post_Rate_Comm/Gleiman_gca2000.txt
./technical/government/Post_Rate_Comm/Mitchell_6-17-Mit.txt
./technical/government/Post_Rate_Comm/Mitchell_RMVancouver.txt
./technical/government/Post_Rate_Comm/Mitchell_spyros-first-class.txt
./technical/government/Post_Rate_Comm/Redacted_Study.txt
./technical/government/Post_Rate_Comm/ReportToCongress2002WEB.txt
./technical/government/Post_Rate_Comm/WolakSpeech_usps.txt
````
As seen in the example above, after performing the command, the outputis a display of path names which match the directories I inputed into the input. This is useful if I wanted to view the path names of the different files within the directory I wanted to view in one list.
