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

![image](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/d1bfaa08-fe19-4092-8b23-31dee0c0a75b)

cat > file2

```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```

![image](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/6f48ac2f-b4c6-43cd-a29a-f9489756645e)

### Display the content of the files

cat < file1

## OUTPUT

![image](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/679b6fb4-09d2-4e10-8537-9f02d7b33602)

cat < file2

## OUTPUT

![image](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/463202da-ff83-4c33-a41f-236040638471)

# Comparing Files

cmp file1 file2

## OUTPUT

![image](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/d62068e7-ef91-4f5f-b3db-aebe35fed595)
comm file1 file2

## OUTPUT

![image](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/83229d38-85f4-4291-a9b3-702f5ebc8917)
diff file1 file2

## OUTPUT

![image](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/560e4a8e-9a84-4d69-89c3-0e0e75c7af44)

#Filters

### Create the following files file11, file22 as follows:

cat > file11

```
Hello world
This is my world
^d
```

![image](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/41c74ac4-567c-4728-9dd3-31be6bf23fb2)
cat > file22

```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```

![image](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/8f8553a3-aab8-4850-9b35-184fe7555063)

cut -c1-3 file11

## OUTPUT

![image](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/06616947-7c8a-4f48-9f5c-11c44922efe7)

cut -d "|" -f 1 file22

## OUTPUT

![image](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/8a394d8d-f6dc-48e0-a732-5fee7d8d6f4d)

cut -d "|" -f 2 file22

## OUTPUT

![image](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/080d5338-3023-40c5-ae9a-51481d380c2f)

cat < newfile

```
Hello world
hello world
^d
```
![s13](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/066a3e80-95b7-4bd3-9fdf-3797ea0d65e7)


cat > newfile

```
Hello world
hello world
```

<br>

![s14](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/6a4a771a-8d50-4c17-b684-a216d4c65cd0)


<br>
grep Hello newfile

grep hello newfile

## OUTPUT
![s15](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/9a8874e5-90be-4b80-81e8-e1beb653a6fd)


## OUTPUT

grep -v hello newfile

![s16](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/2fe32a57-58b5-4659-a3ab-dced1f9a7090)

## OUTPUT

cat newfile | grep -i "hello"
![s17](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/2bdfdc07-95f0-437f-b599-4421377d6efc)


## OUTPUT

cat newfile | grep -i -c "hello"

![s18](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/e5da9b4a-f613-479f-92c8-7b4d02c88773)

## OUTPUT

grep -R ubuntu /etc
![s19](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/76e1c4f4-73cf-43d5-9cd4-77e031a9d8f5)


## OUTPUT

grep -w -n world newfile
![s20](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/950eac77-02b0-47b7-b7e2-4ee02d0b4b16)


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
![s21](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/03363e61-7734-4512-a706-56d2100639cc)


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
![s22](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/e77ed5de-2550-4217-a526-30beee468e0d)


egrep -w 'Hello|hello' newfile

![s23](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/2a1f548d-46c1-4b32-89f7-9f7cede62d8f)

## OUTPUT

egrep -w '(H|h)ello' newfile
![s24](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/b76f3946-be82-453c-a6bf-634dacc57efd)


## OUTPUT

egrep -w '(H|h)ell[a-z]' newfile
![s25](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/91560f92-4631-4bac-af82-0d9f772ac820)


## OUTPUT

egrep '(^hello)' newfile
![s26](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/b53b1880-c6f1-4566-9711-2cd5cb33abed)


## OUTPUT

egrep '(world$)' newfile
![s27](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/46d45ba4-340f-46ad-9f73-9ea76c7bffea)


## OUTPUT

egrep '(World$)' newfile
![s28](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/2dad2bf4-dc14-44a6-a7f5-68bd784b9455)


## OUTPUT

egrep '((W|w)orld$)' newfile
![s29](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/46ba0202-5976-45c6-aa82-5ac54df290b3)


## OUTPUT

egrep '[1-9]' newfile
![s30](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/b89d0b9d-4f99-4a8e-9ef3-7b46a6d232a8)


## OUTPUT

egrep 'Linux.\*world' newfile

## OUTPUT

egrep 'Linux.\*World' newfile

## OUTPUT

egrep l{2} newfile
![s31](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/6e37203c-47f3-43a0-bb7e-313e87a2d910)


## OUTPUT

egrep 's{1,2}' newfile

![s32](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/59a2f0a4-15e0-4862-bafd-1c492bdfa5d9)
)

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
![s33](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/b42e05dc-53b5-4814-aaa0-e19838dd5ff3)


sed -n -e '3p' file23
![s34](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/ee2c2c68-4869-43fa-bb78-3aa255665b24)


