at 2022 twwallow haven studios\
to clarify dtps stands for Data Text Postcompiled Script\

## in code

#### loading data
*load*: loads a file into the object\
*loadEncrypted*: loads an encrypted file\
*txtEncrypted*: parses a encrypted string as a file\
*txt*: parses a string as a file

#### get values from the file 
*getRaw*: gets the exact value of path. is also haow you get strings\
*getNum*: gets the value of the path as a number\
*getBool*: gets the value of path as a boolean\
*getHeadAsArray*: takes in just a section name and returns the entire section as an arraylist of idra

#### insertation
*startSection*: starts a new section\
*insert*: inserts a value into the new section\
*endSection*: ends the section and adds it to the object\
*addSectionArray*: adds a section in the form of an array.  (note that it pushes them as a straight value not a idra)\
*addVarible*: adds a varible

#### compile
compile: compiles and returns a string containing the contents of the object
compileAndEncrypt: compiles then encrypts the string before returning 

## in file

#### varibles
you can declare varibles by using .\
varibles are usualy all uppercase and start with a _\
varibles are global and canot be changed

#### sections
all data must be in a section\
you can declare sections by puting a : in front of the section

#### data
this is were the data is stored\
this entails the name:value

#### escape sequences
datascript has one escape sequence\
the charecter ~ is used to represent a space\
if you want ~ then it must be /~

## example

#### in code -> dtpsTest.cs:
```c#

public class dtpsTest {
    public void main(string[] args) {
        dtps test = (new dtps()).load("hwad.dtsp");

        Console.WriteLine(test.getRaw(":main.hwad"));
    }
}

```

#### in file -> hwad.dtsp:

```
._HELLOWORLD: Hello, ~World!

:main
    hwad: _HELLOWORLD
```
