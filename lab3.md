# **Lab Report 3**
In this lab report, I will be researching the 'find' command, and present alternative ways to use this command, with two examples each.
## **Part 1** `find -name`

`find -name` lets the user find specific files that match what the user inputs by displaying/listing the files. For example, as seen below, are two inputs of `find -name` and the outputs.

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

