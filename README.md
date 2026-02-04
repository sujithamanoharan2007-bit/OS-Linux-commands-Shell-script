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
<img width="641" height="183" alt="image" src="https://github.com/user-attachments/assets/c192f61e-66f2-45e0-a724-9b4a634a49f1" />



cat < file2
## OUTPUT
<img width="687" height="281" alt="image" src="https://github.com/user-attachments/assets/734412b3-b7f7-4db3-84f8-fbad5a20a1d2" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="782" height="90" alt="image" src="https://github.com/user-attachments/assets/c3be5b97-7df5-4f5c-861f-e7dfce3d60f2" />

comm file1 file2
 ## OUTPUT
<img width="817" height="427" alt="image" src="https://github.com/user-attachments/assets/8416cebc-8079-4bc1-8edd-4924344f504f" />

 
diff file1 file2
## OUTPUT
<img width="867" height="535" alt="image" src="https://github.com/user-attachments/assets/dbdebaf1-4f47-4bb1-a51e-836db6cdebfe" />


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
<img width="697" height="158" alt="image" src="https://github.com/user-attachments/assets/f797ef11-fcb4-4638-b28d-ec2c1d05c7d9" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="793" height="207" alt="image" src="https://github.com/user-attachments/assets/43687b7a-ec03-4f89-871d-5f0aaaa7fb67" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="800" height="207" alt="image" src="https://github.com/user-attachments/assets/4d0845b6-0434-419e-91f8-7280002a76a9" />


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
<img width="792" height="107" alt="image" src="https://github.com/user-attachments/assets/b63f3e56-25a0-48cf-b1bc-9fa102b17230" />



grep hello newfile 
## OUTPUT
<img width="793" height="101" alt="image" src="https://github.com/user-attachments/assets/9734ca6f-387c-4460-8ce7-83217c3c3850" />




grep -v hello newfile 
## OUTPUT
<img width="806" height="118" alt="image" src="https://github.com/user-attachments/assets/db645c48-4c9b-49e7-8c89-517bba0a96e5" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="1020" height="152" alt="image" src="https://github.com/user-attachments/assets/7fd48a9d-22eb-407e-88f6-53727dd6464c" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="1033" height="101" alt="image" src="https://github.com/user-attachments/assets/3bdd771f-5d3d-4aff-8a79-8c905cd01325" />




grep -R ubuntu /etc
## OUTPUT
<img width="1183" height="370" alt="image" src="https://github.com/user-attachments/assets/823127ff-0c44-4cab-b7fb-78d59a3c8de7" />



grep -w -n world newfile   
## OUTPUT
<img width="1146" height="148" alt="image" src="https://github.com/user-attachments/assets/c76d2eda-dac6-4c12-af11-36cb3ab89084" />


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
<img width="1135" height="150" alt="image" src="https://github.com/user-attachments/assets/b8a5edf8-3122-4285-8d9b-c72c7a642ed0" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="1057" height="137" alt="image" src="https://github.com/user-attachments/assets/db608af9-5e40-40a7-bd89-7d7e2154c5f2" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="1138" height="155" alt="image" src="https://github.com/user-attachments/assets/e071ad2c-e846-4d12-ac46-a553b28340cf" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="1037" height="106" alt="image" src="https://github.com/user-attachments/assets/5524f339-9280-4114-978f-371819a11877" />



egrep '(world$)' newfile 
## OUTPUT
<img width="1080" height="91" alt="image" src="https://github.com/user-attachments/assets/66715ce0-a921-4fe4-8529-809da43ac824" />



egrep '(World$)' newfile 
## OUTPUT
<img width="1237" height="108" alt="image" src="https://github.com/user-attachments/assets/add55c03-fec2-4474-b742-b34e0d86e5b7" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="1035" height="152" alt="image" src="https://github.com/user-attachments/assets/697f674e-a37a-453b-bba9-194f28b2b3b5" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="1168" height="101" alt="image" src="https://github.com/user-attachments/assets/65e757da-cff3-4288-81ce-c9320903a08c" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="1052" height="110" alt="image" src="https://github.com/user-attachments/assets/c5d06db2-8909-4b12-bbb7-f7dc1436dcab" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="1006" height="103" alt="image" src="https://github.com/user-attachments/assets/9c5dc998-1bd7-4dba-a1ce-9d250df8f7c9" />


egrep l{2} newfile
## OUTPUT
<img width="903" height="156" alt="image" src="https://github.com/user-attachments/assets/3940548e-dc79-47a7-95bf-8392f3816519" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="1190" height="195" alt="image" src="https://github.com/user-attachments/assets/19a2d6b0-25fa-4cc5-b871-4db92be5f448" />


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
<img width="777" height="92" alt="image" src="https://github.com/user-attachments/assets/853e0fad-be03-4a97-ab65-3716b0ca3e68" />



