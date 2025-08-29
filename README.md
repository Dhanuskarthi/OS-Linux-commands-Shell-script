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

<img width="489" height="114" alt="481376506-975dd680-95aa-472b-ab5a-7324f6881d50" src="https://github.com/user-attachments/assets/12dea21b-fd43-4f5a-91e7-38f8677fa3da" />


cat < file2
## OUTPUT
<img width="557" height="128" alt="481376971-e7dc93ed-e92c-4f42-9e51-de7bc27210d2" src="https://github.com/user-attachments/assets/5f8b0a47-c58c-4436-b7ce-68cc67bbcbf3" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="593" height="41" alt="481378813-f3a13449-4062-410f-95b3-f94590d44632" src="https://github.com/user-attachments/assets/7189e3c3-9ccf-415d-a0db-e2a60dbee34f" />

 
comm file1 file2
 ## OUTPUT

 <img width="593" height="156" alt="481378966-ceea12f3-ff6c-48aa-bf69-b1cc9ba5a6b1" src="https://github.com/user-attachments/assets/2af3f358-3ff0-4cdc-9be7-06ef5b81910a" />

diff file1 file2
## OUTPUT
<img width="593" height="186" alt="481379046-2212a7d4-b97c-46cd-becd-e7bef8ff0a97" src="https://github.com/user-attachments/assets/1434a034-a917-49e4-a5be-99e5c099e594" />


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


<img width="593" height="161" alt="481379216-515c793a-bea7-45c7-8ded-ffdbfce548b3" src="https://github.com/user-attachments/assets/724eb890-029f-4130-a833-cc2d110ea946" />


cut -d "|" -f 1 file22
## OUTPUT
<img width="645" height="161" alt="481379339-fcc2c3ee-ae57-4d95-a14f-52dc310334eb" src="https://github.com/user-attachments/assets/52474974-1ab6-4a3f-a613-5d22c67fb736" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="645" height="106" alt="481379403-50d3ee40-8595-4f53-a474-b719040e5998" src="https://github.com/user-attachments/assets/5402f9d4-8202-4988-a5a2-7f399442953f" />


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

<img width="645" height="45" alt="481379694-83a6393d-f8d7-475c-8baf-8b67e7ab1b20" src="https://github.com/user-attachments/assets/26b7afdd-a677-47f2-98e3-538d22dc7684" />


grep hello newfile 
## OUTPUT

<img width="533" height="43" alt="481394123-4a7c2346-0e00-4e47-9b1a-bf3bdb64772c" src="https://github.com/user-attachments/assets/2f962823-7f74-4199-a9c7-d53e2d1b65c1" />



grep -v hello newfile 
## OUTPUT

<img width="533" height="43" alt="481394134-bd02774e-37f2-4ac0-b8e9-af445daa0196" src="https://github.com/user-attachments/assets/9237116e-59cd-47e2-be02-eafa05d8b085" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="621" height="60" alt="481394141-79d7d1dd-d9ba-464e-a7f9-280c55ff7971" src="https://github.com/user-attachments/assets/638fcdd0-74bf-4107-83fd-9272f0cd9c98" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="623" height="42" alt="481394150-2adf4c1f-7c3a-45ea-8faa-064b1f6377db" src="https://github.com/user-attachments/assets/d2f33dbf-b243-403a-bae0-cbc369e6e3cd" />



grep -R ubuntu /etc
## OUTPUT

<img width="526" height="26" alt="481394154-fff42e6d-c575-472f-8bb6-c5eb2974ec04" src="https://github.com/user-attachments/assets/b28b79e8-498b-4f01-bc98-bcf677e40fe7" />


grep -w -n world newfile   
## OUTPUT

<img width="628" height="61" alt="481394160-42ac3f7f-fc43-4787-b34e-64eb49af622d" src="https://github.com/user-attachments/assets/2fe15808-323f-42fd-b643-74e34ba81d22" />

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
<img width="702" height="56" alt="481380239-187441f5-22a7-46a3-9167-4fe10e329c3f" src="https://github.com/user-attachments/assets/fa6719ef-8b2d-42c9-b853-53da31662bdd" />



egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="702" height="56" alt="481380270-a3388b21-8605-472d-8d4f-2b5280188257" src="https://github.com/user-attachments/assets/da2257df-afd2-4713-9c31-4bcc3d40da01" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="722" height="68" alt="481380316-798a874a-d51a-4171-b161-8a702de7f698" src="https://github.com/user-attachments/assets/9f5f5b08-ff3d-4067-99a2-27d2df6da2d9" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="722" height="59" alt="481380346-f32515b5-eb88-40e9-8701-b750751baab2" src="https://github.com/user-attachments/assets/4568a01b-993f-4789-8683-185e1b4469ac" />


egrep '(world$)' newfile 
## OUTPUT

<img width="722" height="59" alt="481380366-d275b315-3de7-4798-ac14-6155dc373d7c" src="https://github.com/user-attachments/assets/9d420d89-7176-4194-882c-fa4663b79889" />


egrep '(World$)' newfile 
## OUTPUT
<img width="722" height="59" alt="481380386-ddfdb890-8bd7-4a42-88f6-737a9ca99307" src="https://github.com/user-attachments/assets/d1de19ae-a928-4c40-872f-55239be277d0" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="722" height="80" alt="481380407-adbd8354-dcb9-48e6-bb0c-08cb99d196ff" src="https://github.com/user-attachments/assets/5ce764e2-373b-4ed8-987c-252774e4d34a" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="722" height="59" alt="481380457-cb816ca9-fcb4-48eb-b660-8d87eaa72cbe" src="https://github.com/user-attachments/assets/228a1dee-0e2d-4f17-a811-df8bcbb8536e" />



egrep 'Linux.*world' newfile 
## OUTPUT

<img width="722" height="64" alt="481380476-dc7db948-d72b-4cdb-aa17-6d69bbbd293b" src="https://github.com/user-attachments/assets/4ba2f994-31cd-46ef-9d2b-ab95eb13f89a" />

egrep 'Linux.*World' newfile 
## OUTPUT

<img width="722" height="52" alt="481380569-09a1ee39-562f-451a-8ddf-c86db3aba5ca" src="https://github.com/user-attachments/assets/19e15002-c445-4d61-9aa4-c8a354df3228" />

egrep l{2} newfile
## OUTPUT
<img width="722" height="73" alt="481380582-eac7b33f-a952-44c1-bbda-85c8daf87bd3" src="https://github.com/user-attachments/assets/4e9bd8a7-1da1-4b79-9d15-017a3c2f17aa" />



egrep 's{1,2}' newfile
## OUTPUT 

<img width="722" height="93" alt="481380627-1818f25b-dba6-4517-af71-5e5e2e78475c" src="https://github.com/user-attachments/assets/218606e2-be46-4d80-b915-e31dce839aef" />

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

<img width="722" height="66" alt="481380689-6f82e0e7-7e7a-4262-b027-c48207456731" src="https://github.com/user-attachments/assets/65aed4cd-02a9-4157-959b-a1391decc136" />


sed -n -e '$p' file23
## OUTPUT

