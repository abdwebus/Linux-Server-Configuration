# Linux Server Configuration

One of the Udacity project for nanodegree full stack web developer program.

## IP Address and SSH

* IP Address: 34.210.67.78
* SSH port: 2200

## URL for the website

* URL: http://ec2-34-210-67-78.us-west-2.compute.amazonaws.com
* Public IP: 34.210.67.78

## Summary of the changes made

* Updated all currently installed packages
* Changed SSH port from 22 to 2200
* Updated Amazon lighsail firewall to allow port 2200 and NTP
* Created grader user
* Gave ```grader``` permission to ```sudo```
* Created an SSH key pair for grader using the ```ssh-keygen```
* Updated the local timezone to UTC
* Installed and configured Apache to serve a Python3 mod_wsgi
* Installed and configured PostgreSQL
* Verified that remote connection is not allowed.
* Created a database user ```catalog```
* Assigned limited permissions
* Installed ```git```
* Cloned Item Catalog project to the server
* Updated console.cloud.google account with the new information


## Notes to Reviewer

Assumming SSH key is saved in ```udacityGrader``` <br />
```ssh grader@34.210.67.78 -p2200 -i ~/.ssh/udacityGrader```


## Reference Resources
* [How To Deploy a Flask Application on an Ubuntu VPS](https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps)
* [How To Secure PostgreSQL on an Ubuntu VP](https://www.digitalocean.com/community/tutorials/how-to-secure-postgresql-on-an-ubuntu-vps)
* [How do I change my timezone to UTC/GMT?](https://askubuntu.com/questions/138423/how-do-i-change-my-timezone-to-utc-gmt/138442)
* [How To Run Your Python Code Off of Amazon Web Services](https://www.youtube.com/watch?v=WE303yFWfV4)
* [Changing the SSH Port for Your Linux Server](https://ca.godaddy.com/help/changing-the-ssh-port-for-your-linux-server-7306)
