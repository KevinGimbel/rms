# rms
### remove safely

`rms` is a command line utility that moves the file or folder to the /tmp/rms directory instead of deleting them directly so they can be restored if needed. On most operating systems the `/tmp/` directory is flushed so your files are only removed once the system reboots.

### Install
Clone the repo somewhere on your system, make the `rms` file executable and link it to a
place inside your path if it isn't already. You can see your path by executing `echo $PATH`.
```bash
$ cd some/path/on/your/system
$ git clone https://github.com/kevingimbel/rms
$ chmod +x rms
# Link into your PATH if it is not already.
$ (sudo) ln -s /home/kevin/apps/scripts/rms /usr/local/bin/
```

### Usage
Call `rms file.txt` to remove *file.txt*, call `rms recover file.txt` to recover it.

```bash
$ rms myfile.md

$ rms --usage
  --usage   | usage   | -u Display usage info
  --version | version | -v Show version
  --recover | recover | -r Recover a file from /tmp/rms
```
