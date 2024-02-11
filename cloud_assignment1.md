## Create a new user named Altschool

```
sudo adduser Altschool
```

## Create a password for the Altschool user

```
sudo passwd Altschool
```

- switch user to newly created user using the following command

```
su Altschool
```

- then use the following command to get to the home directory of the Altschool

```
bash
```

### Creating sub directories in the home directory

```
mkdir code tests personal misc
```

### Change directory to the tests directory using absolute path name

```
cd /home/Altschool/tests
```

### Change directory to the tests directory using relative path name

```
cd ./tests
```

### Use echo to create fileA with text content "Hello A" in the misc directory

```
echo 'Hello A' > /home/Altschool/misc/fileA
```

### Create an empty fileB with dummy content in the misc directory

```
echo 'lorem ipsum dolo toro' > /home/Altschool/misc/fileA
```

### Copy contents of fileA into fileC

```
cp /home/Altschool/misc/fileA /home/Altschool/misc/fileC
```

### Move contents of fileB into fileD

```
mv /home/Altschool/misc/fileB /home/Altschool/misc/fileD
```

### Create a tar archive called misc.tar for the content of misc directory

```
tar -cvf misc.tar /home/Altschool/misc
```

### Compress the tar archive to create misc.tar.gz file

```
gzip /home/Altschool/misc.tar
```

### Create a user and force the user to change his/her password on login

- creating the new user

```
sudo adduser Juliana
```

- setting the user password

```
sudo passwd Juliana
```

- Forcing the user to change password on login

```
sudo passwd --expire Juliana
```

### Lock a user password

```
sudo passwd -l Juliana
```

### Create a user without login shell

```
sudo useradd -s /sbin/nologin Daby
```

### Disable password based authentication for ssh

```
sudo vi /etc/ssh/sshd_config
```

- give the corresponding file a numbering

```
:se nu
```

- Create a new line under line 32 and add this content

```
PasswordAuthentication no
```

- save the file

```
:wq
```

### Disable root login for ssh

```
sudo vi /etc/ssh/sshd_config
```

- give the corresponding file a numbering

```
:se nu
```

- Create a new line under line 32 and add this content

```
PermitRootLogin no
```

- save the file

```
:wq
```
