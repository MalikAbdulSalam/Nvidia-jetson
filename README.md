# Nvidia-jetson
Complete configuration of jetson
# Configure Python 3.8 on Jetson Nano (jetpack 4.6)

Jetpack 4.x supports python 3.6 by default on base environment

Nvidia recommends not to upgrade this python version. If we want to install Python we can build python from source to avoid conflicts. Following are the key steps to install python==3.8:

run following commands one by one in terminal
```bash
sudo apt update sudo apt upgrade 
sudo apt install build-essential libssl-dev zlib1g-dev libncurses5-dev libncursesw5-dev libreadline-dev libsqlite3-dev libgdbm-dev libdb5.3-dev libbz2-dev libexpat1-dev liblzma-dev libffi-dev libc6-dev 
```
Download the Python source code for version 3.8 from the official Python website. You can use the following command to download it directly to your Jetson Nano:
```bash
wget https://www.python.org/ftp/python/3.8.12/Python-3.8.12.tar.xz 
```
Extract the downloaded archive by running the following command:
```bash
tar -xf Python-3.8.12.tar.xz cd Python-3.8.12 
```
Configure the build process:
```bash 
./configure --enable-optimizations 
```
Build Python:
```bash 
make -j4 
```
Once the compilation is complete, you can install Python by running the following command: 
```bash
sudo make altinstall python3.8 --version 
```
That's it! You have successfully installed Python 3.8 on your Jetson Nano. 

Now you have two python versions on Jetson nano 3.6.9 and 3.8.
