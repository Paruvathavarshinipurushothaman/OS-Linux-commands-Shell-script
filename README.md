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

<img width="178" height="92" alt="image" src="https://github.com/user-attachments/assets/253a693c-f5ef-4902-b8bc-6c6dd7af29e7" />


cat < file2
## OUTPUT
<img width="138" height="82" alt="image" src="https://github.com/user-attachments/assets/1f0207bc-a086-498c-bc74-83324de60cba" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="235" height="36" alt="image" src="https://github.com/user-attachments/assets/5896e046-4ef4-4c52-8213-2a37bf8c7bdd" />

comm file1 file2
 ## OUTPUT
<img width="223" height="162" alt="image" src="https://github.com/user-attachments/assets/d36245ba-8194-4605-85dd-615aa68612e2" />

 
diff file1 file2
## OUTPUT
<img width="168" height="155" alt="image" src="https://github.com/user-attachments/assets/f446d926-1994-41ef-ba02-68bcde739973" />


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

<img width="198" height="61" alt="image" src="https://github.com/user-attachments/assets/87404560-6fdc-482e-9e34-bf7f513e7f07" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="164" height="111" alt="image" src="https://github.com/user-attachments/assets/1528d5cf-a592-46bd-828e-8fb88fd43f95" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="200" height="111" alt="image" src="https://github.com/user-attachments/assets/3491937a-e3bc-45ba-8343-40265fdd8b56" />


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
<img width="167" height="44" alt="image" src="https://github.com/user-attachments/assets/15664db8-892c-4f7e-9ed4-a028f521ac7d" />



grep hello newfile 
## OUTPUT

<img width="146" height="34" alt="image" src="https://github.com/user-attachments/assets/f4fad7a1-29b9-44e2-a661-25bb6671ae4c" />



grep -v hello newfile 
## OUTPUT

<img width="192" height="52" alt="image" src="https://github.com/user-attachments/assets/bf3b47a0-ac43-46bc-a284-98d48c1be46a" />


cat newfile | grep -i "hello"
## OUTPUT
<img width="244" height="56" alt="image" src="https://github.com/user-attachments/assets/d532e764-9388-442d-a526-3292825aa76b" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="261" height="53" alt="image" src="https://github.com/user-attachments/assets/51afe62e-70a0-4134-b5c4-5835e374e62e" />



grep -w -n world newfile   
## OUTPUT
<img width="213" height="55" alt="image" src="https://github.com/user-attachments/assets/c97ba65d-3879-4882-8bd2-5bbbddd9cefc" />


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

<img width="223" height="51" alt="image" src="https://github.com/user-attachments/assets/26863ed9-4e0f-49b1-b8ab-f86cd1f18af7" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="243" height="58" alt="image" src="https://github.com/user-attachments/assets/ae5ee488-a4ae-4244-9648-335c6c22999d" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="296" height="58" alt="image" src="https://github.com/user-attachments/assets/307ccc99-498c-4302-94be-59f4dd8f05ec" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="200" height="46" alt="image" src="https://github.com/user-attachments/assets/15d60f7d-44c5-4a3d-8293-6c5aeaadbd14" />



egrep '(world$)' newfile 
## OUTPUT

<img width="196" height="48" alt="image" src="https://github.com/user-attachments/assets/113fe6b6-c3fe-42f5-9147-5572044162ae" />


egrep '(World$)' newfile 
## OUTPUT

<img width="222" height="40" alt="image" src="https://github.com/user-attachments/assets/7d8046a4-402b-414d-8dc8-d25eb9883bf7" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="238" height="78" alt="image" src="https://github.com/user-attachments/assets/c77a6feb-681e-464f-9084-1f29d4de19f0" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="213" height="35" alt="image" src="https://github.com/user-attachments/assets/43e87c2b-59a5-41f3-ba48-8785a7ba4505" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="253" height="41" alt="image" src="https://github.com/user-attachments/assets/82c6addc-15db-49d9-9258-2867e21918f3" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="223" height="40" alt="image" src="https://github.com/user-attachments/assets/d888e826-977d-4d63-af60-d38b5e44202a" />


egrep l{2} newfile
## OUTPUT
<img width="141" height="60" alt="image" src="https://github.com/user-attachments/assets/92e28f13-056c-486b-9112-d4dc58104b6c" />




egrep 's{1,2}' newfile
## OUTPUT 
<img width="194" height="68" alt="image" src="https://github.com/user-attachments/assets/f44795f8-fafc-497d-8d79-4638e13fe6dc" />


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

