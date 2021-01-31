# master-publickey

1、root登陆

mkdir /root/.ssh && chmod 600 /root/.ssh && touch /root/.ssh/authorized_keys && chmod 700 /root/.ssh/authorized_keys
2、下载公钥，路径改成你github

wget -O /root/.ssh/authorized_keys --no-check-certificate https://github.com/TIDealHub/master-publickey/blob/main/id_rsa.pub

3、禁止密码登陆

sed -i 's/^#\?PasswordAuthentication yes/PasswordAuthentication no/' /etc/ssh/sshd_config


