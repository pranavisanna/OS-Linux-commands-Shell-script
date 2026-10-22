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
<img width="634" height="94" alt="image" src="https://github.com/user-attachments/assets/dac02fc2-90fc-4d86-95fb-18188469045b" />




egrep '(World$)' newfile 
## OUTPUT
<img width="709" height="95" alt="image" src="https://github.com/user-attachments/assets/70c27d02-2a11-46dc-8175-51884cbf805d" />


egrep '((W|w)orld$)' newfile 
## OUTPUT


<img width="709" height="95" alt="image" src="https://github.com/user-attachments/assets/51226277-46fa-4327-ad88-259b2a2dd8d3" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="566" height="53" alt="image" src="https://github.com/user-attachments/assets/ad38621c-2781-40c1-95b5-adabacd30112" />




egrep 'Linux.*world' newfile 
## OUTPUT

<img width="686" height="72" alt="image" src="https://github.com/user-attachments/assets/56ae3676-cc51-4640-9473-34ce9195ce74" />


egrep 'Linux.*World' newfile 
## OUTPUT


<img width="686" height="72" alt="image" src="https://github.com/user-attachments/assets/56ae3676-cc51-4640-9473-34ce9195ce74" />

egrep l{2} newfile
## OUTPUT

<img width="704" height="71" alt="image" src="https://github.com/user-attachments/assets/9862bc1c-d1c9-46d3-9d2d-42331ffe7489" />



egrep 's{1,2}' newfile
## OUTPUT 

<img width="684" height="92" alt="image" src="https://github.com/user-attachments/assets/02429e62-c6a9-4443-835c-82d49dff4769" />


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

<img width="595" height="44" alt="image" src="https://github.com/user-attachments/assets/de8f61f1-aa29-4c39-9329-3353268796c0" />



sed -n -e '$p' file23
## OUTPUT

<img width="602" height="50" alt="image" src="https://github.com/user-attachments/assets/5dc3a5f4-179e-4e15-8fb9-f3b3ff9a6a31" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="683" height="212" alt="image" src="https://github.com/user-attachments/assets/8961774d-66c3-4942-aa2b-a4e2b8764fbd" />




sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="696" height="210" alt="image" src="https://github.com/user-attachments/assets/17b26707-fb73-46ba-bdf1-851afac21b3a" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="792" height="213" alt="image" src="https://github.com/user-attachments/assets/97c5370f-58fe-4320-b128-420dfd96db2c" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="682" height="139" alt="image" src="https://github.com/user-attachments/assets/77a1e958-e906-46cf-85f4-0a3f57c867df" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="724" height="96" alt="image" src="https://github.com/user-attachments/assets/ca568c8f-f96e-4f8c-91af-8419521f075b" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="739" height="72" alt="image" src="https://github.com/user-attachments/assets/a6192b4d-66fd-49e6-9cbd-7c8ff36e5833" />



seq 10 
## OUTPUT

<img width="513" height="259" alt="image" src="https://github.com/user-attachments/assets/ff96cb90-d816-4bd9-8f9e-4a3bd4c1aee1" />




seq 10 | sed -n '4,6p'
## OUTPUT

<img width="604" height="89" alt="image" src="https://github.com/user-attachments/assets/471b4dc8-49a9-4b34-9a86-a6ea0cfbf600" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="634" height="92" alt="image" src="https://github.com/user-attachments/assets/fba40d65-9375-4c4a-8602-990a5ff4e554" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="602" height="118" alt="image" src="https://github.com/user-attachments/assets/b7aba2c4-52d4-41a9-bbcc-a406528dd752" />



seq 2 | sed '2i hello'
## OUTPUT

<img width="629" height="99" alt="image" src="https://github.com/user-attachments/assets/c1f7eea0-fedb-41ec-8377-2c082d212bfe" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="656" height="95" alt="image" src="https://github.com/user-attachments/assets/07f1a7a3-495a-4ecb-bf49-6227a928a399" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="752" height="101" alt="image" src="https://github.com/user-attachments/assets/fb1906b6-43d5-43f3-ac53-63b8b6b7182e" />



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

<img width="756" height="213" alt="image" src="https://github.com/user-attachments/assets/97a31431-fcd2-4756-9520-279448640bf0" />


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

<img width="706" height="97" alt="image" src="https://github.com/user-attachments/assets/cb33cfaf-b70a-474a-93eb-e37d6798002b" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="917" height="96" alt="image" src="https://github.com/user-attachments/assets/8fbf2d0c-73c1-40cc-b867-dab66ffabeb6" />



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

<img width="890" height="54" alt="image" src="https://github.com/user-attachments/assets/eddda457-c699-4f07-8388-d62162179d67" />




 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="710" height="213" alt="image" src="https://github.com/user-attachments/assets/4266a675-1695-4783-9f26-d8972629023c" />

cat < scriptest.cash 
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

<img width="393" height="52" alt="image" src="https://github.com/user-attachments/assets/893dd808-80fb-45cf-85d9-f24f7ded916f" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied

 <img width="940" height="25" alt="image" src="https://github.com/user-attachments/assets/88468e7b-c47b-4392-af4a-1ab3b9305943" />

echo $?
## OUTPUT 
 <img width="406" height="42" alt="image" src="https://github.com/user-attachments/assets/b305e9bc-c136-497b-be3f-0fe5851f50cf" />

abcd
 
echo $?
 ## OUTPUT
<img width="436" height="93" alt="image" src="https://github.com/user-attachments/assets/ea86184d-dd24-444a-90d5-0a0f2f9d5791" />


 
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

<img width="506" height="50" alt="image" src="https://github.com/user-attachments/assets/06e397cb-149c-44e0-9431-6616b682905e" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="569" height="237" alt="image" src="https://github.com/user-attachments/assets/7c116c30-6041-4a90-bd8e-5b8dfe17a669" />

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
=<img width="647" height="332" alt="image" src="https://github.com/user-attachments/assets/4670ccf8-4c70-4d6b-8c4b-94765ae4eee6" />


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
<img width="669" height="332" alt="image" src="https://github.com/user-attachments/assets/73c69e62-ba03-4bab-b8c3-19a7c304d694" />

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
<img width="626" height="602" alt="image" src="https://github.com/user-attachments/assets/b417ebec-243f-4a4d-b19a-ffabaf849ed4" />


 
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
<img width="909" height="559" alt="image" src="https://github.com/user-attachments/assets/b48c61bf-f0fb-42d8-bfe2-925a3b7c3e21" />

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
<img width="604" height="243" alt="image" src="https://github.com/user-attachments/assets/5f4eba7d-b7a1-4d38-b980-3f46d7088516" />


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
<img width="751" height="441" alt="image" src="https://github.com/user-attachments/assets/c9d78788-1f74-4e10-9a80-9290077e7317" />

 
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
 
<img width="718" height="824" alt="image" src="https://github.com/user-attachments/assets/1dbbeb1a-2dc3-4b31-a89b-77358755f660" />


 
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
<img width="741" height="720" alt="image" src="https://github.com/user-attachments/assets/29da2b7c-04ca-4f11-8beb-ff84dca69280" />

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
