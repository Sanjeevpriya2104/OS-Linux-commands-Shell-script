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
<img width="618" height="299" alt="Screenshot 2025-09-07 135530" src="https://github.com/user-attachments/assets/a3f9c88a-7cc4-4d73-8438-05e425ad5046" />



cat < file2
## OUTPUT
<img width="623" height="293" alt="Screenshot 2025-09-07 135545" src="https://github.com/user-attachments/assets/8d3277c2-8414-4d95-90bb-0d6205b21196" />


# Comparing Files
cmp file1 file2 comm file1 file2
## OUTPUT
 <img width="937" height="279" alt="Screenshot 2025-09-07 135603" src="https://github.com/user-attachments/assets/26a03002-ff3a-4214-a93d-7cfd26890a3d" />

diff file1 file2
 ## OUTPUT
<img width="834" height="329" alt="Screenshot 2025-09-07 135616" src="https://github.com/user-attachments/assets/a92e586d-1470-4544-866a-a76557d4a3c8" />


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
<img width="708" height="77" alt="Screenshot 2025-09-07 135635" src="https://github.com/user-attachments/assets/ec646b6d-9c7a-4ea2-911f-7da828a0a251" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="704" height="135" alt="Screenshot 2025-09-07 135645" src="https://github.com/user-attachments/assets/58da9358-974c-446a-999f-aeb7e755a674" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="704" height="121" alt="Screenshot 2025-09-07 135654" src="https://github.com/user-attachments/assets/2d7548b4-fdd1-4a75-adb6-ccdafac0b0f1" />


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



grep hello newfile 
## OUTPUT




grep -v hello newfile 
## OUTPUT



cat newfile | grep -i "hello"
## OUTPUT
<img width="706" height="68" alt="Screenshot 2025-09-07 140714" src="https://github.com/user-attachments/assets/f46eab18-bd38-46d5-bf55-fe3fb0d75edd" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="703" height="61" alt="Screenshot 2025-09-07 140723" src="https://github.com/user-attachments/assets/33775bb5-135b-48bb-8f9f-0d7617cfc48e" />




grep -R ubuntu /etc
## OUTPUT
<img width="1260" height="873" alt="Screenshot 2025-09-07 140743" src="https://github.com/user-attachments/assets/585bdca0-4cf2-4f01-a0cd-3d8304b8eb37" />



grep -w -n world newfile   
## OUTPUT



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
<img width="1262" height="91" alt="Screenshot 2025-09-07 140802" src="https://github.com/user-attachments/assets/d00638e6-a4e3-4a1a-8f63-bb90987f30ce" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="1257" height="85" alt="Screenshot 2025-09-07 140835" src="https://github.com/user-attachments/assets/be25b099-17e2-46b9-8a63-ad4a086211cf" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="1260" height="87" alt="Screenshot 2025-09-07 140847" src="https://github.com/user-attachments/assets/7d413cb7-7c0d-4cd6-89d8-35a505b7731c" />




egrep '(^hello)' newfile 
## OUTPUT

<img width="1257" height="72" alt="Screenshot 2025-09-07 140902" src="https://github.com/user-attachments/assets/27eb6200-3678-4b4a-b126-8f1ee37e1ea9" />



egrep '(world$)' newfile 
## OUTPUT

<img width="1053" height="75" alt="Screenshot 2025-09-07 140918" src="https://github.com/user-attachments/assets/03cd77b8-fd8a-4705-ad9e-d594a21bef4c" />



egrep '(World$)' newfile 
## OUTPUT

<img width="1088" height="100" alt="Screenshot 2025-09-07 140945" src="https://github.com/user-attachments/assets/7e3ee3b7-163e-4dc1-931f-f775501803a9" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="1263" height="83" alt="Screenshot 2025-09-07 140959" src="https://github.com/user-attachments/assets/0485a604-9d0a-4a64-8b02-5b563851dfe8" />



egrep '[1-9]' newfile 
## OUTPUT


