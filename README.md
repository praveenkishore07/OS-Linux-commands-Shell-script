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
<img width="542" height="162" alt="1" src="https://github.com/user-attachments/assets/453b17d8-3ee0-4080-8ebf-fba40bca485b" />

cat < file2
## OUTPUT
<img width="461" height="162" alt="2" src="https://github.com/user-attachments/assets/f7db12e8-8a8a-4704-9d85-c6059f065788" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="467" height="92" alt="3" src="https://github.com/user-attachments/assets/bcfc4a6b-c8e6-4504-9954-497dad1cad2b" />


comm file1 file2
 ## OUTPUT
<img width="452" height="300" alt="4" src="https://github.com/user-attachments/assets/4c247446-16da-4261-aa14-50033430cdf9" />

 
diff file1 file2
## OUTPUT
<img width="366" height="265" alt="5" src="https://github.com/user-attachments/assets/4ee21473-0a76-4a8a-9d06-d9c492483c5e" />


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
<img width="442" height="97" alt="6" src="https://github.com/user-attachments/assets/2db0e6f3-dec7-4f7c-9cc3-ae409a0fd9b0" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="320" height="133" alt="image" src="https://github.com/user-attachments/assets/bddb1ee7-ef2c-4d82-aa92-a9fa51c36fa5" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="332" height="121" alt="image" src="https://github.com/user-attachments/assets/eb42ad3a-9853-4c96-8ff1-021388db56f7" />


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
<img width="380" height="91" alt="image" src="https://github.com/user-attachments/assets/e94283f0-c016-4679-b3e1-f75019ab1c7e" />




grep hello newfile 
## OUTPUT
<img width="352" height="90" alt="image" src="https://github.com/user-attachments/assets/86358402-2afd-49ad-9b4f-015234ab00e2" />





grep -v hello newfile 
## OUTPUT
<img width="368" height="96" alt="image" src="https://github.com/user-attachments/assets/f0dbd05c-5001-4954-9877-3aa8f99dff9b" />




cat newfile | grep -i "hello"
## OUTPUT

<img width="347" height="96" alt="image" src="https://github.com/user-attachments/assets/67f799de-a72b-4c26-9e1c-e270664ca0f0" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="360" height="95" alt="image" src="https://github.com/user-attachments/assets/07773fcc-89c6-4ef4-bcc0-b5c6dfe6e9d5" />



grep -R ubuntu /etc
## OUTPUT

<img width="312" height="72" alt="image" src="https://github.com/user-attachments/assets/a1684b88-47a7-4693-ba25-a1d948278d5b" />


grep -w -n world newfile   
## OUTPUT
<img width="372" height="117" alt="image" src="https://github.com/user-attachments/assets/591ec419-7365-48f9-a861-8cec7a65760e" />


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
<img width="357" height="101" alt="image" src="https://github.com/user-attachments/assets/47a3c229-93d2-4d8c-805d-7f726ce04cac" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="373" height="115" alt="image" src="https://github.com/user-attachments/assets/323b0120-eeb3-4afb-813d-38eb2ba68450" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="436" height="93" alt="image" src="https://github.com/user-attachments/assets/bd43ccb6-c084-44aa-82b0-4ecf99bf5342" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="350" height="86" alt="image" src="https://github.com/user-attachments/assets/c61c743f-6bf2-4aef-9381-6e7ff761bd7a" />



egrep '(world$)' newfile 
## OUTPUT
<img width="356" height="102" alt="image" src="https://github.com/user-attachments/assets/34f11abf-fd2a-4258-b84e-945beab1441c" />



egrep '(World$)' newfile 
## OUTPUT
<img width="327" height="100" alt="image" src="https://github.com/user-attachments/assets/561a06a3-a8fa-4ab4-966c-6317c4649ff4" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="382" height="122" alt="image" src="https://github.com/user-attachments/assets/f1755afd-98a7-4e40-9a52-40e64bcc0e7f" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="330" height="85" alt="image" src="https://github.com/user-attachments/assets/1cbae7a2-df76-401e-98a1-5802950f1cc7" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="392" height="98" alt="image" src="https://github.com/user-attachments/assets/57d523e5-624c-4a84-80a9-fc9a0616d8d1" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="327" height="110" alt="image" src="https://github.com/user-attachments/assets/953786ea-4200-4f27-999d-7bc587d35229" />


