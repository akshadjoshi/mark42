# SSH_KEY_ON_BOX

dropping an SSH key and using SSH to access the box/machine

make a dir name - .ssh(in the home folder of box)
```bash
 mkdir .ssh
 vi authorized_keys #if the reverse shell is misbehaving can echo your key
 echo 'contents of .pub file' >> authorized_keys
```

****** drop/create an ssh key ******* (type the following command on your terminal)
```bash
 ssh-keygen -f <file name>  			   # (-i to use key)
 ls 

 cat <file name>                     # (it will be with the extention of .pub)
```
'paste the file contents on the box in **authorized_keys** file created earlier'
> *on our terminal*
```bash
 chomd 600 <file name>  # (this is the private key) 

 ssh -i <file name> user@<machine/box IP>

```

Note : 
1. Always make the file under the name of 'authorized_keys' on the box/machine or else it won't work.
2. Remember to give the correct permission number for execution.
3. If you place the private key i.e id_rsa in your .ssh dir you can login without -i switch 
<!-- https://phoenixnap.com/kb/ssh-permission-denied-publickey#:~:text=If%20you%20want%20to%20use,login%20in%20the%20sshd_config%20file.&text=In%20the%20file%2C%20find%20the,disable%20it%20by%20adding%20no%20. -->




