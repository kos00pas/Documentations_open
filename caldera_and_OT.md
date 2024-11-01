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

#I had problem with packages incompatibilities so i use version 4.2.0 instead of latest:5.0.0
#Cloning and requirements
git clone https://github.com/mitre/caldera.git --recursive --tag 4.2.0
cd caldera
pip3 install -r requirements.txt
pip3 install -r requirements.txt
#Running Caldera
python3 server.py --insecure –build

# 1. check for errors and warning in the execution and solve them if there are needed
# 2. You expect to see in the end of running a big, printed CALDERA, then :

# ***In your browser run: http://localhost:8888 and then the application will start locally
# To login use :
# Username: admin
# Password admin


# 3. When you solve any issue and reach this stage you can continue to Caldera-OT plugins 
#In a different folder do: 
git clone https://github.com/mitre/caldera-ot.git --recursive

# 1. Manually open the new folder and copy ONLY the folders
# (bacnet, dnp3, modbus, profinet, iec61850) 
# to the folder of the original Caldera that you git
# clone before, and specifically to the folder: caldera/plugins
# 2. Open file conf/default.yml and in the section plugins add the
     #following lines: 
# 3. Open a Terminal in the caldera folder and run again the command:

- backnet 
- dnp3
- modbus
- profinet
- iec61850


python3 server.py --insecure --build
# At the http://localhost:8888  you can now find the plugins we just add 