egrep l{2} newfile
## OUTPUT
<img width="335" height="110" alt="image" src="https://github.com/user-attachments/assets/7d5a3706-4218-453b-8e36-b2396b4f9646" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="348" height="127" alt="image" src="https://github.com/user-attachments/assets/5f417fb7-47a7-4dcd-aaf8-79100d5f8163" />


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
<img width="351" height="82" alt="image" src="https://github.com/user-attachments/assets/4951639b-699f-4250-95f6-2f0e25b6f3fe" />



sed -n -e '$p' file23
## OUTPUT
<img width="350" height="72" alt="image" src="https://github.com/user-attachments/assets/239a50bc-13ed-4b44-be14-70e4ca220a11" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="415" height="227" alt="image" src="https://github.com/user-attachments/assets/bcad5b65-6ea2-48f9-93f3-289fd4089ce0" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="415" height="225" alt="image" src="https://github.com/user-attachments/assets/16096af6-7ed0-4473-8294-83b5cbcdcb08" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="428" height="226" alt="image" src="https://github.com/user-attachments/assets/166fba5b-0fd3-4b25-8e7e-96deebf091fa" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="440" height="172" alt="image" src="https://github.com/user-attachments/assets/cf98de5e-34e0-482b-a3ba-8f2f03e86e50" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="367" height="140" alt="image" src="https://github.com/user-attachments/assets/191ff5cf-c19a-4264-8e82-f507b0a8faa6" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="387" height="100" alt="image" src="https://github.com/user-attachments/assets/73bfefe4-cd7d-4e89-90a6-c6afa397fc7a" />



seq 10 
## OUTPUT
<img width="345" height="277" alt="image" src="https://github.com/user-attachments/assets/8f85f0be-5b6b-4885-a675-2e6db3956b7d" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="332" height="130" alt="image" src="https://github.com/user-attachments/assets/66311e2d-53cb-4588-85bd-1dda93ed727b" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="355" height="133" alt="image" src="https://github.com/user-attachments/assets/a0ce0a10-f14e-4f8f-b4ae-e3c6a8a07cf5" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="396" height="160" alt="image" src="https://github.com/user-attachments/assets/a953ce4b-6a2a-4921-8a72-8fbfc70a4323" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="377" height="125" alt="image" src="https://github.com/user-attachments/assets/c729300c-373e-43b1-aebf-08cb60e58ede" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="372" height="140" alt="image" src="https://github.com/user-attachments/assets/1044bd56-778e-48ad-8bc5-077ae91be5d0" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="378" height="140" alt="image" src="https://github.com/user-attachments/assets/39cb86df-370e-49ca-8098-82fd821e65f5" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT 
<img width="398" height="137" alt="image" src="https://github.com/user-attachments/assets/6bd4cff9-666c-4f47-82e7-d926f33e4fff" />


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
<img width="360" height="162" alt="image" src="https://github.com/user-attachments/assets/943dc2b1-dac9-4bee-bfa1-762f80a871bb" />


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
<img width="408" height="158" alt="image" src="https://github.com/user-attachments/assets/84a46fc6-34f1-49ac-84fb-5b3a4d437eb5" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="368" height="225" alt="image" src="https://github.com/user-attachments/assets/7e52b4a4-86c0-45b2-b461-61456c014b3a" />


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
<img width="376" height="117" alt="image" src="https://github.com/user-attachments/assets/efa75473-8fd4-4a77-80ef-5b0abdcc8545" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="462" height="115" alt="image" src="https://github.com/user-attachments/assets/6740f6b5-fb8d-46b6-bdf5-c7aa7d340718" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="438" height="282" alt="image" src="https://github.com/user-attachments/assets/bd16920a-b6b6-44ab-ac1a-02d820818013" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="576" height="273" alt="image" src="https://github.com/user-attachments/assets/ab922e0a-1f75-48ce-b126-77d4c5608e12" />


tar -xvf backup.tar
## OUTPUT
<img width="437" height="262" alt="image" src="https://github.com/user-attachments/assets/954ff535-0305-46ae-87af-3c4c094d6e51" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="498" height="95" alt="image" src="https://github.com/user-attachments/assets/35c6547c-e469-415e-bdd8-a15dc43ea64e" />

