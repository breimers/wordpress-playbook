# wordpress-playbook

Ansible Playbook for launching a simple WP server with SSL

-Requirements:
    
    Ubuntu Server 18
    
    Ansible

-Steps:
    
    1) Install ansible on build machine
    
    2) Set up ssh with Ubuntu server
    
        a) Test SSH connection
        
        b) If using remote host, add '-i mykey.pem'
    
    3) Set up playbook and configure roles
    
    4) Launch ansible-playbook
    
        a) If using remote host, add '--private-key mykey.pem'
        
        b) May need to add '--become' to enable SUDO privileges
    
    5) Set up routing for your server
    
        a) Route53 is a good option
        
    6) Wordpress -> Dashboard -> General Settings
        
        a) Change WP/Site to 'https://www.example.com/"
    
    7) Manage as regular Wordpress site :)

-Thoughts:
    
    The next step would be to automate the dns hosting 
        
        Does ansible have r53 integration?
        
    Another idea is to set the sitename from the beginning if you can automate the dns
    
    Definitely need to delve more into ansible! Can be powerful if combined with a provisioning system a-la-Terraform