<img width="722" height="66" alt="481380708-d2264214-9451-41ac-8bec-53f1e78e74f2" src="https://github.com/user-attachments/assets/1b4cdebd-baca-4939-a5e6-917bc279b39c" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="722" height="206" alt="481380743-e4c02470-b031-4d53-b1b5-f1006640cea7" src="https://github.com/user-attachments/assets/add881a8-da55-4053-94c4-5bdba568a0dc" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="722" height="206" alt="481380764-f71aecfb-1ce3-4197-81c2-707837391e51" src="https://github.com/user-attachments/assets/84a12a40-045a-4fc9-a86a-557cced55d25" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="722" height="206" alt="481380778-edad5acb-35b4-4b2f-91f8-756dd026c0ac" src="https://github.com/user-attachments/assets/424a3a93-09d8-4b42-8c72-f6773b71188d" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="722" height="137" alt="481380791-7c154068-c4d5-4ae2-9de4-1d9cd014efd9" src="https://github.com/user-attachments/assets/57a5aa64-5b40-4950-b605-7d5f21aabc76" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="722" height="97" alt="481380809-b0892e5c-87c5-4413-8f93-0b7701e020e6" src="https://github.com/user-attachments/assets/bc9d704d-d513-487b-8fd9-2a19c1c6c3f8" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="722" height="78" alt="481380826-8cfb83a4-6f35-4225-8940-ecd55d3f4f89" src="https://github.com/user-attachments/assets/033fad3f-881b-4c43-b922-b0ac021163b7" />


seq 10 
## OUTPUT

<img width="722" height="222" alt="481380944-eaeb6c0b-cf07-4c9a-b888-2225c04a17ef" src="https://github.com/user-attachments/assets/576ae20e-a22b-4022-937c-43f897d26cfe" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="722" height="97" alt="481380976-9c06a1e6-2970-440f-8a1a-b6988a420ca6" src="https://github.com/user-attachments/assets/9512342a-b41c-4a03-9dd1-a680fdcdf96f" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="722" height="186" alt="481381062-15c30199-f218-474e-a697-1e41c160344a" src="https://github.com/user-attachments/assets/cbdade84-c033-48da-af8b-daa6a206e70f" />



seq 3 | sed '2a hello'
## OUTPUT


<img width="722" height="112" alt="481381097-ebaec149-df15-4337-af89-7d232581950f" src="https://github.com/user-attachments/assets/ad264a49-bbb7-4f1d-9c85-5b81db692199" />

seq 2 | sed '2i hello'
## OUTPUT
<img width="722" height="97" alt="481386968-7e5eee24-60ac-40b6-9c60-82a7f2e179f1" src="https://github.com/user-attachments/assets/dd377c28-08c8-4887-acd8-3f4de459ee85" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="722" height="97" alt="481386986-fec30d69-e4b0-44a3-b7eb-44ecfb55f283" src="https://github.com/user-attachments/assets/36661410-1ae9-4b04-bc85-c3977c717e7b" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="722" height="97" alt="481387001-7e8acb79-3636-46f7-92fe-4dda9d80041f" src="https://github.com/user-attachments/assets/722a2376-4bf5-484c-9ded-24c6b3bde0c4" />



sed -n '2,4{s/$/*/;p}' file23
<img width="722" height="97" alt="481387037-08bd6dbc-c73c-4094-a891-cdb147db8dc2" src="https://github.com/user-attachments/assets/d297e7ae-f843-4b58-88dd-d749174961d7" />


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

<img width="722" height="130" alt="481387089-62d4a02b-bf75-4592-9d12-1c39f14ecf4c" src="https://github.com/user-attachments/assets/00fb6492-b742-4de2-bfbf-a9a4d087fb74" />

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
<img width="722" height="130" alt="481387125-1eb8eb05-1616-459a-9473-0a5b2dcf1bcc" src="https://github.com/user-attachments/assets/5e224742-eaea-4c33-9771-14ba5d1ad508" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="763" height="206" alt="481387146-d699e8d4-20ce-4952-bda6-75385ecfd001" src="https://github.com/user-attachments/assets/8c2bc3ce-267c-4d4c-a061-04b3ba9d8d9a" />

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
<img width="763" height="96" alt="481387287-f384a6f4-d4e4-4bbf-b0aa-5d24c5c82685" src="https://github.com/user-attachments/assets/d1bb96b2-d201-4991-8331-526304a5a3dd" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="763" height="96" alt="481387306-b30cbff8-5559-4871-b907-b860a2b97c26" src="https://github.com/user-attachments/assets/2632b31c-fc3b-4ae0-bc5d-0e1156de8b5d" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="763" height="126" alt="481387362-b2cb398a-386e-4195-baf3-3728f0e72db2" src="https://github.com/user-attachments/assets/cf8b644b-daff-4f7b-a9b5-a31fe7dbf3ef" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="763" height="81" alt="481387470-3f2a15b8-45ac-43fa-b8b7-3471cfc0a4fa" src="https://github.com/user-attachments/assets/083027f9-8829-4c55-91fc-ffd948d1e8e6" />