<img width="194" height="42" alt="image" src="https://github.com/user-attachments/assets/1de45137-e023-434c-90db-a9653498801c" />


sed -n -e '$p' file23
## OUTPUT
<img width="218" height="34" alt="image" src="https://github.com/user-attachments/assets/cffc9230-aee3-45ae-9653-372cf9d9d7a3" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="281" height="138" alt="image" src="https://github.com/user-attachments/assets/b748cd5c-de67-491e-981b-b0020b37c028" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="241" height="101" alt="image" src="https://github.com/user-attachments/assets/7b277348-2af0-4a13-9140-ce1d0ed1001e" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="243" height="149" alt="image" src="https://github.com/user-attachments/assets/651cfa1b-a2b5-411a-9750-5718b0cd08a0" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="227" height="101" alt="image" src="https://github.com/user-attachments/assets/8b10af4e-2fc8-4cea-9d2a-a18649a3420d" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="229" height="67" alt="image" src="https://github.com/user-attachments/assets/94a7571c-4617-479e-b746-3d3024034a10" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="233" height="53" alt="image" src="https://github.com/user-attachments/assets/8e560c43-db1c-4992-941d-5822a554de49" />



seq 10 
## OUTPUT
<img width="176" height="196" alt="image" src="https://github.com/user-attachments/assets/2e6e8cf2-edae-4ba0-8855-58df61dff310" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="220" height="67" alt="image" src="https://github.com/user-attachments/assets/43f7156f-4582-4912-8d0e-69a744de52ef" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="210" height="68" alt="image" src="https://github.com/user-attachments/assets/766e8c0b-1c8b-43e0-bc89-0e940f166557" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="192" height="84" alt="image" src="https://github.com/user-attachments/assets/586b74e8-c410-4c40-b600-d019cd8c7255" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="228" height="79" alt="image" src="https://github.com/user-attachments/assets/7520e7ae-7e83-4b35-a6a9-aa4cac5ef356" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="243" height="70" alt="image" src="https://github.com/user-attachments/assets/a86318ba-dafc-47b1-8519-19c6554051ab" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="286" height="76" alt="image" src="https://github.com/user-attachments/assets/8b02bce1-7a1d-498d-87d4-40dd59be471b" />


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
<img width="219" height="103" alt="image" src="https://github.com/user-attachments/assets/701243cc-7127-4ef0-95c8-f73d348d48a1" />


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

<img width="214" height="95" alt="image" src="https://github.com/user-attachments/assets/294c7b2f-b5b6-474b-9ebc-8c7160d6a903" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 <img width="273" height="137" alt="image" src="https://github.com/user-attachments/assets/1f3912aa-3534-4691-afd1-8e9f34a11b69" />


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

<img width="206" height="80" alt="image" src="https://github.com/user-attachments/assets/374f1102-6b7c-4cbe-8fa9-7eec8abfefb8" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="279" height="73" alt="image" src="https://github.com/user-attachments/assets/2a21883f-ac70-4490-a295-a482f9e5440e" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="223" height="198" alt="image" src="https://github.com/user-attachments/assets/7ff276b1-b119-4180-bb3a-6a71077f78f2" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="240" height="532" alt="image" src="https://github.com/user-attachments/assets/b847d17b-0abf-4d3e-9957-57c1ba89457c" />


tar -xvf backup.tar
## OUTPUT
<img width="470" height="168" alt="image" src="https://github.com/user-attachments/assets/34de0303-8d4b-4a6c-b723-21f4914e5223" />



chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="160" height="55" alt="image" src="https://github.com/user-attachments/assets/2a3d3c1a-1f52-4697-a033-60011fa1743e" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="226" height="82" alt="image" src="https://github.com/user-attachments/assets/36291c18-2e0b-41ee-a0c1-eab5ec4ecba6" />

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
<img width="575" height="321" alt="image" src="https://github.com/user-attachments/assets/7d693ccc-cd3c-4ac9-a80b-d86ef6006435" />

 
ls file1
## OUTPUT
<img width="95" height="34" alt="image" src="https://github.com/user-attachments/assets/78d2594b-6807-44fc-9117-4b21898c6115" />

echo $?
## OUTPUT
<img width="88" height="39" alt="image" src="https://github.com/user-attachments/assets/2e438b06-63e1-493c-83a9-8743a016a1a3" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="108" height="53" alt="image" src="https://github.com/user-attachments/assets/7281871a-ed3c-48c7-b709-59277b67f645" />


echo $?
 ## OUTPUT
<img width="109" height="38" alt="image" src="https://github.com/user-attachments/assets/17256a7d-98ca-49da-a7d5-7e23fbc3cb70" />


 
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