<img width="914" height="61" alt="Screenshot 2025-09-07 141017" src="https://github.com/user-attachments/assets/ea242469-5203-4064-bd33-95bb078e8683" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="1263" height="87" alt="Screenshot 2025-09-07 141929" src="https://github.com/user-attachments/assets/ea1afbb6-ea7f-4fc1-8df5-7ddaaec64a94" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="1257" height="84" alt="Screenshot 2025-09-07 141939" src="https://github.com/user-attachments/assets/bf8f4642-c3e3-4220-81ba-95fa8d3613c8" />


egrep l{2} newfile
## OUTPUT


<img width="1141" height="71" alt="Screenshot 2025-09-07 141948" src="https://github.com/user-attachments/assets/d29890d2-2ec4-4225-9690-010389d80cfd" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="1253" height="99" alt="Screenshot 2025-09-07 141958" src="https://github.com/user-attachments/assets/0ce89b37-7a98-445d-ad35-6f6f011c9ade" />


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

<img width="1240" height="75" alt="Screenshot 2025-09-07 142012" src="https://github.com/user-attachments/assets/1f08d0a1-83fb-40ff-8408-ac7e3008e9d8" />



sed -n -e '$p' file23
## OUTPUT

<img width="1215" height="73" alt="Screenshot 2025-09-07 142023" src="https://github.com/user-attachments/assets/ca103e9c-90be-4669-8f9e-2c975cb00dde" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="1261" height="194" alt="Screenshot 2025-09-07 142038" src="https://github.com/user-attachments/assets/40f86d22-fa0d-4170-98f6-99277c7acff4" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT


<img width="1090" height="252" alt="Screenshot 2025-09-07 142051" src="https://github.com/user-attachments/assets/58820a19-5590-4f92-b65d-b873fd642c77" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="1265" height="191" alt="Screenshot 2025-09-07 142104" src="https://github.com/user-attachments/assets/275c3c7a-5c33-4953-965f-44660544b29b" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="1318" height="142" alt="Screenshot 2025-09-07 142112" src="https://github.com/user-attachments/assets/c3199003-f9ef-4d56-af0b-ab51a1606318" />



sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="1239" height="96" alt="Screenshot 2025-09-07 142125" src="https://github.com/user-attachments/assets/0089c6b3-b191-4fb9-b914-8a29cc1b6c72" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="1215" height="90" alt="Screenshot 2025-09-07 142136" src="https://github.com/user-attachments/assets/c6d79aba-b65b-486a-8142-ec084c526fa3" />



seq 10 
## OUTPUT

<img width="1196" height="225" alt="Screenshot 2025-09-07 142647" src="https://github.com/user-attachments/assets/11e7f8fc-7d7e-41a9-9f5d-53890d1d32f0" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="1195" height="102" alt="Screenshot 2025-09-07 142708" src="https://github.com/user-attachments/assets/ff53426e-6250-472c-a160-6a88a830f848" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="1094" height="114" alt="Screenshot 2025-09-07 142725" src="https://github.com/user-attachments/assets/5b88ae4e-dca1-4ec9-b353-23cb2226a5dd" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="1224" height="123" alt="Screenshot 2025-09-07 142738" src="https://github.com/user-attachments/assets/7642e4f2-e771-406c-af7a-d43589e99b4d" />



seq 2 | sed '2i hello'
## OUTPUT

