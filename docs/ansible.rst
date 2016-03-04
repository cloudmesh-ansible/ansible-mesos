
Why is this whole documentation not:


pip install ansible  ??????



Ansible Installation on Different Platforms
 On Ubuntu 14.04
 We first update all existing softwares:
$ sudo apt-get update
Install the software-properties-common package which gives us the ability to work with ansible PPA. $ sudo apt-get install software-properties-common
Once the package is installed, we can add the Ansible PPA through following command:
$ sudo apt-add-repository ppa:ansible/ansible
Press “Enter” to accept the PPA addition.
Next, we refresh the system’s package index so that it is aware of the packages available in the PPA. $ sudo apt-get update
Next, to install Ansible:
$ sudo apt-get install ansible
On Ubuntu 13.04 and 12.10
First we need to make sure, the python version installed is minimum 2.7.4
Follow the following steps to update python to desired version:
$ pybaseversion="2.7"
$ pyextversion="10"
$ sudo apt-get update –y
$ sudo apt-get upgrade –y
$ sudo apt-get dist-upgrade –y
$ sudo apt-get install python-setuptools python-pip python-dev libncurses-dev git –y
        $ sudo apt-get install build-essential checkinstall libreadline-gplv2-dev libncursesw5-dev libssl-dev
 libsqlite3-dev tk-dev libgdbm-dev libc6-dev libbz2-dev –y
 $ sudo apt-get install -y gcc-multilib g++-multilib libffi-dev libffi6 libffi6-dbg python-crypto python-
 mox3 python-pil python-ply libssl-dev zlib1g-dev libbz2-dev libexpat1-dev libbluetooth-dev libgdbm-
 dev dpkg-dev quilt autotools-dev libreadline-dev libtinfo-dev libncursesw5-dev tk-dev blt-dev libssl-
 dev zlib1g-dev libbz2-dev libexpat1-dev libbluetooth-dev libsqlite3-dev libgpm2 mime-support
 netbase net-tools bzip2
 $ wget --no-check-certificate
 https://www.python.org/ftp/python/$pybaseversion.$pyextversion/Python-
  $pybaseversion.$pyextversion.tgz
  $ wget --no-check-certificate https://bitbucket.org/pypa/setuptools/raw/bootstrap/ez_setup.py
 
 $ tar -xvzf Python-$pybaseversion.$pyextversion.tgz
$ cd Python-$pybaseversion.$pyextversion
$ ./configure --prefix /usr/local/lib/python2.7.10 --enable-ipv6
$ make
$ sudo make install
$ /usr/local/lib/python$pybaseversion.$pyextversion/bin/python –version
$ sudo /usr/local/lib/python$pybaseversion.$pyextversion/bin/python ez_setup.py
$ sudo ln -sf /usr/local/lib/python$pybaseversion.$pyextversion/bin/pip /usr/bin/pip
$ sudo ln -sf /usr/local/lib/python$pybaseversion.$pyextversion/bin/pip /usr/bin/python To verify the python version:
$ python –V
Next, follow same steps as above to install Ansible
On CentOS
$ sudo rpm –iUvh http://dl.fedoraproject.com/pub/epel/x86_64/e/epel-release-7-5.noarch.rpm Update the packages:
$ sudo yum –y update
Next, to install Ansible:
$ sudo yum –y install ansible To verify installation:
$ ansible –version
On OSX:
The default python version of 2.7.10 and pip 8.0.2 will work Ansible Installation. To install pip:
sudo easy_install pip
To install Ansible:
sudo pip install ansible –quiet
To update Ansible
sudo pip install ansible --upgrade
       $ sudo ln -sf /usr/local/lib/python$pybaseversion.$pyextversion/bin/easy_install
 /usr/bin/easy_install
      Ansible is part of Extra Packages for Enterprise Linux (EPEL), which is a community repository of non-
 standard packages for the RHEL distribution. First, we’ll install the EPEL repository:
                 
