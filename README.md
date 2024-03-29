# WiCS Project

# Installation Instructions: Setting up VSCode, Python, GitHub

1. Set up VSCode
    1. follow instructions 
        
        [Download VSCode](https://code.visualstudio.com/docs/setup/windows)
        
2. Install Python
    1. open your terminal
    2. enter this line to check if you already have python installed
        
        ```powershell
        python --version
        ```
        
    3. if you don't already have it installed follow the instructions on this link
        
        [Download Python](https://www.python.org/downloads/)
        
        to install using terminal on windows enter the following command
        
        ```powershell
        winget install Python.Python.3.12
        ```
        close and reopen your terminal and run the python -V command to make sure python installed properly
        
3. Download Open AI Speech to text
    1. [Download Whisper](https://github.com/openai/whisper) scroll down and follow the set up instructions
    2. use the “small model”
4. Connect GitHub to VSCode
    1. navigate to the source control tab and follow the instructions for installing git
    2. Once you’re signed in and have github installed click the clone repository button
    3. when it asks you for a link paste this https://github.com/quinncage/WiCSProject.git
    4. once you enter the link it will ask you for a location on your computer to store your project, choose one
        1. no need to create a folder, the window that asks you where to store it will create a folder for you with the name of the repo (WiCSProject) automatically
5. to make sure your project is working correctly, record a short audio clip on “Sound Recorder” app on windows and name it EXACTLY “audio.mp3” and move it to the project folder
    1. navigate to the SpeechToText.py file and click the play button in the upper right hand corner of vscode and wait a minute or so (first time takes longer) or you can also open the terminal in vscode using the ctrl + tilde or cmd + tilde and enter the following command on windows
        
        ```powershell
        python SpeechToText.py
        ```

        and the following on a mac
        
        ```bash
        python3 SpeechToText.py
        ```
    
    2. the transcription should appear in the terminal of vscode
  
# Meeting 2 on Zoom (2/26/24)
## To install python on a mac you need to do the following

### Step 0: Uninstalling your existing python installation from the website

(you can copy paste all commands below and run them at once no need to run them one by one)

```bash
python_version_number=3.12
sudo rm -rf /Library/Frameworks/Python.framework/Versions/${python_version_number}/
sudo rm -rf "/Applications/Python ${python_version_number}/"
cd /usr/local/bin && ls -l | grep "/Library/Frameworks/Python.framework/Versions/${python_version_number}" | awk '{print $9}' | sudo xargs rm```
```
### Step 1: Installing Brew

brew is a command line based package manager for mac similar to apt on linux or winget on windows and it can install the right version of python for us

(you can copy paste all commands below and run them at once no need to run them one by one, this command can take some time and it might ask you to install XCode tools as well, install them)

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"```
```
### Step 2: Installing python using brew

```bash
brew install python@3.12```
```
