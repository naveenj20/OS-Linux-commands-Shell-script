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

<img width="314" height="286" alt="image" src="https://github.com/user-attachments/assets/a4cf251e-16cb-41ef-869b-1f13e8442fa6" />

cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
<img width="298" height="249" alt="image" src="https://github.com/user-attachments/assets/f0c968c3-d726-4cd1-9752-db44bfaccefd" />

### Display the content of the files
cat < file1
## OUTPUT

<img width="302" height="144" alt="image" src="https://github.com/user-attachments/assets/58788c06-3398-46a2-9350-3103ad2012da" />





cat < file2
## OUTPUT

<img width="305" height="179" alt="image" src="https://github.com/user-attachments/assets/5c94f01a-da63-4247-844a-5fec91a10c50" />



# Comparing Files
cmp file1 file2
## OUTPUT

<img width="388" height="82" alt="image" src="https://github.com/user-attachments/assets/ea661486-655a-44aa-b541-feb7b805b6c0" />


comm file1 file2
 ## OUTPUT
<img width="372" height="226" alt="image" src="https://github.com/user-attachments/assets/afa2c66b-49c3-4b54-a76b-04eea534f3af" />


diff file1 file2
## OUTPUT
<img width="300" height="276" alt="image" src="https://github.com/user-attachments/assets/00f721f8-8d46-4a17-977c-1f0d32f2b86a" />


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```

<img width="350" height="105" alt="image" src="https://github.com/user-attachments/assets/07fac215-e63d-418c-979d-88f7f96865a1" />


cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```
<img width="329" height="187" alt="image" src="https://github.com/user-attachments/assets/510dea96-6400-4453-9cf3-abb7bfc33ce8" />


cut -c1-3 file11
## OUTPUT

<img width="311" height="96" alt="image" src="https://github.com/user-attachments/assets/c5623151-a255-490b-a1ba-10c7be473d5c" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="353" height="127" alt="image" src="https://github.com/user-attachments/assets/25632725-683e-4fbc-9983-08e849ef5ce0" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="311" height="129" alt="image" src="https://github.com/user-attachments/assets/1b26279e-9cb8-4ec7-a483-91a0852fb079" />