tar -xvf backup.tar
## OUTPUT
<img width="763" height="81" alt="481387516-c09c3255-4d0b-4975-af48-bf5d21e33d33" src="https://github.com/user-attachments/assets/e4907f0c-821b-46df-a87d-ee8f5a32abed" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="763" height="81" alt="481387509-04f00b3b-763a-425c-8e30-070d3c13c170" src="https://github.com/user-attachments/assets/936ab8c1-1e6a-4544-82b6-d98d69b49be1" />

gunzip backup.tar.gz
## OUTPUT
<img width="763" height="81" alt="481387513-b38590b2-abe4-40d3-8c54-a828adc71e5a" src="https://github.com/user-attachments/assets/eafe6073-15fe-44bb-8281-d519fd205085" />

 
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
<img width="763" height="95" alt="481387794-36a8bbb1-80f8-4690-8f94-5e7b31af2fb5" src="https://github.com/user-attachments/assets/d46ea2f4-59f5-4330-a057-11a7d01c8b7f" />


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
<img width="514" height="61" alt="481388294-8e44a24e-b68d-458f-8b96-86960b530be7" src="https://github.com/user-attachments/assets/dfc97b1f-da22-4206-9ced-9aef5a8abee9" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 <img width="514" height="61" alt="481388200-212dffe9-cbc7-49c2-becd-171506d1fe6c" src="https://github.com/user-attachments/assets/cba81d5c-1f0c-4330-9061-77d443169ef1" />

echo $?
## OUTPUT 
 <img width="514" height="61" alt="481388173-79e5f7aa-c11b-4342-9838-283822173062" src="https://github.com/user-attachments/assets/485bbf83-f765-4fc4-bdfe-aade495fe47e" />

abcd
 
echo $?
 ## OUTPUT


 <img width="514" height="61" alt="481388212-9e76bc4a-c383-4a73-9573-60b56e84375b" src="https://github.com/user-attachments/assets/fa6584c4-fda1-4a7b-a2be-616e6f65edc0" />

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


<img width="559" height="243" alt="481388414-19ca9a7c-df4d-4372-bcd5-2c8890daa5f8" src="https://github.com/user-attachments/assets/d311f30f-4bff-4dd6-ba45-109a2de76f48" />

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="598" height="63" alt="481388495-6a69982e-8958-4a2b-b0cc-7be0e00a406b" src="https://github.com/user-attachments/assets/735ead5d-efa7-4e5d-a7f9-e85b187ff4d3" />


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
<img width="598" height="162" alt="481388602-d29452bf-61f4-4629-aabe-e95768aa9fa9" src="https://github.com/user-attachments/assets/84d0f79e-a24e-45dd-9ea1-90a5881b269f" />

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

<img width="598" height="363" alt="481388764-b7672c11-6b39-41d4-bcc8-60909ac05973" src="https://github.com/user-attachments/assets/b7a5d08d-20b0-47a7-9a44-d876f37ff933" />


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
<img width="827" height="71" alt="481394810-948e3813-b245-4cbe-980e-9458728f1e7a" src="https://github.com/user-attachments/assets/7420d6d8-5375-47c7-a9c7-a872dd3ee6be" />

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
<img width="730" height="86" alt="481394822-d4a62e30-83ff-4655-ae8d-08ec9fbfa442" src="https://github.com/user-attachments/assets/828064e3-2525-4133-9a46-575d9f88e7bc" />

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

