# Configure, Launch, and SSH into EC2 Instance

**Configuring & Launching the EC2 Instance:**
EC2 → Launch Instance → Launch Instance \

Choose AMI (Linux 2 AMI)

Choose Instance Type (t2.micro)

Network: choose VPC (Default VPC selected by default)...Subnet: No Preference will have EC2 choose the SN for you...Auto-assign Public IP: Disable if you don't want an auto-assigned IPv4 address, otherwise select "Use subnet setting (Enable)" which is by default to assign IPv4, or select "Enable" which explicitly will assign IPv4

Storage: The default settings are provided by the AMI. AMI's have a Block Mapping Device inside, which lists the Volumes inside the AMI with the Device ID that it used. This AMI contains a block device mapping, which lists the Root/Boot Volume with this Device ID of /dev/xvda.

Add Tags

Security Group: Source of 0.0.0.0/0 allows any IP address on the internet to connect to this Instance. Changing to "My IP" will only allow you to connect to this instance.

Key Pair: Create & Download new key pair. \
A Key Pair has a Private Key (you just downloaded this!)  & Public Key (AWS keeps this copy). \
When you select the Key Pair to use, AWS will place this Public Key on the Instance. We use our Private Key to connect to the instance.