cat > newfile 
```
Hello world
hello world
^d
````
<img width="304" height="99" alt="image" src="https://github.com/user-attachments/assets/73567518-08ef-490a-bd44-f4717fa31496" />



cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT

<img width="270" height="79" alt="image" src="https://github.com/user-attachments/assets/4f602282-2d16-46ac-9388-3f9ad203b2b4" />


grep hello newfile 
## OUTPUT

<img width="330" height="70" alt="image" src="https://github.com/user-attachments/assets/a72fe63b-c853-4f4d-9e52-f040000a4c5b" />



grep -v hello newfile 
## OUTPUT

<img width="314" height="70" alt="image" src="https://github.com/user-attachments/assets/4ecc65aa-8440-4f93-a9e1-22aace536ce9" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="423" height="96" alt="image" src="https://github.com/user-attachments/assets/aeeb45b4-a55d-4d81-9ddc-1eeb03ead82c" />


cat newfile | grep -i -c "hello"
## OUTPUT

<img width="411" height="80" alt="image" src="https://github.com/user-attachments/assets/0612c0c2-455c-4a6a-984c-4b3252818c7c" />



grep -R ubuntu /etc
## OUTPUT
<img width="1547" height="956" alt="image" src="https://github.com/user-attachments/assets/9dbead5e-2da3-4020-8c9f-db280ea6e591" />



grep -w -n world newfile   
## OUTPUT

<img width="503" height="94" alt="image" src="https://github.com/user-attachments/assets/14780e6a-2983-4a19-ad25-b62d0eb1f6c9" />


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

<img width="350" height="176" alt="image" src="https://github.com/user-attachments/assets/cd10d6fb-5ce6-4d20-a1be-a14401359b5e" />


egrep -w 'Hello|hello' newfile 
## OUTPUT

<img width="519" height="91" alt="image" src="https://github.com/user-attachments/assets/4a07ad99-22b9-42be-a673-c8bcb0e81004" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="385" height="98" alt="image" src="https://github.com/user-attachments/assets/cba4fa99-7c0a-4081-a4ed-fce4dbf997be" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="505" height="97" alt="image" src="https://github.com/user-attachments/assets/d1b07ea9-4ab4-45f5-92b2-cb00884ee660" />

egrep '(^hello)' newfile 
## OUTPUT
<img width="408" height="68" alt="image" src="https://github.com/user-attachments/assets/8b0fa1f6-3553-49f7-8d4a-7266fc02687c" />

egrep '(world$)' newfile 
## OUTPUT
<img width="368" height="95" alt="image" src="https://github.com/user-attachments/assets/536eaa00-3221-45b4-86db-f2e7ff0a459d" />


egrep '(World$)' newfile 
## OUTPUT
<img width="365" height="78" alt="image" src="https://github.com/user-attachments/assets/cdaff955-dbd4-4ef2-b345-8da4859cce56" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="400" height="123" alt="image" src="https://github.com/user-attachments/assets/fceab522-3f71-4e0f-8e3d-1ec2103a7dd4" />

egrep '[1-9]' newfile 
## OUTPUT
<img width="322" height="73" alt="image" src="https://github.com/user-attachments/assets/fdadabd9-eda4-40e3-88eb-85bb36f7c7ba" />

egrep 'Linux.*world' newfile 
## OUTPUT
<img width="414" height="74" alt="image" src="https://github.com/user-attachments/assets/b0ec4988-926b-4e90-9c09-d14907d7ce8e" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="378" height="69" alt="image" src="https://github.com/user-attachments/assets/4780326f-901a-4e5a-a978-6bd7784cc2ad" />


egrep l{2} newfile
## OUTPUT
<img width="340" height="93" alt="image" src="https://github.com/user-attachments/assets/3da44cf0-c812-473d-914f-b8e87af1edd2" />

egrep 's{1,2}' newfile
## OUTPUT 
<img width="377" height="124" alt="image" src="https://github.com/user-attachments/assets/e245f297-7c36-43b7-9e27-38c90728870b" />

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
<img width="462" height="251" alt="image" src="https://github.com/user-attachments/assets/b99900e8-adc7-4f8a-b485-dd8077167a6b" />


sed -n -e '3p' file23
## OUTPUT
<img width="377" height="75" alt="image" src="https://github.com/user-attachments/assets/947ac5b1-f986-4a00-957f-d732d1cca895" />



sed -n -e '$p' file23
## OUTPUT
<img width="329" height="69" alt="image" src="https://github.com/user-attachments/assets/1e1c46ae-d5b3-4dd9-ad79-453661fc1224" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="391" height="247" alt="image" src="https://github.com/user-attachments/assets/bda5d066-6c42-49ac-8c90-e0fa146e9abf" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="508" height="254" alt="image" src="https://github.com/user-attachments/assets/bcb6d7f4-7653-49cd-8820-0ca1b5526491" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="557" height="250" alt="image" src="https://github.com/user-attachments/assets/42856930-304f-48db-8571-75508593ce6a" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="421" height="127" alt="image" src="https://github.com/user-attachments/assets/9c04a073-bd92-40cc-8d2a-6b71268b2dd7" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="459" height="101" alt="image" src="https://github.com/user-attachments/assets/fa4fc5c7-f6ad-4f73-b41a-ba014941f1e1" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="400" height="101" alt="image" src="https://github.com/user-attachments/assets/571b44ec-7db8-4c34-a3a8-49993080f598" />



seq 10 
## OUTPUT
<img width="483" height="302" alt="image" src="https://github.com/user-attachments/assets/73daf071-883d-4a56-aa9e-43a47563a0bf" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="327" height="125" alt="image" src="https://github.com/user-attachments/assets/a05c9b6b-2a74-4e3f-a6d8-0f6f1d28b44a" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="370" height="119" alt="image" src="https://github.com/user-attachments/assets/7b3fbb87-146c-4d0d-894b-71bacefd4ac8" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="385" height="146" alt="image" src="https://github.com/user-attachments/assets/6c1e9b1a-49cd-4051-9eed-a81917e9c1f6" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="377" height="127" alt="image" src="https://github.com/user-attachments/assets/32fbf433-748a-40b0-b53c-fd187ec0864d" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="472" height="126" alt="image" src="https://github.com/user-attachments/assets/cd957c73-c770-4fd1-a370-11d96c268f45" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="487" height="122" alt="image" src="https://github.com/user-attachments/assets/b132e94f-c163-4267-a9a2-0587d1cb1552" />


sed -n '2,4{s/$/*/;p}' file23
<img width="411" height="119" alt="image" src="https://github.com/user-attachments/assets/1b75197c-8b41-464c-b357-ea488a047da7" />


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
```
<img width="412" height="178" alt="image" src="https://github.com/user-attachments/assets/fa8c0532-80e5-45a6-852b-86c866222443" />

