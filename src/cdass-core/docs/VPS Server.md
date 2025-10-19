VPS Server Setup & SSH Key Configuration — Documentation
Project: Security Stack Hosting

Domain: therealtechsolutions.com
VPS Provider: RackGenius
OS: Ubuntu Server 22.04 LTS
Purpose: Host Wazuh, CrowdSec, Graylog, and AI awareness modules.

✅ You’ve Achieved:

Secure SSH access and sudo user

Hardened remote login

Wazuh installed, dashboard ready

Clean reboot + snapshot checkpoint

--------------------------------------------------------------------------------------------------------------

1. VPS Deployment Issues

Initially struggled to log in via SSH:

SSH errors included:

Permission denied (publickey)

WARNING: REMOTE HOST IDENTIFICATION HAS CHANGED!

No such host is known / DNS timeouts

Cause: Misconfigured key paths, multiple Windows accounts, incomplete DNS propagation, and deleted keys.

2. SSH Key Management
Steps Taken

Key generation (local machine)

ssh-keygen -t rsa -b 4096 -m PEM -f C:\Users\<User>\.ssh\cdxnode01.pem


Creates:

Private key: cdxnode01.pem → keep safe locally.

Public key: cdxnode01.pem.pub → uploaded to RackGenius.

Uploading public key

Before VPS creation, uploaded cdxnode01.pem.pub to RackGenius → ensures root can login via key-only authentication.

Private key never uploaded to the server.

Known issues

Running SSH as different Windows users caused .pem file not to be found.

Deleting .ssh or old keys in RackGenius caused repeated Permission denied errors.

3. DNS & Host Key Issues

Added cdxnode01.therealtechsolutions.com A record in Squarespace pointing to VPS IP.

Initial nslookup returned server unknown / request timed out:

Cause: DNS propagation delay and ISP resolver caching.

Resolved by:

Using VPS IP directly for SSH.

Clearing old host key:

ssh-keygen -R cdxnode01.therealtechsolutions.com


Verified new ED25519 host key via SSH VNC prompt.

4. VNC & Root Access Recovery

Logged into root via RackGenius VNC console:

Necessary because private key mismatch prevented SSH login.

Confirmed root login and created non-root user analyst.

5. Analyst User & SSH Key Deployment

Create analyst user:

adduser analyst
usermod -aG sudo analyst


Configure SSH folder:

mkdir -p /home/analyst/.ssh
chmod 700 /home/analyst/.ssh
chown analyst:analyst /home/analyst/.ssh


Copy public key to authorized_keys:

nano /home/analyst/.ssh/authorized_keys
# Paste contents of local cdxxnode01.pem.pub
chmod 600 /home/analyst/.ssh/authorized_keys
chown analyst:analyst /home/analyst/.ssh/authorized_keys


Test SSH login locally:

ssh -i C:\Users\<User>\.ssh\cdxnode01.pem analyst@<VPS_IP>


Successful key-based login confirms safe non-root access.

6. SSH Hardening & Firewall

Optional but recommended:

nano /etc/ssh/sshd_config
# Set:
PermitRootLogin no
PasswordAuthentication no
systemctl restart ssh


Configure firewall (UFW)

Ensures only key-based SSH access and minimal open ports for web/stack services.

7. Lessons Learned

Always generate and save private key locally before VPS creation.

Use public key upload during server setup, not afterward.

Keep .ssh folder consistent and accessible to the correct user account.

VNC console is critical recovery tool if SSH key mismatch occurs.

DNS may take time to propagate; IP-based SSH login works reliably.

Always create a non-root user for regular SSH access and harden root access.

Next Steps

Automate initial VPS hardening and software installation for MVP:

Wazuh (SIEM)

CrowdSec (intrusion prevention)

Graylog (logs & dashboards)

AI awareness modules

Store setup scripts and documentation under VPS Server folder in GitHub for repeatable deployments.
