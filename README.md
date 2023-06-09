
# DOXYGEN

Document your source code with Doxygen on Linux 
To use Doxygen, you simply comment your source code in a syntax that Doxygen can read. Doxygen then walks through your source files and creates HTML(.chm) or LaTeX documentation based on those special comments. The C/C++ example project below will illustrate how the source code is commented and how the documentation is generated from it.

## Comments Doxygen Tags

Doxygen reads the sources and checks each file for special comments. Based on those comments and keywords, it builds up the HTML documentation(.chm).

Doxygen comment blocks are easy to create. For line comment just insert a triple forward slash.

/////This line will be included in the Doxygen comments for this function/class/file

Commenting multiple lines is just as easy.

```bash
/*! 
These next few lines will form a comment block    
To start a new paragraph add an empty line    
To end the comment block type asterik and then forward slash. 
*/
By taking a few minutes as you are writing your code to write comment blocks you can tell future developers what you intended and make their life more productive and easier.
```

Comments in Doxygen are divided into two sections, a brief description and a detailed description. Both sections are optional. In the code sample above, the comment block refers to the following line of code, the declaration of a constructor. The sentence behind the @brief will be shown in the compact class overview:

@brief

This tag supplies a brief description of a function for doxygen pages. This message should tell what happens in the function. By convention in Rosetta3 all functions must have brief tags. These included in the header file along with the declaration of the functions.


@param

This tag can be used to document the purpose and meaning of params for functions. You can specify the nature of the param as input output or both in the following manner

@param[in]

@param[out]

@param[in/out]


```bash
/*! @brief Constructor which takes an external buffer to operate on
*
*
* @param[in] pBuf Pointer to existing buffer
* @param[in] size Size of the existing buffer
*/
```

## Deployment and Installing 
STEP 1: Update Your Server

First you need to update the Server by using sudo apt update command as shown below.

```bash
  sudo apt update
```
STEP 2: Install Doxygen

Doxygen:
Next step is to install Doxygen by using sudo apt install doxygen command as shown below. This command will download and install the package along with all its dependencies from default Ubuntu repo


Graghviz:
Doxygen can use the “dot” tool from graphviz to generate more advanced diagrams and graphs. Graphviz is an open-source, cross-platform graph drawing toolkit and can be found at http://www.graphviz.org/. This can do a lot more things but I have used it for my c project so using it to generate the call graphs.

```bash
  sudo apt install doxygen
  sudo apt install graphviz
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
  
By default, Doxygen outputs LaTeX-formatted documentation as well as HTML-based documentation. In this article, I will focus only on HTML-based documentation. You can find out more about LaTeX output in the official Doxygen documentation, in the Getting started section. you can run the documentation without the latex, you just need to set-up the configuration and disable the latex, if you disable it you get the folder of latex, you can directly run through html folder.

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
  
  # CREATE A SINGLE COMMAND IN LINUX SO YOU CAN GENERATE DOCUMENTATION

  
## Deployment

Step 1: From home directory open .bashrc file

```bash
  sudo nano .bashrc
```

Step 2: Add a line at the bottom of the file in the following format
alias <your_custom_command_name>=‘<command_to_be_executed>’

```bash
  alias rundox='firefox /home/goks/DOXY1/html/index.html'
```
  <img width="364" alt="3" src="https://user-images.githubusercontent.com/84590536/233460519-b7a2e68a-1544-4ba3-9dc1-2e4097921b4f.png">
  
 Step 3: reboot the linux and start using the command
  
 Step 4: run the command through terminal 
Once above command successfully run then you will check your output directory and the document will be there.
  
```bash
  rundox
```
  <img width="880" alt="6" src="https://user-images.githubusercontent.com/84590536/233463490-151cc163-d3bd-4527-94a4-8a89198d3580.png">
  
  
## comments in Doxygen are divided into two sections, a brief description and a detailed description. Both sections are optional. In the code sample above, the comment block refers to the following line of code, the declaration of a constructor. The sentence behind the @brief will be shown in the compact class overview:


<img width="449" alt="4" src="https://user-images.githubusercontent.com/84590536/233461920-4e33c9eb-38b5-44cf-8e89-0afe4f4d3ed8.png">
  
  
 ## After a blank line (blank lines are treated as paragraph separators), the actual documentation for the constructor begins. With the @param[in/out] keyword, you can mark the arguments passed to the constructor, and Doxygen will make a clear argument list from it:
  
  <img width="923" alt="5" src="https://user-images.githubusercontent.com/84590536/233462364-fbfb9385-bf51-401f-8b0e-1589530afb73.png">

 ## Conclusion

You have learned how to install Doxygen on an Ubuntu system. We have executed different commands on the terminal for the installation. and we have learned how commands work in Doxygen and how to command your code, and we have learned to use a custom command to run all your documentation. Thanks!




 


