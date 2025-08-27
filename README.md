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

<img width="374" height="156" alt="image" src="https://github.com/user-attachments/assets/8e628045-974a-4d57-ba2e-c8fb7c2b8cea" />


cat < file2
## OUTPUT

<img width="365" height="174" alt="image" src="https://github.com/user-attachments/assets/d807d75a-bef3-46fb-966e-d0075e2e1282" />


# Comparing Files
cmp file1 file2
## OUTPUT

<img width="543" height="85" alt="Screenshot 2025-08-11 113043" src="https://github.com/user-attachments/assets/8e49e2f7-3b0d-4f6c-b485-6b1e714947e6" />


 
comm file1 file2
 ## OUTPUT

<img width="456" height="303" alt="Screenshot 2025-08-11 114006" src="https://github.com/user-attachments/assets/7a12c34c-3a67-46f4-840e-1b14d0ce9393" />



 
diff file1 file2
## OUTPUT

<img width="386" height="274" alt="Screenshot 2025-08-11 113131" src="https://github.com/user-attachments/assets/09a84f1f-70a0-4979-8c51-dda9939020a1" />

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

<img width="470" height="108" alt="Screenshot 2025-08-11 113507" src="https://github.com/user-attachments/assets/a3a4287b-44f1-468f-8d88-06aeff6ab113" />



cut -d "|" -f 1 file22
## OUTPUT



cut -d "|" -f 2 file22
## OUTPUT


<img width="404" height="131" alt="Screenshot 2025-08-11 113720" src="https://github.com/user-attachments/assets/99244201-f07d-47d9-b71c-25b4db496d6b" />



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

<img width="407" height="82" alt="Screenshot 2025-08-11 114257" src="https://github.com/user-attachments/assets/a5a0c87d-01c9-40e9-8845-a722525fccc4" />


grep hello newfile 
## OUTPUT

<img width="446" height="68" alt="Screenshot 2025-08-11 114332" src="https://github.com/user-attachments/assets/346cdae2-dc19-4118-8b5c-e7203bfef36a" />



grep -v hello newfile 
## OUTPUT

<img width="431" height="77" alt="Screenshot 2025-08-11 114355" src="https://github.com/user-attachments/assets/a09854e0-6f30-4c7a-9bf2-bcbe41b3784d" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="407" height="106" alt="Screenshot 2025-08-11 114428" src="https://github.com/user-attachments/assets/bd94d45d-acab-46fe-8022-caf59ae86968" />



cat newfile | grep -i -c "hello"
## OUTPUT


<img width="430" height="77" alt="Screenshot 2025-08-11 114509" src="https://github.com/user-attachments/assets/f72d50a4-0bdc-496e-acd1-79b4d1c6a1fd" />



grep -R ubuntu /etc
## OUTPUT

<img width="798" height="523" alt="Screenshot 2025-08-11 114702" src="https://github.com/user-attachments/assets/e1cb3e73-f1ab-41e2-be1c-3c33c207e951" />



grep -w -n world newfile   
## OUTPUT

<img width="394" height="100" alt="Screenshot 2025-08-11 114759" src="https://github.com/user-attachments/assets/e9bc6c7f-5f9f-46bf-9aaa-1059470c1330" />



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

<img width="415" height="107" alt="Screenshot 2025-08-11 150207" src="https://github.com/user-attachments/assets/4032785a-2603-4e06-a7bf-fbab8f4c94fa" />


egrep -w '(H|h)ello' newfile 
## OUTPUT


<img width="502" height="103" alt="Screenshot 2025-08-11 150318" src="https://github.com/user-attachments/assets/1b86d7c1-8fd2-45d0-86cd-961f87be51b6" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="502" height="103" alt="Screenshot 2025-08-11 150318" src="https://github.com/user-attachments/assets/6348c2fb-82e4-4be5-a10a-70d07d71f826" />



egrep '(^hello)' newfile 
## OUTPUT



egrep '(world$)' newfile 
## OUTPUT

<img width="434" height="76" alt="Screenshot 2025-08-11 150527" src="https://github.com/user-attachments/assets/e823e1f1-9252-4238-a084-1909907d4f5f" />


egrep '(World$)' newfile 
## OUTPUT


