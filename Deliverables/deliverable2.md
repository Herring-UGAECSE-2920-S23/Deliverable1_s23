# Deliverable 2

For this week, after completing a syllabus quiz, you'll be creating a team attendance sheet, documenting the state of existing hardware you have recieved, characterizing the digital potentiometers, and going through the preliminary setup for the Raspberry Pi hardware. 

Right now would also be a good time to read through the rules for the project outlined [in the README](../README.md) for this repository.
 
## Github Exercise
After you've been assigned to a group, make sure you have set up your Github account and submitted your username to the assignment on ELC. Once you've done that, we will have an organization group invite sent to you as soon as groups are assigned from the CATME survey. To view and accept the organization group invite, go to the "Notifications" section on your Github home page. The icon should be in the upper right hand corner of the page, near your profile picture, and should look something like this:


![notifications](images/PRO.png)

Once you've accepted the group invite, you'll have access to your group's repository on the Github organization for the class. From here, you'll need to set up [Git](https://docs.github.com/en/free-pro-team@latest/github/getting-started-with-github/set-up-git) and [Python](https://realpython.com/installing-python/) on your personal computer to complete this assignment (assuming they are not already installed).

>Note: In order to clone Git repositories via SSH (recommended) you need to have the public SSH key for your computer linked to your Github account. Instructions for generating and linking SSH keys are in the Git setup guide linked above.

When you've got Git and Python set up, clone your group Git repository somewhere on your personal computer. From GitBash on Windows or a regular terminal on MacOS/Linux, run the following command, replacing [SSH Address] with the SSH address for your group's Git repository, found under the 'code' button on the repository home page, pictured below:

```
git clone [SSH Address]
```

![notification](images/GITADD.png)
When you have the repository cloned, create a Python script under a directory named `HelloWorldScripts` with the file name being `firstname_lastname.py` replacing `firstname` with your first name and `lastname` with your last name.

In the script, simply print your full name and exit. When done, make sure to save your changes and 'push' them to Github by following [this](https://docs.github.com/en/free-pro-team@latest/github/managing-files-in-a-repository/adding-a-file-to-a-repository-using-the-command-line) guide.

After that, you're finished.


## Solder Raspberry Pi Protection Hat (P)

In order to prevent shorting out the Rapsberry Pi, we have designed a Pi Hat to attach to the top of the Pi. You will need to solder the PCB (printed circuit board) and verify its functionality. This is very important to complete before using GPIO pins. **Be sure the diodes are facing in the correct direction to match the silkscreen.** This will take a good chunk of time, so be sure to plan ahead (it took the TA's around 2 hours).  A helpful hint is to leave the two 2x20 pin headers for last, as this will make it easier to solder the smaller components on the board.  Also, make sure that you see that the female header is facing down on the underside of the PPH (this is what will connect directly to the Pi).  Here is a handy soldering guide for the PPH.

- https://github.com/Herring-UGAECSE-2920-S23/Deliverables_S2023/blob/main/Resources/PCB%20Soldering%20Instructions.pdf

Verify your soldering job by checking for continuity (Does GPIO2 go to GPIO2*, for example).  Check to make sure there are no shorts on unwanted pins (GPIO to GPIO, GND, 3.3V, 5V).  You can use the continuity checker on a multimeter. The schematic will be helpful.  When finished, document this in your team P deliverable.  Use the standard template on ELC.  

- https://github.com/Herring-UGAECSE-2920-S23/Deliverables_S2023/blob/main/Resources/Schem_GPIO_Hat_v4.0.pdf

## Raspberry Pi Setup (P)

Finally, you'll need to go through the Raspberry Pi setup documentation found [here](setup/pi_setup.md). It will guide you through setting up the Pi and getting all of the Python dependencies and environment set up. It will also link to helpful documentation for how to work on the Raspberry Pi, remotely or otherwise.  When finished, document this in your team P devliverable.  Use the standard template on ELC.  

## Practice Committing Changes (P)

After your Raspberry Pi is fully setup along with your github account. You can now use git to save changes on the pi to github or save changes on github to the pi. This is very useful when coding in groups. NOTE:  Everyone on the team MUST have at least one commit.  Yes, roles will develop throughout the semester, but everyone on the team should be familiar with Github.  When finished, document this in your team P deliverable.  Use the standard template on ELC. 

## Template for Submission to ELC
To standarize the submission process, on ELC is file called "Template_Group#_ Deliverable#.  Rename accordingly, and use this to place the items for Progress Deliverable 2 and submit the corresponding assignment dropbox on ELC.  Don't forget to complete the last page.  Each deliverable submission also needs to include the selfie of the group meeting along with the highlights of the topics covered.  

## Create User Manual and Technical Document 

An important part of your team's grade in this course relies on the user manual and technical documentation that will be submitted at the end of the semester. Begin taking photos and recording what your team does each week to ensure your work is organized. This will not be graded on a weekly basis, BUT it is incredibly helpful to have your explanations and work in one place, rather than scrambling at the last minute to remember the details of what was done each week.

# Summary

In summary, for this week you need to:

1. Make sure you have acquired all of the hardware for your team.

2. **P**: Solder Raspberry Pi Hat

3. **P**: Go though the Raspberry Pi setup, and acquaint yourself with working on the Pi/Github/etc.

4. **P**:  Practice Commiting Changes, make sure they are showing up on your repository 

5. Update your User Manual and Technical Documentation with your findings.

6.  When all **P** deliverables are finished, use the template to submit to ELC before the deadline.  **THERE SHOULD BE ONLY 1 SUBMISSION PER GROUP**.  

