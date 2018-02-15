# Ansible role for pure-ftpd

Ansible role to install and configure pure-ftpd on Centos7

## Getting Started

This role is mainly for the webhosting industry as each website is hosted under /home/website_name/public_html
so the ftp virtual user home dir is the publi_html.

### How it works

#### Checks.yml
- Ask for user input for : ftp system user and group, then for virtual host name. 
- check if the pure-ftpd package is installed or not.
- check if pure-ftpd is listening to port 21.
- check if the pure-ftpd system user and group are present or not.

#### Pkg.yml
- Install pip
- Install pexpect
- Install mkpasswd

#### Install-pureftp.yml
- Install pure-ftpd when port and package are not present.
- Copy over the default config file to the install dir.
- Create pure-ftpd system user and home dir when system user is not present.

#### Virtual-user.yml
- Generate password for virtual user.
- Create the new virtual user.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
