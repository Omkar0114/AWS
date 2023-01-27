# Deploying a Golang Application on AWS EC2
<div>
<img align="center" src="https://github.com/Omkar0114/AWS/blob/main/images/instance.png">
</div>


### Testing the project locally

1. Clone this project
```
git clone https://github.com/Omkar0114/AWS.git
```
2. Open your terminal
go inside your cloned project directory using `cd`
Run following command:
```
go run main.go
```
3. Initialise and start the project
Open your browser on 
```
localhost:8080
```

### Set up an AWS EC2 instance

1. Create an IAM user & login to your AWS Console
    - Access Type - Password
    - Permissions - Admin
2. Create an EC2 instance
    - Select an OS image - Ubuntu
    - Create a new key pair & download `.pem` file
    - Instance type - t2.micro
3. Connecting to the instance using ssh
```
ssh -i instance.pem ubunutu@<IP_ADDRESS>
```

### Configuring Ubuntu on remote VM

1. Updating the outdated packages and dependencies
```
sudo apt update
```
2. Install Git - [Guide by DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-install-git-on-ubuntu-22-04)

### Deploying the project on AWS

1. Clone this project in the remote VM
```
git clone https://github.com/Omkar0114/AWS.git
```
2. Open your terminal
go inside your cloned project directory using `cd`
Run following command:
You need to install golang first, on the Remote VM
To install golang, follow this [guide](https://golang.org/doc/install)
Or you can use this command to install golang on Ubuntu
```
sudo apt install golang-go
```
To check if golang is installed or not, run this command
```
go version
```
Now run this command to run the project
```
go run main.go
```
3. Initialise and start the project
Open your browser on 
```
alloted IPv4 address of EC2 instance:8080
```
> NOTE - We will have to edit the **inbound rules** in the security group of our EC2, in order to allow traffic from our particular port

### Project is deployed on AWS 🎉

<div>
<img align="center" src="https://github.com/Omkar0114/AWS/blob/main/images/frontend.png">
</div>
