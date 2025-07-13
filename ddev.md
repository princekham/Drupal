### Ddev on my Raspberry Pi 4

#### Installing Ddev
- Install Docker first; I found my RaspberryPi already had Docker
- Install Ddev (https://ddev.readthedocs.io/en/stable/users/install/ddev-installation/)

```
# Add DDEV’s GPG key to your keyring
sudo sh -c 'echo ""'
sudo apt-get update && sudo apt-get install -y curl
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://pkg.ddev.com/apt/gpg.key | gpg --dearmor | sudo tee /etc/apt/keyrings/ddev.gpg > /dev/null
sudo chmod a+r /etc/apt/keyrings/ddev.gpg

# Add DDEV releases to your package repository
sudo sh -c 'echo ""'
echo "deb [signed-by=/etc/apt/keyrings/ddev.gpg] https://pkg.ddev.com/apt/ * *" | sudo tee /etc/apt/sources.list.d/ddev.list >/dev/null

# Update package information and install DDEV
sudo sh -c 'echo ""'
sudo apt-get update && sudo apt-get install -y ddev

# One-time initialization of mkcert
mkcert -install
```

### Installing mkcert
- for my Raspberry pi 4, i used (https://github.com/FiloSottile/mkcert/releases/download/v1.4.4/mkcert-v1.4.4-linux-arm)

``` wget https://github.com/FiloSottile/mkcert/releases/download/v1.4.4/mkcert-v1.4.4-linux-arm ```

``` sudo cp mkcert-v1.4.4-linux-arm /usr/local/bin/mkcert ```

```    sudo chmod +x /usr/local/bin/mkcert ```

And it works now.


- I had to install docker bec the one I had is low version

### To install docker
- sudo apt update
- sudo apt upgrade -y
- curl -sSL https://get.docker.com | sh
- I was ok with the following codes to install Docker on my Raspberry Pi 4. The codes was suggested by DeepSeek.

```
# Add Docker's GPG key
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

# Add the repository (for Debian)
echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/debian bookworm stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

# Update and install
sudo apt update
sudo apt install docker-ce docker-ce-cli containerd.io
``` 

### Configure Ddev
- I ran 'ddev config' in the drupal10 folder and follow the instructions
- I had to give permission to the drupal10 folder, unlist the project installed and installed again




 
