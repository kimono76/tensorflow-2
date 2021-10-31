# How to Install Anaconda on Fedora 34/33

Anaconda is an distribution which help us with the package management and deployments. It is written on Python and R programming language by data scientists, for data scientists. It includes the packages related to data-science for various platforms like Linux, Windows and macOS.

You can use the conda binary for the package management with your Python applications. Which will provide you a better environment for faster development.

In this step by step tutorial, we will help you to install Anaconda on your Fedora Linux system.
Prerequisites

Login to your Fedora system and open a terminal. Generally the curl package are default installed on Fedora system. Execute the following command to install or update the curl package on your system.

``` 
	sudo dnf install curl -y 
```

## Step 1 – Download the Anaconda Installer

We can download Anaconda installer script from the official site. Visit the Anaconda installer script download page to check for the latest available versions.

Use the curl command line utility to download the Anaconda installer script as below:

``` 
	curl --output anaconda.sh https://repo.anaconda.com/archive/Anaconda3-2021.05-Linux-x86_64.sh 
```

You can also use SHA-256 checksum, to make sure the package is safe and properly downloaded.

Now set the execute permission for script.
``` 
	chmod +x anaconda.sh 
``` 
## Step 2 – How to Install Anaconda on Fedora

Your system is ready to install Anaconda. Let’s move to the text step and execute the Anaconda installer script as below:
``` 
	bash anaconda.sh 
``` 

Follow the wizard instructions to complete Anaconda installation process. You need to provide inputs during installation process as described below:

    01. Use above command to run the downloaded installer script with the bash shell.

    Installing Conda on Fedora
    Start Anaconda Installation on Fedora

    02. Type “yes” to accept the Anaconda license agreement to continue.
    Accept License Agreement in Conda Installer
    Accept License Agreement

    03. Verify the Anaconda installation directory location and then just hit Enter to continue installer to that directory.
    Continue Anaconda Installation
    Continue the Anaconda Installer Process

    04. Type “yes” to initialize the Anaconda installer on your system.
    Intialize Anaconda during Installation
    Intialize Anaconda during Installation

    05. You will see a successful installation message of Anaconda on your system along with more details of installation files and directories.

    Anaconda Installed Successfully on Fedora
    Anaconda Successfully Installed on Fedora Linux

The Anaconda has been successfully installed on Fedora Linux system. Also the installer script has added the environment configuration in .bashrc file of current logged in user.

Use the following command to activate the Anaconda environment:
``` 
	source ~/.bashrc 
``` 

Now we are in the default base of the programming environment. To verify the installation we will open conda list.

``` 
	conda list 
``` 

Output:

# packages in environment at /home/tecadmin/anaconda3:
#
# Name                    Version                   Build  Channel
_ipyw_jlab_nb_ext_conf    0.1.0                    py38_0
_libgcc_mutex             0.1                        main
alabaster                 0.7.12             pyhd3eb1b0_0
anaconda                  2021.05                  py38_0
anaconda-client           1.7.2                    py38_0
anaconda-navigator        2.0.3                    py38_0
anaconda-project          0.9.1              pyhd3eb1b0_1
anyio                     2.2.0            py38h06a4308_1
appdirs                   1.4.4                      py_0
argh                      0.26.2                   py38_0
argon2-cffi               20.1.0           py38h27cfd23_1
asn1crypto                1.4.0                      py_0
astroid                   2.5              py38h06a4308_1

Step 3 – How to Create Conda Environment

Use the following command to create a new Python 3 environment with Anaconda and set its name to “myenv”. You can also choose the specific python version.

conda create -n myenv python=3.9 

Next, activate this environment:

conda activate myenv  

You will see the current environment in command prompt. This indicates that you are now in the new environment you activated.

To deactivate the current environment use command:

conda deactivate  

This will return you to base environment.
How to Update Anaconda

You can easily update the Anaconda and packages using the conda binary. To upgrade the Anaconda on your system, type:

conda update --all 

Output:

Proceed ([y]/n)? y

Press “y” to proceed with the update process. The output will show you all the packages that are newly installing, or upgrading current packages and the removal of unnecessary packages.
How to Uninstall Anaconda

If you no longer used the Anaconda on your system. You can uninstall it by removing the installation directories and files created under the home directory.

rm -rf ~/anaconda3 ~/.conda 

Also edit the ~/.bashrc file and remove the Anaconda environment configuration
