# LPI-Linux-Essentials-Cert--Ubuntu


# See the Ubuntu version
$ lsb_release -a



# See the Ubuntu Kernel
$ uname -r




# GNU version
$ ls --version



 
# X Server is the GUI
$ sudo X -version



GUI is often reffered to Desktop environment. Ex - Gnome, KDE, Unity, Cinnamon, Mate

Red Hat Enterprise Linux is a commercial Linux distro. Others distro are Ubuntu, Fedora, CentOS etc

Embeded system is combo of hardware and software working together. Ex - Android, Raspberry pi...


# connect to Linux using SSH

$ ssh "username"@"public ip address"

say "yes" when prompt

give the password for the above user

$ ifconfig (will show the private ip address of that server, verify that...)


$ whoami

 $ ls   / ls -la

 $ pwd

 $ last  (show last person logged in)

 $ uptime (how long, many the user logged in...)
 
 $ clear
 
 $ man whoami (for help with whoami)
 
 $ man ls
 
 
 
# Check the usae of local disk

$ df -h | grep "/disk path"


# "for" loop in Bash

cloud_user@sorowar0073c:~$ cd Desktop/

cloud_user@sorowar0073c:~/Desktop$ ls


cloud_user@sorowar0073c:~/Desktop$ touch moh

cloud_user@sorowar0073c:~/Desktop$ ls
moh

cloud_user@sorowar0073c:~/Desktop$ for i in {1..100}; do touch moh_$i; done  ("for" loop)

cloud_user@sorowar0073c:~/Desktop$ ls

moh      moh_13  moh_19  moh_24  moh_3   moh_35  moh_40  moh_46  moh_51  moh_57  moh_62  moh_68  moh_73  moh_79  moh_84  moh_9   moh_95
moh_1    moh_14  moh_2   moh_25  moh_30  moh_36  moh_41  moh_47  moh_52  moh_58  moh_63  moh_69  moh_74  moh_8   moh_85  moh_90  moh_96
moh_10   moh_15  moh_20  moh_26  moh_31  moh_37  moh_42  moh_48  moh_53  moh_59  moh_64  moh_7   moh_75  moh_80  moh_86  moh_91  moh_97
moh_100  moh_16  moh_21  moh_27  moh_32  moh_38  moh_43  moh_49  moh_54  moh_6   moh_65  moh_70  moh_76  moh_81  moh_87  moh_92  moh_98
moh_11   moh_17  moh_22  moh_28  moh_33  moh_39  moh_44  moh_5   moh_55  moh_60  moh_66  moh_71  moh_77  moh_82  moh_88  moh_93  moh_99
moh_12   moh_18  moh_23  moh_29  moh_34  moh_4   moh_45  moh_50  moh_56  moh_61  moh_67  moh_72  moh_78  moh_83  moh_89  moh_94

cloud_user@sorowar0073c:~/Desktop$ rm -f moh*

cloud_user@sorowar0073c:~/Desktop$ ls

cloud_user@sorowar0073c:~/Desktop$ 



# Install and remove "htop" utility in Red Hat/CentOS machine:

[cloud_user@ip-10-0-1-10 ~]$ ls

htop-2.2.0-3.el7.x86_64.rpm

[cloud_user@ip-10-0-1-10 ~]$ sudo rpm -i htop-2.2.0-3.el7.x86_64.rpm 

[sudo] password for cloud_user: 
warning: htop-2.2.0-3.el7.x86_64.rpm: Header V3 RSA/SHA256 Signature, key ID 352c64e5: NOKEY

[cloud_user@ip-10-0-1-10 ~]$ htop

hit "q" to come out of htop


[cloud_user@ip-10-0-1-10 ~]$ sudo rpm -e htop

[cloud_user@ip-10-0-1-10 ~]$ htop

-bash: /usr/bin/htop: No such file or directory

[cloud_user@ip-10-0-1-10 ~]$ 




# Installing a DEB Package


cloud_user@ip-10-0-1-10:~$ pwd

/home/cloud_user

cloud_user@ip-10-0-1-10:~$ cat /etc/issue

Ubuntu 16.04.5 LTS \n \l

cloud_user@ip-10-0-1-10:~$ ls

Desktop  Documents  Downloads  htop_2.0.2-1_amd64.deb  Music  Pictures  Public  Templates  Videos

cloud_user@ip-10-0-1-10:~$ sudo dpkg -i htop_2.0.2-1_amd64.deb 

[sudo] password for cloud_user: 

Selecting previously unselected package htop.
(Reading database ... 159983 files and directories currently installed.)
Preparing to unpack htop_2.0.2-1_amd64.deb ...
Unpacking htop (2.0.2-1) ...
Setting up htop (2.0.2-1) ...
Processing triggers for desktop-file-utils (0.22-1ubuntu5.2) ...
Processing triggers for mime-support (3.59ubuntu1) ...
Processing triggers for man-db (2.7.5-1) ...


cloud_user@ip-10-0-1-10:~$ htop

hit "q" to come out

cloud_user@ip-10-0-1-10:~$ sudo dpkg --remove htop

(Reading database ... 159993 files and directories currently installed.)
Removing htop (2.0.2-1) ...
Processing triggers for man-db (2.7.5-1) ...
Processing triggers for desktop-file-utils (0.22-1ubuntu5.2) ...
Processing triggers for mime-support (3.59ubuntu1) ...

cloud_user@ip-10-0-1-10:~$ htop

