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

<img width="434" height="139" alt="image" src="https://github.com/user-attachments/assets/bf3b2ce8-033d-440e-8d78-e7550468b301" />


cat < file2
## OUTPUT

<img width="432" height="175" alt="image" src="https://github.com/user-attachments/assets/72e15d01-b886-4e29-9362-5478ac18662a" />


# Comparing Files
cmp file1 file2
## OUTPUT

<img width="477" height="65" alt="image" src="https://github.com/user-attachments/assets/d0a8a361-dae8-43f1-8665-6e6fff78196e" />

 
comm file1 file2
 ## OUTPUT

<img width="488" height="255" alt="image" src="https://github.com/user-attachments/assets/5331fa72-7c92-4135-9644-b988728771c1" />

 
diff file1 file2
## OUTPUT

<img width="455" height="337" alt="image" src="https://github.com/user-attachments/assets/35f00396-6817-4f7a-99be-d4ef2761a200" />


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

<img width="459" height="88" alt="image" src="https://github.com/user-attachments/assets/8ff656c1-3fa1-4977-a242-5027284ec41e" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="495" height="111" alt="image" src="https://github.com/user-attachments/assets/03571bf5-1883-495a-928b-9e459e2c888c" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="547" height="117" alt="image" src="https://github.com/user-attachments/assets/eb9783e6-9a62-4097-93c5-2186c6ee65c6" />


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

<img width="453" height="70" alt="image" src="https://github.com/user-attachments/assets/469b0db2-8e63-4d1d-aabd-0c4848f8f5b5" />


grep hello newfile 
## OUTPUT

<img width="458" height="64" alt="image" src="https://github.com/user-attachments/assets/671e0906-f1f2-454a-88aa-99d9f1c29680" />



grep -v hello newfile 
## OUTPUT

<img width="458" height="64" alt="image" src="https://github.com/user-attachments/assets/35889d14-bdb9-465b-8021-9df28e045b7c" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="516" height="87" alt="image" src="https://github.com/user-attachments/assets/49a943b2-8c34-49d8-804e-8b2a78415d77" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="546" height="62" alt="image" src="https://github.com/user-attachments/assets/c500a1f7-cb03-47a6-b1c7-c914a42c324b" />



grep -R ubuntu /etc
## OUTPUT

<img width="801" height="263" alt="image" src="https://github.com/user-attachments/assets/7565070d-3494-402c-b7fa-ace5cf428ece" />


grep -w -n world newfile   
## OUTPUT

<img width="639" height="82" alt="image" src="https://github.com/user-attachments/assets/a1d56459-0537-4d85-a025-755224c2d5c1" />


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

<img width="529" height="90" alt="image" src="https://github.com/user-attachments/assets/c386a168-0e63-4dfb-9620-365c645dad58" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="548" height="111" alt="image" src="https://github.com/user-attachments/assets/01e9d48e-df97-45e3-9d92-778895c2f0b6" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="481" height="56" alt="image" src="https://github.com/user-attachments/assets/5fb8808f-5488-4b24-8849-1791803914ea" />


egrep '(world$)' newfile 
## OUTPUT

<img width="516" height="79" alt="image" src="https://github.com/user-attachments/assets/d1aa7f0a-6073-483c-82ad-3f091d445451" />


egrep '(World$)' newfile 
## OUTPUT

<img width="566" height="71" alt="image" src="https://github.com/user-attachments/assets/d7970b7f-3c60-47ff-92e7-4f4f479998e8" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="556" height="111" alt="image" src="https://github.com/user-attachments/assets/02f27de6-e139-4e0d-b51e-f1db56188b89" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="533" height="67" alt="image" src="https://github.com/user-attachments/assets/9ea0f096-35d7-4a75-b0d3-31fa9d4d1624" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="523" height="57" alt="image" src="https://github.com/user-attachments/assets/0c4a6636-8498-43dd-b373-7320735bb673" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="529" height="61" alt="image" src="https://github.com/user-attachments/assets/9445a6c9-910a-4d52-b5d1-e6b892baf927" />


egrep l{2} newfile
## OUTPUT

<img width="534" height="76" alt="image" src="https://github.com/user-attachments/assets/df1a82c9-ec13-4085-a48c-d32cd69fcaa9" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="483" height="104" alt="image" src="https://github.com/user-attachments/assets/0da27f23-650e-4ea9-8ea9-5d7c33397073" />


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

<img width="492" height="59" alt="image" src="https://github.com/user-attachments/assets/4ea5d737-1af6-44ba-8389-5c921f40c866" />


sed -n -e '$p' file23
## OUTPUT

