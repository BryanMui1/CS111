# recommended setup
+ this allows you to not worry about using the virtualbox ui

sudo systemctl start (enable) sshd

tcp 22 -> 8022

ssh 127.0.0.1 -> 8022

scp

## the task
/proc/count
+ needs to be a kernel module

cat /proc/count will allow you to see what tasks is running

## commands
insmod /proc/count  
rmmod proc_count

seq_printf -> prints to the stdout cmdline or smthin like that


**make sure you test all the corner cases!**  
you will have to learn how to write your own tests

