# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# NAME: MADHU SHRUTHI A.R
# REG NO.: 212225040216

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

<img width="386" height="88" alt="image" src="https://github.com/user-attachments/assets/78f0216e-d445-40fe-b55d-0f94d595b1c6" />


cat < file2
## OUTPUT
<img width="377" height="106" alt="image" src="https://github.com/user-attachments/assets/bf12d1de-f927-4801-be3e-525a41a626ca" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="405" height="45" alt="image" src="https://github.com/user-attachments/assets/d6289429-b9a0-4a68-b6e7-0b046104a2e3" />

comm file1 file2
 ## OUTPUT
<img width="410" height="194" alt="image" src="https://github.com/user-attachments/assets/4735c5e9-d46b-4202-8ee8-a7f3190ed30f" />

 
diff file1 file2
## OUTPUT
<img width="447" height="178" alt="image" src="https://github.com/user-attachments/assets/eb5a6ca1-0559-49cd-be14-3941d57901c0" />


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

<img width="425" height="54" alt="image" src="https://github.com/user-attachments/assets/e1d63c9a-d7fe-4dc7-8ca7-f96bb739d417" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="478" height="74" alt="image" src="https://github.com/user-attachments/assets/849e453f-17cc-4d4b-972a-e8653aa4cfe6" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="459" height="73" alt="image" src="https://github.com/user-attachments/assets/18341825-d7cd-489c-a29e-b394d33ef021" />


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
<img width="430" height="37" alt="image" src="https://github.com/user-attachments/assets/1c24738e-cf69-46a2-939d-772690f16866" />



grep hello newfile 
## OUTPUT

<img width="430" height="37" alt="image" src="https://github.com/user-attachments/assets/89bb7166-10b9-44ad-86f0-52fea7df6fc9" />



grep -v hello newfile 
## OUTPUT

<img width="438" height="36" alt="image" src="https://github.com/user-attachments/assets/78a3ec3d-94d2-4299-8906-8f1955919bbe" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="498" height="58" alt="image" src="https://github.com/user-attachments/assets/f8186f59-d881-40b6-99f9-8916fcd6c07a" />



cat newfile | grep -i -c "hello"
## OUTPUT


<img width="535" height="37" alt="image" src="https://github.com/user-attachments/assets/a61c9809-f195-490b-bd5a-8b0c9f4c37cd" />


grep -R ubuntu /etc
## OUTPUT

<img width="694" height="693" alt="image" src="https://github.com/user-attachments/assets/bef4d9bb-9509-4688-a482-758e5b4e0fb9" />


grep -w -n world newfile   
## OUTPUT

<img width="476" height="58" alt="image" src="https://github.com/user-attachments/assets/893964f1-5469-4b35-b882-048c9750add2" />

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

<img width="523" height="55" alt="image" src="https://github.com/user-attachments/assets/56110576-9c23-44c8-8871-9de6fdfd0ecf" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="492" height="57" alt="image" src="https://github.com/user-attachments/assets/b75be75a-90e4-48ce-8180-9fde05127947" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT



<img width="530" height="54" alt="image" src="https://github.com/user-attachments/assets/f8294bc5-d2fb-481a-b612-16756263100b" />

egrep '(^hello)' newfile 
## OUTPUT

<img width="510" height="37" alt="image" src="https://github.com/user-attachments/assets/88ad6cd6-d372-4211-8d70-2a35e2de55b6" />


egrep '(world$)' newfile 
## OUTPUT
<img width="518" height="79" alt="image" src="https://github.com/user-attachments/assets/2b3e4243-d961-4cd6-ab37-c6a851c3a15e" />



egrep '(World$)' newfile 
## OUTPUT
<img width="474" height="36" alt="image" src="https://github.com/user-attachments/assets/1a3a5c7b-f6db-4133-be15-ca3d5d55bf47" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="486" height="70" alt="image" src="https://github.com/user-attachments/assets/90718c15-1aaf-47b6-9b07-4474aaba2aa3" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="466" height="37" alt="image" src="https://github.com/user-attachments/assets/7cf505c8-e663-47ba-a519-bf1b9bf2ba3f" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="495" height="38" alt="image" src="https://github.com/user-attachments/assets/d39ecb97-1322-4a3e-adbf-6f72ebc20903" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="510" height="38" alt="image" src="https://github.com/user-attachments/assets/4e1a6a15-2665-450f-b5c7-34addd64da92" />


egrep l{2} newfile
## OUTPUT

