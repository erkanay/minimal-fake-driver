# Fake Device Driver

This is a minimalistic kernel module which written for learning purposes using C language. 
It conducts relation between non-exist [device driver](https://en.wikipedia.org/wiki/Device_driver) and user space.

## Build Route

First of all clone the repository
```{r, engine='bash', count_lines}
git clone https://github.com/erkanay/fake-driver.git
cd fake-driver
```
Then compile it with
```
make
```
Finally create a [character device file](http://www.tldp.org/LDP/lkmpg/2.4/html/c577.htm) in ```/dev```.
```{r, engine='bash', count_lines}
mknod /dev/fakedevice c 900 1
```
Check it out with
```
dmesg
```

### TODO 
 * Write a simple user application for it

