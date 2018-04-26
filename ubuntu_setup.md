# Installing and setting up Ubuntu 18.04 LTS
> Dual boot with Windows 10 Professional on separate hard drives

## System settings

**System Information**

	manufacturer		PINNACLEMICRO
	product			P65_P67RGRERA
    os                      Windows 10 Professional

**System Enclosure**

	manufacturer		PINNACLEMICRO
	chassis type		Notebook

**Processor**

	manufacturer		Intel(R) Corporation
	model			Intel(R) Core(TM) i7-6700HQ CPU @ 2.60GHz
	clock speed		3100.0 MHz
    number of cores	        4 (max 4)
	number of threads       8 (max 8)
	codename                Skylake

**BIOS**

	vendor			American Megatrends Inc.
	version			1.05.15
	date			04/27/2016
	ROM size		5120 KB

**Baseboard**	

	vendor			PINNACLEMICRO
	model			P65_P67RGRERA

**Memory**

	location		Motherboard
	usage			System Memory
	max capacity		65536 MBytes
	max# of devices		4
    memory Type		DDR4
    memory Size		24 GBytes
    channels		Dual
    memory Frequency	1064.4 MHz (1:16)

**Graphics**

	Name			NVIDIA GeForce GTX 970M
	Board Manufacturer	Clevo
	Memory size		3 GB
	Memory type		GDDR5


# Installing Ubuntu 18.04 LTS

## Create an installation boot drive

## First steps following installation

1. After logging in for the first time, open a terminal and run the following commands (updating and upgrading should have occurred during the setup phase, but it's good to double-check this before proceeding)
    ```
    sudo apt update
    sudo apt upgrade
    ```
1. Enable the firewall (which is inactive by default) by issuing the following terminal command:
    ```
    sudo ufw enable
    ```
    OR
    install the firewall GUI using the following command
    ```
    sudo apt install gufw
    ```
    The firewall configuration utility should now be installed
1. It may be neccesary to update/install various drivers for your machine at this stage. This is going to be somewhat uncharted territory:
    - The following is from one user who had success installing Linux on a Clevo machine:
        > I followed this when installing.
        >    Afterwards, I removed gdm3 and installed both lightdm and NVIDI drivers:
        > ```
        > sudo apt install lightdm
        > sudo apt purge gdm3
        > sudo apt-get remove gdm3
        > sudo apt-get install nvidia-384
        > ```
    - Here is another site that describes some issues encountered with installing Ubuntu 16.06 on a Clevo P650RE latop: [link](http://forum.notebookreview.com/threads/clevo-p650re-running-ubuntu-16-06-stuck-nvidia-geforce-gtx-970m.794709/)


1. Remove unwanted apps
    - Amazon
    - Aisleriot Solitaire
    - GNOME Mahjongg
1. Download and install alternate web browsers.  This process is, unfortunately, still manual:
    - [Vivaldi](https://vivaldi.com/download/)
    - [Chrome](https://google.com/chrome/)
1. Open Vivaldi and 
    - import bookmarks (from flash drive, eg.)
    - customize default settings
        - Set Google as the default search engine and delete other search engine entries
1. Change the default applications in Ubunutu such that Vivaldi is the default browser
    

## Desktop environment (DE) setup

1. Install _GNOME Tweaks_ from the Ubuntu Software center. Spend some time customising the DE from within this tool once installed.

### Add GNOME extensions

In order to install GNOME extensions you need to first do the following:
1. Open a terminal and issue the following command:
    ```
    sudo apt install chrome-gnome-shell
    ```
2. Open Vivaldi and install the _GNOME Shell integration_ extension from the [Chrome webstore](https://chrome.google.com/webstore/search/GNOME)

You should now be able to search for and install GNOME extensions from within Vivaldi

List of extensions to install:
- [Extensions]()
    The Extensions extension allows the user to enable/disable other extensions and to access their settings in one singular extension. Extensions either sit next to your other icons and extensions in the panel or in the user drop-down menu.

    Redundancies aside, Extensions is a great way to gain easy access to all your extensions without the need to open up the GNOME Tweak Tool to do so.
- [Drop Down Terminal]()
- [Apt Update Indicator]()
    For distributions that utilize Apt as their package manager, such as Ubuntu or Debian, the Apt Update Indicator extension allows for a more streamlined update experience in GNOME.

    The extension settles into your top bar and notifies the user of updates waiting on their system. It also displays recently added repos, residual config files, files that are auto removable, and allows the user to manually check for updates all in one basic drop-down menu. 
- [Caffeine]()
    Caffeine is a utility extension that will prevent your Ubuntu Gnome from going to sleep mode. Sometimes, it is very disturbing when your OS goes into the sleep mode. To prevent this problem, this extension can be a good solution.
 - [Auto Move Windows]()
    Caffeine is a utility extension that will prevent your Ubuntu Gnome from going to sleep mode. Sometimes, it is very disturbing when your OS goes into the sleep mode. To prevent this problem, this extension can be a good solution.   
- [Clipboard Indicator]()
- [Dash to Dock]()
- [Workspaces to Dock]()
    This extension is almost same as Dash to Dock extension. Now, you can easily thumbnail all the activities overview into a dock on your Linux desktop.
- [User Themes]()
- [Refresh Wi-Fi Connections]()
    One minor annoyance in GNOME is that the Wi-Fi Networks dialog box does not have a refresh button on it when you are trying to connect to a new Wi-Fi network. Instead, it makes the user wait while the system automatically refreshes the list. Refresh Wifi Connections fixes this. It simply adds that desired refresh button to the dialog box, adding functionality that really should be included out of the box.
- [CPU Power Manager]()
- [Gno-Menu]()
- [Music Integration]()

### Install new themes

1. To install the _Cummunitheme_ Snap package, use the command below:
    ```
    sudo snap install communitheme
    ```

## Software setup

### Work apps

### Creative apps

### Play apps

- Clementine
- Gradio