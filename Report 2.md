# Lab Report2

## Change 1

![code change diff1](https://github.com/KaifYang/LABREPORT/blob/main/Change1.png)

[Test File](https://github.com/KaifYang/markdown-parser/blob/main/test2.md): Empty file lead to infinite loop.

![output1](https://github.com/KaifYang/LABREPORT/blob/main/Run%201.png)

**Symptom: Error showing huge line numbers**

The Empty file makes the loop in the code keeps on running. This is because the file is empty, and there is no open braket for it to find.

I added a check in the loop so that it will stop if it does not detect any braket.

***

## Change 2


![code change diff2](https://github.com/KaifYang/LABREPORT/blob/main/Change%202.png)

[Test File](https://github.com/KaifYang/markdown-parser/blob/main/test3.md) : The file with the link to image

![output2](https://github.com/KaifYang/LABREPORT/blob/main/Run2.png)

**Symptom: The result should only return web link but the image link is returned**

The loop cannot detect whether the brackets belong to web link or image link, so it will put the link detected in the arraylist anyways.

I added another check in the loop to check if there is a "!" mark before the bracket so that the image link can be regonized and will not be put into the arraylist.

***

## Change 3

![code change diff3](https://github.com/KaifYang/LABREPORT/blob/main/Change3.png)

[Test File](https://github.com/KaifYang/markdown-parser/blob/main/test4.md) : Added a paragraph in a new line in between the two brakets

![output3](https://github.com/KaifYang/LABREPORT/blob/main/Run3.png)

**Sympton: The result returned both link while one of the link is invalid in markdown**

You are nolonger able to click on the link to go to the site because the formatting is wrong, but the link is still returned.

This is because the method only detects the presence of the marks.
I added another check so that if the content between the two braket is too long the link will not be returned.

