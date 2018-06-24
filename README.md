This QEMU patch introduces irix/solaris userland emulation. It currently runs
only under linux (though BSD support would probably be feasable).

### compiling

Configure QEMU for irix/solaris userland emulation and compile (see the original
QEMU README for further instructions):

```
configure --target-list=irix-linux-user,irixn32-linux-user,irix64-linux-user,solaris-linux-user
make && make install
```

### using

I recommend using binfmt. I have prepared some scripts for this which you can
obtain from my qemu-irix-helpers repository at github. Adapt the wrapper scripts
to your setup and install them somewhere in your executable path. Activate them
with the binfmt install scripts.

Now you should be able to directly execute irix/solaris binaries from the shell.
As a rather simple test, try:

```
<target rootfs>/bin/ls
```

send bug reports, fixes etc to Kai-Uwe Bloem  (<derkub@gmail.com>)