<img width="444" height="54" alt="image" src="https://github.com/user-attachments/assets/ee71300f-ca7f-4b0f-8361-38356d05074c" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="449" height="70" alt="image" src="https://github.com/user-attachments/assets/57cb203b-0d1d-492e-a457-6ee5e749c171" />


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
<img width="443" height="40" alt="image" src="https://github.com/user-attachments/assets/b9ead3c3-354f-4cdf-9a67-ab69a7ddaf50" />



sed -n -e '$p' file23
## OUTPUT
<img width="445" height="42" alt="image" src="https://github.com/user-attachments/assets/a0481719-73aa-4e9b-aef4-0689cb160aac" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="488" height="162" alt="image" src="https://github.com/user-attachments/assets/c5c2955d-94d6-418b-9bba-ab7b519065f2" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="489" height="151" alt="image" src="https://github.com/user-attachments/assets/3710200a-9a44-408c-891f-9c7420e33478" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT


<img width="519" height="162" alt="image" src="https://github.com/user-attachments/assets/d08a2f84-8fed-479c-9526-49b090752a52" />

sed -n -e '1,5p' file23
## OUTPUT

<img width="462" height="105" alt="image" src="https://github.com/user-attachments/assets/e3fa7139-1d59-48b1-b765-d48eca07fadd" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="493" height="70" alt="image" src="https://github.com/user-attachments/assets/50e8c1f4-9f51-453e-8ffa-ae9da6f7f74d" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="526" height="60" alt="image" src="https://github.com/user-attachments/assets/f1fcd3ab-b619-4fe8-a960-41238d7493a7" />


seq 10 
## OUTPUT


<img width="330" height="200" alt="image" src="https://github.com/user-attachments/assets/2c8c1aee-16ad-49e0-8ca6-c7be9989307b" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="460" height="73" alt="image" src="https://github.com/user-attachments/assets/07455f64-f9e0-447a-8ebd-0f1a1225742a" />



seq 10 | sed -n '2,~4p'
## OUTPUT


<img width="468" height="68" alt="image" src="https://github.com/user-attachments/assets/57130794-20d2-4d37-87f7-86e70b7413f4" />

seq 3 | sed '2a hello'
## OUTPUT

<img width="456" height="88" alt="image" src="https://github.com/user-attachments/assets/9ff0972e-343e-4f3c-9199-03c3950af12d" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="450" height="72" alt="image" src="https://github.com/user-attachments/assets/b6c1c12d-ddf6-42f8-9704-26e7d65083c3" />



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="542" height="78" alt="image" src="https://github.com/user-attachments/assets/183e1b62-a436-4240-bc19-cea9e28695cb" />


sed -n '2,4{s/$/*/;p}' file23

## OUTPUT

<img width="550" height="75" alt="image" src="https://github.com/user-attachments/assets/32705ac2-92c1-4b47-a279-ca119a5f5f18" />

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
<img width="363" height="109" alt="image" src="https://github.com/user-attachments/assets/f1b9d19d-9f94-4ba3-b846-50e8e68e62b5" />


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

<img width="362" height="108" alt="image" src="https://github.com/user-attachments/assets/b294a002-9e77-4f82-a37e-5e9cc9f87b70" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="529" height="162" alt="image" src="https://github.com/user-attachments/assets/347d5fac-f46f-4a08-957d-9822cfb2eede" />

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

<img width="477" height="70" alt="image" src="https://github.com/user-attachments/assets/fca88f08-2f9a-4dc8-9bf2-b8a3e54674e8" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="558" height="73" alt="image" src="https://github.com/user-attachments/assets/04f85c23-8607-4982-98ea-5c1cb779bd85" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="457" height="57" alt="image" src="https://github.com/user-attachments/assets/d960292c-47ec-4944-887f-c66f60ff9bfe" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="510" height="204" alt="image" src="https://github.com/user-attachments/assets/59ca779c-56e4-4b4d-9bda-9502952b3c0c" />


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
<img width="459" height="494" alt="image" src="https://github.com/user-attachments/assets/7b619950-aa91-48c7-8605-edae6b83c105" />

 
ls file1
## OUTPUT
<img width="351" height="41" alt="image" src="https://github.com/user-attachments/assets/1a6c3489-f4fe-4f0c-96a7-23e977aa7c0a" />

echo $?
## OUTPUT 
<img width="348" height="34" alt="image" src="https://github.com/user-attachments/assets/3d792abf-b58d-44dd-93ca-fe79c7182449" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="346" height="34" alt="image" src="https://github.com/user-attachments/assets/d9e4b6dd-931a-4667-ab00-72d09889eafb" />

abcd
 
echo $?
 ## OUTPUT
