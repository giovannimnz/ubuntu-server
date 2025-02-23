cd ~

sudo rm -rf ubuntu-config

git clone https://github.com/giovannimnz/nodes.git

sudo apt install iptables iptables-persistent -y

cd /home/ubuntu/nodes/iptables

sudo iptables-restore < iptables-backup-v4.conf

sudo ip6tables-restore < iptables-backup-v6.conf

sudo netfilter-persistent save

sudo netfilter-persistent reload

