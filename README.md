# install-ruby-ubuntu

https://wiki.archlinux.org/title/RVM#RVM_uses_wrong_OpenSSL_version

https://rvm.io/


sudo wget https://www.openssl.org/source/openssl-1.1.1o.tar.gz

sudo tar -xf openssl-1.1.1o.tar.gz

cd openssl-1.1.1o

sudo ./config --prefix=/usr/local/ssl --openssldir=/usr/local/ssl shared zlib

sudo make
sudo make test
sudo make install

sudo vi /etc/ld.so.conf.d/openssl-1.1.1o.conf

/usr/local/ssl/lib

sudo ldconfig -v


sudo mv /usr/bin/c_rehash /usr/bin/c_rehash.backup
sudo mv /usr/bin/openssl /usr/bin/openssl.backup

sudo open /etc/environment

:/usr/local/ssl/bin"

source /etc/environment


Agregar https://raw.githubusercontent.com/rubygems/rubygems/master/lib/rubygems/ssl_certs/rubygems.org/GlobalSignRootCA_R3.pem

a gem which rubygems sin el .rb


sudo wget -O /usr/local/ssl/cert.pem "https://curl.haxx.se/ca/cacert.pem" para solucionar problemas de certificado de open ssl
