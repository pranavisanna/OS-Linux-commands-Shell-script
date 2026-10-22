# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > op1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d


```
cat > op2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d

```
### Display the content of the files
cat < file1
## OUTPUT
<img width="435" height="121" alt="image" src="https://github.com/user-attachments/assets/29ec3df2-8fd0-4a4e-867d-fe54d3919406" />





cat < file2
## OUTPUT
<img width="482" height="137" alt="image" src="https://github.com/user-attachments/assets/69c0f26f-da85-4d86-b68d-e7a2d7b53752" />



# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="505" height="46" alt="image" src="https://github.com/user-attachments/assets/697ce4e3-ea22-4c61-b252-2c4a3db88441" />

comm file1 file2
 ## OUTPUT
<img width="547" height="252" alt="image" src="https://github.com/user-attachments/assets/0668f606-4a86-4f85-b146-44d9a97edc87" />

 
diff file1 file2
## OUTPUT
<img width="521" height="236" alt="image" src="https://github.com/user-attachments/assets/472eff77-1739-4608-9dc9-668b76bfcc52" />



#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT

<img width="673" height="255" alt="image" src="https://github.com/user-attachments/assets/0fea25d6-8804-40a6-b64f-df0038555e6c" />




cut -d "|" -f 1 file22
## OUTPUT

<img width="685" height="117" alt="image" src="https://github.com/user-attachments/assets/dbb18ed5-8083-4e92-8e14-802d5be4f1d9" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="657" height="115" alt="image" src="https://github.com/user-attachments/assets/58346380-b5f8-4c20-8293-f6e20a6e1ee3" />

cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
<img width="582" height="49" alt="image" src="https://github.com/user-attachments/assets/748f829b-f62c-49dd-95e7-b8f3df05f00b" />



grep hello newfile 
## OUTPUT
<img width="630" height="47" alt="image" src="https://github.com/user-attachments/assets/11e28491-d93c-48a9-8226-967e78a10021" />




grep -v hello newfile 
## OUTPUT
<img width="577" height="47" alt="image" src="https://github.com/user-attachments/assets/854bb3ae-4502-4010-a99f-fe8102d39a52" />


cat newfile | grep -i "hello"
## OUTPUT
<img width="577" height="47" alt="image" src="https://github.com/user-attachments/assets/1280c0c5-1e7c-49f1-8b01-eb8d452039d4" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="753" height="50" alt="image" src="https://github.com/user-attachments/assets/d0f1a505-e505-4050-bd0d-c128284a4888" />



grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
<img width="654" height="68" alt="image" src="https://github.com/user-attachments/assets/2407c43b-ac0e-4e6c-a356-ed5c1efa21d3" />

cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT
<img width="683" height="71" alt="image" src="https://github.com/user-attachments/assets/b7f03ae4-dd1e-4067-94f0-44240cd10ba9" />




egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="674" height="74" alt="image" src="https://github.com/user-attachments/assets/2033a594-7fd4-458c-ab5f-9756e19df98d" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="760" height="69" alt="image" src="https://github.com/user-attachments/assets/1eedbcaf-f376-458e-ad5a-c3d99b8fe25c" />





egrep '(^hello)' newfile 
## OUTPUT
<img width="605" height="48" alt="image" src="https://github.com/user-attachments/assets/eb069cf5-cd0a-4c06-82ac-f86ae911f128" />


egrep '(world$)' newfile 
## OUTPUT
<img width="940" height="47" alt="image" src="https://github.com/user-attachments/assets/eb10d803-e087-4ba1-9544-63d956ef98c5" />



egrep '(World$)' newfile 
## OUTPUT
<img width="940" height="47" alt="image" src="https://github.com/user-attachments/assets/8569c086-59fa-4ca5-a345-acba60221744" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="940" height="47" alt="image" src="https://github.com/user-attachments/assets/d2720ee5-5d3d-4f06-b6b1-e281c18548c8" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="940" height="26" alt="image" src="https://github.com/user-attachments/assets/137ada6c-e2d4-457c-9768-561f8a6fc4d0" />



egrep 'Linux.*world' newfile 
## OUTPUT

<img width="940" height="35" alt="image" src="https://github.com/user-attachments/assets/c1c8da58-dd40-485b-83fe-e65184f5feba" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="940" height="35" alt="image" src="https://github.com/user-attachments/assets/e2ffe50d-335d-41f9-88a1-b67d4e1276bd" />


egrep l{2} newfile
## OUTPUT

<img width="940" height="35" alt="image" src="https://github.com/user-attachments/assets/a36793a6-c4d5-4575-82e5-142657c379d0" />



egrep 's{1,2}' newfile
## OUTPUT 

<img width="940" height="46" alt="image" src="https://github.com/user-attachments/assets/3d318ce9-bfff-4531-8b9d-104baff8540f" />


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT

<img width="940" height="25" alt="image" src="https://github.com/user-attachments/assets/476db4a1-d5b2-4c05-bcde-1ff30b45b3bc" />



sed -n -e '$p' file23
## OUTPUT



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="940" height="100" alt="image" src="https://github.com/user-attachments/assets/fef9e61d-a082-436b-b37a-37bace3dbbae" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="940" height="100" alt="image" src="https://github.com/user-attachments/assets/8d2c1c45-ef91-4419-ae18-0e29d34b7b03" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="940" height="100" alt="image" src="https://github.com/user-attachments/assets/ce29a338-10bf-4559-a99a-bcde13ee325c" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="940" height="72" alt="image" src="https://github.com/user-attachments/assets/fc2b270f-2599-476f-9954-d6f1dbba285e" />




sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="940" height="49" alt="image" src="https://github.com/user-attachments/assets/51ca4fcc-b997-4598-b392-1352a93a7ab9" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="940" height="38" alt="image" src="https://github.com/user-attachments/assets/0bbb6d1c-13b3-4a97-ae08-c70f01ab842e" />



seq 10 
## OUTPUT

<img width="940" height="126" alt="image" src="https://github.com/user-attachments/assets/c052bcf6-5cc7-4f1d-9ff8-fbe4cd9869ae" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="940" height="50" alt="image" src="https://github.com/user-attachments/assets/9f5ef9c5-7e91-4c16-b19c-e23ed5ed7e77" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="940" height="50" alt="image" src="https://github.com/user-attachments/assets/76bc82cf-bf4b-4c69-ab7f-8a31be945a57" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="940" height="58" alt="image" src="https://github.com/user-attachments/assets/74aa1f63-ce97-4b6b-8d9f-fbecd0baf11f" />



seq 2 | sed '2i hello'
## OUTPUT

<img width="940" height="47" alt="image" src="https://github.com/user-attachments/assets/b4e9cd4a-88ff-4edf-bfcb-20d8b8a38708" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="940" height="50" alt="image" src="https://github.com/user-attachments/assets/1856f671-229b-406d-86f3-d4b78a8b2b95" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="940" height="50" alt="image" src="https://github.com/user-attachments/assets/eb3cf1f1-65b8-4407-8781-ec5ad72421ac" />



sed -n '2,4{s/$/*/;p}' file23


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="940" height="102" alt="image" src="https://github.com/user-attachments/assets/1857109a-f918-4a89-bf5f-525d7d42c3fa" />

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT

<img width="940" height="49" alt="image" src="https://github.com/user-attachments/assets/25afee9b-914c-4088-9ab3-23b4efcd1c8d" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="940" height="49" alt="image" src="https://github.com/user-attachments/assets/707ef46d-f7c2-4d68-9bb6-29b99caff4a2" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="940" height="34" alt="image" src="https://github.com/user-attachments/assets/9cbc0da4-ab2e-4f8b-a846-b44b09d26ce6" />



 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="940" height="103" alt="image" src="https://github.com/user-attachments/assets/abeb60cd-0016-461e-b342-eb6c95c96cca" />


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT

 
ls op1
## OUTPUT

<img width="940" height="25" alt="image" src="https://github.com/user-attachments/assets/9fc7ce67-fe3c-4660-ab63-51aa222fc719" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied

 <img width="940" height="25" alt="image" src="https://github.com/user-attachments/assets/88468e7b-c47b-4392-af4a-1ab3b9305943" />

echo $?
## OUTPUT 
 <img width="940" height="25" alt="image" src="https://github.com/user-attachments/assets/ad8752b9-b0dd-4b99-b979-d345c4ae34a1" />
 
abcd
 
echo $?
 ## OUTPUT
<img width="940" height="112" alt="image" src="https://github.com/user-attachments/assets/8d1daca9-4cb2-4e57-bd11-15ea8d8a493a" />


 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT
<img width="940" height="26" alt="image" src="https://github.com/user-attachments/assets/a08e41ff-dda4-4ef6-8065-21392e848fe3" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="940" height="117" alt="image" src="https://github.com/user-attachments/assets/df75856a-7ab9-487a-ba13-50afdb7449e5" />


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT



# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT


# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 
 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
<img width="940" height="174" alt="image" src="https://github.com/user-attachments/assets/b31fae22-168c-42c9-94e8-88b6a7069413" />

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT
<img width="940" height="174" alt="image" src="https://github.com/user-attachments/assets/9b9ff07f-32aa-4bd9-ad76-55e8dd0a9380" />

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
<img width="940" height="174" alt="image" src="https://github.com/user-attachments/assets/09f435a9-3cf6-4ab2-af79-3195310f81d3" />

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT
<img width="940" height="192" alt="image" src="https://github.com/user-attachments/assets/c22e6151-4d41-46a5-aa96-ac354da93f07" />

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 
cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT
<img width="940" height="118" alt="image" src="https://github.com/user-attachments/assets/f3ca8ec2-b987-4509-84f3-ffc7eafda07d" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 
<img width="966" height="214" alt="image" src="https://github.com/user-attachments/assets/3802d4f1-f1be-42a2-b203-db2aac946c7c" />

 
 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
 <img width="940" height="48" alt="image" src="https://github.com/user-attachments/assets/5878717a-d76d-48a6-85a5-d2a2c36c8c2a" />

cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 
<img width="940" height="148" alt="image" src="https://github.com/user-attachments/assets/adce6900-83b6-4456-beeb-73ac4583fbb3" />

 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
 <img width="940" height="148" alt="image" src="https://github.com/user-attachments/assets/ec06343e-5cd8-4b25-8284-362d87972c6f" />

cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 
<img width="940" height="343" alt="image" src="https://github.com/user-attachments/assets/ec2d6b4b-a46f-4857-b714-d07f60686fc0" />


# RESULT:
The Commands are executed successfully.
