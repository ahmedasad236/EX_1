# Exercise1

*   ### **make a directory called LC in your home dir** 
    Done using **(mkdir)** command
---
*   ### **use touch to create a new file called test in your LC dir**
    Done
---
* 
    Done using the following command 
    ```
    $ echo "#!/bin/sh" > test
    
    $ echo "curl --head --silent https://www.google.com/
    " >> test   
    ```
    ```
    I tried this with vim, too
    ``` 

    *  **```Sh```** 
    (or the Shell Command Language) is a programming language described by the POSIX standard. It has many implementations (ksh88, dash, ...).
    
    * **```bash```** 
    : Basically bash is sh, with more features and better syntax. Most commands work the same, but they are different.

___
* ### **try to execute the file, i.e. type the path to the script (./test) into your shell and press enter. Understand why it doesn’t work by consulting the output of ls (hint: look at the permission bits of the file). is it executable ?** 
    It is not exeecutable as the file string is ```-rw-rw-r--``` there is no 'x' that stands for Execution
___
* ### **Run the command by explicitly starting the sh interpreter, and giving it the file test as the first argument, i.e. sh test. Why does this work, while ./test didn’t?**

    We dont have permissionto run test, we are allowed only to run  ```sh```
___
* ### **Look up the chmod program (e.g. use man chmod).**

    **Done**
___ 
* ### **Use chmod to make it possible to run the command ./test rather than having to type sh test. How does your shell know that the file is supposed to be interpreted using sh?**
    ```
    $ chmod u=rwx test
    ```
    ```
    $ ./test
    ```
---
* ### **make a python file called testpy , in the same manner make the file print "hello world" when executing it ./testpy**

    ```
    $ echo "#!/usr/bin/python3" > test.py
    ```
    
    ```
    $ echo "print("Hello, World :)")" >> test.py
    ```

    ```
    $ chmod u=rwx test.py
    ```

    ```
    $ ./test.py
    ```
---
* ### **what is the diiference between > and >> explain with exapmles**

    Using (```>```) to write to the file after deleting every thing in this file.

    Using (```>>```) to write to the file without deleting anything in this file

    **EX: Using ```>```**
    ```
    $ echo "Hello, Hema :)" > test.txt 
    ```

    ```
    $ echo "Hello, Abo Salah :)" > test.txt
    ```
    ```
    $ cat test.txt
    ```
    *The Output will be*
    ```
    Hello, Abo Salah:)
    ```
    ___
    **EX: Using ```>>```**
    ```
    $ echo "Hello, Hema :)" > test.txt 
    ```

    ```
    $ echo "Hello, Abo Salah :)" >> test.txt
    ```
    ```
    $ cat test.txt
    ```
    *The Output will be*
    ```
    Hello, Hema:)
    Hello, Abo Salah:)
    ```
---
* ### **we talked about aliases. it is very common to alias ll to ls -alh How can you do it ?**

   ```
   $ alias ll="ls -alh"
   ```

   ```
    $ ll
   ```  