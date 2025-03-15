# Server-setup

SSL for single site

sudo add-apt-repository ppa:certbot/certbot
sudo apt update
sudo apt install python3-certbot-nginx
sudo certbot --nginx -d site.name


SSL For Multi-tenent


sudo apt install snapd
sudo snap install core; sudo snap refresh core
sudo apt-get remove certbot
sudo snap install --classic certbot
sudo ln -s /snap/bin/certbot /usr/bin/certbot
sudo certbot --nginx
sudo certbot renew --dry-run