gunzip backup.tar.gz
## OUTPUT
<img width="237" height="336" alt="image" src="https://github.com/user-attachments/assets/e74ba1e0-f833-4803-a743-22c4a08f81cf" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="793" height="398" alt="image" src="https://github.com/user-attachments/assets/f5c8486e-107a-4060-823d-02df1550d701" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="417" height="138" alt="image" src="https://github.com/user-attachments/assets/5b6f9b08-ebd6-485d-92b3-bfc61f19ccae" />


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
<img width="593" height="382" alt="image" src="https://github.com/user-attachments/assets/6275976f-a091-4d4a-af86-77c7d0bd003b" />

 
ls file1
## OUTPUT
<img width="411" height="80" alt="image" src="https://github.com/user-attachments/assets/93230215-7c36-4be2-87e3-85f1a9e8cb2d" />

echo $?
## OUTPUT 
<img width="390" height="92" alt="image" src="https://github.com/user-attachments/assets/28e98526-6fc8-4a52-8790-189dd0a47a6b" />


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="402" height="90" alt="image" src="https://github.com/user-attachments/assets/2ad5fae2-aa1a-42a5-b83c-6dbe2b2c763f" />

abcd
 
echo $?
 ## OUTPUT
<img width="421" height="72" alt="image" src="https://github.com/user-attachments/assets/9c03fe05-f591-4c8f-9e31-2230fa8c8b83" />

 
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
<img width="475" height="247" alt="image" src="https://github.com/user-attachments/assets/58ce71f3-862a-446c-b967-fab726f72e0c" />



./strcomp.sh 
## OUTPUT
<img width="577" height="100" alt="image" src="https://github.com/user-attachments/assets/4fba5969-bdce-48e4-b2bb-f336518ae6f1" />


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
<img width="582" height="97" alt="image" src="https://github.com/user-attachments/assets/32f49ca1-e271-4149-b053-478d02cf1626" />

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

<img width="522" height="387" alt="image" src="https://github.com/user-attachments/assets/dad34d9a-419a-41e5-9850-b7051073dd90" />




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
<img width="582" height="112" alt="image" src="https://github.com/user-attachments/assets/63e5dc69-3ebc-4d8d-bea7-5be7a699d71e" />


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
<img width="590" height="125" alt="image" src="https://github.com/user-attachments/assets/46b8a161-5546-4103-b832-432db4313644" />


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
<img width="592" height="105" alt="image" src="https://github.com/user-attachments/assets/452cc8ce-9208-408b-8c19-98d5d43e9b5d" />


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
<img width="592" height="91" alt="image" src="https://github.com/user-attachments/assets/f6458b70-a2d6-4252-bbe0-c99c2814888a" />


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
<img width="406" height="85" alt="image" src="https://github.com/user-attachments/assets/cf812b6b-db17-4643-aff7-a18ab8240822" />

 
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
## OUTPUT 
 <img width="420" height="201" alt="image" src="https://github.com/user-attachments/assets/f111a0b1-718d-438b-8f01-77f64b6ee275" />

 
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

<img width="593" height="185" alt="image" src="https://github.com/user-attachments/assets/911f7969-cc64-45a1-8dd2-e6976c2e4516" />
 
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
## OUTPUT 
<img width="541" height="182" alt="image" src="https://github.com/user-attachments/assets/a75769d4-015f-4a29-8db7-1816bb4b8c5b" />

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
<img width="572" height="235" alt="image" src="https://github.com/user-attachments/assets/b941fe57-3eb4-419e-ab11-86cd7b10b3dc" />

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

<img width="593" height="172" alt="image" src="https://github.com/user-attachments/assets/26f5f434-9ac2-4463-8fc8-fda36ff49ec0" />

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
<img width="392" height="192" alt="image" src="https://github.com/user-attachments/assets/05dd0d7e-263d-406d-b036-83c94e168ca8" />


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
<img width="335" height="181" alt="image" src="https://github.com/user-attachments/assets/a3860995-80e6-4e23-8271-b239858a3924" />


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
<img width="337" height="170" alt="image" src="https://github.com/user-attachments/assets/4b26fc3a-ef41-4f4b-b9c2-3a000e12a7d3" />


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
<img width="366" height="320" alt="image" src="https://github.com/user-attachments/assets/2afc899b-1f60-4a74-b9a4-49a0b54b782c" />

 
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
<img width="597" height="141" alt="image" src="https://github.com/user-attachments/assets/40a43cec-b74c-4b4e-a967-47b2ddc24b03" />
 
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
<img width="597" height="141" alt="image" src="https://github.com/user-attachments/assets/40a43cec-b74c-4b4e-a967-47b2ddc24b03" />


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
