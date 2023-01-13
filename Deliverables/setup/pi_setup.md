# Initial Setup

This section goes through the one-time setup students will need to perform upon receiving their kits. Please be aware you may not have to complete the ***Raspberry Pi OS Installation*** if you have a previously used pi. You can tell if you have a previously used by by connecting your pi using a monitor, keyboard, and mouse, you will see this(wallpaper may vary) upon startup.

![pic](RPW.png)

## Hardware

The first thing we'll need to set up is our Raspberry Pi 4 hardware! Each group should have received a kit including the CanaKit Raspberry Pi 4 set, which includes a Raspberry Pi 4, a USB Type C power supply, and some assorted electronics/components we'll use later.

A lot of this information can also be found in the CanaKit Quickstart Guide pictured below, however it does not go into very much detail.

![CanaKit Quickstart Guide](CANA.png)

### Heat Sinks

Your kit should have included some heat sinks with it, this is to make sure we are not overheating some of the more sensitive Raspberry Pi 4 components when in use such as the CPU, the SDRAM, and the USB 3.0 controller. Below is an image of where these three heat sinks should go on the board.

![Bare Rpi board w/ heatsinks](BARE.png)

### Case

In the future we'll make some modifications to this setup the make room for our various I/O breakout boards and hat, but for now we'll simply put the Pi into the included case as shown below:

![Case 1](CS1.png)

![Case 2](CS2.png)

