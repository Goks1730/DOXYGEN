
# DOXYGEN

Documentation generator


## Deployment
STEP 1: Update Your Server

First you need to update the Server by using sudo apt update command as shown below.

```bash
  sudo apt update
```
STEP 2: Install Doxygen

Next step is to install Doxygen by using sudo apt install doxygen command as shown below. This command will download and install the package along with all its dependencies from default Ubuntu repo

```bash
  sudo apt install doxygen
```
STEP 3: Check Version

After successful installation, you can check the current installed version by using doxygen --version command as shown below.

```bash
  doxygen --version
```
STEP 4: Generate Documentation

First you need to create configuration file of your source code by using doxygen -g <file> syntax. In this example, we are generating configuration file sample.conf using doxygen -g sample.conf command as shown below.

```bash
  doxygen -g sample.conf
```


## sample.conf 

![App Screenshot](https://via.placeholder.com/468x300?text=App+Screenshot+Here)




STEP 6: Run the File

Once the configuration file is edited, you can generate the documentation for your project by running doxygen sample.conf command as shown below.

```bash
  doxygen sample.conf
```

## 
## Screenshots

![Alt text](C:\Users\GOKUL KUMAR M\Downloads?raw=true "Optional Title")



