# Lab Report2

## Change 1


![Change1](https://user-images.githubusercontent.com/103291661/165021281-fd9cc4c5-b46e-4dd0-8bdd-297d97f19a9b.png)


[Test File](https://github.com/KaifYang/markdown-parser/blob/main/test2.md): Empty file lead to infinite loop.


![Run 1](https://user-images.githubusercontent.com/103291661/165021296-0fb5c05f-2549-4960-919a-3f386d53b194.png)

**Symptom: Error showing huge line numbers**

The Empty file makes the loop in the code keeps on running. This is because the file is empty, and there is no open braket for it to find.

I added a check in the loop so that it will stop if it does not detect any braket.

***

## Change 2


![Change 2](https://user-images.githubusercontent.com/103291661/165021326-669eafbc-f90c-423f-b0b3-d0aa71217e62.png)


[Test File](https://github.com/KaifYang/markdown-parser/blob/main/test3.md) : The file with the link to image


![Run2](https://user-images.githubusercontent.com/103291661/165021335-8ecb8fbb-a420-4228-8f80-a021ce9e875c.png)


**Symptom: The result should only return web link but the image link is returned**

The loop cannot detect whether the brackets belong to web link or image link, so it will put the link detected in the arraylist anyways.

I added another check in the loop to check if there is a "!" mark before the bracket so that the image link can be regonized and will not be put into the arraylist.

***

## Change 3


![Change3](https://user-images.githubusercontent.com/103291661/165021352-dfbc40f0-ac2f-4909-bde1-653f33bc0c3d.png)


[Test File](https://github.com/KaifYang/markdown-parser/blob/main/test4.md) : Added a paragraph in a new line in between the two brakets


![Run3](https://user-images.githubusercontent.com/103291661/165021362-1fd419d3-ce09-4395-8954-887a3667f8b6.png)


**Sympton: The result returned both link while one of the link is invalid in markdown**

You are nolonger able to click on the link to go to the site because the formatting is wrong, but the link is still returned.

This is because the method only detects the presence of the marks.
I added another check so that if the content between the two braket is too long the link will not be returned.

