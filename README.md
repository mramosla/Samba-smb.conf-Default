# Samba-smb.conf-Default

## Backup smb.conf
sudo cp /etc/samba/smb.conf /etc/samba/smb.conf.default

# Replace smb.conf
sudo cp smb.conf /etc/samba/smb.conf

## Edit smb.conf
sudo vi /etc/samba/smb.conf

netbios name = <servername>

# Bind interface if needed
interfaces = 127.0.0.0/8 eth0 

## Convert unix user
sudo smbpasswd -a <username>

## Browse to home share map drive
\\server IP\share

# Stop/Start/Restart Samba

sudo systemctl stop smbd

sudo systemctl start smbd

sudo systemctl restart smbd

# Get status
sudo systemctl status smbd