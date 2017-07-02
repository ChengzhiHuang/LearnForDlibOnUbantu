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
<br/>The book I used to learn `bash` is [The Command Line Crash Course](https://github.com/ChengzhiHuang/LearnForDlibOnUbantu/blob/ChengzhiHuang-README-Change/Terminal_Crash_Course%20bookmard%20by%20ChengzhiHuang.pdf),I will upload it if it doesn't violate the rules.
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
#### 1.1.4 ls
```Bash
$ ls # list directory
$ ls -a # list all in current directory
$ ls -R # list directory recusively including son's directory and son's son's son and so on
```
<br/>You can use the above `cd` command to goto diffenent directory and use `ls` command to see the directorys in it.

---
#### 1.1.5 rm
```Bash
$ rm a.txt # remove a single file named a.txt
$ rm -R I_am_a_coder! # remove all the I_am_a_coder! 's directories
```
<br/>Be careful when you use this command!You can type `Ctrl` + `c` to interrupt all the commands.

---
#### 1.1.6 sudo
```Bash
$ ls /root # ls: cannot open directory '/root': Permission denied
$ sudo ls /root # that is ok,you need sudo to promote the authority
$ su - # get into the root users.From "chengzhi@chengzhi-platform" to "chengzhi@chengzhi-platform"
$ exit # ruturn to your own users.
```
<br/>If you haven't set your  `root` 's passwd,you cannot went into root,whatever you type for the password!!!
<br/>See it in next section 1.2.

---
### 1.2 Give your account `root` access
#### 1.2.1 Set your `root`'s password
<br/>If you have already set it ,skip it.
```Bash
$ sudo passwd root
```
<br/>For the default settings for Ubantu,root has been .So you have to set the password and then use it.

---
#### 1.2.2 Give your account all authority as `root`
```Bash
$ su - root # change into root 
$ gedit /etc/sudoers # use the txt editor "gedit" to open the file "sudoers"
```
<br/>After you complete above,find the line below:
```Bash
root	ALL=(ALL:ALL) ALL
```
<br/>Add your account just below it , my name is chengzhi ,so i add this.You can add your own.
```Bash
chengzhi	ALL=(ALL:ALL) ALL
```
<br/>After adding , the file may look like this:
```Bash
# User privilege specification
root	ALL=(ALL:ALL) ALL
chengzhi	ALL=(ALL:ALL) ALL
```
<br/>Maybe there will be some output for gedit when you are doing the 1.2.2,regardless of it.
<br/>Finally,restart your computer,and it is done.

---
### 1.3 Install important packages and choose your IDE.
<br/>Such as cmake,git,gnn,g++ and so on.

## 2.Begin with the Dlib!
---
### 2.1 DownLoad the Dlib
<br/>[Click here to download](http://dlib.net/files/dlib-19.4.tar.bz2)
<br/>You can tar it either using the Achieve Manager or tar commands.

---
### 2.2 Build it!
<br/>The official document is [here](http://dlib.net/compile.html).
<br/>First,get `into` the directory of Dlib.

---
### 2.3 Open with Clion 

---
### 2.4 Build it for gprof to analyze
<br/>At first I have to say thanks to my buddies PengFei and JianKang,they gave me a lot of help.
<br/>I use two examples to show how to use gprof.
<br/>If you want to learn more of GNU profiler,you can goto [this article](https://www.ibm.com/developerworks/cn/linux/l-gnuprof.html) given by IBM.

---
#### 2.4.1 The first example

##### 2.4.1.1 Compile the `compress_stream_ex.cpp`
<br/>The first one is compress_string_ex.
<br/>We shall go to the folder Dlib/example .
```Bash
g++ -std=c++11 -O3 -pg -I.. ../dlib/all/source.cpp -lpthread -lX11 compress_stream_ex.cpp -o compress_stream_ex.out
```
<br/>This command is to build and compile the compress_stream_ex.cpp.
<br/>The parameters of g++ is the form of:
```bash
gcc [options] [filenames]
```
<br/>I'll tell you the meaning for each parameter below.
<br/>`-std=c++11` means to use the standard of C++11.
<br/>`-O3` (the big O,not zero) means to optimize for the highest level.\[0-3],zero is the lowest.
<br/>`-pg` means to add some codes to the program so that we can use gprof.
<br/>`-I` (the big i,not 1 nor the right char of k in keyboard)means to to add additional directories to the search path.The below complains more accurate:
>> **[2.3 Search Path](https://gcc.gnu.org/onlinedocs/cpp/Search-Path.html)**
There are a number of command-line options you can use to add additional directories to the search path. The most commonly-used option is -Idir, which causes dir to be searched after the current directory (for the quote form of the directive) and ahead of the standard system directories. You can specify multiple -I options on the command line, in which case the directories are searched in left-to-right order. 

> <br/>So the `-I..` means to search in the father's directory.
<br/>Also,`../dlib/all/source.cpp` means to add the cpp into the search path.

<br/>`-l` (the right char of k in keyboard)means to link to the `.so` file ,and the file name shou follow it.`-lpthread` is the library of `libpthread-stubs0-dev`, `pthread` is its name.`-lX11` is the library of `libX11-dev`,X11 is its name.The library on Ubantu16.04 always have a `-dev` on the tail of the package name.So you can delete the front `lib` and the tail `-dev` .
<br/>`compress_stream_ex.cpp` is the file you want to compile(:finally!!!
<br/>`-o` (the small o,not zero,nor the big O)means the output file's name.If you don't add ,it will generate the `a.out`.
<br/>Auuuuuuuuuuu,this part is over~

---
##### 2.4.1.2 Run the compress_stream_ex.out
<br/>This is a easy part.Just type the below command:
```bash
./a.out -c --in "./faces/testing_with_face_landmarks.xml" --out ./faces/afterCompress
```
<br/>You may see the argument's meaning in [here](http://dlib.net/compress_stream_ex.cpp.html).`-c` means to choose compress function,`--in` shows the file to compress ,`--out` is the output fils's path.

---
##### 2.4.1.3 Get the gprof file and read it
```bash
gprof compress_stream_ex.out gmon.out -p
```
<br/>You will see a lot of outputs.I show you some of it.
>Flat profile:
>Each sample counts as 0.01 seconds.
> no time accumulated

>  %   cumulative   self              self     total           
> time   seconds   seconds    calls  Ts/call  Ts/call  name    
>  0.00      0.00     0.00    72370     0.00     0.00  dlib::entropy_encoder_kernel_2::encode(unsigned int, unsigned int, unsigned int)
>  0.00      0.00     0.00       73     0.00     0.00  non-virtual thunk to dlib::map_kernel_1<std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> >, std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> >, dlib::binary_search_tree_kernel_2<std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> >, std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> >, dlib::memory_manager_kernel_2<char, 10ul>, std::less<std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> > > >, dlib::memory_manager_kernel_2<char, 10ul> >::remove_any(std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> >&, std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> >&)
>  0.00      0.00     0.00       56     0.00     0.00  dlib::text_field::on_mouse_up(unsigned long, unsigned long, long, long)
>  0.00      0.00     0.00       26     0.00     0.00  dlib::auto_mutex::unlock()
>  0.00      0.00     0.00       25     0.00     0.00  dlib::mfp_kernel_1_base_class<4ul>::mp_impl_T<dlib::mfp_kernel_1_base_class<4ul>::mp_null<dlib::mfp_kernel_1_base_class<4ul>::dummy> >::~mp_impl_T()

<br/>You can see the most fequency function is encode() which was called for 72370 times.This way cannot see the tiny time of the function runs.But it is also the way to find the most important part to optimizie the program.You can also run another command to see stack of function information of the program:
```bash
gprof compress_stream_ex.out gmon.out -q
```
<br/>When we wants to optimize , we must find the key function can contribute most to the program,maybe the slowest (comparing to other lib's function for the same facility) and most frequency used ones.This tip is given by JianKang.I think it is a great method and saying whenever I do the optimization work!

---
#### 2.4.2 The second example
##### 2.4.2.1 Compile the `face_detection_ex.cpp`
<br/>When I type as above :
```Bash
g++ -std=c++11 -O3 -pg -I.. ../dlib/all/source.cpp -lpthread -lX11 face_detection_ex.cpp -o face_detection_ex.out
```
<br/>The compiler is success ,but when I run it with :
```Bash
./face_detection_ex.out ./faces/2007_007763.jpg
```
<br/>It tells me `You must #define DLIB_JPEG_SUPPORT and link to libjpeg to read JPEG files.Note that you must cause DLIB_JPEG_SUPPORT to be defined for your entire project.So don't #define it in one file. Instead, use a compiler switch like -DDLIB_JPEG_SUPPORT`.
<br/>So I know to add `-ljpeg` and `-D DLIB_JPEG_SUPPORT` to the compiler.
So I run the command:
```Bash
g++ -std=c++11 -O3 -pg -D DLIB_JPEG_SUPPORT -I.. ../dlib/all/source.cpp -lpthread -lX11 -ljpeg  face_detection_ex.cpp
```
>In function \`dlib::save_jpeg(dlib::array2d<dlib::rgb_pixel, dlib::memory_manager_stateless_kernel_1<char> > const&, std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> > const&, int)':
>source.cpp:(.text+0x3813c): undefined reference to `jpeg_std_error'

<br/>A lot of errors occuered of undefined reference.So after I google it ,I find to install the `libjpeg`
```bash
sudo apt-get install libjpeg-dev
```
<br/>And then ,the commad runs right and successful.
<br/>If you want to deal with other photo type,you shall add it yourself for exercise~

---
##### 2.4.2.2 Run the face_detection_ex.out
<br/>It's the same to 2.4.1.2.The You may see the argument's meaning in [here](http://dlib.net/face_detection_ex.cpp.html).
```Bash
./face_detection_ex.out ./faces/2007_007763.jpg
```
<br/>You can add a list of pictures path to it.

---
##### 2.4.1.3 Get the gprof file and read it
```bash
gprof face_detection_ex.out gmon.out -p
```
<br/>And I find that 61.22% of time is used on `dlib::crc32>::decompress(std::istream&, std::ostream&) const`
<br/>Maybe I'll try to optimize it next week~
