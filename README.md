# Server Provisioning (ansible/aws)
Basic server provisioning tool for AWS instances running RedHat.

## Getting Started
1. Create your AWS instance running RedHat.
    * Ensure that your security group allows TCP connections to port 22 and a custom port you like.
2. Configure `hosts.example` and copy to `/etc/ansible/` as `hosts`.
    * Replace `< ip address >` with the public ip of your AWS instance.
3. Configure `group_vars/aws.yml.example` and copy to `group_vars/aws.yml`.
    * Replace `< user >` with the user you would like ansible to use.
    * For AWS RedHat instances, this is normally `ec2-user`.
    * Replace `< path to key >` with the path to your `.pem` file.
    * Replace `< port >` with the custom port you set up for your security group.
4. Run using `ansible-playbook main.yml`.
