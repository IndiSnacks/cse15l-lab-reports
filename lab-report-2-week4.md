# Lab Week 4 - Report 2
## by Sahil Gathe
April 24, 2022

# Bug Fix 1: Dealing with Image Files
With this code we olny want web linkes to be outputed when given a ```.md``` file; however the code would also return image lines. To fix this issues we checked for each line and made sure that the line did not begain with a ```!``` which would indicate an image file. 

Here are the change logs form GitHub for ```MarkdownPhaser.java```
![Image](ImagesReport2\Commit1.png)

and [test-file.md](ImagesReport2\test-file.md) which was the file that caused the bug
![Image](ImagesReport2\Commit1_1.png)


# Bug Fix 2: The Infinite Loop
The second bug that we tried to fix was the infinate loop caused leaving an empty line. This was cause by the while loop being ittrated using ```currentIndex = closeParen + 1;```. If there is no ```closingParen``` in the line of code the varible would be just set to ```-1``` and would not allow the code to ittrate out of the while loop. To fix this we just checked to to see if ```closeParen``` was ever set to ```-1``` if so we would break out of the loop. 

Here are the change logs form GitHub for ```MarkdownPhaser.java```
![Image](ImagesReport2\Commit2.png)

and [Testfile2.md](ImagesReport2\test-file2.md) which was used to test the bug 
![Image](ImagesReport2\Commit2_2.png)



# Bug Fix 3: Incorrect Parentheses
The thrid bug we fixed was caused by parentheses being placesed where they were not supposed to be placed. This would cause the loop to again become infinite. This is becuase the varible ```closePeran``` would not actully indicate the end of a line; therefore this would not allow the code to ittrate throught he ```while``` loop correctly. This bug was fixed by making sure the ```closePeran``` was always larger then ```openPeran``` if not the code will break the loop.

Here are the change logs form GitHub for ```MarkdownPhaser.java```
![Image](ImagesReport2\Commit3.png)

and [Testfile3.md](ImagesReport2\test-file3.md) which was used to test the bug 
![Image](ImagesReport2\Commit3_3.png)