The program 'htop' is currently not installed. You can install it by typing:
sudo apt install htop


# Compiling from Source in Red Hat/ CentOS

[cloud_user@ip-10-0-1-10 ~]$ pwd

/home/cloud_user

[cloud_user@ip-10-0-1-10 ~]$ ls

htop-2.2.0.tar.gz

[cloud_user@ip-10-0-1-10 ~]$ tar xzf htop-2.2.0.tar.gz   (extract the zip file)

[cloud_user@ip-10-0-1-10 ~]$ ls

htop-2.2.0  htop-2.2.0.tar.gz


[cloud_user@ip-10-0-1-10 ~]$ cd htop-2.2.0

[cloud_user@ip-10-0-1-10 htop-2.2.0]$ ls


[cloud_user@ip-10-0-1-10 htop-2.2.0]$ ./configure


[cloud_user@ip-10-0-1-10 htop-2.2.0]$ ./configure   (TO configure)


[cloud_user@ip-10-0-1-10 htop-2.2.0]$ make   (to compile the source code into binaries)


[cloud_user@ip-10-0-1-10 htop-2.2.0]$ sudo make install

[sudo] password for cloud_user:



[cloud_user@ip-10-0-1-10 htop-2.2.0]$ htop

press "q" to come out


cloud_user@ip-10-0-1-10 htop-2.2.0]$ cd


can run "htop" from any directory

[cloud_user@ip-10-0-1-10 ~]$ htop



[cloud_user@ip-10-0-1-10 ~]$ cd htop-2.2.0

[cloud_user@ip-10-0-1-10 htop-2.2.0]$ sudo make uninstall

[sudo] password for cloud_user: 

( cd '/usr/local/share/applications' && rm -f htop.desktop )
 ( cd '/usr/local/bin' && rm -f htop )
 ( cd '/usr/local/share/man/man1' && rm -f htop.1 )
 ( cd '/usr/local/share/pixmaps' && rm -f htop.png )


[cloud_user@ip-10-0-1-10 htop-2.2.0]$ htop

-bash: /usr/local/bin/htop: No such file or directory


[cloud_user@ip-10-0-1-10 htop-2.2.0]$


# Determining Which Distribution Is Running on a Host


- view the release files 

$ cat /etc/*release*


-  view the issue files

$ cat /etc/*issue*


- Run a Utility to Determine the Linux Distribution

$ lsb_release -a


- host name

$ hostname


- host details

$ hostnamectl

# --------------------------------------------------------------------

~ means home directory


($) means the current user is unprivileged and the inerterface is ready for input


(#) means root user, with all privileges


 - long listing, human readable
 
 $ ls -lh


 - all, long listing, size, human readable
 
  $ ls -alsh
  
  
  - alias
  
  $ ll
  
  
- declare some variables
  
[cloud_user@sorowar0072c ~]$ var1="Some value"

[cloud_user@sorowar0072c ~]$ echo $var1

Some value


- home directory

[cloud_user@sorowar0072c ~]$ $HOME

-bash: /home/cloud_user: Is a directory
  
  
  
 - PRIMARY prompt string
 
 [cloud_user@sorowar0072c ~]$ echo $PS1
 
 
 - A colon seperated list of directories where the shell looks for commands
 
 [cloud_user@sorowar0072c ~]$ $PATH
 
 
# Lambda Essentials: Linux

mkdir /tmp/lambdafunction

cp lambda_handler.py /tmp/lambdafunction

cd /tmp/lambdafunction

wget https://files.pythonhosted.org/packages/ae/2a/0a0ab2833e5270664fb5fae590717f867ac6319b124160c09f1d3291de28/Pillow-5.4.1-cp37-cp37m-manylinux1_x86_64.whl

unzip Pillow-5.4.1-cp37-cp37m-manylinux1_x86_64.whl

rm -rf Pillow-5.4.1.dist-info

zip -r9 lambda.zip PIL lambda_handler.py
 

# Lambda Essentials: Powershell


mkdir "lambdafunction"

copy "lambda_handler.py" "lambdafunction"

cd "lambdafunction"

- copy the file

wget "https://files.pythonhosted.org/packages/ae/2a/0a0ab2833e5270664fb5fae590717f867ac6319b124160c09f1d3291de28/Pillow-5.4.1-cp37-cp37m-manylinux1_x86_64.whl" -outfile "Pillow-5.4.1-cp37-cp37m-manylinux1_x86_64.whl"


unzip .\"Pillow-5.4.1-cp37-cp37m-manylinux1_x86_64.whl"

- (zip PIL and lambda_handler.py and put in lambda.zip)

- (COMMAND:-

$ZIPFile = @{
   Path= "E:\SourceLocationOfYourFolder\PIL", "E:\SourceLocationOfYourFile\lambda_handler.py"
   CompressionLevel = "Fastest"     
   DestinationPath = "E:\DestinationLocationForYourZip\lambda.zip"
  }
   Compress-Archive @ZIPFile
   
   
)   
   

$ZIPFile = @{Path= ".\PIL", ".\lambda_handler.py"
   CompressionLevel = "Fastest"
   DestinationPath = ".\lambda.zip"
   }
   Compress-Archive @ZIPFile
   

- OR  (zip PIL and lambda_handler.py using GUI and put in lambda.zip)

rm -rf Pillow-5.4.1.dist-info











References: 

https://linuxacademy.com


 
 
  















