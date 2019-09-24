# Samba-smb.conf-Default

## Backup smb.conf
sudo cp /etc/samba/smb.conf /etc/samba/smb.conf.default

## Edit smb.conf
netbios name = <servername>

## Convert unix user
sudo smbpasswd -a <username>

# Stop/Start/Restart Samba

sudo systemctl stop smbd

sudo systemctl start smbd

sudo systemctl restart smbd

# Get status
sudo systemctl status smbd