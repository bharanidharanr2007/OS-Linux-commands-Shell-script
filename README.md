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
<img width="436" height="157" alt="image" src="https://github.com/user-attachments/assets/43a1aca0-8310-4145-a433-db7fe0bf29e8" />




cat < file2
## OUTPUT
<img width="337" height="214" alt="image" src="https://github.com/user-attachments/assets/76ee0da6-152a-411b-8d04-1bdba3f6b810" />



# Comparing Files
cmp file1 file2
## OUTPUT
<img width="346" height="129" alt="image" src="https://github.com/user-attachments/assets/9f790508-c194-4f55-b62e-6cc92010d389" />

 
comm file1 file2
 ## OUTPUT
 <img width="359" height="270" alt="image" src="https://github.com/user-attachments/assets/c3e05552-13a8-4133-9ac6-79b67aad748b" />


 
diff file1 file2
## OUTPUT
<img width="375" height="276" alt="image" src="https://github.com/user-attachments/assets/cc4d7697-bddd-49a4-ab8d-38bb7d14090b" />



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
<img width="317" height="88" alt="image" src="https://github.com/user-attachments/assets/669d3a2a-be3d-43b5-bb29-4ac4a7268f54" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="325" height="119" alt="image" src="https://github.com/user-attachments/assets/c52f0746-2714-4787-9488-96b0e864bd28" />




cut -d "|" -f 2 file22
## OUTPUT
<img width="311" height="177" alt="image" src="https://github.com/user-attachments/assets/f50e410a-c108-4297-9014-2cccb8eb037b" />



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
<img width="305" height="120" alt="image" src="https://github.com/user-attachments/assets/ac159610-5a06-48eb-ade0-cbe171643096" />




grep hello newfile 
## OUTPUT
<img width="309" height="124" alt="image" src="https://github.com/user-attachments/assets/f14e3ff5-2ed2-41f7-8070-6f9857011840" />





grep -v hello newfile 
## OUTPUT
<img width="314" height="124" alt="image" src="https://github.com/user-attachments/assets/acd39e23-56a9-467c-bc6e-139a25eb3b53" />




cat newfile | grep -i "hello"
## OUTPUT
<img width="370" height="142" alt="image" src="https://github.com/user-attachments/assets/c30ed6ff-db95-4d85-a701-f73d28a97bdd" />





cat newfile | grep -i -c "hello"
## OUTPUT
<img width="406" height="123" alt="image" src="https://github.com/user-attachments/assets/b124f8b4-221c-4289-ae9c-32ba8994f994" />





grep -R ubuntu /etc
## OUTPUT
<img width="533" height="753" alt="image" src="https://github.com/user-attachments/assets/f7087353-7b97-4c8c-925b-492ffd584193" />




grep -w -n world newfile   
## OUTPUT
<img width="367" height="148" alt="image" src="https://github.com/user-attachments/assets/9b241f3f-f87e-424a-a02c-6e18086c97b3" />



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
<img width="409" height="152" alt="image" src="https://github.com/user-attachments/assets/b5d9a1b0-3235-47dc-b66f-5985948c309c" />




egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="380" height="144" alt="image" src="https://github.com/user-attachments/assets/f793bf7d-b986-465a-bd0f-cdba4a56dc1c" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="458" height="152" alt="image" src="https://github.com/user-attachments/assets/eff5cedb-3925-449b-ba5a-78f4d110defe" />





egrep '(^hello)' newfile 
## OUTPUT
<img width="344" height="128" alt="image" src="https://github.com/user-attachments/assets/b6c3ff1f-1055-4a22-b10d-085cc3a3b5b3" />



egrep '(world$)' newfile 
## OUTPUT
<img width="371" height="142" alt="image" src="https://github.com/user-attachments/assets/3bd91671-bbf0-4373-a92d-0efc8d1733b9" />




egrep '(World$)' newfile 
## OUTPUT
<img width="353" height="120" alt="image" src="https://github.com/user-attachments/assets/e55d0a87-0c48-4aa9-b057-baaf691f422b" />



egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="375" height="179" alt="image" src="https://github.com/user-attachments/assets/33690fac-af22-45d4-8bb2-b234c56c7a5c" />




egrep '[1-9]' newfile 
## OUTPUT
<img width="309" height="121" alt="image" src="https://github.com/user-attachments/assets/0931f99d-bb8c-4ba7-b5d1-40765a155200" />




