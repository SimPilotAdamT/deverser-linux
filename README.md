# Déverser Linux
Simple GNU/Linux script to dump onboard SHSH with a valid Generator for iOS devices

## What is this/What does this do

Déverser Linux is a simple GNU/Linux script to dump onboard SHSH from iOS devices and convert it to useable SHSH which contains a generator! This is different to just dumping 'ApTicket.der' from the device's filesystem, like some jailbreaks such as Unc0ver allow for, as the 'ApTicket.der' doesn't contain the generator for the ApNonce it is valid for, meaning restores/downgrades using converted ApTicket.der's are not possible unless you know the generator.

This script simply dumps iBoot from /dev/rdisk1 on the device, copies the dump to your computer then converts the dump to valid SHSH using [img4tool](https://github.com/tihmstar/img4tool). This is all possible and easy to do manually, this script just allows for those who are less comfortable with the command line or less knowledgeable to have a simple method to dump onboard SHSH.

Even though this script will give you valid SHSH for the currently installed iOS version on your device, you are still limited by signed SEP compatiblity when restoring/downgrading with this dumped SHSH, so please bare that in mind when using this script.

Déverser is just a small project I made in 2 hours while I was bored, if it's useful to someone then that's great, I hope you enjoy it! Don't expect fast support or any features to be added to this script, it works as-is and that's all I care about.

## Requirements

* A machine with a distro with [img4tool](https://github.com/tihmstar/img4tool) and openssh. The following is needed if you don't have img4tool and you want Déverser to automatically install img4tool:
  * Buildsystem
    * autoconf
    * automake
    * libtool
    * pkg-config
  * Externel
    * openssl
    * [libplist](https://github.com/libimobiledevice/libplist)
  * Other (but no less important)
    * [libgeneral](https://github.com/tihmstar/libgeneral)

* A jailbroken device with OpenSSH installed (Specific jailbreak doesn't matter, E.G checkra1n, Unc0ver, chimera, etc)

## Usage

1. Run `git clone https://github.com/SimPilotAdamT/deverser-linux.git`, then `cd deverser-linux`.
2. Run `chmod +x deverser-linux.sh`.
3. Run `bash ./deverser-linux.sh`.
4. Follow the on screen instructions.
5. If nothing has gone wrong, the SHSH2 blobs for the latest version of iOS will be in the deverser-linux folder in your filesystem.

## Issues/Bugs/Fixes/Improvements

If you have any bugs/issues open an issue [here](https://github.com/SimPilotAdamT/deverser-linux/issues) with details about your macOS machine (OS version, other basic info), iOS device (iOS version, jailbreak, etc) and details about what is not working.

Any ideas/fixes/improvements can be sent in a pull request [here](https://github.com/SimPilotAdamT/deverser-linux/pulls).

## Credits

Adam (Me) - (No Twitter acc yet ;-;) - For modifying Matty's script to work on GNU/Linux

Matty - [@moski_dev](https://twitter.com/moski_dev) - For writing the original script for MacOS

Tihmstar - [@tihmstar](https://twitter.com/tihmstar) - For creating img4tool
