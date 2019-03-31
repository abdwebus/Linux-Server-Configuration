# Linux Server Configuration

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

### grader user's SSH key

-----BEGIN OPENSSH PRIVATE KEY-----
b3BlbnNzaC1rZXktdjEAAAAABG5vbmUAAAAEbm9uZQAAAAAAAAABAAABFwAAAAdzc2gtcn
NhAAAAAwEAAQAAAQEA4zWNC0uAGaDSNc3yLxUM+kHTc5OQWC3dAum6iw9rnwRjdgm5zOQV
wW39N8oB1CHTAtxxVrtayDkHdZYxktBtC6CHPIx0gTiF1U6JSfbDt59Ts+bI8zlWYKJuMh
mUQbZFXvoB2cdr3QjJP1k77PDKVCnQWb2ZbxJ++49cRs5VaGN/U3RP845QKrsdG4fyNW6G
Rfwpxh7YonpgX4UuyHMJgB3tg+L+hESwv8Lwtxxe8wRUbih3JBpNlzYolDJg6usAsgiMKi
O8pj/BuljuVIjCBI9GFY9ABojqq2/IgPjwaaifdwh1kAT/Vbw6/nvdQxgvcoY5lRb6QQtE
BCVBb1ypQQAAA9iYz60dmM+tHQAAAAdzc2gtcnNhAAABAQDjNY0LS4AZoNI1zfIvFQz6Qd
Nzk5BYLd0C6bqLD2ufBGN2CbnM5BXBbf03ygHUIdMC3HFWu1rIOQd1ljGS0G0LoIc8jHSB
OIXVTolJ9sO3n1Oz5sjzOVZgom4yGZRBtkVe+gHZx2vdCMk/WTvs8MpUKdBZvZlvEn77j1
xGzlVoY39TdE/zjlAqux0bh/I1boZF/CnGHtiiemBfhS7IcwmAHe2D4v6ERLC/wvC3HF7z
BFRuKHckGk2XNiiUMmDq6wCyCIwqI7ymP8G6WO5UiMIEj0YVj0AGiOqrb8iA+PBpqJ93CH
WQBP9VvDr+e91DGC9yhjmVFvpBC0QEJUFvXKlBAAAAAwEAAQAAAQAXujPshgnuozjQnZ05
BX3BdLZcT4C3dLKr5zSv6QBYLuEkJofcucT72jyjYtkmChI7LkI3yIEGf84jnXe32URJ/o
2g6RoRlJGFYRo9OyPdPSpEk0lQ/R/kH5JacQlmg15jOMCQuZ6uCojZsLvtVogKmgNEG+S2
ELxqEOKWEl4g9HClSl41Uw3/P7i0j2vkuhkhLoU5pOwtF9naeBoczl/SJZNUTrlPwrSE4U
60V0hhbCtOxPjts+LD3OOTbP/ihslbVLDfnthQafAUWoVszrqyruV/as/lK1+NOYCnB8vK
/emMx/+pQz1nPJoqigyLGyxbN21/IaoQgWb3nvc0cnkBAAAAgQDcPZgIV7M12RHJ5edPy3
yzJGbLMNLJiwEGqDYN+r4SPEu4LyJR8oKOdK+Wy/pt804wSt1LKJiYfMk0VmUdsVu1vhV4
MGPgE83hDvvQOzlz/ZU00nb+Tw0LZcaOuGL5HojHPYaM20wu/NghLSN/9fOGIY6ewl9CVk
RXrpdYnZSm5AAAAIEA+TLL9atBvl6DwevGBjMFIM8MGjjgc31pqxFQGlqwQy0ePNfYD66C
rM89pq0CIxquwhfzpPhGtHoAu0tvGMlqqYZdVn/6oC6hUVL9EJ0HlK2L4J7kmjiGQfxD0X
P+ift8YngsveLcrILgZlM1bL/gB/6mOOXQ9PD/9TwkyCTOMykAAACBAOlpHFO17GOg6Wfk
ywgh6DRqiEizUQeOi+KNuQXhsr3tDiXnXXZyjyJT8yA72gUOxoHrEV9QARCrgqbgTnRJWZ
fge59vOIZGwi4JTNZpGQ9c8Dz6xQGsEvDHXupQJAncYQitaDG4HvKGejnYJzQF2SpbC9CP
ld+G+YXNnXgdweBZAAAAIGFiZWQtbWFjQEFiZWRzLU1hY0Jvb2stUHJvLmxvY2FsAQI=
-----END OPENSSH PRIVATE KEY-----

### Entry to login as grader

Assumming SSH key is saved in ```udacityGrader``` <br />
```ssh grader@34.210.67.78 -p2200 -i ~/.ssh/udacityGrader```



## Challenges

Login functionality won't work, google sign in button won't appear. Apache error.log doesn't show any error.
However, the browser console show below error
```
[Error] The source list for Content Security Policy directive 'script-src' contains an invalid source: ''strict-dynamic''. It will be ignored.
[Error] The source list for Content Security Policy directive 'script-src' contains an invalid source: ''strict-dynamic''. It will be ignored.
https://plus.google.com/_/widget/render/signin?usegapi=1&scope=openid+email&clientid=1006081047827-0cu5n09g26engs2feit5te0v9eov84fm.apps.googleusercontent.com&redirecturi=postmessage&accesstype=offline&cookiepolicy=single_host_origin&approvalprompt=force&origin=http://ec2-34-210-67-78.us-west-2.compute.amazonaws.com&url=http://ec2-34-210-67-78.us-west-2.compute.amazonaws.com/login&gsrc=3p&ic=1&jsh=m;/_/scs/apps-static/_/js/k%3Doz.gapi.en_US.k075T-KPfhg.O/am%3DwQ/rt%3Dj/d%3D1/rs%3DAGLTcCPwAoUJo6Gd1t5JO7oWH71meRocYw/m%3D__features__#_methods=onPlusOne%2C_ready%2*C_close%2C_open%2C_resizeMe%2C_renderstart%2Concircled%2Cdrefresh%2Cerefresh%2Conauth%2Conload&id=I0_1554071445290&_gfid=I0_1554071445290&parent=http%3A%2F%2Fec2-34-210-67-78.us-west-2.compute.amazonaws.com&pfname=&rpctoken=38951306
[Error] Failed to load resource: the server responded with a status of 404 () (signin, line 0)
```

### Google configurations

![](images/image1.png)
![](images/image2.png)

## Reference Resources
* [How To Deploy a Flask Application on an Ubuntu VPS](https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps)
* [How To Secure PostgreSQL on an Ubuntu VP](https://www.digitalocean.com/community/tutorials/how-to-secure-postgresql-on-an-ubuntu-vps)
* [How do I change my timezone to UTC/GMT?](https://askubuntu.com/questions/138423/how-do-i-change-my-timezone-to-utc-gmt/138442)
* [How To Run Your Python Code Off of Amazon Web Services](https://www.youtube.com/watch?v=WE303yFWfV4)
* [Changing the SSH Port for Your Linux Server](https://ca.godaddy.com/help/changing-the-ssh-port-for-your-linux-server-7306)