egrep 'Linux.*world' newfile 
## OUTPUT
<img width="369" height="131" alt="image" src="https://github.com/user-attachments/assets/0cc76997-87a5-40bd-98ef-9cb94b8c8592" />



egrep 'Linux.*World' newfile 
## OUTPUT
<img width="379" height="127" alt="image" src="https://github.com/user-attachments/assets/125badb8-d31b-4676-8a88-03e230c5f415" />



egrep l{2} newfile
## OUTPUT
<img width="324" height="152" alt="image" src="https://github.com/user-attachments/assets/040e9112-4ef6-45a9-a4f6-d02441eff9df" />




egrep 's{1,2}' newfile
## OUTPUT 
<img width="336" height="176" alt="image" src="https://github.com/user-attachments/assets/12f93bc2-374d-4c0a-8d77-8d8edf23786e" />



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
<img width="323" height="122" alt="image" src="https://github.com/user-attachments/assets/9bf6594a-1896-4774-9e88-b9251dabc2d1" />




sed -n -e '$p' file23
## OUTPUT
<img width="322" height="135" alt="image" src="https://github.com/user-attachments/assets/20ff10a5-d50a-4268-9aec-3236750c4f6d" />




sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="360" height="296" alt="image" src="https://github.com/user-attachments/assets/12827d94-472f-4337-91b8-5ace9ebf567a" />




sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="385" height="298" alt="image" src="https://github.com/user-attachments/assets/54e5f9ea-f9c9-45dc-8853-8b4aaad0fb24" />




sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="399" height="301" alt="image" src="https://github.com/user-attachments/assets/8152ac14-44a6-4b80-8b9a-6226fa656810" />




sed -n -e '1,5p' file23
## OUTPUT
<img width="365" height="223" alt="image" src="https://github.com/user-attachments/assets/3fca72ee-9df1-4a4e-9141-733563a2941c" />




sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="378" height="179" alt="image" src="https://github.com/user-attachments/assets/0047b1e4-7f37-40d3-affe-747d0baee213" />





sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="449" height="146" alt="image" src="https://github.com/user-attachments/assets/28f9adbc-c7f1-4071-be47-c71406c63316" />




seq 10 
## OUTPUT
<img width="397" height="349" alt="image" src="https://github.com/user-attachments/assets/f52cf228-c5cc-4ea0-b61d-cb72039c8179" />




seq 10 | sed -n '4,6p'
## OUTPUT
<img width="476" height="171" alt="image" src="https://github.com/user-attachments/assets/8455701b-49a8-47a2-a21b-f1732425f011" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="487" height="170" alt="image" src="https://github.com/user-attachments/assets/96f55cc6-87f0-4637-8238-ed334607f17c" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="545" height="199" alt="image" src="https://github.com/user-attachments/assets/31565e5e-9765-40c8-adf8-9183274b3fe6" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="413" height="119" alt="image" src="https://github.com/user-attachments/assets/b4efcebb-8573-495b-951b-636cf2737fdf" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="659" height="171" alt="image" src="https://github.com/user-attachments/assets/9a9a65a2-3ee1-4b3b-8bc9-73b595989d8e" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="551" height="180" alt="image" src="https://github.com/user-attachments/assets/193bd6ca-3ff3-4966-b2fd-338cb5cfce1d" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="601" height="167" alt="image" src="https://github.com/user-attachments/assets/bfbdf09c-bee8-4b79-8873-f3bd0fde1dd0" />


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
<img width="681" height="224" alt="image" src="https://github.com/user-attachments/assets/024b37b0-b6da-4f24-908f-ef82ee0280da" />


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

<img width="479" height="178" alt="image" src="https://github.com/user-attachments/assets/25ae95db-41d7-47c6-a2f0-120787a7dd6a" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="636" height="307" alt="image" src="https://github.com/user-attachments/assets/9a3b2041-81ce-4ea4-93a5-256510a5963e" />

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
<img width="538" height="180" alt="image" src="https://github.com/user-attachments/assets/9abca860-155c-4fe5-a413-92b3f638b37d" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="840" height="173" alt="image" src="https://github.com/user-attachments/assets/7185ef2b-f9b7-442b-8501-340ca6160128" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="851" height="776" alt="image" src="https://github.com/user-attachments/assets/3aad05ad-02a5-4216-aae8-3c56d664efd5" />

<img width="522" height="680" alt="image" src="https://github.com/user-attachments/assets/3725ea97-33a9-4f37-b228-19f9877380cf" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="912" height="803" alt="image" src="https://github.com/user-attachments/assets/b0e5758a-dff0-4a59-a652-50034b4bcc25" />
<img width="934" height="778" alt="image" src="https://github.com/user-attachments/assets/971f7953-3a0f-45a0-abc8-9e7d0de4afbb" />


