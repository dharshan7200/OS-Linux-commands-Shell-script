OS-Linux-commands-Shell-scripting
Operating systems Lab exercise

Linux commands-Shell scripting
Linux commands-Shell scripting

AIM:
To practice Linux Commands and Shell Scripting

DESIGN STEPS:
Step 1:
Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

Step 2:
Execute the following commands

Step 3:
Testing the commands for the desired output.

COMMANDS:
Create the following files file1, file2 as follows:
cat > file1

chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
image

cat > file2

anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
image

Display the content of the files
cat < file1

OUTPUT
image

cat < file2

OUTPUT
image

Comparing Files
cmp file1 file2

OUTPUT
imageg
comm file1 file2

OUTPUT
image
diff file1 file2

OUTPUT
image

#Filters

Create the following files file11, file22 as follows:
cat > file11

Hello world
This is my world
^d
image cat > file22

1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
image

cut -c1-3 file11

OUTPUT
image

cut -d "|" -f 1 file22

OUTPUT
image

cut -d "|" -f 2 file22

OUTPUT
image

cat < newfile

Hello world
hello world
^d
image
cat > newfile

Hello world
hello world

image
grep Hello newfile

grep hello newfile

OUTPUT
image

OUTPUT
grep -v hello newfile

image

OUTPUT
cat newfile | grep -i "hello"

image

OUTPUT
cat newfile | grep -i -c "hello"

image

OUTPUT
grep -R ubuntu /etc

image

OUTPUT
grep -w -n world newfile

image

OUTPUT
cat < newfile

Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
image


cat > newfile
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
image

egrep -w 'Hello|hello' newfile

image

OUTPUT
egrep -w '(H|h)ello' newfile

image

OUTPUT
egrep -w '(H|h)ell[a-z]' newfile

image

OUTPUT
egrep '(^hello)' newfile

image

OUTPUT
egrep '(world$)' newfile

image

OUTPUT
egrep '(World$)' newfile

image

OUTPUT
egrep '((W|w)orld$)' newfile

image

OUTPUT
egrep '[1-9]' newfile

image

OUTPUT
egrep 'Linux.*world' newfile

OUTPUT
egrep 'Linux.*World' newfile

OUTPUT
egrep l{2} newfile

image

OUTPUT
egrep 's{1,2}' newfile

image

OUTPUT
cat > file23

1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
image

sed -n -e '3p' file23

image

OUTPUT
sed -n -e '$p' file23

image

OUTPUT
sed -e 's/Ram/Sita/' file23

image

OUTPUT
sed -e '2s/Ram/Sita/' file23

image

OUTPUT
sed '/tom/s/5000/6000/' file23

image

OUTPUT
sed -n -e '1,5p' file23

image

OUTPUT
sed -n -e '2,/Joe/p' file23

image

OUTPUT
sed -n -e '/tom/,/Joe/p' file23

image

OUTPUT
seq 10

image

OUTPUT
seq 10 | sed -n '4,6p'

image

OUTPUT
seq 10 | sed -n '2,~4p'

image

OUTPUT
seq 3 | sed '2a hello'

image

OUTPUT
seq 2 | sed '2i hello'

image

OUTPUT
seq 10 | sed '2,9c hello'

image

OUTPUT
sed -n '2,4{s/^/$/;p}' file23

image

OUTPUT
sed -n '2,4{s/$/*/;p}' file23

image

Sorting File content
cat > file21

1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
sort file21

image

OUTPUT
cat > file22

1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
image

uniq file22

image

OUTPUT
Using tr command
cat file23 | tr [:lower:] [:upper:]

image

OUTPUT
cat < urllist.txt

www. yahoo. com
www. google. com
www. mrcet.... com
^d
image

cat > urllist.txt

www. yahoo. com
www. google. com
www. mrcet.... com
image

cat urllist.txt | tr -d ' '

image

OUTPUT
cat urllist.txt | tr -d ' ' | tr -s '.'

image

OUTPUT
Backup commands
tar -cvf backup.tar *

image

OUTPUT
mkdir backupdir

mv backup.tar backupdir

image

tar -tvf backup.tar

image

OUTPUT
tar -xvf backup.tar

image

OUTPUT
gzip backup.tar

ls .gz

image

OUTPUT
gunzip backup.tar.gz

image

OUTPUT
Shell Script
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
image

chmod 755 my-script.sh ./my-script.sh

image

OUTPUT
cat << stop > herecheck.txt

