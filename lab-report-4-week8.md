# Lab Week 6 - Report 3
## by Sahil Gathe
May 22, 2021

## Links
* [Our Group's Repository](https://github.com/UDXS/markdown-parser)

* [Review Group's Repository](https://github.com/canitry/markdown-parser)

## Expected Outcome

* Snipit 1: ```[url.com, `google.com, google.com, ucsd.edu]```
* Snipit 2: ```[b.com, a.com(()), example.com]```
* Snipit 3: ```[https://www.twitter.com, https://sites.google.com/eng.ucsd.edu cse-15l-spring-2022/schedule, https://cse.ucsd.edu/]```

## Implmentation and Outcomes
### Snipit 1: 
    ```
    @Test
    public void LabTest1() throws Exception {
        ArrayList<String> links = MarkdownParse.getLinks(Files.readString(Path.of("LabReport-Test1.md")));
        String[] expected = {"url.com", "`google.com", "google.com", "ucsd.edu"};

        assertArrayEquals(expected, links.toArray());
    } 
    ```
Review Group's Code: Passed
![Image](ImageReport4\OtherPass.png)

Our Group's Code: Failed
![Image](ImageReport4\FailedTest1.png)

### Snipit 2
    ```
    @Test
    public void LabTest2() throws Exception {
        ArrayList<String> links = MarkdownParse.getLinks(Files.readString(Path.of("LabReport-Test2.md")));
        String[] expected = {"b.com", "a.com(())", "example.com"};

        assertArrayEquals(expected, links.toArray());
    }
    ```

Review Group's Code: Passed
![Image](ImageReport4\OtherPass.png)

Our Group's Code: Failed
![Image](ImageReport4\TestFali2.png)

### Snipit 3
    ```
    @Test
    public void LabTest3() throws Exception {
        ArrayList<String> links = MarkdownParse.getLinks(Files.readString(Path.of("LabReport-Test3.md")));
        String[] expected = {"https://www.twitter.com", "https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule", "https://cse.ucsd.edu/"};

        assertArrayEquals(expected, links.toArray());
    }
    ```

Review Group's Code: Passed
![Image](ImageReport4\OtherPass.png)

Our Group's Code: Failed
![Image](ImageReport4\FailedTest3.png)


## Conclusion
### Snipit 1:

Our code would be able to passe this test with a small change. Our code currently dose not account for a link haveing more then 2 brackets. We would need to ensure that  ```openBracket``` and ```closeBracket``` are the proper bakets in for the link. To do this we would just need to ensure that ```openBracket``` is the first bracket that appears in the line and ```closingBracket``` is the last that appears in the line.

### Snipit 2:

Our code would be able to passe this test with a small change. Our code currently dose not account for a link haveing parentheses within links and the names of links. We would need to ensure that  ```openParen``` and ```closeParen``` are the proper parentheses in for the link. To do this we would just need to ensure that ```openParan``` is the first perenthese after the last bracket that appears in the line and ```closeParan``` is the last perenthese that appears in the line.

### Snipit 3:

This snipit fails for the same reason sinpit 2 fails. Our code  dose not account for a link haveing parentheses within links and the names of links. We sould be able to fix this with a small change which is ensure that ```openParan``` is the first perenthese after the last bracket that appears in the line and ```closeParan``` is the last perenthese that appears in the line.