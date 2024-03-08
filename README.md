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

![image](./images/s1.png)

cat > file2

```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```

![image](./images/s2.png)

### Display the content of the files

cat < file1

## OUTPUT

![image](./images/s3.png)

cat < file2

## OUTPUT

![image](./images/s4.png)

# Comparing Files

cmp file1 file2

## OUTPUT

![imageg](./images/s5.png)<br>
comm file1 file2

## OUTPUT

![image](./images/s6.png)<br>
diff file1 file2

## OUTPUT

![image](./images/s7.png)

#Filters

### Create the following files file11, file22 as follows:

cat > file11

```
Hello world
This is my world
^d
```

![image](./images/s8.png)
cat > file22

```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```

![image](./images/s9.png)

cut -c1-3 file11

## OUTPUT

![image](./images/s10.png)

cut -d "|" -f 1 file22

## OUTPUT

![image](./images/s11.png)

cut -d "|" -f 2 file22

## OUTPUT

![image](./images/s12.png)

cat < newfile

```
Hello world
hello world
^d
```

![image](./images/s13.png)<br>
cat > newfile

```
Hello world
hello world
```

<br>

![image](./images/s14.png)
<br>
grep Hello newfile

grep hello newfile

## OUTPUT

![image](./images/s15.png)

## OUTPUT

grep -v hello newfile

![image](./images/s16.png)

## OUTPUT

cat newfile | grep -i "hello"

![image](./images/s17.png)

## OUTPUT

cat newfile | grep -i -c "hello"

![image](./images/s18.png)

## OUTPUT

grep -R ubuntu /etc

![image](./images/s19.png)

## OUTPUT

grep -w -n world newfile

![image](./images/s20.png)

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

![image](./images/s21.png)

<br>
cat > newfile

```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

![image](./images/s22.png)

egrep -w 'Hello|hello' newfile

![image](./images/s23.png)

## OUTPUT

egrep -w '(H|h)ello' newfile

![image](./images/s24.png)

## OUTPUT

egrep -w '(H|h)ell[a-z]' newfile

![image](./images/s25.png)

## OUTPUT

egrep '(^hello)' newfile

![image](./images/s26.png)

## OUTPUT

egrep '(world$)' newfile

![image](./images/s27.png)

## OUTPUT

egrep '(World$)' newfile

![image](./images/s28.png)

## OUTPUT

egrep '((W|w)orld$)' newfile

![image](./images/s29.png)

## OUTPUT

egrep '[1-9]' newfile

![image](./images/s30.png)

## OUTPUT

egrep 'Linux.\*world' newfile

## OUTPUT

egrep 'Linux.\*World' newfile

## OUTPUT

egrep l{2} newfile

![image](./images/s31.png)

## OUTPUT

egrep 's{1,2}' newfile

![image](./images/s32.png)

## OUTPUT

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

![image](./images/s33.png)

sed -n -e '3p' file23

![image](./images/s34.png)

## OUTPUT

sed -n -e '$p' file23

![image](./images/s35.png)

## OUTPUT

sed -e 's/Ram/Sita/' file23

![image](./images/s36.png)

## OUTPUT

sed -e '2s/Ram/Sita/' file23

![image](./images/s37.png)

## OUTPUT

sed '/tom/s/5000/6000/' file23

![image](./images/s38.png)

## OUTPUT

sed -n -e '1,5p' file23

![image](./images/s39.png)

## OUTPUT

sed -n -e '2,/Joe/p' file23

![image](./images/s40.png)

## OUTPUT

sed -n -e '/tom/,/Joe/p' file23

![image](./images/s41.png)

## OUTPUT

seq 10

![image](./images/s42.png)

## OUTPUT

seq 10 | sed -n '4,6p'

![image](./images/s43.png)

## OUTPUT

seq 10 | sed -n '2,~4p'

![image](./images/s44.png)

## OUTPUT

seq 3 | sed '2a hello'

![image](./images/s45.png)

## OUTPUT

seq 2 | sed '2i hello'

![image](./images/s46.png)

## OUTPUT

seq 10 | sed '2,9c hello'

![image](./images/s47.png)

## OUTPUT

sed -n '2,4{s/^/$/;p}' file23

![image](./images/s48.png)

## OUTPUT

sed -n '2,4{s/$/\*/;p}' file23

![image](./images/s49.png)

# Sorting File content

cat > file21

```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
```

sort file21

![image](./images/s50.png)

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

![image](./images/s51.png)

uniq file22

![image](./images/s52.png)

## OUTPUT

# Using tr command

cat file23 | tr [:lower:] [:upper:]

![image](./images/s53.png)

## OUTPUT

cat < urllist.txt

```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
```

![image](./images/s54.png)

cat > urllist.txt

```
www. yahoo. com
www. google. com
www. mrcet.... com
```

![image](./images/s55.png)

cat urllist.txt | tr -d ' '

![image](./images/s56.png)

## OUTPUT

cat urllist.txt | tr -d ' ' | tr -s '.'

![image](./images/s57.png)

## OUTPUT

# Backup commands

tar -cvf backup.tar \*

![image](./images/s58.png)

## OUTPUT

mkdir backupdir

mv backup.tar backupdir

![image](./images/s59.png)

tar -tvf backup.tar

![image](./images/s60.png)

## OUTPUT

tar -xvf backup.tar

![image](./images/s61.png)

## OUTPUT

gzip backup.tar

ls .gz

![image](./images/s62.png)

## OUTPUT

gunzip backup.tar.gz

![image](./images/s63.png)

## OUTPUT

# Shell Script

```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```

![image](./images/s64.png)

chmod 755 my-script.sh
./my-script.sh

![image](./images/s65.png)

## OUTPUT

cat << stop > herecheck.txt

```
hello in this world
i cant stop
for this non stop movement
stop
```

![image](./images/s66.png)

cat herecheck.txt

![image](./images/s67.png)

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

![image](./images/s68.png)

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

![image](./images/s69.png)

chmod 777 scriptest.sh

./scriptest.sh 1 2 3

![image](./images/s70.png)

## OUTPUT

ls file1

![image](./images/s71.png)

## OUTPUT

echo $?

![image](./images/s72.png)

## OUTPUT

./one
bash: ./one: Permission denied

echo $?

![image](./images/s73.png)

## OUTPUT

abcd

echo $?

![image](./images/s74.png)

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

![image](./images/s76.png)

## OUTPUT

chmod 755 strcomp.sh

./strcomp.sh

![image](./images/s77.png)

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

![image](./images/s78.png)

./psswdperm.sh

![image](./images/s79.png)

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

![image](./images/s81.png)


./ifnested.sh

![image](./images/s80.png)

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

![image](./images/s82.png)

$ chmod 755 iftest.sh

$ ./iftest.sh

![image](./images/s83.png)

## OUTPUT

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
![image](./images/s84.png)

$ chmod 755 ifnested.sh

$ ./ifnested.sh

![image](./images/s85.png)

## OUTPUT

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

![image](./images/s86.png)

$ chmod 755 elifcheck.sh

$ ./elifcheck.sh

![image](./images/s87.png)

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

![image](./images/s88.png)

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

![image](./images/s89.png)

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

![image](./images/s90.png)

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

$ ./untiltest.sh

![image](./images/s91.png)

cat forin1.sh

```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```

![image](./images/s92.png)

$ chmod 755 forin1.sh

$ ./forin1.sh

![image](./images/s93.png)

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

![image](./images/s94.png)

cat forin3.sh

```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ chmod 755 forin3.sh

