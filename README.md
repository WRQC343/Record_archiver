![Logo](https://gmrs-link.com/images/link-scripting_50_1_50.png)          
![Release Version](https://img.shields.io/badge/Version-v1.5.0-blue?color=blue)
![OS Version](https://img.shields.io/badge/OS-Linux_*_Hamvoip-red?color=red)

# Record Archiver

This script is designed for users who have recording enabled on the node and wish to archive the recordings nightly at midnight.    
Saves the last 5 days of recordings.

## Installation & Setup

1. SSH into the node and open a bash terminal. Then copy and paste the line below.

```bash
bash -c "$(curl -fsSL https://raw.githubusercontent.com/Justice57201/Record_archiver/main/RA_installer.sh)"
```

## Setup

For demonstration, let's assume your recordings are saving to /etc/asterisk/local/Recordings/

1. Navigate to /root/Rec-arc.sh and open it in the editor.

2. Now, to set the file locations for your files, edit this line to match your setup.

```bash
   "/etc/asterisk/local/Recordings/1234/:/etc/asterisk/local/Recordings/Backups/:node-1234"
```

   - Change the directory to match yours.
   - Change the 1234 to your node number.

3. Should you have a multi-node, add more location strings to the file, like below.

```bash
FOLDERS=(
    "/etc/asterisk/local/Recordings/1234/:/etc/asterisk/local/Recordings/Backups/:node-1234"
    "/etc/asterisk/local/Recordings/5678/:/etc/asterisk/local/Recordings/Backups/:node-5678"
)
```

4. Save the file & you're done.

   