<img width="466" height="135" alt="Screenshot 2025-08-11 150605" src="https://github.com/user-attachments/assets/2196843a-27e6-4c6a-b0d7-300c79614f97" />



egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="416" height="129" alt="Screenshot 2025-08-11 151249" src="https://github.com/user-attachments/assets/0894f06e-9550-4acd-a55f-4a6fad3adfae" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="443" height="80" alt="Screenshot 2025-08-11 151323" src="https://github.com/user-attachments/assets/5df1fa98-aea7-4623-a615-74410049ab2f" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="415" height="97" alt="Screenshot 2025-08-11 183724" src="https://github.com/user-attachments/assets/05c5ef62-5b0b-4228-a0f6-ce58ad58b852" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="459" height="68" alt="Screenshot 2025-08-25 115210" src="https://github.com/user-attachments/assets/53aa5169-95a2-46f9-9aff-2d8c20579175" />


egrep l{2} newfile
## OUTPUT

<img width="361" height="144" alt="image" src="https://github.com/user-attachments/assets/62b5f69a-810e-4950-965f-dc3c7286f262" />




egrep 's{1,2}' newfile
## OUTPUT 


<img width="473" height="127" alt="Screenshot 2025-08-11 183941" src="https://github.com/user-attachments/assets/5010c167-fb5a-4274-839e-42fc8bf339b9" />




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


<img width="456" height="70" alt="Screenshot 2025-08-11 184356" src="https://github.com/user-attachments/assets/cf3cdb1f-2e49-4d82-a469-aad57e1fa200" />




sed -n -e '$p' file23
## OUTPUT

<img width="446" height="72" alt="Screenshot 2025-08-11 184438" src="https://github.com/user-attachments/assets/f081cfca-8999-4831-98eb-242edb83a5a3" />





sed  -e 's/Ram/Sita/' file23
## OUTPUT


<img width="407" height="250" alt="Screenshot 2025-08-11 185019" src="https://github.com/user-attachments/assets/2efb3e46-4479-4d39-a17e-4e915c8d6f1a" />





sed  -e '2s/Ram/Sita/' file23
## OUTPUT



<img width="378" height="229" alt="Screenshot 2025-08-11 185116" src="https://github.com/user-attachments/assets/60bd0b5a-123d-4eaf-8b77-3ea1b89baaa0" />






sed  '/tom/s/5000/6000/' file23
## OUTPUT



<img width="456" height="236" alt="Screenshot 2025-08-11 185218" src="https://github.com/user-attachments/assets/30d89feb-cfb9-43c2-9004-c2cbfda96fb6" />






sed -n -e '1,5p' file23
## OUTPUT



<img width="415" height="188" alt="Screenshot 2025-08-11 185250" src="https://github.com/user-attachments/assets/dd491b3d-124c-4312-a427-bdbbf08cb9b0" />






sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="409" height="134" alt="Screenshot 2025-08-11 190219" src="https://github.com/user-attachments/assets/fbb89e09-8aab-4a82-82d6-f96a4f6148b3" />





sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


<img width="461" height="103" alt="Screenshot 2025-08-11 190421" src="https://github.com/user-attachments/assets/2cd9cebc-63a0-429d-b42f-28bcb0df26a6" />






seq 10 
## OUTPUT

<img width="449" height="295" alt="Screenshot 2025-08-11 190532" src="https://github.com/user-attachments/assets/3dcee15d-3131-4a8e-9c2e-63f30f073335" />












seq 10 | sed -n '4,6p'
## OUTPUT


<img width="398" height="123" alt="Screenshot 2025-08-11 190631" src="https://github.com/user-attachments/assets/9a381111-315d-4b46-990f-f440f31b7e51" />









seq 10 | sed -n '2,~4p'
## OUTPUT


<img width="362" height="123" alt="Screenshot 2025-08-11 190748" src="https://github.com/user-attachments/assets/c761c91c-27c5-456f-b7a8-c364cd1988f4" />






seq 3 | sed '2a hello'
## OUTPUT

<img width="423" height="136" alt="Screenshot 2025-08-11 190824" src="https://github.com/user-attachments/assets/17728148-e3b5-47d7-9565-69160b76b330" />







seq 2 | sed '2i hello'
## OUTPUT

