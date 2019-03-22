# panasonic-hbtn
Panasonic Toughpad FZ-M1 Tablet Button driver for Linux

This driver enables the 'Rotation lock' and 'A' buttons on the FZ-M1.
This does not bind any functionality to the keys, but makes them available as X86Launch1 and X86Launch2.

## Usage
```bash
cd /usr/local/src/
git clone https://github.com/KaarelP2rtel/panasonic-hbtn.git

cd panasonic-hbtn
make all
make install

depmod -a
modprobe panasonic-hbtn
```
Then try out if those buttons are in working order.

Finally,
```bash
update-initramfs -u
```

Tested with FZ-M1 mk1 with Debian stretch with kernel 4.9.0-8-amd64.