sed -n -e '$p' file23
## OUTPUT
<img width="835" height="92" alt="image" src="https://github.com/user-attachments/assets/b3c644d2-e814-4aaf-b4b5-adf1205cef6b" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="908" height="411" alt="image" src="https://github.com/user-attachments/assets/3b5b4daf-f8dd-431a-a89f-20d530c41252" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="897" height="422" alt="image" src="https://github.com/user-attachments/assets/5988c398-8cac-4cf8-a27c-f1b7e3813f9e" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="1007" height="437" alt="image" src="https://github.com/user-attachments/assets/4e18184c-0074-42cf-8847-5919340ae707" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="967" height="283" alt="image" src="https://github.com/user-attachments/assets/172248ea-3a75-478c-bfea-4d88ac594d8d" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="921" height="196" alt="image" src="https://github.com/user-attachments/assets/32008154-fbb0-46e8-bb0b-089161a247e6" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="1002" height="135" alt="image" src="https://github.com/user-attachments/assets/7be699cb-1933-4dd4-923c-43b62024c787" />



seq 10 
## OUTPUT
<img width="1017" height="510" alt="image" src="https://github.com/user-attachments/assets/e3fac3ae-5c07-4f73-ab2c-a729a03180e2" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="1025" height="197" alt="image" src="https://github.com/user-attachments/assets/372dcb07-a005-473f-a1ef-982584a72a3c" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="815" height="175" alt="image" src="https://github.com/user-attachments/assets/8930c08d-f57f-4cbd-8aa8-859b05918fd9" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="945" height="180" alt="image" src="https://github.com/user-attachments/assets/7e0b0463-1475-4ab9-9473-051078dc726a" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="921" height="217" alt="image" src="https://github.com/user-attachments/assets/b22dc9c4-dc25-4e39-8b65-631d776d9696" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="913" height="180" alt="image" src="https://github.com/user-attachments/assets/35ea63c7-120f-48ec-b3bc-3c9f03d8f3fb" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="997" height="166" alt="image" src="https://github.com/user-attachments/assets/e4e4ee1f-4f8b-4a68-a016-fe4829a4c3e8" />


sed -n '2,4{s/$/*/;p}' file23

<img width="965" height="181" alt="image" src="https://github.com/user-attachments/assets/c26da17e-0019-404b-a9af-1d8eb541104e" />

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
<img width="592" height="291" alt="image" src="https://github.com/user-attachments/assets/7517449c-9771-430a-9989-ad1a5fff3752" />


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

<img width="618" height="281" alt="image" src="https://github.com/user-attachments/assets/e3e4c68e-f85e-46ad-9a49-c402a98069da" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="1125" height="402" alt="image" src="https://github.com/user-attachments/assets/b5bdb8dc-7d6a-4ddc-a78c-173b8e7f1188" />

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

<img width="1022" height="175" alt="image" src="https://github.com/user-attachments/assets/8429e849-2f6b-4fbe-bdc8-7ee55fb29e5a" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="1145" height="185" alt="image" src="https://github.com/user-attachments/assets/79e6ef81-9aed-4b37-aad2-f254fb807740" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="342" height="127" alt="image" src="https://github.com/user-attachments/assets/d8ed69fc-859d-4751-8c4a-859df05ea3f6" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="342" height="127" alt="image" src="https://github.com/user-attachments/assets/a66e4178-86d8-4703-8dcb-4a185f08a722" />

tar -xvf backup.tar
## OUTPUT
<img width="1168" height="233" alt="image" src="https://github.com/user-attachments/assets/2c14ed64-bed5-46f8-bffe-e58e7e417487" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="1155" height="230" alt="image" src="https://github.com/user-attachments/assets/a301ba27-d219-4441-a744-d6fe3ecce06b" />

gunzip backup.tar.gz
## OUTPUT
 <img width="1191" height="346" alt="image" src="https://github.com/user-attachments/assets/0e469229-75bb-4dd8-abce-25ea7af57804" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="1178" height="481" alt="image" src="https://github.com/user-attachments/assets/dbfd2320-ab28-412b-9262-0242b983f218" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="675" height="183" alt="image" src="https://github.com/user-attachments/assets/b727db62-4b2d-48cf-bb6d-b3a69d36b3bd" />


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
<img width="867" height="678" alt="image" src="https://github.com/user-attachments/assets/ce171dc9-9da2-4332-90e2-d515327ce6b5" />

 
ls file1
## OUTPUT
<img width="513" height="91" alt="image" src="https://github.com/user-attachments/assets/3288e1bc-8178-4257-8320-475940c9aeb1" />

