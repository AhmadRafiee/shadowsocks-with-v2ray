- change domain name
- change configuration file
- change user:group all files
- client install tools



### install certbot on ubuntu 20.04
```bash
sudo apt-add-repository ppa:certbot/certbot
apt update
apt install certbot -y
certbot --version
```

### create certificate with certbot command.
before creating a certificate you need to set DNS records for the domain name
```bash
certbot certonly --standalone --preferred-challenges http --non-interactive --agree-tos --email <YOUR_EMAIN_ADDRESS> -d <DOMAIN_NAME>
```
