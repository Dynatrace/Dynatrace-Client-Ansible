# Dynatrace-Client-Ansible

An [Ansible](http://www.ansible.com) role for automated deployments of the [Dynatrace](http://bit.ly/dttrial) Client. 

**Note**: Currently, we support only Linux hosts, support for installing Windows hosts is in the making.

## Download

The role is available via:

- [Ansible Galaxy](https://galaxy.ansible.com/list#/roles/2856)
- [GitHub](https://github.com/Dynatrace/Dynatrace-Client-Ansible)

## Requirements

Download the Dynatrace Client installer from [downloads.compuwareapm.com](http://downloads.compuwareapm.com) and place the artifact as ```dynatrace-client.jar``` in the role's ```files``` directory from where it will be picked up during the automated installation.

## Role Variables

As defined in ```defaults/main.yml```:

| Name                                         | Default                 | Description |
|----------------------------------------------|-------------------------|-------------|
| *dynatrace_client_installer_bitsize*         | 64                      | 32 or 64    |
| *dynatrace_client_linux_install_dir*         | /opt                    | The Dynatrace Client will be installed into the directory *$dynatrace_client_linux_install_dir*/dynatrace-*$major*-*$minor*-*$rev*, where *$major*, *$minor* and *$rev* are given by the installer. A symbolic link to the actual installation directory will be created in *$dynatrace_client_linux_install_dir*/dynatrace. |
| *dynatrace_client_linux_installer_file_name* | dynatrace-collector.jar | The file name of the Dynatrace Client installer in the role's ```files``` directory. |
| *dynatrace_client_role_name*                 | Dynatrace-Collector     | The actual name of this role in an [Ansible Playbook's](http://docs.ansible.com/playbooks.html) ```roles``` directory. |

## Example Playbook

	- hosts: all
	  roles:
	    - { role: Dynatrace-Client }

## Additional Resources

- [Slide Deck: Automated Deployments](http://slideshare.net/MartinEtmajer/automated-deployments-slide-share)
- [Slide Deck: Introduction to Automated Deployments with Ansible](http://www.slideshare.net/MartinEtmajer/introduction-to-automated-deployments-with-ansible)
- [Tutorials: Automated Deployments with Dynatrace and Ansible](https://community.compuwareapm.com/community/display/COE/Tutorials+on+Automated+Deployments#TutorialsonAutomatedDeployments-ansible)

## Questions?

Feel free to post your questions on the Dynatrace Community's [Continuous Delivery Forum](https://community.dynatrace.com/community/pages/viewpage.action?pageId=46628921).

## License

Licensed under the MIT License. See the LICENSE file for details.
[![analytics](https://www.google-analytics.com/collect?v=1&t=pageview&_s=1&dl=https%3A%2F%2Fgithub.com%2FdynaTrace&dp=%2FDynatrace-Client-Ansible&dt=Dynatrace-Client-Ansible&_u=Dynatrace~&cid=github.com%2FdynaTrace&tid=UA-54510554-5&aip=1)]()