<img width="508" height="63" alt="image" src="https://github.com/user-attachments/assets/e6cd43a2-b182-4673-82d6-9487f2402fc8" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="538" height="255" alt="image" src="https://github.com/user-attachments/assets/d5c0fdcd-5ddf-454e-91c9-93dce459278b" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="534" height="258" alt="image" src="https://github.com/user-attachments/assets/f2d1ad1c-30a6-408d-961e-39c9c4f7ff20" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="536" height="86" alt="image" src="https://github.com/user-attachments/assets/2e5cfbc4-d4cb-4f21-a362-a4404527a93c" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="521" height="177" alt="image" src="https://github.com/user-attachments/assets/dcc27a2e-0f5e-45ce-80b6-af0e1c7172e0" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="515" height="126" alt="image" src="https://github.com/user-attachments/assets/79c3605a-d966-428e-ae50-57aba19e12bf" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="547" height="247" alt="image" src="https://github.com/user-attachments/assets/b1c68300-d4f7-4189-9f91-0ca3a7f41a87" />


seq 10 
## OUTPUT

<img width="509" height="308" alt="image" src="https://github.com/user-attachments/assets/e9480da6-0215-445b-9ce4-e2fa9e645dc2" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="491" height="117" alt="image" src="https://github.com/user-attachments/assets/e8d5c5da-c989-4a22-ac50-a0757b7edb00" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="492" height="108" alt="image" src="https://github.com/user-attachments/assets/6c455074-ef50-4a52-8213-de3e40403195" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="504" height="137" alt="image" src="https://github.com/user-attachments/assets/ea561ae6-c477-4bb0-87d8-07391ab1520c" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="501" height="107" alt="image" src="https://github.com/user-attachments/assets/b0c46fa8-d417-4713-8882-966f113503b1" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="490" height="114" alt="image" src="https://github.com/user-attachments/assets/a4aaabfb-dd9a-47b1-bb65-7d3724bed5ea" />



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="551" height="116" alt="image" src="https://github.com/user-attachments/assets/04a274d2-6617-43c4-9102-0b054557acb4" />
<img width="514" height="116" alt="image" src="https://github.com/user-attachments/assets/17e60b95-009b-4e5c-9f3f-28e5d7f25cad" />


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

<img width="527" height="175" alt="image" src="https://github.com/user-attachments/assets/c826e1dc-a90e-4c17-a487-aa2e581bd86d" />


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

<img width="444" height="167" alt="image" src="https://github.com/user-attachments/assets/30ca8d6a-144c-4239-bf68-bd3aa7c655de" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

 <img width="605" height="243" alt="image" src="https://github.com/user-attachments/assets/068b80c0-369b-4850-b141-0c8d11e5fe11" />


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

<img width="493" height="110" alt="image" src="https://github.com/user-attachments/assets/33bb58ca-f6a2-4fbb-9507-0178b3ff76a1" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="694" height="494" alt="image" src="https://github.com/user-attachments/assets/dae7598e-aff3-4f94-8339-56d57c304d25" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="556" height="373" alt="image" src="https://github.com/user-attachments/assets/9e8c6c98-2748-4b69-b9d0-27de928ef6e9" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="694" height="494" alt="image" src="https://github.com/user-attachments/assets/111bf3aa-6529-46ab-9e5d-9f7daa023f9a" />


tar -xvf backup.tar
## OUTPUT

<img width="800" height="311" alt="image" src="https://github.com/user-attachments/assets/193f52bc-d722-4abf-a8f4-016ae0e8afd7" />


gzip backup.tar

ls .gz
## OUTPUT

<img width="651" height="46" alt="image" src="https://github.com/user-attachments/assets/818c998f-63bc-4b86-8628-7a2b965fee6c" />

 
gunzip backup.tar.gz
## OUTPUT

<img width="793" height="121" alt="image" src="https://github.com/user-attachments/assets/ab085b11-0c15-4230-a365-a23ee12e3b71" />


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="796" height="117" alt="image" src="https://github.com/user-attachments/assets/78b40cef-e3f2-4d00-9a0c-c1c9a879e2ca" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="699" height="174" alt="image" src="https://github.com/user-attachments/assets/76399990-2c13-468d-bf16-77d95273ac34" />


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

<img width="805" height="148" alt="image" src="https://github.com/user-attachments/assets/a8d12bce-0c3e-4aad-b15b-9e90c2055088" />

 
ls file1
## OUTPUT

<img width="668" height="153" alt="image" src="https://github.com/user-attachments/assets/2b8ac5c4-bebc-491b-bf48-290276820871" />


echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

<img width="805" height="157" alt="image" src="https://github.com/user-attachments/assets/1652fbec-656d-4bff-8933-bca5397a30cb" />

 
abcd
 
