
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

<img width="418" alt="Screenshot 2023-04-20 225640" src="https://user-images.githubusercontent.com/84590536/233444725-319f4ed3-54cd-425e-97a5-d320adcad39d.png">
  
 
## configuration Set-up

Once the configuration file is generated require few configuration as per your project and path requirements. So edit generated configuration file and update following options

[![PROJECT NAME! NAME](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)
[![FOLER_PATH INPUT](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
[![YES EXTRACT](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
[![YES EXTRACT_STATIC](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)
[![*/C FILE_PATTERN](https://img.shields.io/badge/license-AGPL-blue.svg)](http://www.gnu.org/licenses/agpl-3.0)
[![YES RECURSIVE](https://img.shields.io/badge/license-AGPL-blue.svg)](http://www.gnu.org/licenses/agpl-3.0)
[![YES INLINE_SOURCE](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)
[![YES CHM_FILE](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
[![NO GENERATE_LATEX](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)
[![PATH PROJECT_LOGO](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)






STEP 6: Run the File

Once the configuration file is edited, you can generate the documentation for your project by running doxygen sample.conf command as shown below.

```bash
  doxygen sample.conf
```

## 
## Screenshots

![Alt text](C:\Users\GOKUL KUMAR M\Downloads?raw=true "Optional Title")



