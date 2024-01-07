# nginx-stream-install

this repo helps start nginx with stream module

first install some dependencys

```
sudo apt-get install build-essential libpcre3 libpcre3-dev zlib1g zlib1g-dev libssl-dev
```

after that choose vers and download. im going with 1.24

```
wget https://nginx.org/download/nginx-1.24.0.tar.gz
tar -xzvf nginx-1.24.0.tar.gz
cd nginx-1.24.0/
```

configure and make

```
./configure --with-stream
make
sudo make install
```

final configuration is show the correct nginx path. because this method install nginx /usr/local/nginx so you must show in the .basrc

```
echo 'PATH=$PATH:/usr/local/nginx/sbin/' > ~/.basrc
```

now you can use nginx with stream module.
