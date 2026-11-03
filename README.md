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
<img width="662" height="195" alt="image" src="https://github.com/user-attachments/assets/d6b9d9c3-832d-4416-aaa7-cac63408265d" />



cat < file2
## OUTPUT
<img width="670" height="218" alt="image" src="https://github.com/user-attachments/assets/ee6be1c1-56fb-4f32-82d1-a71d731e86e0" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="588" height="77" alt="image" src="https://github.com/user-attachments/assets/efb20180-9e49-4e3f-9f03-fc74368ea413" />

comm file1 file2
 ## OUTPUT
<img width="621" height="225" alt="image" src="https://github.com/user-attachments/assets/8c86794c-b446-4dcd-83b0-25e7f52de473" />

 
diff file1 file2
## OUTPUT
<img width="668" height="336" alt="image" src="https://github.com/user-attachments/assets/d0ecc059-6d63-4803-aa55-d3e33f845305" />


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
<img width="617" height="112" alt="image" src="https://github.com/user-attachments/assets/c1042ea7-11b7-445a-a0ea-29d62b9cf7fe" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="651" height="133" alt="image" src="https://github.com/user-attachments/assets/ffeb14fe-9218-4d55-b86f-095fa11cf762" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="628" height="136" alt="image" src="https://github.com/user-attachments/assets/e2e56449-d877-4e1f-83ac-c35b5227364f" />



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
<img width="612" height="66" alt="image" src="https://github.com/user-attachments/assets/bf7d0899-f65a-473f-82ac-33d462e9d63c" />




grep hello newfile 
## OUTPUT
<img width="607" height="71" alt="image" src="https://github.com/user-attachments/assets/763b67af-0f23-4931-9635-0976a50a96bc" />




grep -v hello newfile 
## OUTPUT
<img width="656" height="87" alt="image" src="https://github.com/user-attachments/assets/f2b07bb9-4520-49a3-974f-cd1de671b06d" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="617" height="77" alt="image" src="https://github.com/user-attachments/assets/ee45cabc-47fe-4003-b80c-0e98811f56b4" />








grep -R ubuntu /etc
## OUTPUT
<img width="893" height="652" alt="image" src="https://github.com/user-attachments/assets/0bd2deec-619b-46dc-8ce2-1c86e7963c77" />



grep -w -n world newfile   


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
<img width="573" height="96" alt="image" src="https://github.com/user-attachments/assets/7b737c62-1ea7-4735-9f5c-646ee4c5c096" />




egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="562" height="100" alt="image" src="https://github.com/user-attachments/assets/53119e31-127b-4406-b48f-722c88f91401" />




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="561" height="90" alt="image" src="https://github.com/user-attachments/assets/de8d5b81-0635-40f7-b577-d6d0d945be25" />





egrep '(^hello)' newfile 
## OUTPUT
<img width="622" height="67" alt="image" src="https://github.com/user-attachments/assets/0415cc01-e370-42f8-9be7-d67789c81596" />



egrep '(world$)' newfile 
## OUTPUT
<img width="575" height="95" alt="image" src="https://github.com/user-attachments/assets/28ed75fc-fdfa-49c5-95cc-ac599ba3f0da" />



egrep '(World$)' newfile 

## OUTPUT
<img width="657" height="138" alt="image" src="https://github.com/user-attachments/assets/78ac4ca1-2677-4f36-b891-aa81d6c22927" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="605" height="87" alt="image" src="https://github.com/user-attachments/assets/8f145319-3229-42cf-908f-8a36f061044a" />






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
<img width="615" height="71" alt="image" src="https://github.com/user-attachments/assets/d587b09c-bc67-4e44-9075-45dab4a08367" />



sed -n -e '$p' file23
## OUTPUT
<img width="576" height="75" alt="image" src="https://github.com/user-attachments/assets/19c90884-38cc-4d8a-aa77-f3b5253c904b" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="575" height="300" alt="image" src="https://github.com/user-attachments/assets/725f7644-21f9-4e66-a5a5-b03291d7fd60" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="581" height="303" alt="image" src="https://github.com/user-attachments/assets/c7477a5a-62f4-4ac1-9ab0-a392af937b58" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="583" height="300" alt="image" src="https://github.com/user-attachments/assets/da0364c3-470c-4247-b4ee-a029969c79c3" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="552" height="185" alt="image" src="https://github.com/user-attachments/assets/125ab1ae-7341-48dc-bf09-e4b62ac1f053" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="547" height="130" alt="image" src="https://github.com/user-attachments/assets/e43285d7-3c3f-4542-a58d-9e8a19f3edf8" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="562" height="105" alt="image" src="https://github.com/user-attachments/assets/61c59230-4a3e-4722-9bbd-5cb04b0db04a" />



seq 10 
## OUTPUT
<img width="580" height="342" alt="image" src="https://github.com/user-attachments/assets/87c0ea56-768d-44c5-9270-7da95a83955f" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="600" height="122" alt="image" src="https://github.com/user-attachments/assets/2136bbc2-01f9-45fa-be44-1526f644e008" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="567" height="133" alt="image" src="https://github.com/user-attachments/assets/85fcc099-e0e3-412b-83d7-05cdb01d794c" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="562" height="160" alt="image" src="https://github.com/user-attachments/assets/f946db25-2385-4949-a5fb-6c7f8d12b718" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="571" height="138" alt="image" src="https://github.com/user-attachments/assets/d0083e9a-9238-4f0a-b21d-4c4bcc2cf467" />


seq 10 | sed '2,9c hello'



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
<img width="583" height="155" alt="image" src="https://github.com/user-attachments/assets/e9305e10-e27c-43d7-be40-cffff532bacc" />



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
<img width="607" height="166" alt="image" src="https://github.com/user-attachments/assets/a4705e4d-9f42-48c7-8838-52d3f1b0bd4d" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 <img width="562" height="300" alt="image" src="https://github.com/user-attachments/assets/c8531fec-563d-42bd-9967-03c51c0eb10d" />


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
<img width="461" height="145" alt="image" src="https://github.com/user-attachments/assets/3587bcac-cdfa-404c-a70a-5c13a701e9f9" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="550" height="127" alt="image" src="https://github.com/user-attachments/assets/7365f1b4-cc25-4f3f-9e88-161d18771e77" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="872" height="628" alt="image" src="https://github.com/user-attachments/assets/b2c7b3af-8745-4b78-89a7-fcb7d9c65b9c" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="887" height="667" alt="image" src="https://github.com/user-attachments/assets/6b1e75d7-5952-49e9-8811-5b45b7e17f82" />


tar -xvf backup.tar
## OUTPUT
<img width="861" height="617" alt="image" src="https://github.com/user-attachments/assets/dcdd2d61-f874-41b0-9d41-566fea924620" />

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

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
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
<img width="572" height="317" alt="image" src="https://github.com/user-attachments/assets/dcfb285b-fc17-4860-9ea2-e5e4715f9a55" />


# RESULT:
The Commands are executed successfully.
