To be able and connect one vm to another through ssh :
Uncomment the 'PasswordAuthentication' field in /etc/ssh/sshd_config in target vm
Use 'ssh TARGET_VM_IP' with password 'vagrant' to ssh into the target.
