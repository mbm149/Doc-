# Setups to remote in a Linux VirtualBox VM  from your local VS Code



<h2> Step 1 Install SSH on the VM </h2>  

-- On the VM
ip address (to find the VM's ip address)
sudo apt update
sudo apt install openssh-server 
sudo systemctl status ssh 

<h2> Step 2 Configure The VM </h2> 

Settings --> Network --> Advance --> Port Forwarding 

![Screenshot from 2023-01-18 11-30-50](https://user-images.githubusercontent.com/105382530/213265197-d38aa296-c039-4049-ab41-b6577b239463.png)

Plus(+) 
Name :
Protocol : TCP
Host IP : 127.0.0.1 
Host Port : 2222
Guest IP : (the IP from the VM) 
Guest Port : 22

![Screenshot from 2023-01-18 11-30-57](https://user-images.githubusercontent.com/105382530/213265086-20197cfe-39a7-4e4a-9627-f5e6edc1ed03.png)


<h2> Step 3 Install Remote SSH extension on VS Code </h2> 

![Screenshot from 2023-01-18 11-40-52](https://user-images.githubusercontent.com/105382530/213266726-176d7116-8ed3-4ee4-9901-176e74bb174c.png)

<h2> Step 4 Configure SSH file </h2> 

Ctrl + Shift + P (to open the Command Palette) and type open SSH configuration file 
![Screenshot from 2023-01-18 11-42-52](https://user-images.githubusercontent.com/105382530/213267262-7494c123-ffa5-4eb5-b755-46a7821855a5.png)

or click on this icon on the button left corner 

![Screenshot from 2023-01-18 11-42-22](https://user-images.githubusercontent.com/105382530/213268191-0bdb2457-469a-4ffa-ba0f-6a149acd28ec.png)

Inside the config file enter the VM details, and save the file
![Screenshot from 2023-01-18 11-50-20](https://user-images.githubusercontent.com/105382530/213268645-c8ed008d-5a95-4aef-8281-90fa92e2d164.png)

<h2> Step 5 Connect the VM to VS code </h2> 

Select the Remote Explorer icon, and now you will be able to see the Hostname

![Screenshot from 2023-01-18 12-01-35](https://user-images.githubusercontent.com/105382530/213270820-3d6a2ecf-e68f-4fd1-810c-e69ccf44a8df.png)

Click on the Hostname arrow to connect in the current Window

![Screenshot from 2023-01-18 12-08-47](https://user-images.githubusercontent.com/105382530/213272198-a0cfcb21-d8ad-4958-9581-059c65393cd8.png)


If your VM has a password, it will prompt to enter the VM password

![Screenshot from 2023-01-18 12-03-11](https://user-images.githubusercontent.com/105382530/213271480-60a9d84d-13c9-4a18-8178-de1a7556d4d0.png)


Then Now VS Code has established a connection with your VM and now you can use it as your enviroment 
![Screenshot from 2023-01-18 12-04-22](https://user-images.githubusercontent.com/105382530/213271456-81cdf585-3179-4f09-827e-b73e6dc37bdd.png)

(Side note: the VM needs to be running before you ssh into it) 




