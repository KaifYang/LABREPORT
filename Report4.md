[Link to our team's repository](https://github.com/mdsflyboy/markdown-parser)

[Link to the reviewed repository](https://github.com/Sking56/markdown-parser)


# Expected output

## Snippit 1

![Snippit 1](https://user-images.githubusercontent.com/103291661/169722450-0a12192f-7506-4ea7-b285-2a8d3e9a3d01.png)

## Snippit 2

![Snippit 2](https://user-images.githubusercontent.com/103291661/169722459-b546913c-77b6-4166-a65a-4ad6ca304c38.png)

## Snippit 3

![Sinppit 3](https://user-images.githubusercontent.com/103291661/169722463-46bc8cf2-adf9-4d74-b858-6db92690a15a.png)


# Turned into test

![test](https://user-images.githubusercontent.com/103291661/169723765-fab46ad1-8d3c-4630-b38b-8c6ca1565aa7.png)

# Testing

## Group repo
All three failed 

![group repo fail](https://user-images.githubusercontent.com/103291661/169726723-1fd7920c-0c2a-4498-b97a-ed06af0c6d47.png)
![group repo fail2](https://user-images.githubusercontent.com/103291661/169726727-6d299f40-5042-40be-8dc7-4a7f853d654d.png)



## Review repo
All three failed

![Review repo fail](https://user-images.githubusercontent.com/103291661/169725585-93bf1e70-a1e6-4979-b391-d9bbc491c8ed.png)


# Questions

```
Do you think there is a small (<10 lines) code change that will make your program work for
snippet 1 and all related cases that use inline code with backticks?
If yes, describe the code change. If not, describe why it would be a more involved change.
```

I think a small code change might be able to solve the problem. We can detect the position of backticks just like the 
parentheses and the brackets and then compare its postion relative to those. If the first backtick is outside and the second is 
inside then we are not going to return this weblink.

```
Do you think there is a small (<10 lines) code change that will make your program work for
snippet 2 and all related cases that nest parentheses, brackets, and escaped brackets? 
If yes, describe the code change. If not, describe why it would be a more involved change.
```

I don't think small code change is going to fix the issue because we are not able to determine which one of the parentheses or
bracket is the outmost one since we are taking the md as a whole string. The logic might have to be redesigned for markdown-parse.

```
Do you think there is a small (<10 lines) code change that will make your program work for
snippet 3 and all related cases that have newlines in brackets and parentheses?
If yes, describe the code change. If not, describe why it would be a more involved change.

```
I don't think a small code change is going to fix the issue because you have to be able to detect 
that the link is in another lane. Because we are taking the md down as a string, we are not able
to determine whether the sentence is at this line or the next line. We might have to take the text into
a list where each entry represents a line, but our previous markdown-parser logic will not work anymore.
