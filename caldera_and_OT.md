Any Linux or MacOS
Recommended hardware to run on is 8GB+ RAM and 2+ CPUs
# Python
sudo apt update
sudo apt install python3
sudo apt install python3-pip
python3 –version # verify installation, mine: 3.11.9

#NodeJS
sudo apt update
curl -fsSL https://deb.nodesource.com/setup_current.x | sudo -E bash -
sudo apt install -y nodejs
node -v # verify installation, mine: 22.8.0

#Go
wget https://go.dev/dl/go1.19.9.linux-amd64.tar.gz
sudo tar -C /usr/local -xzf go1.19.9.linux-amd64.tar.gz

nano ~/.bashrc
#Add the following line at the end of the file:
#export PATH=$PATH:/usr/local/go/bin
# Save and exit the editor
source ~/.bashrc # reload your .bashrc
go version # verify installation, mine: 1.19.9

From <https://ucy-my.sharepoint.com/personal/cpashi02_ucy_ac_cy/Documents/PhD/Technical_Documentations/KIOS_projects/Caldera-OT/Caldera-and-OT.docx> 
