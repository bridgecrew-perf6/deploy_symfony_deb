# Symfony deb packet

## Description

This code creates symfony test app with all depends,  interactive migrations with MySQL, it uses symlynk_deploy method, it also installs: 
- precompiled nginx with conf
- php8.1
- mysql-server
- symfony


## Requrements to build 
  - Ubuntu OS 21.10 (it will work with earlier versions)
  - dh-make 
  - devscripts
  - mysql-server
  - (>=) gcc 10.3
  - (>=) g++ 10.3 
  - php repo (php8.1)
  
  

To add php repo

Run
```
sudo apt install software-properties-common
```
```
sudo add-apt-repository ppa:ondrej/php  
```


# How to

## Method 1

### Build deb
1. Clone repo
2. Check files owner, if it isn't your user fix it
3. Navigate in directory test-symfony/debian
4. Build deb 

```
debuild -b
```
If all is ok, deb will be built outside test-symfony/

### Install deb
Run
```
sudo apt install ./package.deb
```

### Test

Test in your browser  http://yourip:80

## Method 2

1. Clone repo
2. install prepared deb  test-symfony_1.9.1-ubuntuubuntu1_amd64.deb

```
sudo apt install ./package.deb
```

## License
GNU GPL v3