echo $?
## OUTPUT 
<img width="516" height="100" alt="image" src="https://github.com/user-attachments/assets/273ed9b6-c5f3-43e9-95a2-69164c5c6f40" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="477" height="107" alt="image" src="https://github.com/user-attachments/assets/bb32e1e7-e25c-42eb-a51c-dedc40b0cc97" />

 
abcd
 
echo $?
 ## OUTPUT
 <img width="977" height="447" alt="image" src="https://github.com/user-attachments/assets/1ac4ac01-6b4a-4043-9ddf-8a5f01338627" />



 
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

<img width="982" height="510" alt="image" src="https://github.com/user-attachments/assets/cd9e001e-718d-4633-abdb-bba15c6464bc" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="1188" height="483" alt="image" src="https://github.com/user-attachments/assets/e032bd9d-9dbd-40d0-ac5e-c97ae528e51d" />


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
<img width="1187" height="348" alt="image" src="https://github.com/user-attachments/assets/3bdeaa00-e5d7-4730-ba23-b24e7e48a51b" />


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

<img width="1021" height="813" alt="image" src="https://github.com/user-attachments/assets/5439d002-1e56-429b-859a-393bc11ece1d" />


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
<img width="1093" height="812" alt="image" src="https://github.com/user-attachments/assets/53fc5bde-b31c-4d33-9793-772f30d0ca87" />


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

<img width="1166" height="805" alt="image" src="https://github.com/user-attachments/assets/ad74ee4f-94d1-412b-9caf-197852207b47" />


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
<img width="1153" height="812" alt="image" src="https://github.com/user-attachments/assets/268a5cbf-0389-46d5-afce-9b55cd322ff7" />


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
<img width="1036" height="522" alt="image" src="https://github.com/user-attachments/assets/573569fa-ae42-4b9d-9858-fcc98e4f30be" />

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
<img width="887" height="312" alt="image" src="https://github.com/user-attachments/assets/5418ba75-257f-4db7-b84a-c7e1e9d586fe" />


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
<img width="852" height="421" alt="image" src="https://github.com/user-attachments/assets/8aa356af-1b90-42e3-91b5-38ed91c1af38" />


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
<img width="796" height="422" alt="image" src="https://github.com/user-attachments/assets/e0e05e06-9c38-43ba-8c01-087c5d75be2a" />


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
<img width="1186" height="447" alt="image" src="https://github.com/user-attachments/assets/1deff3d0-ca3f-4e72-bf38-66583d089944" />

 
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
<img width="1193" height="441" alt="image" src="https://github.com/user-attachments/assets/acec8a3f-0887-46d5-ab34-100f26db2dd2" />


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
<img width="1187" height="443" alt="image" src="https://github.com/user-attachments/assets/5089a3cc-7f32-4b76-8d61-529fb8645cca" />

 
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
<img width="913" height="457" alt="image" src="https://github.com/user-attachments/assets/ef69207b-6da9-49ed-984f-d595a9e4d4c0" />



 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="938" height="278" alt="image" src="https://github.com/user-attachments/assets/6beebf08-94cb-459d-89f5-3ac437117b9f" />


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
 
 ./funcex.sh  <img width="522" height="27" alt="image" src="https://github.com/user-attachments/assets/70ff6e89-3303-4193-8b72-c34bfb484c30" />


 
 ./funcex.sh 1 2  <img width="411" height="35" alt="image" src="https://github.com/user-attachments/assets/f31a3063-8275-407d-ad95-1427845693d5" />


 
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
 <img width="211" height="85" alt="image" src="https://github.com/user-attachments/assets/dfcc965a-b412-4f0e-b1e7-a11591c5ac25" />

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
 <img width="542" height="102" alt="image" src="https://github.com/user-attachments/assets/0fc4e3c0-da4b-45cf-bbc1-e88cbdd298b5" />

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
 <img width="782" height="568" alt="image" src="https://github.com/user-attachments/assets/12686b37-68bd-42a8-a4a3-f4ec4c0a41f6" />

 
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
 <img width="460" height="368" alt="image" src="https://github.com/user-attachments/assets/134c8b77-38e7-4c9d-bc6a-3fe331108bf5" />

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
<img width="490" height="111" alt="image" src="https://github.com/user-attachments/assets/6f9d649d-1bbe-4b20-ae72-4fa2f6d19390" />



# RESULT:
The Commands are executed successfully.
