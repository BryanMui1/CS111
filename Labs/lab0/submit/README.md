# A Kernel Seedling
**Proc Count is a Linux Kernel module that counts the number of currently running processes/counts that run on the machine**

### What is /proc and why do I need it?  
/proc is intended as a directory that allows acess to basic processor and system information!  
there are similar processes to count that allows to view other system information


## Building
+ first cd to the correct directory where the proc plugin was downloaded
```shell
cd 'the/directory/you/downloaded'
```
+ then run the make command
```shell
make
```
The command should execute and create a proc_count.ko file

## Running
+ to run the plugin, you will need sudo access to build the module  
+ build the module using the following command:
```shell
sudo insmodule proc_count.ko
```
To check if the module is loaded, run:
```shell
lsmod
```
and proc_count should be one of the listed kernels 

## Execute proc_count
To execute proc_count run the following: 
```shell
cat /proc/count
```

## Cleaning Up
+ To remove the plugin from modules, run the following 
```shell
sudo rmmod proc_count
```

## Testing
+ The kernel module directory also comes with a testing feature. To run the unit-tests, python must be installed, proc_count must not be loaded into the kernel, then run the following command:
```python
python -m unittest
```
If everything is working propely, then there should be some sort of string output of 'OK' indicating that all tests were passed

Report which kernel release version you tested your module on
(hint: use `uname`, check for options with `man uname`).
It should match release numbers as seen on https://www.kernel.org/.

To test the current kernel module(for trouble shooting purposes), run
```shell
uname -r -s -v
```
TODO: kernel ver?