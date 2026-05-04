# ftp-server-mnager
A ubuntu FTP server manager that uses vsftpd.

## How to install
### The normal way
You can directly download the .deb file:
```bash
curl -L https://github.com/Mehran-user/ftp-server-mnager/releases/download/release/ftp-server-mnager.deb -o ftp-server-mnager.deb
```
Then, install it:
```bash
sudo apt update
sudo apt install ./ftp-server-mnager.deb
```

### Building from source
Make a directory:
```bash
mkdir ftp-server-mnager
cd ftp-server-mnager
```

Clone this repo (you may want to install git):
```bash
git clone https://github.com/Mehran-user/ftp-server-mnager.git .
```

Package the deb using dpkg:
```bash
cd ../
dpkg-deb --build ftp-server-mnager
```

Install the deb:
```bash
sudo apt update
sudo apt install ./ftp-server-mnager.deb
```

(Optional) Delete the directory (**WARNING**: DELETION):
```bash
cd ../
rm -r ftp-server-mnager
```

### Manually adding the files
cd into downloads:
```bash
mkdir ~/Downloads # Most servers don't include a downloads folder
cd ~/Downloads
```

Download the files:
```bash
curl -L https://raw.githubusercontent.com/Mehran-user/ftp-server-mnager/refs/heads/main/usr/bin/ftp-installer -o ftp-installer
curl -L https://raw.githubusercontent.com/Mehran-user/ftp-server-mnager/refs/heads/main/usr/bin/change-ftp-users -o change-ftp-users
```

Move the files into /usr/bin/:
```bash
sudo mv ftp-installer /usr/bin/ftp-installer
sudo mv change-ftp-users /usr/bin/change-ftp-users
```

Make each file executable:
```bash
sudo chmod +x /usr/bin/ftp-installer
sudo chmod +x /usr/bin/change-ftp-users
```

(Optional) Remove Downloads directory if you're not using it (**WARNING:** DELETION):
```bash
rm -r ~/Downloads
```

## Tests
This tool has been tested to work on Ubuntu 26.04 LTS (GNU/Linux 7.0.0-15-generic x86_64) in a Virtual Machine (QEMU/KVM).

## Vibe coding disclosure
This tool has been coded by [ChatGPT](https://chatgpt.com), with a programmer with knowledge of very basic bash syntax and linux (ubuntu) commands.
