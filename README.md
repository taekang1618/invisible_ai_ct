# invisible_ai_ct
Invisible AI Coding Test

## Step 1
Clone the repo

## Step 2
Install ansible using instructions outlined here https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html

## Step 3
Install boto3
```python 3 -m pip install boto3```

## Step 4
Set environment variables:
```
# Configure directories
export SSH_KEYDIR=$HOME/.secrets

# Configure AWS
export AWS_ACCESS_KEY={aws_access_key}
export AWS_SECRET_KEY={aws_secret_key}
```
and create a `.pem` file for ssh-ing into your provisioned ec2 instance.

Change the `.pem` file name in `./main.yml` next to `ansible_ssh_private_key_file`.

## Step 5
Run the ansible playbook
```
ansible-playbook main.yml
```