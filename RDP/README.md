`Run these Commands in GC Shell`
```
wget -O kali.sh https://bit.ly/3YdzRyF > /dev/null 2>&1

chmod +x kali.sh

./kali.sh
```

`Run These in RPD Kali machine`
```
vim /etc/apt/sources.list
deb http://http.kali.org/kali kali-rolling main contrib non-free 
deb-src http://http.kali.org/kali kali-rolling main contrib non-free
```

```
sudo su
gpg --keyserver keyserver.ubuntu.com --recv-key 7D8D0BF6
gpg --fingerprint 7D8D0BF6
gpg -a --export 7D8D0BF6 | apt-key add -
apt update
```