## OUTPUT

sed -n -e '$p' file23

![s35](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/66c427e4-9c69-4361-ab10-72e3bcbcdbc6)

## OUTPUT

sed -e 's/Ram/Sita/' file23
![s36](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/581bd435-7e50-4795-b4c1-cb821c4f855c)


## OUTPUT

sed -e '2s/Ram/Sita/' file23
![s37](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/9cac1774-3a80-4bc4-802b-da467ac52278)


## OUTPUT

sed '/tom/s/5000/6000/' file23
![s38](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/6407d217-36eb-4812-b5fb-0206f894161c)


## OUTPUT

sed -n -e '1,5p' file23
![s39](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/a7976645-7f32-41d6-a2a4-de10b8e5d714)


## OUTPUT

sed -n -e '2,/Joe/p' file23

![s40](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/14684372-b6e1-4a41-b0f9-ac24046442b4)


## OUTPUT

sed -n -e '/tom/,/Joe/p' file23
![s41](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/75055124-2a90-44a1-9fb9-cb4361c1d056)


## OUTPUT

seq 10
![s42](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/c252d6b7-b82e-4d65-8a5f-a1b93fd53398)


## OUTPUT

seq 10 | sed -n '4,6p'

![image](./images/s43.png)

## OUTPUT

seq 10 | sed -n '2,~4p'
![s43](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/791b15e1-0e01-4c9b-a878-f04a12cc68bc)


## OUTPUT

seq 3 | sed '2a hello'
![s45](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/6bad967c-7346-441f-8f56-b6551c1e2f8b)


## OUTPUT

seq 2 | sed '2i hello'
![s46](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/fe27b991-5690-44c0-b4dc-25ff34c1c878)


## OUTPUT

seq 10 | sed '2,9c hello'
![s47](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/8347bd1f-a553-429f-b663-990070cde0b9)


## OUTPUT

sed -n '2,4{s/^/$/;p}' file23
![s48](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/f959643b-494a-4f38-a415-9f5f8d6978ad)


## OUTPUT

sed -n '2,4{s/$/\*/;p}' file23
![s49](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/88ee8a96-e164-4878-b665-60f66793e1c4)


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

![s50](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/6d12a2cb-c138-42e4-9a6f-a07e2f6a5ded)


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
![s51](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/c2fec405-9b98-4e5d-a114-269892b859f0)

uniq file22
![s52](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/e4f8c5b6-f25a-4a9c-b660-0bfd7bed7b3c)


## OUTPUT

# Using tr command

cat file23 | tr [:lower:] [:upper:]
![s53](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/e07b932d-209e-405a-bf03-0f32edcecab8)


## OUTPUT

cat < urllist.txt

```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
```
![s54](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/133d4864-e7c7-4bf7-a141-cc8fbd805709)


cat > urllist.txt

```
www. yahoo. com
www. google. com
www. mrcet.... com
```
![s55](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/71a56968-800f-463c-9799-9512a2f01504)


cat urllist.txt | tr -d ' '
![s56](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/668e6737-a302-4271-a827-0bb4bf53b973)


## OUTPUT

cat urllist.txt | tr -d ' ' | tr -s '.'
![s57](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/15ef2a8b-dce2-4a50-ac8e-46630a94b713)


## OUTPUT

# Backup commands

tar -cvf backup.tar \*
![s58](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/57874a59-a451-441a-a94b-72e84f9057a4)


## OUTPUT

mkdir backupdir

mv backup.tar backupdir
![s59](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/da330861-a256-4817-b254-49d0e8583dd0)


tar -tvf backup.tar
![s60](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/f8951454-beec-406a-a60e-06cc579604ce)


## OUTPUT

tar -xvf backup.tar
![s61](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/4d477976-0b07-4d9a-a733-8c2df2829ff7)


## OUTPUT

gzip backup.tar

ls .gz
![image](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/857d7982-00e5-4c2a-b9dd-2de602c1536d)

## OUTPUT

gunzip backup.tar.gz

![image](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/37e7722a-af8b-4fac-9090-4a717a19263f)

## OUTPUT

# Shell Script

```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```

![image](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/97b7a17e-b989-4500-a84c-d43deea03ec0)

chmod 755 my-script.sh
./my-script.sh

![image](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/0fc185dd-d3be-4a80-8a20-605b7cbf426a)

## OUTPUT

cat << stop > herecheck.txt

```
hello in this world
i cant stop
for this non stop movement
stop
```
![s66](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/6798fbf7-79be-44b0-a85e-3ffb6386ad8d)


