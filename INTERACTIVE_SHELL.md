## netcat 

**HOW TO MAKE REVERSE SHELL INTERACTIVE** 

>RUN THESE ON THE REVERSE SHELL OBTAINED 

```bash
which python #(or python3, python2 to know if the mac has python installed or not)
```
```bash
python3 -c 'import pty;pty.spawn("/bin/bash")' #(the command will change depending on the python version)
python -c 'import pty;pty.spawn("/bin/bash")' 
```

**CTRL + Z** (lil bit counter intuitive)(that ctrl z will force the netcat listner to go in background basically the reverseshell window will go behind and your terminal window will come upfront to put the next commands required)


```bash
stty raw -echo; fg
```
PRESS 'ENTER' TWICE TO GET BACK #(your rc will be interative)

#can give the bellow command to specify the rows & columns of the reverse shell

```bash
stty rows 81 columns 87 #(give this command on the reverse shell so obtained) 
```
#IF YOU **DONT HAVE PYTHON** ON THE REVERSE SHELL OR MAC SO OBTAINED USE THIS

```bash
script -q /dev/null bash
```
rest everthing will be the same 

>CTRL Z 

and then 

>stty raw -echo; fg

>PRESS 'ENTER' TWICE TO GET BACK


Note: don't forget to set environment (if you use script cmd) 
```bash
export TERM=xterm-256color
```