sort file21
## OUTPUT

<img width="428" height="176" alt="image" src="https://github.com/user-attachments/assets/439499aa-9a57-4342-8543-fdfb5c09db2c" />


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
```
<img width="334" height="203" alt="image" src="https://github.com/user-attachments/assets/f4ff7088-fb2d-4245-89cb-dcb3ad585910" />


uniq file22
## OUTPUT

<img width="380" height="228" alt="image" src="https://github.com/user-attachments/assets/72ee977e-4855-4ff6-b906-93acb07acb01" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

 <img width="483" height="305" alt="image" src="https://github.com/user-attachments/assets/4d7c3161-0b45-4a2e-adc3-a315e1cddc96" />


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
<img width="336" height="124" alt="image" src="https://github.com/user-attachments/assets/3faaee69-0a68-45be-b9d0-23dccdc5fa27" />

cat urllist.txt | tr -d ' '
 ## OUTPUT
<img width="333" height="131" alt="image" src="https://github.com/user-attachments/assets/125b748c-f58a-45f1-b7a3-cffbc9b84443" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="508" height="126" alt="image" src="https://github.com/user-attachments/assets/7887d718-4710-4158-9e00-0136b4cb313f" />

#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="547" height="914" alt="image" src="https://github.com/user-attachments/assets/d64ff5c4-4657-460c-a5b2-0a4f473a1bb3" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="847" height="865" alt="image" src="https://github.com/user-attachments/assets/ac6db1cd-b34d-477e-b08b-043556c272f6" />


tar -xvf backup.tar
## OUTPUT
<img width="493" height="614" alt="image" src="https://github.com/user-attachments/assets/73efea29-9e91-44f7-824e-9cd31eb87951" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="441" height="72" alt="image" src="https://github.com/user-attachments/assets/33d45938-560b-4ff7-a039-9b6493b1fbb4" />

gunzip backup.tar.gz
## OUTPUT
<img width="1723" height="184" alt="image" src="https://github.com/user-attachments/assets/c2e4271c-28b8-4085-8078-a21cd8803618" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="323" height="345" alt="image" src="https://github.com/user-attachments/assets/b908dd37-294c-4158-97fb-10e5c0bfc2a5" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="396" height="279" alt="image" src="https://github.com/user-attachments/assets/8bf14759-e6a8-4263-b119-e21bc52d250c" />


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

<img width="376" height="330" alt="image" src="https://github.com/user-attachments/assets/89ce9fc9-57c5-4b15-a82e-0d7d9b0bc8e4" />

 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT

<img width="648" height="448" alt="image" src="https://github.com/user-attachments/assets/3c978476-08fc-44b0-b38c-e77832322812" />

 
ls file1
## OUTPUT

<img width="234" height="78" alt="image" src="https://github.com/user-attachments/assets/0fdc5223-bf64-48ab-a9f3-b8f5a3509dbc" />


echo $?
## OUTPUT 

<img width="295" height="68" alt="image" src="https://github.com/user-attachments/assets/8ee896fe-e71f-4ba7-95d7-a6c6f5f56aab" />


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

<img width="295" height="68" alt="image" src="https://github.com/user-attachments/assets/8ee896fe-e71f-4ba7-95d7-a6c6f5f56aab" />

abcd

 
echo $?
 ## OUTPUT

<img width="295" height="68" alt="image" src="https://github.com/user-attachments/assets/8ee896fe-e71f-4ba7-95d7-a6c6f5f56aab" />
 
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

<img width="396" height="276" alt="image" src="https://github.com/user-attachments/assets/fd6e0ff4-d3a9-436b-9027-28cc64b58486" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="643" height="98" alt="image" src="https://github.com/user-attachments/assets/8a785057-f8af-4c43-94c7-8b0d8283d0a6" />


# check file ownership
cat > psswdperm.sh 
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
<img width="608" height="226" alt="image" src="https://github.com/user-attachments/assets/4e6f5919-9452-4f25-aab2-c807a68dd4af" />


./psswdperm.sh
## OUTPUT
<img width="714" height="99" alt="image" src="https://github.com/user-attachments/assets/4c8c88cc-b679-4288-aa78-461313f2f3b0" />

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

<img width="483" height="476" alt="image" src="https://github.com/user-attachments/assets/2ff8c78e-e2a0-49fd-acd9-98f0bee6e368" />


./ifnested.sh 
## OUTPUT

<img width="717" height="152" alt="image" src="https://github.com/user-attachments/assets/329f7109-5fdd-4954-b874-37eea2949fa1" />


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

<img width="616" height="368" alt="image" src="https://github.com/user-attachments/assets/15775690-3bb6-4cb2-a386-65f932456897" />


$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT
<img width="665" height="125" alt="image" src="https://github.com/user-attachments/assets/88a9321e-c11c-459f-87c7-c0692cf64d27" />

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

<img width="583" height="473" alt="image" src="https://github.com/user-attachments/assets/100e1d92-1f06-44e9-b470-9f382bbc9da2" />


$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT
<img width="667" height="199" alt="image" src="https://github.com/user-attachments/assets/83150867-ba69-4a76-8ab9-ae2c82e81348" />

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = kabe ]
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
<img width="633" height="553" alt="image" src="https://github.com/user-attachments/assets/b056c870-584d-4a8e-899c-04a2a1f4eb74" />


$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
<img width="687" height="207" alt="image" src="https://github.com/user-attachments/assets/1053059e-b7cf-4d54-b5f7-f0d38b1ea136" />


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
<img width="549" height="274" alt="image" src="https://github.com/user-attachments/assets/0ac22972-9c32-4e90-aaf4-8777669820a7" />


$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
<img width="692" height="199" alt="image" src="https://github.com/user-attachments/assets/a4e7ef32-856e-4c03-9b0b-81a763ed4765" />


# using the case command
cat >casecheck.sh 
```bash
case $USER in
kabe | Kabe)
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
<img width="620" height="368" alt="image" src="https://github.com/user-attachments/assets/c5b1c158-e5bf-471f-87b1-6624c4b2d353" />

