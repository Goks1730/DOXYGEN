
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
  
  A sample.conf file will be generated in your folder as shown below.

<img width="418" alt="Screenshot 2023-04-20 225640" src="https://user-images.githubusercontent.com/84590536/233444725-319f4ed3-54cd-425e-97a5-d320adcad39d.png">
  
 
## configuration Set-up

Once the configuration file is generated require few configuration as per your project and path requirements. So edit generated configuration file and update following options

|     configuration       | YES/NO/PATH_ADDRESS                                                                |
| ----------------- | ------------------------------------------------------------------ |
| PROJECT NAME! | ![#00b48a](https://via.placeholder.com/10/0a192f?text=+) CUSTOM |
| FOLER_PATH INPUT | ![#00b48a](https://via.placeholder.com/10/00b48a?text=+) DECLARE_PATH |
| EXTRACT | ![#00d1a0](https://via.placeholder.com/10/00b48a?text=+) YES |
| EXTRACT_STATIC | ![#00d1a0](https://via.placeholder.com/10/00b48a?text=+) YES |
| FILE_PATTERN | ![#00d1a0](https://via.placeholder.com/10/00b48a?text=+) C |
| RECURSIVE | ![#00d1a0](https://via.placeholder.com/10/00b48a?text=+) YES |
| INLINE_SOURCE | ![#00d1a0](https://via.placeholder.com/10/00b48a?text=+) YES |
| CHM_FILE | ![#00d1a0](https://via.placeholder.com/10/00b48a?text=+) YES |
| PATH PROJECT_LOGO | ![#00d1a0](https://via.placeholder.com/10/00b48a?text=+) DECLARE_PATH |
| GENERATE_LATEX | ![#00b48a](https://via.placeholder.com/10/0a192f?text=+) NO |





STEP 6: Run the File

Once the configuration file is edited, you can generate the documentation for your project by running doxygen sample.conf command as shown below.

```bash
  doxygen sample.conf
```
Once you run above command. Doxygen will process the generate document as shown below.

<img width="377" alt="2" src="https://user-images.githubusercontent.com/84590536/233454265-7cba5e8d-07d2-4494-84fc-ff988bb825cd.png">
  
  ## You should now notice two newly created folders:

`html`

`latex`
  
By default, Doxygen outputs LaTeX-formatted documentation as well as HTML-based documentation. In this article, I will focus only on HTML-based documentation. You can find out more about LaTeX output in the official Doxygen documentation, in the Getting started section.

 html/index.html will have HTML documentation. you can open directly or run through command prompt
  
  STEP 7: Opening through command prompt

```bash
  cd html
```
  STEP 8: Open the Documentation in browser

```bash
  firefox index.html
  or
  google-chrome index.html
```
  
  