cat herecheck.txt
![s67](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/7fef5535-e5e5-43c1-aca7-e55bb3c24de9)


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
![s68](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/bed2223e-4039-437f-8022-c79fc9450dc9)



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
![s69](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/4b697cc1-bd43-4e44-9916-d6d6e7a8aa2e)


chmod 777 scriptest.sh

./scriptest.sh 1 2 3
![s70](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/fc64ec20-5d6c-42d9-aeac-a992c208e516)


## OUTPUT

ls file1
![s71](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/c558e2ec-c5d2-4663-8230-8151dd06a49b)


## OUTPUT

echo $?
![s72](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/f73a1a21-98b5-4886-9954-3d76b18a1d03)


## OUTPUT

./one
bash: ./one: Permission denied

echo $?
![s73](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/9f7a2aae-5224-4994-813c-205dc8ad6322)


## OUTPUT

abcd

echo $?
![s74](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/9596f3f7-ae59-4309-9c46-90f01dfe1a9f)


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
![s76](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/33da8183-c876-42ab-b0d0-5a6ef0c72fad)


## OUTPUT

chmod 755 strcomp.sh

./strcomp.sh
![s77](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/09ef6c4f-1aa1-4f49-804a-3cc43aa6ece0)


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
![s78](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/96143ae1-89d9-4ef1-83f9-968f96df60b7)


./psswdperm.sh
![s79](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/527fe054-e443-402b-8380-ffc9a0dcf36a)


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
![s81](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/d54c6b6b-ceb2-43f2-acf2-79be917cc115)



./ifnested.sh
![s80](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/474d1a23-d586-4808-9a67-001f6d78e252)


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
![s82](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/82668e74-1132-451a-8a36-32e4b0f2c688)


$ chmod 755 iftest.sh

$ ./iftest.sh

![s83](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/ebc6f63c-4f52-456a-90dd-faccc9615718)

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
![s84](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/4e1da425-fc48-447c-92f7-0f24fa98c76e)

$ chmod 755 ifnested.sh

$ ./ifnested.sh

![s85](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/b156efba-54d4-4aa6-8d13-346a5b34aba4)

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
![s86](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/fc9df084-2db1-4094-84af-4f34ba32eba7)


$ chmod 755 elifcheck.sh

$ ./elifcheck.sh
![s87](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/4ba8f3d9-32c0-4658-95eb-5bceb5771ed8)


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
![s88](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/67a3608e-c74c-4c46-8c2f-119e9a085fad)


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
![s89](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/80554d8c-d695-489c-8f2a-59d0c05159c6)


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
![s90](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/a1ca2d49-edca-4461-9f23-37a9becd2d64)


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
![s91](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/5187bbf5-2c8c-4427-9d88-76bbf12b8313)


cat forin1.sh

```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
![s92](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/623435f8-fdf2-4df3-a68c-fde3dc6a541b)


$ chmod 755 forin1.sh

$ ./forin1.sh
![s93](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/9661b3b2-3f46-450d-a8b3-b4275043c723)


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
![s94](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/f831e275-ef93-4bf4-9558-54d909c0ed92)


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
![s95](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/4ca8f75d-bf6a-4fa5-bc27-8bb34a90d688)



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
Khammam
<br>
![Screenshot 2024-03-08 114549](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/74770248-0e49-46ae-a44c-ebf12c5cc27c)


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
![s98](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/7887f468-52b2-402f-9c03-04066b841fc4)


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
![s99](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/2d6eb440-0b22-4f49-a854-1d94ef4dd77a)


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
![s100](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/b244e1df-a0e2-4e30-b5de-5722dd124373)


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
![s101](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/97e18019-46b5-4018-965d-e89ed48f6a1c)


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
![s102](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/a544cfc0-496e-4773-b21d-7da806471267)


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
![s103](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/c553768b-dfbf-4bad-8cc7-37874ba860ef)


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
![s104](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/cd6131ef-a7e8-492a-9659-7f74d1132b55)


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
![s105](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/6901226d-88c0-4f48-af4f-dcb87364be9f)


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
![s106](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/aa053f0c-670c-4837-859f-771ccfc31dcd)

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
![s107](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/12285fa6-26e7-4b6d-b64b-ba292200456f)


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
![s108](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/c7be0253-a039-46c7-b10a-76ae199141e5)


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
![s109](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/e44165c1-43b1-4065-9409-2d66e20fc38a)


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
![s110](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/aaed686c-6e65-44f4-ba8f-068558bba2e8)


awk -f nc.awk data.dat

![s111](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/ca2d32f4-7cc3-49d4-bfa5-d976f219a692)



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

![s112](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/4eab42a8-e022-419a-8e59-f260a7b90c55)


# RESULT:

The Commands are executed successfully.
