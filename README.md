# ansible-redmine-ubuntu

Install Redmine on Ubuntu.

```console
sudo apt install software-properties-common
sudo apt-add-repository --yes --update ppa:ansible/ansible
sudo apt install -y ansible git
```

```console
git clone https://github.com/onozaty/ansible-redmine-ubuntu.git
cd ansible-redmine-ubuntu
sudo ansible-playbook -i hosts playbook.yml
```
