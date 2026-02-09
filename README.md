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

<img width="559" height="107" alt="Screenshot 2026-02-02 094810" src="https://github.com/user-attachments/assets/e3026033-7361-41c7-9c36-b9221d6e24a2" />

cat < file2
## OUTPUT

<img width="594" height="143" alt="Screenshot 2026-02-02 094802" src="https://github.com/user-attachments/assets/a712bbfe-aa4b-4a41-ae17-231968a1e0bb" />

# Comparing Files
cmp file1 file2
## OUTPUT

<img width="675" height="55" alt="image" src="https://github.com/user-attachments/assets/ff2dc779-5e1c-49b8-a2f9-cc4b5ac0d1ad" />

comm file1 file2
 ## OUTPUT

 <img width="778" height="252" alt="image" src="https://github.com/user-attachments/assets/b276ba46-bcaf-4934-9e93-9ac20c64d5cb" />

diff file1 file2
## OUTPUT
 
<img width="690" height="232" alt="Screenshot 2026-02-02 094818" src="https://github.com/user-attachments/assets/d2af7d4c-e56f-4998-adca-1ffdb6d611eb" />

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

<img width="685" height="70" alt="Screenshot 2026-02-02 095123" src="https://github.com/user-attachments/assets/2bbbbe2f-fc8f-4a5f-b755-8241d0435d2d" />

cut -d "|" -f 1 file22
## OUTPUT

<img width="712" height="88" alt="Screenshot 2026-02-02 095129" src="https://github.com/user-attachments/assets/53d8a5cc-8fc9-4694-9991-6bf5232b0465" />

cut -d "|" -f 2 file22
## OUTPUT

<img width="674" height="88" alt="Screenshot 2026-02-02 095136" src="https://github.com/user-attachments/assets/6abcc582-ffa2-4890-a4be-96bd31c65d9a" />

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

<img width="616" height="47" alt="image" src="https://github.com/user-attachments/assets/4cb119a1-1b19-4f02-bcff-b5a9def70a6d" />

grep hello newfile 
## OUTPUT

<img width="517" height="65" alt="image" src="https://github.com/user-attachments/assets/4d14f6e1-3989-4c65-a83f-c9585c7de5b1" />

grep -v hello newfile 
## OUTPUT

<img width="628" height="47" alt="image" src="https://github.com/user-attachments/assets/58b1a259-3038-415a-b2d0-a9f10e01a64b" />

cat newfile | grep -i "hello"
## OUTPUT

<img width="786" height="75" alt="Screenshot 2026-02-06 092031" src="https://github.com/user-attachments/assets/720637ea-00cc-4c3d-9ebd-1cd9c80ee5c2" />

cat newfile | grep -i -c "hello"
## OUTPUT

<img width="812" height="50" alt="image" src="https://github.com/user-attachments/assets/a965af0c-3f71-48ab-8f24-616b0bfd27a0" />

grep -R ubuntu /etc
## OUTPUT

<img width="1340" height="730" alt="image" src="https://github.com/user-attachments/assets/b6107189-2bb5-4ed2-acdf-d851271847eb" />

grep -w -n world newfile   
## OUTPUT

<img width="837" height="86" alt="image" src="https://github.com/user-attachments/assets/23ab6a88-4640-4486-a78c-564ec168e80a" />

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

<img width="917" height="85" alt="image" src="https://github.com/user-attachments/assets/e56ffc10-60db-4043-930c-526186581e17" />

egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="933" height="77" alt="image" src="https://github.com/user-attachments/assets/f9bd1c2a-4094-416d-b548-ba1e4265122d" />

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="1046" height="92" alt="image" src="https://github.com/user-attachments/assets/d69efa96-2353-44a6-87ae-c61bb2b5524f" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="697" height="96" alt="image" src="https://github.com/user-attachments/assets/dbe99154-1d0d-4ce5-be5b-faaa978f9846" />

egrep '(world$)' newfile 
## OUTPUT

<img width="918" height="92" alt="image" src="https://github.com/user-attachments/assets/ea813005-c788-4111-9539-219c03ed293c" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="912" height="118" alt="image" src="https://github.com/user-attachments/assets/47e7490f-6e7d-4872-9b45-85521f358915" />


egrep '[1-9]' newfile 
## OUTPUT


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="950" height="57" alt="image" src="https://github.com/user-attachments/assets/c1b99279-19fb-4f97-bbfa-a97ec588b663" />

egrep l{2} newfile
## OUTPUT

<img width="721" height="70" alt="image" src="https://github.com/user-attachments/assets/e31743a2-5703-4f97-9956-2e8434170e6c" />

egrep 's{1,2}' newfile
## OUTPUT 

<img width="777" height="100" alt="image" src="https://github.com/user-attachments/assets/cb160802-1536-479a-8d00-dd66dfd1958f" />

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

<img width="768" height="47" alt="image" src="https://github.com/user-attachments/assets/26dc088c-7ea1-49b8-a234-cc091df95cba" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="817" height="188" alt="image" src="https://github.com/user-attachments/assets/cbae3ff0-2f9a-4ec7-b510-5bc8b79cd6d3" />

sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="850" height="178" alt="image" src="https://github.com/user-attachments/assets/380e92c5-9a9d-4829-a5d2-388ebe8b14fa" />

sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="890" height="180" alt="image" src="https://github.com/user-attachments/assets/d8c96375-6879-4673-a420-32a4a7d0b35d" />

sed -n -e '1,5p' file23
## OUTPUT

<img width="836" height="140" alt="image" src="https://github.com/user-attachments/assets/6718f887-6320-4a23-8946-0943dc1bc447" />

sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="911" height="98" alt="image" src="https://github.com/user-attachments/assets/1c9b4df8-8667-4eb4-a1b8-ac208ee2627d" />

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="803" height="72" alt="image" src="https://github.com/user-attachments/assets/6cc66e32-5431-4c58-bf20-da45fe8ad85d" />

seq 10 
## OUTPUT

<img width="736" height="256" alt="image" src="https://github.com/user-attachments/assets/88da9f76-f3f4-4df1-8d62-d533a50a624d" />

seq 10 | sed -n '4,6p'
## OUTPUT

<img width="822" height="93" alt="image" src="https://github.com/user-attachments/assets/c3131565-13b8-4124-8228-595d45de433b" />

seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="741" height="83" alt="image" src="https://github.com/user-attachments/assets/f4b06d2e-fde7-4608-b582-e5fe6db208d7" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="707" height="111" alt="image" src="https://github.com/user-attachments/assets/aec4483f-32d1-42ea-8098-d85e3809b906" />

seq 2 | sed '2i hello'
## OUTPUT

<img width="834" height="90" alt="Screenshot 2026-02-09 083629" src="https://github.com/user-attachments/assets/f9f7198d-5353-4e02-b442-28ebe5a3eebb" />

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="862" height="92" alt="Screenshot 2026-02-09 083756" src="https://github.com/user-attachments/assets/6d42c400-67d6-4515-8990-0d52665aea59" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="825" height="93" alt="image" src="https://github.com/user-attachments/assets/95c86b76-1a95-473f-a20a-a3ffa9c44ea4" />


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

<img width="760" height="142" alt="image" src="https://github.com/user-attachments/assets/5eab0d33-2262-42a2-bf2c-574728c3dd9f" />

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

<img width="637" height="140" alt="image" src="https://github.com/user-attachments/assets/c128fcbb-d245-4857-bdf0-2fbafc645931" />

#Using tr command
cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="893" height="182" alt="image" src="https://github.com/user-attachments/assets/5c261abe-27f9-4bcc-aaf1-790cb6ec754d" />

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

<img width="777" height="91" alt="image" src="https://github.com/user-attachments/assets/51bbe9af-4be5-4159-ad5b-661a6de6463c" />

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="848" height="82" alt="image" src="https://github.com/user-attachments/assets/f709dc09-91fe-4ff3-a65d-d4c0eab42835" />

#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="888" height="273" alt="image" src="https://github.com/user-attachments/assets/91bc4b09-3d1d-43b5-aaa4-6085cfc32620" />

tar -xvf backup.tar
## OUTPUT

<img width="813" height="282" alt="image" src="https://github.com/user-attachments/assets/8c53ef3e-5c61-4219-9d22-5b78b5bf2b47" />
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="932" height="232" alt="image" src="https://github.com/user-attachments/assets/846079c1-d605-459e-b292-3d5141b5dc19" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="373" height="83" alt="image" src="https://github.com/user-attachments/assets/9fea9505-f115-4d88-bb7b-f86793696eee" />

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

<img width="915" height="107" alt="image" src="https://github.com/user-attachments/assets/d80df47f-ffd5-40bc-80dc-ef866de14226" />
 
ls file1
## OUTPUT

<img width="452" height="78" alt="image" src="https://github.com/user-attachments/assets/4d92f9c7-a66d-4ea4-a4a6-ae2254746feb" />

echo $?
## OUTPUT 

<img width="578" height="43" alt="image" src="https://github.com/user-attachments/assets/b7ce8fd9-50f4-4341-97f4-e90f8518f9df" />

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

<img width="911" height="117" alt="image" src="https://github.com/user-attachments/assets/7d7d0dc5-2b87-4428-8cdb-b51ea3caf564" />

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

<img width="905" height="210" alt="image" src="https://github.com/user-attachments/assets/22e9bc76-d922-4f0f-880b-43e2650363c3" />

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

<img width="820" height="437" alt="image" src="https://github.com/user-attachments/assets/2ecece82-01f2-4f92-9679-3d03bf7e09b0" />

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

<img width="946" height="105" alt="image" src="https://github.com/user-attachments/assets/7564e2df-a0d7-400a-8c84-95180bf39ff7" />

# check if a file
cat > ifnested.sh 
```cat > ifnested.sh 
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

<img width="908" height="460" alt="image" src="https://github.com/user-attachments/assets/ec03ce9e-8227-427f-8904-efadfed78273" />

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
 ##Output

 <img width="902" height="342" alt="image" src="https://github.com/user-attachments/assets/076eb46c-3ae0-4ca0-9849-1879638501f7" />

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
##Output

<img width="917" height="233" alt="image" src="https://github.com/user-attachments/assets/739a237e-6886-4520-9f25-c4e2fdc8ce85" />
 
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
