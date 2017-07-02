# LearnForDlibOnUbantu
<br/>This repository is for my learning for the ['Dlib C++ Library'](http://dlib.net/) on Ubantu16.04 .
<br/>I want to make `HARDWARE OPTIMIZATION` for some of functions in this lib .
<br/>The Library has already done some of the optimizations ,such as using the SSE, SVX instructions.
<br/>Of course,your CPU has to be under the support of it.That is to say, your CPU has to be after year 2011.
<br/>I'm a beginner of developing of C++ on Linux ,so by this time,I will mark down the record my learing progress.
<br/>My English is poor(:,so if you notice that there are syntax errors or somewhere that causes ambiguity,email me!
<br/>My e-amil is 1324634934@qq.com .I'm in Southeast University's Software engineering for junior by now.
<br/>The purpose for this is to help you be familiar with basic operations for `Ubantu`, its `bash` and `GUN`.
<br/>So that you can get into the way faster!!!

---
## 1.Something you should do after installing the Ubantu system!
<br/>If you are familiar with the Ubantu,just please [skip]() it.
### 1.1 Learn to use `bash`
<br/>The book I used to learn `bash` is [The Command Line Crash Course](),I will upload it if it doesn't violate the rules.
<br/>So now ,I will only show you some useful commands.If you wants more,follow the book I mentioned above.
<br/>All the `>` before the command is to show the same `$` before your bash when you type characters.
<br/>So you don't have to type it.
<br/>pwd,mkdir,cd,ls,rm,sudo
#### 1.1.1 pwd
```Bash
$ pwd # print working directory
```
<br/>It will show you the current directory your bash is in.
<br/>It can be used when you want to copy the current file's diectory. 

---
#### 1.1.2 mkdir
```Bash
$ mkdir "I am a coder!" # make a directory names "I am a coder!"
```
<br/>You can create a new directory just on your current directory.
<br/>If my current directory is "/home/chengzhi" ,and then ,the new directory will be "/home/chengzhi/I am a coder!"
<br/>Attention to the `"` double quotation mark.
<br/>If the direction's name you want to make contains ` ` white space,you have to use the `"` to encircle the name.
<br/>Therefore if you want to make a directory without white space in its name,you can just type below:
```Bash
$ mkdir I_am_a_coder! # make a directory names "I_am_a_coder!"
```

---
#### 1.1.3 cd
```Bash
$ cd "I am a coder!" # change directory to "I am a coder!"
$ pwd # /home/chengzhi/Desktop/I am a coder!
$ cd ../ # return to the father directory
$ pwd # /home/chengzhi/Desktop
$ cd I_am_a_coder! # change directory to "I_am_a_coder!"
$ pwd # /home/chengzhi/Desktop/I_am_a_coder!
$ cd .. # the same meaning as cd ../
$ pwd # /home/chengzhi/Desktop
```
<br/>The "/home/chengzhi/Desktop" is my current working directory,it can be different to you,but it doesn't matter.
<br/>The `"` double quotation mark 's use is same when you use `directory` means.
<br/>You can use the below to goto the father's father directory (if it is turly exists) by add .. and seperate them with `/`.
```Bash
$ pwd # /home/chengzhi/Desktop/dlib-19.4/examples/build
$ cd ../../ # goto the father's father directory
$ pwd # /home/chengzhi/Desktop/dlib-19.4
$ cd ../../../ # goto the father's father's father directory
$ pwd # /home
```
<br/>You can add `../` as much as you like. 

---
#### 1.1.3 ls
```Bash
$ ls # list directory
$ ls -a # list all in current directory
$ ls -R # list directory recusively including son's directory and son's son's son and so on
```
<br/>You can use the above `cd` command to goto diffenent directory and use `ls` command to see the directorys in it.
### 1.2 Give your account `root` access

## 2.Begin with the Dlib!
### DownLoad
