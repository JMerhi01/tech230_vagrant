# Vagrant

Vagrant is used to send very specific instructions, keep it consistent on a larger scale. 

![Alt text](9e7d2afc-b331-4b89-ae05-67a9376a433e.jpg)

In vs code, bash terminal: 

`vagrant init` - get the vagrant file, get rid of the green comments. 

Example: 

```
Vagrant.configure("2") do |config|
 
  config.vm.box = "ubuntu/xenial64" # This is the operating system
	
  
end
```

`vagrant up` - to sent the instructions to virtual box

`vagrant destroy` - shutdown and destroy the vm

`vagrant ssh` - protocol being used to access the vm

---

`sudo` = give me admin rights
`apt-get` = apt is the package manager, get them.
`update` = download these packages.

`upgrade` = installs these packages.

`sudo apt-get update` 

`sudo apt-get upgrade`

---

### Setting up a web server:

`sudo apt-get install nginx -y` Install nginx, confirmed y.

`sudo systemctl start nginx` Start the service

`sudo systemctl status nginx` Check the status of nginx

Add an IP address by going to instructions:

```jsx
Vagrant.configure("2") do |config|
 
  config.vm.box = "ubuntu/xenial64" # This is the operating system
	config.vm.network "private_network", ip:"192.168.10.100"
  
end
```

Restart the VM to apply changes:
`logout` - Leave
`vagrant reload` - Restart with new config

---

If you get locked out of terminal :

ctrl c or q

`vagrant ssh` - go back in