$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
## OUTPUT 
<img width="373" height="126" alt="image" src="https://github.com/user-attachments/assets/7afe7f86-3a0b-442e-86d0-2ecef9df6a47" />


cat > whiletest.sh
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
<img width="382" height="241" alt="image" src="https://github.com/user-attachments/assets/af4fcd59-9d03-4b12-8c2b-8bd5a9f89f37" />

$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
## OUTPUT 
<img width="465" height="349" alt="image" src="https://github.com/user-attachments/assets/ba699ab5-e0bf-427a-b89d-2159d0b89094" />


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
<img width="376" height="218" alt="image" src="https://github.com/user-attachments/assets/babf1daa-58bc-420b-98da-75305a1c48cc" />

$ chmod 755 untiltest.sh
 
 ./utiltest.sh
 ## Output
<img width="549" height="227" alt="image" src="https://github.com/user-attachments/assets/0d604579-e547-4ae6-b14c-19cf80d5b0d1" />

 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 <img width="679" height="202" alt="image" src="https://github.com/user-attachments/assets/a6f56684-0fcc-474a-b173-76082329a53a" />

$ chmod 755 forin1.sh
 
./forin1.sh

## Output

<img width="694" height="304" alt="image" src="https://github.com/user-attachments/assets/a6978693-35ae-44a0-94a9-bc90a693c31f" />

cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```


cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```

<img width="654" height="203" alt="image" src="https://github.com/user-attachments/assets/44f64ddf-4ce1-4d9f-8107-b1475066e377" />

$ chmod 755 forin2.sh
 
$ ./forin2.sh 

## Output
<img width="628" height="223" alt="image" src="https://github.com/user-attachments/assets/a8318d08-cb48-499e-bc43-f68a23ff190e" />


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

<img width="638" height="202" alt="image" src="https://github.com/user-attachments/assets/e719fd5e-d8c0-4c9e-9d79-924fb23829b4" />


## Output

<img width="701" height="303" alt="image" src="https://github.com/user-attachments/assets/8cafb469-8621-4ef8-929d-deeaaef7e6b5" />



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

<img width="452" height="224" alt="image" src="https://github.com/user-attachments/assets/94da23a7-2f23-4045-b7bf-51ee0e47a3da" />

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

<img width="408" height="200" alt="image" src="https://github.com/user-attachments/assets/e0698b74-7109-4026-84a9-aa32aa15e0db" />


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````

<img width="326" height="189" alt="image" src="https://github.com/user-attachments/assets/04de2de3-1f7b-4dbb-9bec-881ed34d1ffd" />

$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
<img width="348" height="223" alt="image" src="https://github.com/user-attachments/assets/b9fb9b8d-0a5e-4ff2-af97-6d33a525147a" />

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
<img width="487" height="203" alt="image" src="https://github.com/user-attachments/assets/6c76a562-6b6e-4eb4-a1f0-8e60e4891944" />