echo $?
 ## OUTPUT

<img width="716" height="156" alt="image" src="https://github.com/user-attachments/assets/be8af67f-fd1d-4150-bd3b-af05c174ca01" />

 
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

<img width="703" height="197" alt="image" src="https://github.com/user-attachments/assets/71ebf48b-1d0f-460c-bbcb-6cd9437c55da" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="657" height="90" alt="image" src="https://github.com/user-attachments/assets/4f63b09a-48d4-4b1f-8426-ffb8451bce3d" />


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

<img width="654" height="71" alt="image" src="https://github.com/user-attachments/assets/9156bcba-ccd4-45d5-8b95-e085e31fcfc6" />


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

<img width="646" height="437" alt="image" src="https://github.com/user-attachments/assets/20fcb242-c002-46f3-bca3-317b39856a72" />


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

<img width="676" height="100" alt="image" src="https://github.com/user-attachments/assets/f595730b-065e-439c-8f7c-18a647653c45" />


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

<img width="664" height="143" alt="image" src="https://github.com/user-attachments/assets/27baa84c-d333-4d5f-b6c9-05b29c10aef9" />


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

<img width="660" height="73" alt="image" src="https://github.com/user-attachments/assets/095fa538-b42e-4ddd-b48e-a27ceec5cdbe" />


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

<img width="662" height="239" alt="image" src="https://github.com/user-attachments/assets/c60c49cc-51de-464d-948d-60cd825d9037" />


 
 
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
 
<img width="703" height="126" alt="image" src="https://github.com/user-attachments/assets/95be849b-5ab2-4213-9f29-928e62d50658" />
 
 
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

<img width="633" height="220" alt="image" src="https://github.com/user-attachments/assets/ebad0978-38c9-4c70-858a-98ddc1f0b8cc" />

 
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

<img width="731" height="176" alt="image" src="https://github.com/user-attachments/assets/ac57b0a6-f674-413b-aaad-a1db2facafa7" />

 
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

<img width="512" height="179" alt="image" src="https://github.com/user-attachments/assets/764ad4ad-33ce-41ed-aeb7-bfc0741a316e" />

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

<img width="784" height="260" alt="image" src="https://github.com/user-attachments/assets/4d330b02-560c-4286-a67c-aa530c5a16ae" />


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

<img width="620" height="220" alt="image" src="https://github.com/user-attachments/assets/e986a63c-392b-4e75-8291-0e3ba280ec30" />


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

<img width="591" height="214" alt="image" src="https://github.com/user-attachments/assets/9257d1d0-c432-4941-8b92-aad9b42911d1" />


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

 <img width="625" height="413" alt="image" src="https://github.com/user-attachments/assets/b1caa890-b056-4837-84cc-82a127d31499" />

 
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

<img width="602" height="179" alt="image" src="https://github.com/user-attachments/assets/93695eb5-2812-48e8-8e28-1d96ac402522" />


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

<img width="665" height="214" alt="image" src="https://github.com/user-attachments/assets/d4436819-305b-4469-9b01-34802af5690a" />

 
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

<img width="569" height="115" alt="image" src="https://github.com/user-attachments/assets/870de7b3-e7b9-45a8-a058-d3387b07ec5b" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="562" height="113" alt="image" src="https://github.com/user-attachments/assets/b8443621-879e-4dac-8096-f777ac4ccb27" />


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

<img width="602" height="63" alt="image" src="https://github.com/user-attachments/assets/401d7705-0c79-4cb3-be1c-66f7f06c0f9a" />

 
 ./funcex.sh 1 2

 <img width="799" height="38" alt="image" src="https://github.com/user-attachments/assets/57ca6647-7867-4cb3-a29e-31467d185965" />

 
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

<img width="627" height="175" alt="image" src="https://github.com/user-attachments/assets/70ae8bbc-5531-46d4-9429-9a3f3fb905e1" />

 
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

<img width="549" height="139" alt="image" src="https://github.com/user-attachments/assets/c6b6897c-6026-491b-ab66-0342bea73b41" />

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
 
 <img width="579" height="441" alt="image" src="https://github.com/user-attachments/assets/d8399f23-c05e-40e7-8081-db02df1d4f3b" />

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

<img width="554" height="351" alt="image" src="https://github.com/user-attachments/assets/7737468d-d73c-4e79-9de5-691cdaf7204f" />

 
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

<img width="557" height="142" alt="image" src="https://github.com/user-attachments/assets/3b87afff-46d9-480b-8634-3bc9946c88d6" />


# RESULT:
The Commands are executed successfully.
