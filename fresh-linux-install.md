Debian 9 Net Install
upgrade firefox: https://linuxconfig.org/how-to-install-latest-firefox-browser-on-debian-9-stretch-linux

su -
apt install sudo git vim
vim /etc/sudoers
logout
sudo wget -O FirefoxSetup.tar.bz2 "https://download.mozilla.org/?product=firefox-latest&os=linux64&lang=en-US"
sudo mkdir /opt/firefox
sudo tar xjf FirefoxSetup.tar.bz2 -C /opt/firefox/
sudo mv /usr/lib/firefox-esr/firefox-esr /usr/lib/firefox-esr/firefox-esr_orig
sudo ln -s /opt/firefox/firefox/firefox /usr/lib/firefox-esr/firefox-esr