<img width="500" height="126" alt="Screenshot 2025-08-11 192533" src="https://github.com/user-attachments/assets/b99cbc07-c7f5-4a38-944d-1e3ddf8b8505" />







seq 10 | sed '2,9c hello'
## OUTPUT


<img width="391" height="135" alt="Screenshot 2025-08-11 192633" src="https://github.com/user-attachments/assets/31ff0a9d-eb15-4a68-97e2-9cbdaec02b84" />








sed -n '2,4{s/^/$/;p}' file23
## OUTPUT



<img width="516" height="136" alt="Screenshot 2025-08-11 192740" src="https://github.com/user-attachments/assets/c71c8dd2-53da-4f14-8ef5-b4e3d02d6ad3" />





sed -n '2,4{s/$/*/;p}' file23
## OUTPUT


<img width="387" height="133" alt="Screenshot 2025-08-11 192858" src="https://github.com/user-attachments/assets/7b6b19a1-2818-4033-ba36-244ba9020050" />






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

<img width="365" height="200" alt="Screenshot 2025-08-11 193352" src="https://github.com/user-attachments/assets/1a9a9ca0-4f35-4005-beac-e6c6d36da50e" />




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

<img width="335" height="190" alt="Screenshot 2025-08-11 193721" src="https://github.com/user-attachments/assets/f01e2c5e-96da-414f-9aaa-17fdbb8a9eb9" />







#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

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

<img width="374" height="137" alt="image" src="https://github.com/user-attachments/assets/329ca012-f3d2-4284-9b9a-cd42fa6bc3c3" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="511" height="157" alt="Screenshot 2025-08-11 194626" src="https://github.com/user-attachments/assets/c5cda69e-a7ae-4ae1-b55c-02e1a34dfe48" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="336" height="307" alt="Screenshot 2025-08-11 194714" src="https://github.com/user-attachments/assets/43ee9b4e-8715-451c-8fec-9e05fac137de" />




mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="613" height="296" alt="Screenshot 2025-08-11 194838" src="https://github.com/user-attachments/assets/d311066e-73bd-4ed0-a65b-e5ca90b8af65" />



tar -xvf backup.tar
## OUTPUT

<img width="357" height="349" alt="image" src="https://github.com/user-attachments/assets/74482222-cbca-4a5a-beb5-f62f7fa2a6a8" />




gzip backup.tar
## OUTPUT

<img width="297" height="53" alt="Screenshot 2025-08-11 195120" src="https://github.com/user-attachments/assets/ea962dcd-799c-410e-8be4-3f16008f7d01" />







ls .gz
## OUTPUT

<img width="455" height="75" alt="Screenshot 2025-08-11 195134" src="https://github.com/user-attachments/assets/bd9db73f-f1b8-4375-a6d9-128910b90e20" />


 
gunzip backup.tar.gz
## OUTPUT


<img width="589" height="152" alt="Screenshot 2025-08-11 195247" src="https://github.com/user-attachments/assets/29ccbd78-e4fc-4153-8da2-4b2eeffd2a09" />




 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="581" height="302" alt="Screenshot 2025-08-11 195710" src="https://github.com/user-attachments/assets/fa456597-0d50-438c-9a7a-7fdc65019b13" />




 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="414" height="279" alt="Screenshot 2025-08-11 195853" src="https://github.com/user-attachments/assets/bd1da3ee-bb46-46d0-84af-5ae954259d05" />





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



<img width="443" height="318" alt="Screenshot 2025-08-11 201937" src="https://github.com/user-attachments/assets/28f9a947-7ded-4d83-98a9-5422666c47ab" />



 
ls file1
## OUTPUT


<img width="477" height="76" alt="Screenshot 2025-08-11 202133" src="https://github.com/user-attachments/assets/abd5789c-aeb1-40db-a11e-9be718a5ace3" />




echo $?
## OUTPUT 


<img width="450" height="79" alt="Screenshot 2025-08-11 201955" src="https://github.com/user-attachments/assets/ff555755-f588-4446-b091-fe03b91c5477" />

 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


<img width="343" height="77" alt="image" src="https://github.com/user-attachments/assets/3c3717f3-bba1-4cda-82b5-7a9dd45211cb" />

 
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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


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
