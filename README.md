# FileMakerServer-LetsEncrypt-Ubuntu-Nginx

A bash script for fetching and renewing Let's Encrypt (certbot) certificates for FileMaker Server running nginx on Ubuntu 20.

### Initial Setup Instructions:

1. Setup Ubuntu + install FMS (must be 19.5.1 or later for nginx)
2. Install `sudo apt install certbot`
3. download `wget https://raw.githubusercontent.com/nickorr/FileMakerServer-LetsEncrypt-Ubuntu-Nginx/main/get-ssl.sh`
4. add execution `chmod +x ./get-ssl.sh`
5. edit content of script `vi ./get-ssl.sh`
6. run `sudo ./get-ssl.sh`

### Renewal Setup Instructions:

1. download `wget https://raw.githubusercontent.com/nickorr/FileMakerServer-LetsEncrypt-Ubuntu-Nginx/main/get-ssl.sh`
2. add execution `chmod +x ./renew-cert.sh`
3. edit content of script `vi ./renew-cert.sh` (only fms usr/pwd edit needed)
4. run `sudo ./renew-cert.sh`

### Restart FM service

`sudo service fmshelper stop`

`sudo service fmshelper start`

## TODO

Add instructions for automating.
Some error checking would be nice.
Needs to have a secure way of storing the admin account details.
