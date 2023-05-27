# Set a Linux remote server

How to connect from a macbook pro to a home linux machine?
We'll be exploring this via ssh. My linux machine is an Ubuntu LTS 22.03 and I'll be using my macbook pro OS Sierra.
# 1. Connect to a linux machine
This steps will help you to connect to your linux machine from a macbook pro via SSH.
## 1.1 Steps in Linux machine
First of all, see if you have any ubuntu updates and update: ```sudo apt update```

Now download <b>openssh-server</b> ```sudo apt openssh-server```

Check if its running with the command ```sudo systemctl status ssh```

IMAGE

If you want to stop/start/restart ssh just use ```sudo systemctl <command> ssh``` 
and replace command with one of the options mentioned.

Get the IP address with the command ```sudo ip a```

IMAGE

What you'll need from this linux machine:
- IP address
- user and password (the same when you start session in the linux machine)
## 1.2 Steps in Macbook pro


# 2. Connection completely remote
First, be sure that you were able to connect to the linux machine following previous steps (this is a must if both machines are reachable, e.g. both machines are connected to the same network). 

Now, in order to connect from any place outside from your network (e.g. you are in a cafe, university, etc.) you must do some extra steps. These steps involve working
mostly with the router, making static IPs, have a domain name for your home network, and others.

### 2.1 Port forwarding
The first step is port forwarding. You must allow your router to receive SSH connections and redirect them to your linux machine. This can be done ...
