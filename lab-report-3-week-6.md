# Streamlining ssh Configuration

**I edited the .ssh/config file through directly opening it from the open file function in VSCode:**

![1edit](https://user-images.githubusercontent.com/103291661/167342679-3a1a2adb-111d-4f3f-bea8-b100e99a3a28.png)
 
**The ssh command logging me into my account using just the alias I chose:**

![1login](https://user-images.githubusercontent.com/103291661/167342704-abd20187-c7a8-490f-b9a5-dea030b19738.png)

**An scp command copying a file to my account using just the alias I chose:**

![1scp](https://user-images.githubusercontent.com/103291661/167342751-0803b0f1-cb35-4420-a896-e1eecd4e8ff8.png)


***



# Setup Github Access from ieng6

**Where the public key I made is stored on Github:**

![2key](https://user-images.githubusercontent.com/103291661/167342824-bda44438-2b47-4de4-9b5a-52dc38c98e82.png)

**Where the public and private key I made is stored in ieng6:**

![2 key in ieng6](https://user-images.githubusercontent.com/103291661/167342844-374def4a-f3ec-465e-90a0-9bae328468d6.png)

**Running git commands to commit and push a change to Github while logged into my ieng6 account:**

![2 add and commit and push](https://user-images.githubusercontent.com/103291661/167342857-cba4d931-89bb-4739-8e19-c36c67937c22.png)

**Here is [the link to the commit](https://github.com/KaifYang/LABREPORT/commit/e68cdca699cf81e44e5415fda7a418c0682ebbd8)**

***

# Copy whole directories with scp -r

**Copying my whole markdown-parse directory to my ieng6 account:**

![3copying](https://user-images.githubusercontent.com/103291661/167346962-c2405f83-3579-4528-a686-499abd455450.png)

**Logging into my ieng6 account after doing this and compile and run the tests for my repository:**

![3 compile and run tests](https://user-images.githubusercontent.com/103291661/167347067-97f4800c-fb10-485b-af47-f74b39ed2055.png)

**Combining scp, ;, and ssh to copy the whole directory and run the tests in one line:**


![3 runtogether 1](https://user-images.githubusercontent.com/103291661/167347120-0894db2a-cf84-45de-97d8-0e704bcbe3fa.png)
![3 runtogether 2](https://user-images.githubusercontent.com/103291661/167347128-5efc398d-0ce5-4582-8512-9bd7790895bb.png)

