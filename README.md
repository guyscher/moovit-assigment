*add disk on aws
lsblk

fdisk /dev/xvdf
mkfs.ext4 /dev/xvdf
mount /dev/xvdf /vlog/

apt install nodejs
apt install npm
npm install pm2 -g

pm2 start server.js

apt install nginx
cp nginx.conf /etc/nginx/nginx.conf
systemctl restart nginx

curl http://guy-lb-1827943115.eu-west-2.elb.amazonaws.com/