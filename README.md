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



 









