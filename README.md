Bot for Experitest Cloud
=========

This role will install Bot for linux os hosts

Requirements
------------
* [ansible-role-java8](https://github.com/ExperitestOfficial/ansible-role-java8) must be installed on all machines. <br>
* This role assumes that you have [postgresql server](https://github.com/ExperitestOfficial/ansible-role-postgresql-server) already installed. <br>
* Supports linux os hosts only.

Role Variables
--------------
To run this role - need to provide the following parameters of Experitet Cloud

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-----:|:-----:|
| state | should the application be present or absent | present, absent | present | no |
| custom_download_url | custom url to download the war file from | string |  | no |
| custom_jar_download_url | custom url to download the jar file from | string |  | no |
| app_version | application version to install | string | 1.0.406  | no |
| server_port | port number for the server | string | 8083 | no |
| installation_root_folder | the root folder in which the application will be installed under bot-{version} folder | string | for linux: /opt/Experitest | no |
| java_version | java jre version to install | string | 8u292-b10 | no |
| clear_temp_folder | remove temp folder after installation | boolean | False | no |

