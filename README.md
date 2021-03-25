# Launch SSH into EC2 Instance

**Configuring & Launching the EC2 Instance:**
EC2 → Launch Instance → Launch Instance \
Choose AMI (Linux 2 AMI) \
Choose Instance Type (t2.micro) \
Network: choose VPC (Default VPC selected by default)...Subnet: No Preference will have EC2 choose the SN for you...Auto-assign Public IP: Disable if you don't want an auto-assigned IPv4 address, otherwise select "Use subnet setting (Enable)" which is by default to assign IPv4, or select "Enable" which explicitly will assign IPv4\
