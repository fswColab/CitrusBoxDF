# CitrusBox 1.0
***Date:*** *April 30, 2020*

 ***Author:*** *Alexandre Rebillard*
 ***Email:*** *haldrex.mail@gmail.com*

 ##### Feel free to contribute
 
CitrusBox is light weight virtual machine base on Debian 10 that gives an easy way to use the nolanlab/citrus R package and its user interface.
___



###Get started

##### 1. Get citrusbox's shared folder
First, with the host machine, be sure you can access the *smb://citrusbox/vault/* shared folder, username and password are both *'citrus'*. If not, you can find a lot of info about how (**mac:** https://www.techrepublic.com/article/how-to-connect-your-macos-device-to-an-smb-share/, **win:** https://www.techrepublic.com/article/how-to-connect-to-linux-samba-shares-from-windows-10/).


In case that the 'citrusbox' hostname is unreachable, you should try with ip address instead of hostname. eg: *smb://192.168.0.92/vault/*. You can get it with 'ip a' command on citrusbox's terminal.

##### 2. Place *.fcs* files in vault
Once you get connected to the vault, copy your *.fcs* files. It's recommanded to create folder for each analysis since citrus autodetect every siblings in the directory of the specified .fcs file.


##### 3. Login into citrusbox
Login with username *'citrus'* and password *'citrus'*. Open terminal and start a R shell, then import citrus and launch UI.

```R
lybrary('citrus')
citrus.launchUI()
```
It will prompt you to enter a file name. Enter *'/var/vault/[fcsfilename.fcs]'*.  Only specify a single file of the *.fcs* files' directory, citrus will autodetect siblings. 

##### 4. ENJOY
Once the *.fcs* files fully loaded, firefox will pop-up with the citrus UI.
More info on citrus package at https://github.com/nolanlab/citrus.

### VM info

##### General
	hostname: citrusbox
	Distibution: Debian 10
	Desktop environment: Mate
	Disk size: 25G (Dynamic allocation)
	R version: 3.5
	Last update: 2020-04-30

##### Users
	root (default password: "toor")
	citrus (default password: "citrus")

##### Smb user
	citrus (default password: "citrus")

##### Installed R packages
	foreach
	glmnet v2.0-16 (https://cran.r-project.org/src/contrib/Archive/glmnet/glmnet_2.0-16.tar.gz)
	pamr
	ggplot2
	survival
	BiocManager
	flowcore (via BiocManager)
	impute (via BiocManager)
	samr
	curl
	devtools
	brew
	shiny
	nolanlab/Rclusterpp (via github)
	nolanlab/citrus (via github)

Builded by Haldrex https://github.com/haldrex