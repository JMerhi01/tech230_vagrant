## Vagrant
Vagrant is a tool used for building and managing virtual machine environments in a single workflow. It is easy to use and focuses on automation. 

![Alt text](9e7d2afc-b331-4b89-ae05-67a9376a433e.jpg)

### Vagrant Commands
Note: vscode Bash Terminal is used until Vagrant initialises.

Note: This means up until vagrant ssh.


 `vagrant init` -  Used to get the Vagrant file

Example:
~~~
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64" 
end
~~~
`vagrant up` - Used to initiate the instructions in the Vagrant file

`vagrant ssh` - SSH is the protocol to access the VM

`sudo` - Gives admin rights

<!-- `apt-get` - Apt is the package manager

`update` - Download these packages

`upgrade` - Install these packages -->

` sudo apt-get update` - Uses apt pack manager to download updates

` sudo apt-get upgrade` - Uses apt pack manager to install updates

` vagrant reload` - Restarts the VM using any new config

`vagrant destroy` - Used to shut-down and delete the VM

`"ctrl c" or "q"` if locked out of terminal 
# 
### Vagrant Web Server SetUp
#### Setup Process: 

`sudo apt-get install nginx -y` - Installs nginx

`sudo systemctl start nginx` - Starts nginx

`sudo systemtcl status nginx` - Checks status of nginx

#### Add an IP address to the instructions:
Example
```
Vagrant.configure("2") do |config|
 config.vm.box = "ubuntu/xenial64" 
	config.vm.network "private_network", ip:"192.168.10.100"`
end
```
Restart the VM to apply changes using `vagrant reload` 