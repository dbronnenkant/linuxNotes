# Debian 9 Net Install
# Debian Backgound
https://wallup.net/linux-debian-9/
https://goo.gl/images/tL141f

# Install Additional Packages
su -
apt install sudo git vim apt-transport-https
vim /etc/sudoers
logout

# Upgrade Firefox
# https://linuxconfig.org/how-to-install-latest-firefox-browser-on-debian-9-stretch-linux
sudo wget -O FirefoxSetup.tar.bz2 "https://download.mozilla.org/?product=firefox-latest&os=linux64&lang=en-US"
sudo mkdir /opt/firefox
sudo tar xjf FirefoxSetup.tar.bz2 -C /opt/firefox/
sudo mv /usr/lib/firefox-esr/firefox-esr /usr/lib/firefox-esr/firefox-esr_orig
sudo ln -s /opt/firefox/firefox/firefox /usr/lib/firefox-esr/firefox-esr

# Install Sublime Text
sudo wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add
echo "deb https://download.sublimetext.com/ apt/stable/" | sudo tee /etc/apt/sources.list.d/sublime-text.list
echo "deb https://download.sublimetext.com/ apt/dev/" | sudo tee /etc/apt/sources.list.d/sublime-text.list
sudo apt update
sudo apt -y install sublime-text