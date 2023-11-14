Bot for Continuous Testing Cloud
=========

This role installs the bot for Linux hosts.

Requirements
------------
* [ansible-role-java8](https://github.com/ExperitestOfficial/ansible-role-java8) installed on all machines. <br>
* [PostgreSQL server](https://github.com/ExperitestOfficial/ansible-role-postgresql-server) installed. <br>

Only Linux hosts are supported.

Role Variables
--------------
To run this role, you need to provide these Continuous Testing Cloud parameters:

| Name                         | Description                                                                            |       Type       |                  Default                  | Required |
|------------------------------|----------------------------------------------------------------------------------------|:----------------:|:-----------------------------------------:|:--------:|
| state                        | should the application be present or absent                                            | present, absent  |                  present                  |    no    |
| custom_download_url          | Custom URL to download the war file from                                               |      string      |                                           |    no    |
| extra_java_options           | Extended java options                                                                  | array of strings |                    []                     |    no    |
| extra_application_properties | Additional properties to be overriden in application.properties                        |       dict       |                    {}                     |    no    |
| extra_logback_properties     | Additional properties to be overriden in logback.properties                            |       dict       |                    {}                     |    no    |
| db_connection_string         | PostgreSQL connection string                                                           |      string      | jdbc:postgresql://localhost:5432/reporter |    no    |
| db_username                  | Username for db connection                                                             |      string      |                 postgres                  |    no    |
| db_password                  | Password for db connection                                                             |      string      |                                           |   yes    |
| installation_root_folder     | Root folder in which the application will be installed under reporter-{version} folder |                  |                                           |          |
| app_version                  | Application version to install                                                         |      string      |                  1.0.406                  |    no    |
| server_port                  | Port number for the server                                                             |      string      |                   8099                    |    no    |
| installation_root_folder     | Root folder in which the application will be installed under bot-{version} folder      |      string      |        for linux: /opt/Experitest         |    no    |
| java_version                 | Java JRE version to install                                                            |      string      |                 8u292-b10                 |    no    |
| clear_temp_folder            | Remove temp folder after installation                                                  |     boolean      |                   False                   |    no    |

