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
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
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

<img width="435" height="121" alt="image" src="https://github.com/user-attachments/assets/9a597e63-caa9-4625-83bc-c2e3ee1b8029" />


cat < file2
## OUTPUT
<img width="482" height="137" alt="image" src="https://github.com/user-attachments/assets/93ef1482-ce50-418b-b582-77821e72249d" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="505" height="46" alt="image" src="https://github.com/user-attachments/assets/4e7be8fc-8fa7-4144-a021-55905b5b17f7" />

comm file1 file2
 ## OUTPUT

 <img width="547" height="252" alt="image" src="https://github.com/user-attachments/assets/22a598db-a49f-4df4-acb2-31276056dbd2" />

diff file1 file2
## OUTPUT

<img width="521" height="236" alt="image" src="https://github.com/user-attachments/assets/e8ecf655-c12a-4521-9dcb-f7d3ecc77a76" />

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
<img width="673" height="255" alt="image" src="https://github.com/user-attachments/assets/08b1332f-6613-4ff6-b6c1-ac56d8e3f3ff" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="685" height="117" alt="image" src="https://github.com/user-attachments/assets/bfef7927-d9b1-4c79-9c37-392866f0a8b6" />



cut -d "|" -f 2 file22
## OUTPUT

<img width="657" height="115" alt="image" src="https://github.com/user-attachments/assets/a075e33a-6bf0-4f1b-ad54-1f97222d7ab3" />

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

<img width="582" height="49" alt="image" src="https://github.com/user-attachments/assets/498753ff-5c14-4192-b4ae-11664459196d" />


grep hello newfile 
## OUTPUT


<img width="630" height="47" alt="image" src="https://github.com/user-attachments/assets/c2918c72-97c2-4c75-8471-5b80e5008cd9" />


grep -v hello newfile 
## OUTPUT

<img width="577" height="47" alt="image" src="https://github.com/user-attachments/assets/1eb10e4f-bca8-4049-be34-7ab516c8fe25" />


cat newfile | grep -i "hello"
## OUTPUT


<img width="577" height="47" alt="image" src="https://github.com/user-attachments/assets/c3a64b63-6034-4d59-b575-e7cb67ca0076" />


cat newfile | grep -i -c "hello"
## OUTPUT


<img width="753" height="50" alt="image" src="https://github.com/user-attachments/assets/ed969e25-260f-4149-b4a9-6b3bc2d264a3" />


grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
<img width="654" height="68" alt="image" src="https://github.com/user-attachments/assets/c2b322fd-ea10-4d27-a4ed-8db3066d9092" />


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

<img width="683" height="71" alt="image" src="https://github.com/user-attachments/assets/d7ee3296-421d-4ace-af84-d0a62c4363f6" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="674" height="74" alt="image" src="https://github.com/user-attachments/assets/7a68b24d-9e04-42e4-9ce3-e631bcefa88a" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="760" height="69" alt="image" src="https://github.com/user-attachments/assets/bc3c26d8-cc45-4152-8f23-8b24c19bd21c" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="605" height="48" alt="image" src="https://github.com/user-attachments/assets/babb4fc3-08a8-4bf9-83df-62c1d2fafe83" />


egrep '(world$)' newfile 
## OUTPUT

<img width="634" height="94" alt="image" src="https://github.com/user-attachments/assets/27e052b3-ccb2-4eb9-b9b8-8424b237871b" />


egrep '(World$)' newfile 
## OUTPUT

<img width="709" height="95" alt="image" src="https://github.com/user-attachments/assets/a98a3c0d-8ca4-471e-9671-85feebfcb2f2" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="709" height="95" alt="image" src="https://github.com/user-attachments/assets/4bb07639-a962-4091-bb3d-d1927fefc028" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="566" height="53" alt="image" src="https://github.com/user-attachments/assets/44f951b9-f633-4898-91e3-f09f75f327fe" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="686" height="72" alt="image" src="https://github.com/user-attachments/assets/dac4bc16-8ef3-4e97-ae73-2d7fe5ae5419" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="686" height="72" alt="image" src="https://github.com/user-attachments/assets/369716bf-3f5f-44b5-b7e0-ad42a070563c" />


egrep l{2} newfile
## OUTPUT

<img width="704" height="71" alt="image" src="https://github.com/user-attachments/assets/89716999-6c8f-40fb-a160-cfcef31c33e4" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="684" height="92" alt="image" src="https://github.com/user-attachments/assets/865727a4-8adb-4bba-a9c0-51b8cf1188ef" />

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

<img width="595" height="44" alt="image" src="https://github.com/user-attachments/assets/4bf0987d-505d-46bf-977c-69fb956cfd8f" />


sed -n -e '$p' file23
## OUTPUT

<img width="602" height="50" alt="image" src="https://github.com/user-attachments/assets/73909282-9800-43ce-8b52-8b8963302509" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="683" height="212" alt="image" src="https://github.com/user-attachments/assets/11a93b17-cc78-4885-bc0e-abe77030856e" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="696" height="210" alt="image" src="https://github.com/user-attachments/assets/e3a568c0-62bc-4879-bec5-d308a28d3a3b" />

sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="792" height="213" alt="image" src="https://github.com/user-attachments/assets/f7955bdd-e5f8-447f-8d9c-3bec84169385" />

sed -n -e '1,5p' file23
## OUTPUT
<img width="682" height="139" alt="image" src="https://github.com/user-attachments/assets/8d21858a-17ec-47ea-bb61-c0478c8688e8" />

sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="724" height="96" alt="image" src="https://github.com/user-attachments/assets/c5e1e359-9861-4b6e-9cc0-e784a74006b8" />

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="739" height="72" alt="image" src="https://github.com/user-attachments/assets/c1633705-00c0-4949-84dc-a56f5c947ef0" />

seq 10 
## OUTPUT
<img width="513" height="259" alt="image" src="https://github.com/user-attachments/assets/780f53a3-aa8c-4177-9c18-e542c559df97" />

seq 10 | sed -n '4,6p'
## OUTPUT
<img width="604" height="89" alt="image" src="https://github.com/user-attachments/assets/3c250699-b639-4d03-8b30-ca82cf3f9486" />

seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="634" height="92" alt="image" src="https://github.com/user-attachments/assets/786a5355-c0e8-43ef-b197-8f60fc853d5e" />

seq 3 | sed '2a hello'
## OUTPUT
<img width="602" height="118" alt="image" src="https://github.com/user-attachments/assets/5d04f6e9-3337-4949-8a80-790830bc885b" />

seq 2 | sed '2i hello'
## OUTPUT
<img width="629" height="99" alt="image" src="https://github.com/user-attachments/assets/2b444305-18d0-4c7a-812e-91bac6facb44" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="656" height="95" alt="image" src="https://github.com/user-attachments/assets/75226842-1a53-42b2-a55f-af06c6453628" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="752" height="101" alt="image" src="https://github.com/user-attachments/assets/938d6c7b-a5ca-4de0-8f0b-dec8d8345e68" />

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
<img width="756" height="213" alt="image" src="https://github.com/user-attachments/assets/fa36355c-c2ad-419d-80f1-0fc686a9f089" />

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

<img width="706" height="97" alt="image" src="https://github.com/user-attachments/assets/0bb297a7-358c-4b56-b566-2e3657ed7c4d" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="917" height="96" alt="image" src="https://github.com/user-attachments/assets/b909758f-1630-484f-901c-2ceb1ac541df" />


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

 <img width="890" height="54" alt="image" src="https://github.com/user-attachments/assets/603eb9e1-78f1-4320-9b28-c291e42e5806" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="710" height="213" alt="image" src="https://github.com/user-attachments/assets/1ef95bb3-3d27-4834-8439-beb10c9d3485" />

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

 
ls file1
## OUTPUT
<img width="393" height="52" alt="image" src="https://github.com/user-attachments/assets/cab3a4a6-3663-42d5-9537-7f1436c0ca48" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="406" height="42" alt="image" src="https://github.com/user-attachments/assets/dd6c0fbc-ffbb-4410-b132-6a2d6663ce18" />

abcd
 
echo $?
 ## OUTPUT

<img width="436" height="93" alt="image" src="https://github.com/user-attachments/assets/1e9cf9fd-dfd4-4a3a-8398-80d6fc2f78ad" />

 
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


<img width="506" height="50" alt="image" src="https://github.com/user-attachments/assets/54938ced-e0ea-4653-889e-a7f9892097f9" />

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="569" height="237" alt="image" src="https://github.com/user-attachments/assets/a063cb23-3a69-43e7-ae1f-d8b81592185f" />

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
<img width="647" height="332" alt="image" src="https://github.com/user-attachments/assets/80e15ca1-dc00-47d7-a676-82c2ac98a994" />

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
<img width="669" height="332" alt="image" src="https://github.com/user-attachments/assets/830f85af-e35b-47e4-818b-ae757b2e1394" />

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

 <img width="626" height="602" alt="image" src="https://github.com/user-attachments/assets/cfce0ce3-2bb4-4c12-b891-cfe092640232" />

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
<img width="909" height="559" alt="image" src="https://github.com/user-attachments/assets/1abf3c50-592a-4620-97d0-de4d3ec82d59" />

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

 <img width="909" height="559" alt="image" src="https://github.com/user-attachments/assets/380e6259-1552-4163-8571-e8f948384a6e" />

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
<img width="604" height="243" alt="image" src="https://github.com/user-attachments/assets/c0351bc4-c15f-4537-8694-57368e06a0e1" />


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

 <img width="751" height="441" alt="image" src="https://github.com/user-attachments/assets/0a3b4c5b-fff2-4869-893f-4085b2ac4b8f" />

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
 <img width="775" height="555" alt="image" src="https://github.com/user-attachments/assets/da79d991-f629-4d73-b28f-78be868232b5" />

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
 
 <img width="718" height="824" alt="image" src="https://github.com/user-attachments/assets/e5b6e305-0b4c-4a17-b31d-3efde0cff220" />

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
 <img width="741" height="720" alt="image" src="https://github.com/user-attachments/assets/badfa1dd-9d63-44b8-b6dc-05821ffe8fa0" />


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

# RESULT:
The Commands are executed successfully.
