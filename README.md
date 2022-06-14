# install-ruby-ubuntu

https://wiki.archlinux.org/title/RVM#RVM_uses_wrong_OpenSSL_version

https://rvm.io/

sudo apt update
sudo apt install git curl libssl-dev libreadline-dev zlib1g-dev autoconf bison build-essential libyaml-dev libreadline-dev libncurses5-dev libffi-dev libgdbm-dev

sudo apt install gcc g++ make
curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash -

curl -sL https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt update
sudo apt install yarn nodejs

sudo apt install postgresql postgresql-contrib libpq-dev -y
sudo wget https://www.openssl.org/source/openssl-1.1.1o.tar.gz

systemctl start postgresql
systemctl enable postgresql

sudo -i -u postgres psql
create role mudango_developer with SUPERUSER login password 12345678;

sudo add-apt-repository ppa:canonical-hwe-team/backport-iwlwifi
sudo apt-get update
sudo apt-get install backport-iwlwifi-dkms 

https://askubuntu.com/questions/1149116/intel-wifi-support-for-ax200-cyclone-peak


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

https://github.com/rbenv/rbenv

Agregar https://raw.githubusercontent.com/rubygems/rubygems/master/lib/rubygems/ssl_certs/rubygems.org/GlobalSignRootCA_R3.pem

a gem which rubygems sin el .rb


sudo wget -O /usr/local/ssl/cert.pem "https://curl.haxx.se/ca/cacert.pem" para solucionar problemas de certificado de open ssl
