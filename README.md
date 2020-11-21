## Gitlab Installation 

### The first thing you need to run is the update or upgrade.
```
sudo apt update
```
#### Then install the necessary dependencies
```
sudo apt-get install -y curl openssh-server ca-certificates
```
#### If you want GitLab to send notification emails you can either install Postfix from the command below or if you want to use another transactional mail service such as SendGrid, MailChimp, etc you can configure using GitLab SMTP settings after installation.
```
sudo apt-get install -y postfix
```
#### Installing GitLab CE
```
curl -sS https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh | sudo bash
```
#### Once it is done and the repository is enabled you can install GitLab CE package by using this command below
```
sudo apt-get install gitlab-ce
```
#### If you want to set up using your server address, do the below
```
sudo EXTERNAL_URL="http://gitlabce.example.com" apt-get install gitlab-ce
```
#### Once you have the package installed, you can run the provided configuration utility. It provides an automatic configuration. You can modify things later if you need to.
```
sudo gitlab-ctl reconfigure
```
```
gitlab-ctl start
```
### ADD HTTP and HTTPS protocols in security group.

### In Gitlab Dashboard reset password and the username is root for the Gitlab.