tar -xvf backup.tar
## OUTPUT
<img width="896" height="574" alt="image" src="https://github.com/user-attachments/assets/a6e90351-a12b-4f54-be6a-5e3020ac6eb3" />
<img width="764" height="801" alt="image" src="https://github.com/user-attachments/assets/09fede50-ced8-4890-aee2-00cd914854ef" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="656" height="125" alt="image" src="https://github.com/user-attachments/assets/93ce2a40-67bc-4f20-bfc6-4f3f79bf6c76" />
 
gunzip backup.tar.gz
## OUTPUT
<img width="955" height="209" alt="image" src="https://github.com/user-attachments/assets/1c8fe6ef-6f02-43e8-9e0d-53cbadd4b404" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="573" height="233" alt="Screenshot 2025-09-11 111127" src="https://github.com/user-attachments/assets/f6d104f3-613b-4289-a75e-8525a177da30" />




 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


<img width="319" height="182" alt="Screenshot 2025-09-11 111418" src="https://github.com/user-attachments/assets/720ff5e8-effa-4e6b-aa62-f9b3672d4e12" />



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
<img width="446" height="487" alt="Screenshot 2025-09-11 112138" src="https://github.com/user-attachments/assets/0ded6124-fc56-4569-a71d-bc6b0572dead" />



 
ls file1
## OUTPUT
<img width="302" height="126" alt="Screenshot 2025-09-11 112250" src="https://github.com/user-attachments/assets/21e8b381-e314-4ddb-bc1d-30c5ca5764e7" />



echo $?
## OUTPUT 
<img width="330" height="148" alt="Screenshot 2025-09-11 112308" src="https://github.com/user-attachments/assets/51ad66b2-94dc-40d4-9cef-29c7480d61b8" />


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

<img width="330" height="130" alt="Screenshot 2025-09-11 112354" src="https://github.com/user-attachments/assets/b9b4dc49-ebec-477a-9b6f-989c5c8857bd" />

 
abcd

## OUTPUT

<img width="381" height="76" alt="Screenshot 2025-09-11 112416" src="https://github.com/user-attachments/assets/080a3b36-c9bf-473c-a816-89dfc6d5103a" />

 
echo $?
 ## OUTPUT

<img width="328" height="72" alt="Screenshot 2025-09-11 112433" src="https://github.com/user-attachments/assets/e726a4b2-9ceb-483f-832f-457cccd60283" />



 
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
## OUTPUT

<img width="358" height="249" alt="Screenshot 2025-09-11 112610" src="https://github.com/user-attachments/assets/5b841e47-2d42-4133-8e5e-5c10963362ca" />




chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="459" height="412" alt="Screenshot 2025-09-11 112703" src="https://github.com/user-attachments/assets/2549b477-bb84-4476-9681-0fd30f73826d" />



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
<img width="630" height="305" alt="Screenshot 2025-09-11 113044" src="https://github.com/user-attachments/assets/5aeb2f88-72f7-4111-876a-c4cbef62f316" />
<img width="583" height="127" alt="Screenshot 2025-09-11 131848" src="https://github.com/user-attachments/assets/c39b814b-e22a-4433-b4ca-6ffd950f8297" />

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
<img width="632" height="722" alt="Screenshot 2025-09-11 134356" src="https://github.com/user-attachments/assets/3e9dd7df-6394-437f-be92-baadfd78211d" />




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
## OUTPUT
<img width="657" height="654" alt="Screenshot 2025-09-11 135136" src="https://github.com/user-attachments/assets/552c9cd5-b5d2-461d-99fb-ca1eea1120f3" />



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
## OUTPUT

