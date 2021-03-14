# https-cert
A self-signed pair of pem/cert files to quickly setup a webserver

# setup
````
sudo mkdir /etc/nginx/https-cert-tli
sudo curl -Lo /etc/nginx/https-cert-tli/tli_demo.pem https://raw.githubusercontent.com/TurboLabIt/https-cert/main/tli_demo.pem
sudo curl -Lo /etc/nginx/https-cert-tli/tli_demo.crt https://raw.githubusercontent.com/TurboLabIt/https-cert/main/tli_demo.crt
sudo chown www-data:www-data /etc/nginx/https-cert-tli -R
sudo chmod ug=rX,o= /etc/nginx/https-cert-tli -R
````

# server {}
````
ssl_certificate /etc/nginx/https-cert-tli/tli_demo.crt;
ssl_certificate_key /etc/nginx/https-cert-tli/tli_demo.pem;
````
