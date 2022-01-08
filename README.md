# myubuntu
My Own Ubuntu Base Box in Vagrant

## creation of box from an existing vm

vagrant init hashicorp/precise64
vagrant up
Install all required softwares
sudo apt-get clean
sudo dd if=/dev/zero of=/EMPTY bs=1M
sudo rm -f /EMPTY
cat /dev/null > ~/.bash_history && history -c && exit
vagrant package --output mynew.box

## using the new box
vagrant box add mynewbox mynew.box
vagrant destroy
rm Vagrantfile
vagrant init mynewbox


