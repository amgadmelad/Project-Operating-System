# Project-Operating-System
# Project Name:Adding a "hackers" system call in ubuntu.
# Team members:
1)bola Magdy AbdelKader.

2)Amgad Melad Esaac.

3)Mina Samir Labib.
                            ------------------------------------------------------------------------------------------------------------------
# Now we will start to add our system call in ubuntu.
# We will enter the following codes line by line to make sure that we have all the necessary and required packages to add a system call and then compile the kernel successfully:

1) apt-get update                                   2) apt-get upgrade      

![IMG-20210607-WA0037](https://user-images.githubusercontent.com/82906996/121091821-e436bf80-c7ea-11eb-8202-69683433ab78.jpg)

# We will have to write sudo in start of approx. write sudo –s on terminal and give my password and then I will be free to give password on every command.

![IMG-20210607-WA0036](https://user-images.githubusercontent.com/82906996/121091973-23fda700-c7eb-11eb-98b7-3be812744f6b.jpg)

 ![IMG-20210607-WA0035](https://user-images.githubusercontent.com/82906996/121092935-a0dd5080-c7ec-11eb-85be-482f85253842.jpg)

 ![IMG-20210607-WA0034](https://user-images.githubusercontent.com/82906996/121093023-c23e3c80-c7ec-11eb-9399-92fd21a391ea.jpg)
 
 ![IMG-20210607-WA0032](https://user-images.githubusercontent.com/82906996/121093177-f0bc1780-c7ec-11eb-8008-edc8fac877cf.jpg)
 
 ![IMG-20210607-WA0030](https://user-images.githubusercontent.com/82906996/121093743-bf901700-c7ed-11eb-849e-40d697d8a21d.jpg)

# Define a new system call sys_hello():

# I've created a directory with hacker name in the kernel source directory in /usr/src/linux-3.13/ And I created a hacker.c file in hacker directory with below content.

#include <linux/kernel.h>

asmlinkage long sys_hackers(void)
{
        printk(“Hello world\n”);
        return 0;
}


![IMG-20210607-WA0028](https://user-images.githubusercontent.com/82906996/121094058-49d87b00-c7ee-11eb-872d-53a14a7c596f.jpg)

# Now we make menuconfig 

![IMG-20210607-WA0026](https://user-images.githubusercontent.com/82906996/121094773-70e37c80-c7ef-11eb-81a1-e90818549229.jpg)

![IMG-20210607-WA0025](https://user-images.githubusercontent.com/82906996/121094801-7c36a800-c7ef-11eb-8e74-3f5fa488aeec.jpg)

![IMG-20210607-WA0024](https://user-images.githubusercontent.com/82906996/121094828-8658a680-c7ef-11eb-8a45-a8a60f96beb5.jpg)

![IMG-20210607-WA0024](https://user-images.githubusercontent.com/82906996/121094919-a8eabf80-c7ef-11eb-91b9-f57321fecba6.jpg)

# We do "Sudo make modules_install -j3

![IMG-20210607-WA0021](https://user-images.githubusercontent.com/82906996/121095499-bbb1c400-c7f0-11eb-8790-698841fcf015.jpg)

![IMG-20210607-WA0020](https://user-images.githubusercontent.com/82906996/121095545-c9674980-c7f0-11eb-944b-7a3658c2ec04.jpg)

# We will install sudo make install -j3

![IMG-20210607-WA0017](https://user-images.githubusercontent.com/82906996/121095662-0a5f5e00-c7f1-11eb-8950-68968091bc12.jpg)

![IMG-20210607-WA0016](https://user-images.githubusercontent.com/82906996/121095705-1ea35b00-c7f1-11eb-8957-ba5e68d7289d.jpg)

![IMG-20210607-WA0014](https://user-images.githubusercontent.com/82906996/121095755-3b3f9300-c7f1-11eb-98d5-a3fe4b53f6f4.jpg)

![IMG-20210607-WA0013](https://user-images.githubusercontent.com/82906996/121095806-4bf00900-c7f1-11eb-8dd7-7d00d99e9362.jpg)

![IMG-20210607-WA0012](https://user-images.githubusercontent.com/82906996/121095876-6de98b80-c7f1-11eb-9e2b-9552cf53e11a.jpg)

![IMG-20210607-WA0011](https://user-images.githubusercontent.com/82906996/121095889-74780300-c7f1-11eb-97db-8843b2ae2211.jpg)















                                            