<img width="688" height="712" alt="Screenshot 2025-09-11 135313" src="https://github.com/user-attachments/assets/8aaa7914-b3e9-4255-9f0a-17a24230820b" />

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
<img width="671" height="703" alt="Screenshot 2025-09-11 140256" src="https://github.com/user-attachments/assets/13e07134-5a72-418e-a9cc-6dafc211f5de" />



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
<img width="643" height="426" alt="Screenshot 2025-09-11 140558" src="https://github.com/user-attachments/assets/3be32be0-9e16-4998-9eba-8f15be913206" />


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
## OUTPUT
<img width="490" height="491" alt="Screenshot 2025-09-11 140658" src="https://github.com/user-attachments/assets/e4955bad-2950-4779-b521-afbccf0f5ea5" />


 
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
 ## OUTPUT
 <img width="459" height="633" alt="Screenshot 2025-09-11 141033" src="https://github.com/user-attachments/assets/f2c3ad7f-c180-451b-9a8e-aaed2a208af8" />
 
 
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
## OUTPUT

 <img width="562" height="500" alt="Screenshot 2025-09-11 141138" src="https://github.com/user-attachments/assets/22fa10d8-5716-413c-a532-400a02d52f87" />

 
 
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
## OUTPUT
 
 <img width="753" height="549" alt="Screenshot 2025-09-11 141245" src="https://github.com/user-attachments/assets/30624c82-4988-4ced-940d-037375c2bfdb" />

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
## OUTPUT
<img width="780" height="476" alt="Screenshot 2025-09-11 141350" src="https://github.com/user-attachments/assets/25821d48-d8fe-4b9a-bc84-1eff5f0183e2" />

 
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
## OUTPUT
<img width="780" height="476" alt="Screenshot 2025-09-11 141350" src="https://github.com/user-attachments/assets/4429c136-202b-4669-bc41-2a5f4f5461b7" />


 
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
## OUTPUT
 <img width="633" height="523" alt="Screenshot 2025-09-11 141540" src="https://github.com/user-attachments/assets/f7210fdb-0e37-4d8d-aed9-5c0914ebeda0" />

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
<img width="753" height="549" alt="Screenshot 2025-09-11 141245" src="https://github.com/user-attachments/assets/cb6c5747-da2a-4679-a5fd-902f31a09d75" />

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

<img width="364" height="335" alt="Screenshot 2025-09-11 142708" src="https://github.com/user-attachments/assets/f30ff641-9415-4c98-b700-d2fa08c3d558" />

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
<img width="405" height="462" alt="Screenshot 2025-09-11 145106" src="https://github.com/user-attachments/assets/3ed0ccfc-b06b-483e-b868-25d6eb651b8d" />


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
<img width="408" height="479" alt="Screenshot 2025-09-11 171525" src="https://github.com/user-attachments/assets/f28778f0-047c-48d5-94dd-754a20732a22" />


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
<img width="446" height="755" alt="Screenshot 2025-09-11 145216" src="https://github.com/user-attachments/assets/29ecb3c8-93ac-47be-859c-1a9094c47218" />

 
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
<img width="709" height="232" alt="Screenshot 2025-09-11 164849" src="https://github.com/user-attachments/assets/6442f8dc-252e-4939-a704-d9030ecc625d" />

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
 <img width="726" height="278" alt="Screenshot 2025-09-11 164945" src="https://github.com/user-attachments/assets/c83f3506-a379-412f-8bb4-e748f6612388" />

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

<img width="454" height="390" alt="Screenshot 2025-09-11 165156" src="https://github.com/user-attachments/assets/83bd2660-f050-4225-b7a5-b9c0068b2cd0" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT


<img width="454" height="390" alt="Screenshot 2025-09-11 165156" src="https://github.com/user-attachments/assets/0a67ff76-350e-48e3-8391-7ee1ff79b854" />

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
<img width="361" height="127" alt="Screenshot 2025-09-11 165542" src="https://github.com/user-attachments/assets/4abe3b57-d55f-4bca-b942-e96d92b92c4f" />

 ./funcex.sh 

 
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
 <img width="321" height="229" alt="Screenshot 2025-09-11 171911" src="https://github.com/user-attachments/assets/92298dff-3c6c-4eee-9e61-823c8ad4731b" />
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
<img width="358" height="189" alt="Screenshot 2025-09-11 165824" src="https://github.com/user-attachments/assets/60f0fa2d-e156-440c-9748-1d2b729f7cb9" />

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
## OUTPUT
<img width="349" height="726" alt="Screenshot 2025-09-11 165930" src="https://github.com/user-attachments/assets/3e84d3db-c5bb-4712-a18a-761eb325dfe8" />

 ./argshift.sh 1 2 3
 
 
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
<img width="424" height="422" alt="Screenshot 2025-09-11 170123" src="https://github.com/user-attachments/assets/0b7108be-3d3d-457d-9cb8-cefa9adf7298" />

 
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


<img width="505" height="790" alt="Screenshot 2025-09-11 170338" src="https://github.com/user-attachments/assets/18c746ae-251f-4bbb-990f-f0e87bba38ed" />




# RESULT:
The Commands are executed successfully.