<img width="255" height="105" alt="image" src="https://github.com/user-attachments/assets/7da9d4dc-64ef-4549-963d-619b3c99afaa" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="237" height="45" alt="image" src="https://github.com/user-attachments/assets/85e19a50-577b-48c4-802c-760aa3bec5c6" />


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
<img width="382" height="34" alt="image" src="https://github.com/user-attachments/assets/8665d4f3-c2a9-4587-a5fc-58c0b68f1f1f" />

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
<img width="350" height="82" alt="image" src="https://github.com/user-attachments/assets/3e5e73e1-232d-44af-b9be-f0518ca516bd" />



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
<img width="289" height="62" alt="image" src="https://github.com/user-attachments/assets/e04408a2-6a0e-4848-9d85-a4590e2413af" />

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
<img width="337" height="80" alt="image" src="https://github.com/user-attachments/assets/df698551-b1ab-4b8c-9a4a-66df57613b32" />

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

<img width="412" height="110" alt="image" src="https://github.com/user-attachments/assets/92b73f77-a17e-4dc8-8f65-bcf12079e300" />

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
<img width="301" height="39" alt="image" src="https://github.com/user-attachments/assets/8ff94a16-cdd8-4f2d-98ab-7e7ffbe04e02" />


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
 <img width="160" height="216" alt="image" src="https://github.com/user-attachments/assets/58df6480-050f-4a85-b48a-49b6d7a1b8de" />

 
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
 <img width="173" height="106" alt="image" src="https://github.com/user-attachments/assets/e71a4bf8-1727-447e-94ce-df0578d04516" />

 
 
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
 <img width="248" height="140" alt="image" src="https://github.com/user-attachments/assets/509ea7c7-75af-40ba-882d-08c36be7da2d" />

 
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
 <img width="252" height="82" alt="image" src="https://github.com/user-attachments/assets/98d17f8e-d288-4dba-b874-92a04526adc1" />

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
 <img width="182" height="148" alt="image" src="https://github.com/user-attachments/assets/86d93071-3e03-4dcf-81ec-a2bf01a799fd" />

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
<img width="180" height="91" alt="image" src="https://github.com/user-attachments/assets/dfa96d14-5ca4-47c9-8a7d-99bf079c469a" />


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
<img width="153" height="115" alt="image" src="https://github.com/user-attachments/assets/8625de79-0b73-44f2-91c3-090712d26b83" />

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
<img width="168" height="114" alt="image" src="https://github.com/user-attachments/assets/849c7e17-fdf4-4d70-ad03-97bfb81e4327" />

 
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
 <img width="483" height="84" alt="image" src="https://github.com/user-attachments/assets/8df965f7-b303-46b7-a402-c13b9d858a6c" />

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
 <img width="503" height="117" alt="image" src="https://github.com/user-attachments/assets/c43810ab-55d2-4c34-b808-821bc207babd" />

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
<img width="326" height="58" alt="image" src="https://github.com/user-attachments/assets/8a35c95b-739d-4800-b897-bb0669e01fb1" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="468" height="60" alt="image" src="https://github.com/user-attachments/assets/05d84972-21ac-4a64-b157-8b7f81698a3a" />



$ ./exread1.sh 
 <img width="269" height="64" alt="image" src="https://github.com/user-attachments/assets/25cd5250-4b64-4388-872b-50efa88cff00" />

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
<img width="162" height="39" alt="image" src="https://github.com/user-attachments/assets/7ca37104-b042-45b2-adf9-18658277cb8d" />

 
 ./funcex.sh 1 2
<img width="294" height="59" alt="image" src="https://github.com/user-attachments/assets/4863a0c4-58bb-49bb-a533-1540f6000e58" />

 
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
 <img width="182" height="69" alt="image" src="https://github.com/user-attachments/assets/e73894da-6a15-4f76-9246-e3d0053a59ee" />

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
 <img width="182" height="69" alt="image" src="https://github.com/user-attachments/assets/c8b2a3f1-fab0-4db4-a0f3-a0b9ee66f004" />

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
 <img width="240" height="246" alt="image" src="https://github.com/user-attachments/assets/1239373b-a0ac-4ef7-9376-af1b0230380b" />

 
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
<img width="280" height="302" alt="image" src="https://github.com/user-attachments/assets/1923cab8-e5e1-464e-a902-415454d94aaf" />

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
<img width="212" height="99" alt="image" src="https://github.com/user-attachments/assets/df3f135d-630e-430e-82e1-28f0ec6f5ded" />


# RESULT:
The Commands are executed successfully.
