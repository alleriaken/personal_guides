# Update computer
`sudo apt-get update`
`sudo apt-get upgrade`
`sudo apt-get install software-properties-common`

# Add ansible ppa
`sudo apt-add-repository ppa:ansible/ansible`

# Update computer again
`sudo apt-get update`

# Install Ansible
`sudo apt-get install ansible`

# Check ansible version
`ansible --version`

# Create hosts file
`sudo vim /etc/ansible/hosts`

[tipemeservers]
74.207.253.253

# Generate ssh key
ssh-keygen -t rsa -b 4096 -C "My ansisble key"

# Copy ssh key to server
`ssh-copy-id -i $HOME/.ssh/id_rsa.pub root@74.207.253.253`

# Send ping to server
ansible -i ~/hosts -m ping all

# Check server uptime
ansible -i hosts -m shell -a 'uptime' all

# Create playbook.yml
`vim playbook.yml`

# Run ansible
ansible-playbook -i hosts playbook.yml 

