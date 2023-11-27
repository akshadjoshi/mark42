
**TO MAKE REVERSE SHELL INTERACTIVE** 

>RUN THESE ON THE REVERSE SHELL OBTAINED


# python3, python2 to know if the mac has python installed or not

```bash
which python
# OR
which python3
```
## python3
```bash
python3 -c 'import pty;pty.spawn("/bin/bash")'
```
## python
```bash

python -c 'import pty;pty.spawn("/bin/bash")' 
```

PRESS **CTRL + Z** 

(lil bit counter intuitive)(that ctrl z will force the netcat listner to go in background basically the reverseshell window will go behind and your terminal window will come upfront to put the next commands required)


```bash
stty raw -echo; fg
```
**PRESS ENTER TWICE** TO GET BACK # (your rc will be interative)

command to **specify the rows & columns of the reverse shell**

```bash
export SHELL=bash
```
```bash
stty rows 50 columns 211
```
**or**

```bash
stty rows 81 columns 87 #(give this command on the reverse shell so obtained)
```

```bash
export TERM=xterm-256color
```
****

## DON'T HAVE PYTHON ON THE REVERSE SHELL OR MAC SO OBTAINED USE THIS

```bash
script -q /dev/null bash
```
rest everything will be the same 

>CTRL Z 

and then 

>stty raw -echo; fg

>PRESS 'ENTER' TWICE TO GET BACK


Note: don't forget to set environment (if you use script cmd) 
```bash
export TERM=xterm-256color
```
#### pts vs tty

pty - fake terminal (get this when take ssh connection)

tty - terminal tag


## ZSH

### Python 3

```bash
python3 -c 'import pty;pty.spawn("/bin/bash")'
```

### Python 2
```bash
python -c 'import pty;pty.spawn("/bin/bash")'
```

>Press CTRL + Z

- Print current terminal settings

```bash
stty -a | head -n1 | cut -d ';' -f 2-3 | cut -b2- | sed 's/;  /\n/'
```

- Switch to raw mode and resume the shell

```bash
stty raw -echo; fg
```

- Type **'reset'** and press **CTRL + D**

  Setting specific environment variables for SHELL, TERM, and PATH.

```bash
export SHELL=bash
export TERM=xterm-256color
```

- Set terminal rows and columns **(Replace <rows> and <columns> with your terminal dimensions)**

```bash
stty rows 37 columns 146
```

- Start an interactive bash shell

```bash
bash -i
```

- Additional environment configurations and PS1 assignment

```bash
export PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
export TERM=xterm
export SHELL=bash
cat /etc/profile; cat /etc/bashrc; cat ~/.bash_profile; cat ~/.bashrc; cat ~/.bash_logout; env; set
export PS1='[\u@\h \W]\$ '
```
