# Agrodrone Branch
This is a fork of the ardupilot code for the Agrodrone project for Drone4agro.
This version is set at ardupilot 3.4.2

## How to install and upload to pixhawk
First you need the code base, this can be retrieved from github if not already available on the PC.

### Clone the ropo to the desktop for new installation
If the code has already been downloaded, skip to the next section.
Assuming git is installed on your PC and set up correctly.

Note: Since this repository is private, you need to have access on your own github account.

- Open the git console, this is most likely found under Start, and then typing powershell.
- move to the directory where you want to place the agrodrone code. For example, by typing: `cd /C/Users/Admin/Desktop/APMCustom/` in the powershell.
- Then, clone the agropilot code here by typing, `git clone https://github.com/annesteenbeek/agropilot.git`
- Now all the required sub modules need to be installed (mavlink, px4 firmware etc...). These are stored as seperate repositories and are added by typing: `git submodule update --init --recursive`
- Now the agrodrone code is on your local machine

### Adding custom mavlink messages for agrodrone
TODO

### Updating the exisitng code
To update the code that has already been downloaded on the pc:
- Open the git console 
- Go to the source code folder, for example by typing `cd /C/Users/Admin/Desktop/APMCustom/agropilot`
- Check if new code is available by typing `git pull`

### Uploading 
- Start the PX4Console, this can be found under Start | All Programs | PX4 Toolchain | PX4Console
- Go to the folder where ardupilot was was installed. For example: `cd /C/Users/Admin/Desktop/APMCustom/agropilot/`
- Then build the code by typing `make px4-v2`. The code should now be compiling
- Then load the MP and connect to the pixhawk Load custom software under installation tab. Open the custom software while the drone is not connected via MAV link, but connected, then load the custom software and the title that appears, then approve, then await tones, then connect mav to continue 