$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT
<img width="319" height="179" alt="image" src="https://github.com/user-attachments/assets/9017f648-6819-416b-bd61-e54fdf5a2ac4" />

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
<img width="365" height="304" alt="image" src="https://github.com/user-attachments/assets/364353fa-1eb3-4beb-8389-7066be2cb9d3" />

$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
<img width="385" height="349" alt="image" src="https://github.com/user-attachments/assets/621ba0a8-44db-49de-8343-9e454881e00b" />

 
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
<img width="459" height="326" alt="image" src="https://github.com/user-attachments/assets/3738aa8b-b8ed-4f70-8a19-3094cb0d4516" />

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 

## Output
<img width="721" height="177" alt="image" src="https://github.com/user-attachments/assets/9c341919-bbd6-48d8-8731-03645b7ba9d9" />

 
cat forcontinue.sh 
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
<img width="565" height="324" alt="image" src="https://github.com/user-attachments/assets/c35e9be6-1826-41c2-a97d-b037b9550aa2" />

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
<img width="748" height="229" alt="image" src="https://github.com/user-attachments/assets/8fdc3858-1139-4ebd-9000-6559f4c473ac" />

cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 <img width="607" height="185" alt="image" src="https://github.com/user-attachments/assets/34b47d02-c182-44cc-9118-a537fb863bf0" />

$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT
<img width="452" height="157" alt="image" src="https://github.com/user-attachments/assets/b7b4585c-a002-4320-a0c1-5bc1904d339a" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
```
<img width="569" height="150" alt="image" src="https://github.com/user-attachments/assets/4a0058f3-3fa6-4d82-846b-14004a0cf4e3" />

$ chmod 755 exread1.sh 

$ ./exread1.sh

## OUTPUT

<img width="437" height="54" alt="image" src="https://github.com/user-attachments/assets/d3c139b0-5abf-4edb-b430-68d198b95636" />

 
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
<img width="680" height="351" alt="image" src="https://github.com/user-attachments/assets/2bcf5674-e1f2-46c4-9acf-b4279f725a42" />

## OUTPUT
 ./funcex.sh 
<img width="361" height="185" alt="image" src="https://github.com/user-attachments/assets/e8f70b07-4fbb-4cbb-abc3-50bda5cb1911" />

 
 ./funcex.sh 1 2

 <img width="306" height="120" alt="image" src="https://github.com/user-attachments/assets/b7a5d7fb-3897-44a2-885b-285ba09a8914" />

cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
<img width="310" height="171" alt="image" src="https://github.com/user-attachments/assets/d66b806c-8eb9-409a-9347-655c84f9acd4" />

$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3

<img width="322" height="125" alt="image" src="https://github.com/user-attachments/assets/1cf33db1-ea11-46ef-b361-2e01568c4c11" />


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
<img width="505" height="294" alt="image" src="https://github.com/user-attachments/assets/81f35d4d-e9b2-41b5-95cc-3726eb9e6c96" />

$ chmod 777 argshift1.sh
## OUTPUT
$ ./argshift1.sh 1 2 3
<img width="411" height="169" alt="image" src="https://github.com/user-attachments/assets/370cf794-5672-4747-ada9-4baa6142cba6" />


cat > argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```

<img width="503" height="301" alt="image" src="https://github.com/user-attachments/assets/382cde1d-b1f2-4046-bb60-2fbf75cc5b2c" />

## OUTPUT
 ./argshift.sh 1 2 3
<img width="483" height="449" alt="image" src="https://github.com/user-attachments/assets/46ebc91a-2f5e-4c9d-bca3-9ee5ee7320bf" />
 
 
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
<img width="471" height="319" alt="image" src="https://github.com/user-attachments/assets/c50be7ab-44bc-4c11-ac65-a36570229ea8" />

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
<img width="406" height="294" alt="image" src="https://github.com/user-attachments/assets/da08efcd-36ad-4133-ac8a-ae367e878d6f" />



awk -f nc.awk data.dat
## OUTPUT 
<img width="512" height="375" alt="image" src="https://github.com/user-attachments/assets/64d299a9-be99-43c9-95a0-1a9ffb0cb95a" />



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
<img width="638" height="573" alt="image" src="https://github.com/user-attachments/assets/859c34dc-f8ef-4e19-b756-a1a6c0d6c7aa" />

## OUTPUT 
<img width="505" height="304" alt="image" src="https://github.com/user-attachments/assets/adca3444-629a-4329-b124-8d6360c5f89e" />


# RESULT:
The Commands are executed successfully.