<img width="1161" height="107" alt="Screenshot 2025-09-07 142750" src="https://github.com/user-attachments/assets/b56b91c1-7bc6-4ab1-9fd2-1697425310c5" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="1185" height="109" alt="Screenshot 2025-09-07 142759" src="https://github.com/user-attachments/assets/636dee65-51b9-4bfc-ba5b-6ae11e93e966" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="1246" height="111" alt="Screenshot 2025-09-07 142812" src="https://github.com/user-attachments/assets/04fb92f7-48dd-4883-b6ba-a22eda326cd2" />



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
<img width="1237" height="99" alt="Screenshot 2025-09-07 142822" src="https://github.com/user-attachments/assets/ddb51fce-1503-4661-894c-d82683dabd72" />


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
<img width="1045" height="163" alt="Screenshot 2025-09-07 142832" src="https://github.com/user-attachments/assets/c479fc2e-e993-482f-afc4-fb9ac2c2b973" />


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
<img width="991" height="107" alt="Screenshot 2025-09-07 142842" src="https://github.com/user-attachments/assets/665f572e-55bb-47d1-899b-b266c77ade79" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="1119" height="110" alt="Screenshot 2025-09-07 142853" src="https://github.com/user-attachments/assets/c2bc2d38-fa96-4ec7-a8a3-81a950c7cd20" />
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="1125" height="261" alt="Screenshot 2025-09-07 142908" src="https://github.com/user-attachments/assets/56e62108-98a0-485f-8ba3-e0d30ef5b211" />
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


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
<img width="810" height="867" alt="Screenshot 2025-09-06 172904" src="https://github.com/user-attachments/assets/ef505062-5da5-4ca6-a8e3-3fe6ad19a8d8" />

 
ls file1
## OUTPUT
<img width="810" height="867" alt="Screenshot 2025-09-06 172904" src="https://github.com/user-attachments/assets/85e290af-f254-4153-bf26-b98cbd1d8393" />

echo $?
## OUTPUT 

 <img width="549" height="75" alt="Screenshot 2025-09-06 172957" src="https://github.com/user-attachments/assets/5879461a-3eaa-46a9-bf88-2c629b48f714" />
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="549" height="75" alt="Screenshot 2025-09-06 172957" src="https://github.com/user-attachments/assets/c70cfa0d-5a69-4dd7-9333-ec4f673a92e5" />


abcd
 
echo $?
 ## OUTPUT
<img width="594" height="80" alt="Screenshot 2025-09-06 173102" src="https://github.com/user-attachments/assets/12f6710c-1a28-42dd-82eb-3cad70c5315d" />

 
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
<img width="911" height="443" alt="Screenshot 2025-09-06 173144" src="https://github.com/user-attachments/assets/27dbadfc-8359-4c5c-9347-6a5866eabfae" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="775" height="139" alt="Screenshot 2025-09-06 173217" src="https://github.com/user-attachments/assets/af50e54c-d794-4eb6-a5de-db4b524fa659" />


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
<img width="852" height="350" alt="Screenshot 2025-09-06 173247" src="https://github.com/user-attachments/assets/2ccd8792-3815-4606-8a6c-1439e02b42a2" />

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
<img width="728" height="856" alt="Screenshot 2025-09-06 173344" src="https://github.com/user-attachments/assets/9bcbde1f-c98b-4770-8a4b-c59110eced7c" />


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
<img width="759" height="453" alt="Screenshot 2025-09-06 173456" src="https://github.com/user-attachments/assets/e30dd3ce-e7ad-4107-98ef-a91145d6e356" /

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

<img width="760" height="569" alt="Screenshot 2025-09-06 173532" src="https://github.com/user-attachments/assets/851d918a-fdc2-4826-8e8f-5989901fd67f" />


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
<img width="849" height="548" alt="Screenshot 2025-09-06 173601" src="https://github.com/user-attachments/assets/eab02498-1740-48e2-a54d-d65a5e2142b5" />


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
<img width="870" height="297" alt="Screenshot 2025-09-06 173639" src="https://github.com/user-attachments/assets/ba4e5b1c-4b81-4e0e-ad7b-960b60a7da27" />

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

##OUTPUT

<img width="713" height="354" alt="Screenshot 2025-09-06 173708" src="https://github.com/user-attachments/assets/414926ca-70e7-4f7f-a9e2-2769a1f6ece4" />
 
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

##OUTPUT

<img width="692" height="465" alt="Screenshot 2025-09-06 173943" src="https://github.com/user-attachments/assets/19971575-95ec-443f-aa94-97973491ac27" />
 
 
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
 
 ##OUTPUT
 
 <img width="642" height="314" alt="Screenshot 2025-09-06 174021" src="https://github.com/user-attachments/assets/0abd8c65-c275-450c-8e28-d742cc64e72d" />

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
##OUTPUT
<img width="760" height="406" alt="Screenshot 2025-09-06 174110" src="https://github.com/user-attachments/assets/2db6c81a-b145-4b32-b91d-7c24222c1e2e" />

 
 
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

