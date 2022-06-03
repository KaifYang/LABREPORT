**I used vimdiff to compare the result files and found the difference**

***

![5 1](https://user-images.githubusercontent.com/103291661/171960148-5f240912-105f-4a17-82b1-bd0239d9db37.png)

[Link to file 201](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/201.md)

For test file 201, my implementation was correct because the semicolon next to the brackets should not register the line as a link

![201pre](https://user-images.githubusercontent.com/103291661/171961065-5843ab1d-dc06-48e8-bb7a-c059b917fbfe.png)

The main problem with the implement of course file is that it is not able to find out if there is something inbetween the close braket and open parenthesis.
The file simply detect the open parenthesis where ever it is and take it as effective.
The file should not recognize the link when there is distance between the open parenthesis and close braket.

![201 prob](https://user-images.githubusercontent.com/103291661/171962076-169bc437-1a2c-4a30-9fd7-38b3cc23e0f0.png)


***

![5 2](https://user-images.githubusercontent.com/103291661/171960160-15f688d8-47fb-40a0-8e41-8ddd32183f99.png)

[Link to file 22](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/22.md)

For test file 22, it should return “/bar\* “ti\*tle”, so my file was correct

![22pre](https://user-images.githubusercontent.com/103291661/171961083-64444828-2380-437a-9fa2-8ddb5398bb62.png)

The problem with the code here is that it does not accept links with space in it. However, the markdown file takes whatever is inside the two parenthesis that are in the same line, so I believe the first half of the if statement should be deleted. 

![22 prob](https://user-images.githubusercontent.com/103291661/171962852-2401d9a2-c643-447f-9ae2-8dc11cc04d9a.png)




