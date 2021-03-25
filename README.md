# Configure, Launch, and SSH/RDP into EC2 Instances

**Configuring, Launching, and SSH into the EC2 Linux Instance:** \
EC2 → Launch Instance → Launch Instance

Choose AMI (**Linux 2 AMI**)

Choose Instance Type (t2.micro)

Network: choose VPC (Default VPC selected by default)...Subnet: No Preference will have EC2 choose the SN for you...Auto-assign Public IP: Disable if you don't want an auto-assigned IPv4 address, otherwise select "Use subnet setting (Enable)" which is by default to assign IPv4, or select "Enable" which explicitly will assign IPv4

Storage: The default settings are provided by the AMI. \
AMI's have a Block Mapping Device inside, which lists the Volumes inside the AMI with the Device ID that it used. This AMI contains a block device mapping, which lists the Root/Boot Volume with this Device ID of /dev/xvda.

Add Tags

Security Group: Source of 0.0.0.0/0 allows any IP address on the internet to connect to this Instance. Changing to "My IP" will only allow you to connect to this instance.

Key Pair: Create & Download new key pair. \
A Key Pair has a Private Key (you just downloaded this!)  & Public Key (AWS keeps this copy). \
When you select the Key Pair to use, AWS will place this Public Key on the Instance. We use our Private Key to connect to the instance.

\
**Status Checks:**

**System Status Checks (AWS):** Make sure the traffic can reach the hardware the instance is running on. Verifies that your instance is reachable. Ensures that your EC2 Host, power, networking, and software systems are all working.

**Instance Status Checks (You):** Verifies that your instance's operating system is accepting traffic.

\
**Connecting to your EC2 Instance via SSH:** \
EC2 → Instances → Instances \
Right click your Instance → Connect → SSH Client → Copy the ssh command \
Command Prompt \
cd into directory where you saved your Key Pair \
paste the copied SSH command, hit enter, and type yes to the authentication prompt

