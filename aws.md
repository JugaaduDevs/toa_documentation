# How to login

1. Copy aws.pem file in a folder of your choosing
2. Run the below SSH Command to connect 

 ` ssh -i ~/.ssh/aws.pem ubuntu@ec2-13-244-118-121.af-south-1.compute.amazonaws.com`

3. If you want create alias (Linux and Mac), open your .bashrc or .zshrc files and add the following to it

	`alias aws="ssh -i "~/.ssh/aws.pem" ubuntu@ec2-13-244-118-121.af-south-1.compute.amazonaws.com"
	`

# Where the project is located ?

Location: `~/backend/toi-api-ts`

# How to update the code

Use git pull to update the code in the project. All SSH keys and agents are already setup.

# How to check logs

STDOUT logs: /var/log/toi/stdout.log <br>
STDERR logs: /var/log/toi/sterr.log

# How to start/stop/restart nodejs

Start: sudo service toi start <br>
Stop: sudo service toi stop <br>
Restart: sudo service toi restart

Service config: vim /etc/systemd/system/toi.service

If you change service config, run the below command
 `sudo systemctl daemon-reload`