hello in this world
i cant stop
for this non stop movement
stop
image

cat herecheck.txt

image

OUTPUT
cat < scriptest.sh

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
image

cat scriptest.sh

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
image

chmod 777 scriptest.sh

./scriptest.sh 1 2 3

image

OUTPUT
ls file1

image

OUTPUT
echo $?

image

OUTPUT
./one bash: ./one: Permission denied

echo $?

image

OUTPUT
abcd

echo $?

image

OUTPUT
mis-using string comparisons
cat < strcomp.sh

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
cat strcomp.sh

\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
image

OUTPUT
chmod 755 strcomp.sh

./strcomp.sh

image

OUTPUT
check file ownership
cat < psswdperm.sh

\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
cat psswdperm.sh

/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
image

./psswdperm.sh

image

OUTPUT
check if with file location
cat>ifnested.sh

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
cat ifnested.sh

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
image

./ifnested.sh

image

OUTPUT
using numeric test comparisons
cat > iftest.sh

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
cat iftest.sh

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
image

$ chmod 755 iftest.sh

$ ./iftest.sh

image

OUTPUT
check if a file
cat > ifnested.sh

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
cat ifnested.sh

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
image

$ chmod 755 ifnested.sh

$ ./ifnested.sh

image

OUTPUT
looking for a possible value using elif
cat elifcheck.sh

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
image

$ chmod 755 elifcheck.sh

$ ./elifcheck.sh

image

OUTPUT
testing compound comparisons
cat> ifcompound.sh

\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
$ chmod 755 ifcompound.sh

$ ./ifcompound.sh

image

OUTPUT
using the case command
cat >casecheck.sh

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
$ chmod 755 casecheck.sh

$ ./casecheck.sh

image

cat > whiletest

#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
$ chmod 755 whiletest.sh

$ ./whiletest.sh

image

cat untiltest.sh

\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
$ chmod 755 untiltest.sh

$ ./untiltest.sh

image

cat forin1.sh

\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
image

$ chmod 755 forin1.sh

$ ./forin1.sh

image

cat forin2.sh

\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
$ chmod 755 forin2.sh

$ ./forin2.sh

image

cat forin3.sh

\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
$ chmod 755 forin3.sh

$ ./forin3.sh

image

OUTPUT
cat forinfile.sh

#!/bin/bash
# reading values from a file
file="cities"
for state in "cat $file"
do
echo "Visit beautiful $state“
done
$ chmod 777 forinfile.sh

$ cat cities

Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

image

image

OUTPUT
cat forctype.sh

#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
$ chmod 755 forctype.sh $ ./forctype.sh

image

OUTPUT
cat forctype1.sh

#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
$ chmod 755 forctype.sh $ ./forctype1.sh

image

OUTPUT
cat fornested1.sh

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
$ chmod 755 fornested1.sh

$ ./fornested1.sh

image

OUTPUT
cat forbreak.sh

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
OUTPUT
$ chmod 755 forbreak.sh

$ ./forbreak.sh

image

cat forcontinue.sh

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
$ chmod 755 forcontinue.sh

$ ./forcontinue.sh

image

OUTPUT
cat exread.sh

#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
$ chmod 755 exread.sh

$ ./exread.sh

image

OUTPUT
cat exread1.sh

#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
$ chmod 755 exread1.sh

$ ./exread1.sh

image

OUTPUT
cat funcex.sh

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
OUTPUT
./funcex.sh

./funcex.sh 1 2

image

cat argshift.sh

#!/bin/bash
 while (( "$#" )); do
  echo $1
  shift
done
$ chmod 777 argshift.sh

OUTPUT
$ ./argshift.sh 1 2 3

image

cat argshift1.sh

args=("$@")
ELEMENTS=${#args[@]}
for (( i=0;i<$ELEMENTS;i++)); do
    echo ${args[${i}]}
done
$ chmod 777 argshift.sh

OUTPUT
$ ./argshift.sh 1 2 3

image

cat argshift.sh

#!/bin/bash
set -x
while (( "$#" )); do
  echo $1
  shift
done
set +x
OUTPUT
./argshift.sh 1 2 3

image

cat > nc.awk

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
image

cat>data.dat

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
image

awk -f nc.awk data.dat

image

OUTPUT
cat > palindrome.sh

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
OUTPUT
$ chmod 755 palindrome.sh

$ ./palindrome.sh

image

RESULT:
The Commands are executed successfully.
