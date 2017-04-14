# tomcat-jenkins
jenkins inside tomcat deployment

## possible issues
1. https://github.com/ansible/ansible/issues/14426 - as workaround pushed configuration as root
2. https://github.com/ansible/ansible/issues/13856 - installed Windows Management Framework 4.0

## run command
ansible-playbook -i hosts site.yml --ask-vault-pass

## how-to: vault encrypting
ansible-vault create filename 

## configure Windows connection
1. [Install TLS 1.2](https://support.microsoft.com/en-us/help/3080079/update-to-add-rds-support-for-tls-1.1-and-tls-1.2-in-windows-7-or-windows-server-2008-r2)
2. [Upgrade Powershell to 3.0 version](https://github.com/ansible/ansible/blob/devel/examples/scripts/upgrade_to_ps3.ps1)
3. [Run remote configuration script](https://github.com/ansible/ansible/blob/devel/examples/scripts/ConfigureRemotingForAnsible.ps1)