$ ./forin3.sh

![image](./images/s95.png)


## OUTPUT

cat forinfile.sh

```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in "cat $file"
do
echo "Visit beautiful $state“
done
```

$ chmod 777 forinfile.sh

$ cat cities

Hyderabad <br>
Alampur      <br>
Basara<br>
Warangal<br>
Adilabad<br>
Bhadrachalam<br>
Khammam<br>

![image](./images/s97.png)

![image](./images/s96.png)

## OUTPUT

cat forctype.sh

```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
```

$ chmod 755 forctype.sh
$ ./forctype.sh

![image](./images/s98.png)

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

![image](./images/s99.png)

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

![image](./images/s100.png)

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
echo "The for loop is completed"
```

## OUTPUT

$ chmod 755 forbreak.sh

$ ./forbreak.sh

![image](./images/s101.png)

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
echo "The for loop is completed"
```

$ chmod 755 forcontinue.sh

$ ./forcontinue.sh

![image](./images/s102.png)

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

![image](./images/s103.png)

## OUTPUT

cat exread1.sh

```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
```

$ chmod 755 exread1.sh

$ ./exread1.sh

![image](./images/s104.png)

## OUTPUT


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

![image](./images/s105.png)

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

![image](./images/s106.png)

cat argshift1.sh

```bash
args=("$@")
ELEMENTS=${#args[@]}
for (( i=0;i<$ELEMENTS;i++)); do
    echo ${args[${i}]}
done
```

$ chmod 777 argshift.sh

## OUTPUT

$ ./argshift.sh 1 2 3

![image](./images/s107.png)

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

![image](./images/s108.png)

cat > nc.awk

```bash
BEGIN{}
{
print len=length($0),"\t",$0
wordcount+=NF
chrcnt+=len
}
END{}
{
print "total characters",chrcnt
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
```

![image](./images/s109.png)

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

![image](./images/s110.png)

awk -f nc.awk data.dat

![image](./images/s111.png)

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

$ chmod 755 palindrome.sh

$ ./palindrome.sh

![image](./images/s112.png)

# RESULT:

The Commands are executed successfully.