##OUTPUT

<img width="794" height="368" alt="Screenshot 2025-09-06 174202" src="https://github.com/user-attachments/assets/a3d54332-d76e-4c0a-a067-a69be64d415f" />

 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
##OUTPUT

<img width="689" height="366" alt="Screenshot 2025-09-06 174306" src="https://github.com/user-attachments/assets/c130d607-1627-4ff5-8f57-b72a78f57071" />

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

##OUTPUT

<img width="690" height="365" alt="Screenshot 2025-09-06 174358" src="https://github.com/user-attachments/assets/d045df75-3dd3-4143-8576-e91fc57897c2" />

 
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
##OUTPUT
<img width="690" height="365" alt="Screenshot 2025-09-06 174358" src="https://github.com/user-attachments/assets/3e429ed6-a4f9-400e-af46-7544b8c2be93" />


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
<img width="656" height="353" alt="Screenshot 2025-09-06 174558" src="https://github.com/user-attachments/assets/0c17843c-f99f-4fe5-b494-f68b88f99d20" />

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
<img width="616" height="342" alt="Screenshot 2025-09-06 174630" src="https://github.com/user-attachments/assets/6d11c99f-ae83-44a6-bf9e-6ebcc0934d64" />
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
<img width="535" height="618" alt="Screenshot 2025-09-06 174716" src="https://github.com/user-attachments/assets/f6532c12-d3f8-48f6-a55b-4af90e9d3b0a" />

 
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
$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 ## OUTPUT
 <img width="842" height="438" alt="Screenshot 2025-09-06 174827" src="https://github.com/user-attachments/assets/1521f28b-6c7b-4eb2-ba7c-4cd0c11983a0" />
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

 <img width="813" height="471" alt="Screenshot 2025-09-06 174917" src="https://github.com/user-attachments/assets/c03a6432-a215-4c26-a9ad-5c3c94de2ab0" />

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

<img width="523" height="265" alt="Screenshot 2025-09-06 174950" src="https://github.com/user-attachments/assets/74c1aba8-8d48-49c7-b8b5-dc42b8ccd735" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="532" height="262" alt="Screenshot 2025-09-06 175020" src="https://github.com/user-attachments/assets/8b28279e-e613-42c2-9669-99c6c5b898b3" />



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
 ./funcex.sh 

 
 ./funcex.sh 1 2
 
## OUTPUT
<img width="615" height="381" alt="Screenshot 2025-09-06 175122" src="https://github.com/user-attachments/assets/356b3b8c-b123-4f24-9f9b-b59f599b61af" />
 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh
<img width="685" height="593" alt="Screenshot 2025-09-06 175151" src="https://github.com/user-attachments/assets/ae90edd9-d40a-41a1-a587-ee25706cbecf" />

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

<img width="566" height="376" alt="Screenshot 2025-09-06 175248" src="https://github.com/user-attachments/assets/ce08479a-a5b6-4665-b690-529119fedecb" />

$ ./argshift.sh 1 2 3
 
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
 ./argshift.sh 1 2 3
 
 ## OUTPUT
 <img width="682" height="545" alt="Screenshot 2025-09-06 175541" src="https://github.com/user-attachments/assets/275b7485-8fec-4d7c-a887-084326539d75" />

 
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

<img width="617" height="908" alt="Screenshot 2025-09-06 175622" src="https://github.com/user-attachments/assets/a33fd5b3-c014-4c36-9b7b-91f87ca472fc" />

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
<img width="693" height="650" alt="Screenshot 2025-09-06 175658" src="https://github.com/user-attachments/assets/aef21498-c69b-4ec1-b9ef-eb80acfb2c39" />


# RESULT:
The Commands are executed successfully.