At this stage, it would be wise to attach the small fan to the lid of the case as shown below (it's secured by plastic clips, so be careful), and then fit the lid to the top of the case.

![Case 3](CS3.png)

![Case 4](CS4.png)

## Software

Now, we'll go through the OS installation, and make sure our Python environment is correctly configured with all of the software dependencies you'll need for the project.

### Raspberry Pi and SD Card Issues

The Raspberry PI is very finicky when it comes to the SD Card.  Please read the following information for best practices.

https://hackaday.com/2022/03/09/raspberry-pi-and-the-story-of-sd-card-corruption/

### Raspberry Pi OS Installation

To install Raspberry Pi OS Installation, we'll need to boot up the Pi for first-time setup. The Raspberry Pi documentation regarding first time OS installation can be found [here](https://www.raspberrypi.com/software/).



### Raspberry Pi OS Configuration

Now that you've got Raspberry Pi OS installed, we need to do a bit of configuration to enable all of the settings we need.

On the Pi desktop (or in an SSH terminal), open a terminal window from the task bar, it should look something like this:

![raspi terminal image](TERMINAL.png)

Then, run the `raspi-config` command to configure some settings on the Pi:

```
sudo raspi-config
```

It should bring up a dialogue window that looks similar to this:

![raspi-config window](CONFIG.png)

From here, we need to change a few settings: 

1. Go into Boot Options -> Desktop / CLI and select the last option, `Desktop Autologin`
2. Go into Interfacing Options and enable: `SSH`, `VNC`, `SPI`, and `I2C`
3. Finally, go into Advanced Options -> Resolution and select the highest possible resolution (1920x1080 @ 60Hz 16:9)

After changing these settings, go ahead and reboot the Pi. You can do this from the command line with:

```
sudo reboot
```

Now you *should* be ready to move on!

### Networking

To successfully connect the Raspberry Pi to the internet we have a few options. We could connect it directly to a network with the built-in ethernet and WiFi adapters, however if your WiFi network is configured incorrectly (accidentally or on purpose, thanks Spectrum) or if you try to connect to the PAWS-Secure network on campus you'll quickly run into issues. 

To remedy this, we suggest setting up an Ethernet Bridge between your computer (one with WiFi capability) and the Raspberry Pi, which will share your computer's internet connection with it! Setting these up is fairly straight forward, and we've provided guides for a few Operating Systems below.

#### [Windows](https://communities.efi.com/s/article/How-to-bridge-WiFi-with-Ethernet-in-Windows-10?language=en_US)

#### [MacOS](https://support.apple.com/guide/mac-help/bridge-virtual-network-interfaces-on-mac-mh43557/mac)

#### [Linux](https://www.raspberrypi.org/forums/viewtopic.php?t=13211) (If you use something other than Ubuntu, you're on your own)

Once you have the bridge setup, simply connect an ethernet cable to both your computer and your 

Of course, if you would like, you can use WiFi to connect to your Raspberry Pi by using the networking menu on the Raspberry Pi desktop or by following [these command-line instructions](https://www.raspberrypi.org/documentation/configuration/wireless/wireless-cli.md).

### SSH and VNC Viewer

Now that you've got your Pi connected to the internet through your computer, we can use and access it without a monitor using a couple of tools: SSH and VNC Viewer. 

SSH is protocol used to connect to and use remote devices using a Command-Line Interface. It is secure, and an industry standard in remote work, server administration, and much more.

VNC is also a protocol used to connect to and control remote devices, however instead of using the command-line, VNC allows the user to view the desktop of the remote device, and control it graphically.

To use these two technologies, you'll need a compatible client for you computer. For VNC, you'll be using the popular [VNC Viewer](https://www.realvnc.com/en/connect/download/viewer/). To use SSH on Windows you'll need an SSH client such as [MobaXterm](https://mobaxterm.mobatek.net/), while for MacOS and Linux you can simply use your system's terminal with `ssh` command as follows:

```
ssh pi@[IP Address of Pi]
```

When prompted for a password, the default password for the Pi is "raspberry".

To use either of these tools, you'll need the IP address of the Raspberry Pi on the network (presumably over the ethernet bridge we set up earlier). Luckily, the [Raspberry Pi Foundation has compiled a guide](https://www.raspberrypi.org/documentation/remote-access/ip-address.md) for how to do this. 

> Note: If you're using the ethernet bridge setup, you'll need to use nmap with the `broadcast` IP address for your ethernet port. [here is a quick guide](https://documentation.progress.com/output/ua/OpenEdge_latest/index.html#page/gsins/determining-the-broadcast-address.html) to finding it on Unix (MacOS/Linux) and on Windows.

No matter which option you choose, we will be using the Command-Line frequently in setup and some of our other tutorials, so its worth the effort to get familiar with the interface. A great guide for learning Linux Command-Line can be found [here](https://linuxcommand.org/lc3_learning_the_shell.php).

### System Dependencies

After we have the Pi connected to the internet, we can start installing some of the system dependencies we'll need for this project. System dependencies are simply programs or piece of code we need to be able to write and run our software.

First, we'll make sure we have an up-to-date system by running these two command consecutively:
```
sudo apt update
sudo apt upgrade
```

Then we need to install the dependencies using these commands:
```
sudo apt install pigpio python-pigpio python3-pigpio git
```
It will be helpful to start the `pigpio` daemon at start up. To do this, run the following command.

```
sudo systemctl enable pigpiod
```

### Python Environment and Dependencies

Now that we have the Pi connected to the internet, and can connect with/interact with it without having to have peripherals connected, we can start setting up our programming environment for this project. You'll be using Python to program your XY Plotter as its easy to pick up and has very good packages for using the hardware we have.

To make dealing with dependencies less of a headache, we'll be using a [Python Virtual Environment](https://realpython.com/python-virtual-environments-a-primer/), which confines all packages installed to that environment, making it easier to work on multiple projects (which may need different versions of the same package) on the same computer.

With that being said, let's jump right into it by opening up a terminal on the Pi in your preferred way (SSH/VNC or keyboard/mouse/monitor).

First, we'll need to install `pip`, the Python package manager, which will allow us to install the Python modules we need for this project.
```
sudo apt install python3-pip
```

When the installation completes, check that it installed correctly by running:
```
pip3 --version
```

After that, we'll use `pip` to install `virtualenv` and `virtualenvwrapper`:
```
sudo pip3 install virtualenv virtualenvwrapper
```

Then we'll set up our terminal environment to use `virtualenv` with these commands:
```
echo -e "\n# virtualenv and virtualenvwrapper" >> ~/.bashrc
echo "export WORKON_HOME=$HOME/.virtualenvs" >> ~/.bashrc
echo "export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3" >> ~/.bashrc
echo "source /usr/local/bin/virtualenvwrapper.sh" >> ~/.bashrc
```
and Finally:
```
source ~/.bashrc
```

Now we can create our new virtual environment, you can name it whatever you like, just make sure you can remember it, we'll use the name 'plotter':
```
mkvirtualenv plotter -p python3
```

Then we can use the `workon` command to change into our newly create virtual environment:
```
workon plotter
```

Now that we're in our virtual environment, you should see `(plotter)` on the left of your terminal prompt. Install the follow Python dependencies with `pip`:
```
pip3 install RPI.GPIO
pip3 install adafruit-blinka
pip3 install adafruit-circuitpython-motorkit
pip3 install wiringpi
pip3 install pigpio
pip3 install pigpio_encoder
```

Now that we have our Python dependencies in order, we can leave the virtual environment using the command:
```
deactivate
```

### Setting up Git

Git is an industry standard version control system, which is extremely useful for managing and working on software projects. Here is a [great guide for setting up git with a Github account](https://docs.github.com/en/free-pro-team@latest/github/getting-started-with-github/set-up-git). You should use SSH to clone and commit to repositories, and only ONE team member should connect their Github account with the Raspberry Pi git configuration.

Note: You'll have to install and setup git on every device you intend to work on, this includes generating SSH Keys, and adding them to the account.

Congratulations! Your Pi should have everything it needs to run your project!

## Next Steps

Now that you have your Pi set up, you can move on to [Working on the Pi](working_on_pi.md).