<img width="775" height="53" alt="481394834-695f3f25-5926-418f-b471-3bb98791ae1b" src="https://github.com/user-attachments/assets/d082b9e6-8bab-4b3a-b949-1f7d0c7f862a" />

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
<img width="824" height="57" alt="481394850-4236dd29-ac6a-4803-b45f-a270e675e965" src="https://github.com/user-attachments/assets/432a6dbe-f5c8-496a-b903-40c8b274e30e" />

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

<img width="898" height="132" alt="481394891-6e5afeab-e971-42ea-bb04-2a0bad404202" src="https://github.com/user-attachments/assets/adc334b4-9ebd-4032-93b0-6c04bf091655" />

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
<img width="816" height="263" alt="481394904-d5b53d07-74b5-4c2b-99b5-1205c9e00276" src="https://github.com/user-attachments/assets/cb602308-c276-4dd4-916b-a4e805b3d0fe" />


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
<img width="698" height="206" alt="481394918-1e5d0cde-fc29-428d-bd20-af34e6817007" src="https://github.com/user-attachments/assets/cad4dc8d-30de-4efe-9fdb-5015e891c747" />

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
<img width="832" height="201" alt="481394924-76b2a94b-3df4-44f2-9017-0af124eaaed4" src="https://github.com/user-attachments/assets/7e9d18e2-7cb5-451e-abed-df7c88c0127c" />

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
<img width="823" height="347" alt="481395103-18110009-1a7e-4f31-9453-129d4316ad93" src="https://github.com/user-attachments/assets/3fde8c53-e2a7-4824-9689-74a132e2ff64" />

 
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
<img width="796" height="241" alt="481395095-d2cb1cf1-f74d-448f-ad94-d08292d52a4d" src="https://github.com/user-attachments/assets/0708fef5-ac05-426c-94e0-77d2abb0e163" />

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
 <img width="706" height="269" alt="481395072-3061404e-911b-4e3f-aeb8-dc1f28d79ba1" src="https://github.com/user-attachments/assets/d03cbc6f-751f-4c87-9006-19654fff4434" />

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
<img width="711" height="144" alt="481395062-9dce4fe2-1a37-4729-b535-0c7b7e51aa2b" src="https://github.com/user-attachments/assets/b9077bc6-4060-4556-9876-7f2a5c34ce61" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT


<img width="721" height="137" alt="481395054-f399a0e4-7e8b-49db-8260-fd4a3717ac2d" src="https://github.com/user-attachments/assets/999df837-0e29-4bf2-9c8a-06929571e6d7" />

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
<img width="742" height="236" alt="481395038-d1a4cfb5-195d-4d1a-8224-1384f8842029" src="https://github.com/user-attachments/assets/04118141-df87-4413-8b5b-6ce14ed3e20f" />

 
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
 <img width="736" height="157" alt="481395028-90b4ab09-aaba-40ff-9559-6a1af0e8328a" src="https://github.com/user-attachments/assets/79413ca3-ea95-4235-bd3b-5c54a00e15b5" />

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
 <img width="825" height="229" alt="481395020-f0f5d814-f8a9-4b73-8f97-af22d3234098" src="https://github.com/user-attachments/assets/515f0065-30dc-4fc6-b4ea-20f605ea2cc3" />

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
 
 <img width="833" height="321" alt="481395012-3becd8ee-e6e0-41bb-bb75-ad0a44140034" src="https://github.com/user-attachments/assets/745f169f-7d92-40e2-8a37-fb8b4c76d185" />

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
 <img width="801" height="520" alt="481394990-458e3958-b9f5-4f14-b161-4732ff661a7d" src="https://github.com/user-attachments/assets/38ed361a-aed6-4f6d-bb80-0b8991f7fddf" />

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
<img width="831" height="729" alt="481394973-babdfcc8-9fbf-403b-9823-b29a88eb22bd" src="https://github.com/user-attachments/assets/77de7f4f-23c0-441d-aa37-2d27d43f2215" />


# RESULT:
The Commands are executed successfully.