<img width="366" height="180" alt="image" src="https://github.com/user-attachments/assets/ac531ade-0003-47ac-8c3b-ad8b4af69b6f" />


 
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

<img width="409" height="171" alt="image" src="https://github.com/user-attachments/assets/a8d53bb1-60e6-4202-aa11-e9b663e2438f" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="471" height="76" alt="image" src="https://github.com/user-attachments/assets/562d0f7d-63f7-48a3-82b6-3cfeef10ab53" />


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
<img width="462" height="383" alt="image" src="https://github.com/user-attachments/assets/75ace8cc-15fc-4ec9-8454-3b2af17c1557" />

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
<img width="404" height="543" alt="image" src="https://github.com/user-attachments/assets/bd7f3dc1-1287-45b7-9d7e-b61d9b5920b2" />



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
<img width="420" height="488" alt="image" src="https://github.com/user-attachments/assets/b07aeb27-6c08-41e3-9449-cf79aee61b34" />

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

cat < ifnested.sh 
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
<img width="458" height="605" alt="image" src="https://github.com/user-attachments/assets/937fea9f-b699-4572-bc2c-9592d55ca6a7" />

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
<img width="463" height="561" alt="image" src="https://github.com/user-attachments/assets/ad0fe457-8627-4767-870c-2ec6de039158" />

<img width="467" height="86" alt="image" src="https://github.com/user-attachments/assets/079e2171-c58f-4b39-8cbc-ca979f27c1aa" />

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
<img width="492" height="234" alt="image" src="https://github.com/user-attachments/assets/dd3a1e8b-d5bc-42f1-bd84-cbfc0be07648" />

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

<img width="481" height="283" alt="image" src="https://github.com/user-attachments/assets/baa59407-8ca0-4d52-a6c4-92c771c399a9" />

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
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh

## OUTPUT

<img width="456" height="399" alt="image" src="https://github.com/user-attachments/assets/4271670b-e1bd-45d6-ac60-dba016dea26b" />

 
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

<img width="456" height="290" alt="image" src="https://github.com/user-attachments/assets/302e33e0-ec29-43af-a01f-a400fcd09e8b" />

 
cat>forin1.sh 
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
 
cat > forin2.sh 
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
<img width="491" height="702" alt="image" src="https://github.com/user-attachments/assets/aace6cd3-0823-4d1e-afbf-40c95ebe25cb" />
<img width="475" height="268" alt="image" src="https://github.com/user-attachments/assets/9ae42c86-5acb-43a4-b2d0-8a9002d7e68a" />

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
<img width="483" height="327" alt="image" src="https://github.com/user-attachments/assets/5c216db7-c074-4ec6-a96a-5f61ebad4827" />


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
<img width="459" height="267" alt="image" src="https://github.com/user-attachments/assets/ae51c9b6-29fc-4907-b289-893896da2af0" />


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
<img width="465" height="360" alt="image" src="https://github.com/user-attachments/assets/3496f75b-e6cf-4024-88e2-3de095cf1d2d" />

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
<img width="471" height="470" alt="image" src="https://github.com/user-attachments/assets/c6906261-9e28-48d9-ad6d-a76be85deef0" />

 
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
<img width="453" height="122" alt="image" src="https://github.com/user-attachments/assets/dd266f1c-4d82-48a3-bef0-8f8846353fd3" />


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
<img width="463" height="225" alt="image" src="https://github.com/user-attachments/assets/930e53a1-ccc4-4065-afdd-55a31956d232" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 
$ ./exread1.sh 

## OUTPUT

<img width="436" height="184" alt="image" src="https://github.com/user-attachments/assets/5d604575-0d48-4f43-ad9d-ace9118111a9" />

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
## OUTPUT

<img width="453" height="308" alt="image" src="https://github.com/user-attachments/assets/7a2eaa4a-60e9-4412-9974-117f43de4281" />

  
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
 <img width="446" height="262" alt="image" src="https://github.com/user-attachments/assets/e5062beb-bb3b-46fa-832a-129f84348d4c" />

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
<img width="469" height="300" alt="image" src="https://github.com/user-attachments/assets/8ec97eb8-e73b-42ed-9e32-f333d9059e8f" />
 
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
 <img width="508" height="671" alt="image" src="https://github.com/user-attachments/assets/39dc6205-1363-4c10-b3da-51a505162543" />

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
<img width="476" height="588" alt="image" src="https://github.com/user-attachments/assets/2b209e45-b9ad-4fd9-b87f-7127ef25de91" />


# RESULT:
The Commands are executed successfully.
