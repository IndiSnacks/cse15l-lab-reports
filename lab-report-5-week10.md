# Lab Week 6 - Report 3
## by Sahil Gathe
June 5, 2022
***
## Test [194](ImageReport5\194.md)

I found that the results were diffenrt by using the ```vimdiff``` command as seen below.

### Expected:
![image](ImageReport5\Expected1.png)

### Actual:
![image](ImageReport5\issue1.png)

### ```my-markdown-parser```: Falied
### ```CSE15l-markdown-parser```: Failed
![img](ImageReport5\fix1.png)

* ```my-markdown-parser``` failed since it checks for barckets by checking charaters. Therefore, if there are a lot of breackts it runs into a index out of bounds error and dose not return anything. 

***
## Test [519](ImageReport5\519.md)

I found that the results were diffenrt by using the ```vimdiff``` command as seen below.

### Expected:
![image](ImageReport5\Expected2.png)

### Actual:
![image](ImageReport5\issue2.png)

### ```my-markdown-parser```: Passed
### ```CSE15l-markdown-parser```: Failed
![img](ImageReport5\fix2.png)

* ```CSE15l-markdown-parser``` failed since it dosen't account for images. Before creating the return arrylist the code should check to see if the link is an img by checking for a ```!``` and excluding that line form the list. 