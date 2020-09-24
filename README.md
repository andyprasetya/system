# Manufacturing System
## Installation guide
## Implementation guide
## Developer guide
## User guide

## Requirements
By number of workplaces
* up to 10 workplaces -> 1GB RAM, 1 logical processor, approx. 10GB HDD of data per year
* up to 80 workplaces -> 8GB RAM, 8 logical processors, approx. 80GB HDD of data per year
* etc.


## Description
Manufacturing system is used for collecting data from factory machines and factory operators.<br>
Everything is stored in (postgresql) database with web as user interface.<br>
Additional software is used for processing data.<br>
Every part (every service) of system check for necessary database tables at startup. Tables are created or updated if necessary.



### Database (PostgreSQL)
* running on port 54321, user postgres, password Zps05.....
* Tuning database: https://pgtune.leopard.in.ua/#/
    * update config file located in `SHOW config_file;`, usually /var/lib/postgresql/data/postgresql.conf
    * default: DB version 12
    * default: OS Type Linux
    * default: DB Type Mixed type of applications
    * default: number of connections: 10 per 1 workplace (for example: 100 per 10 workplaces)
* Github: https://github.com/petrjahoda/database
* DockerHub: https://hub.docker.com/repository/docker/petrjahoda/database

### Zapsi Service
* collects data from zapsi devices
* Github: https://github.com/petrjahoda/zapsi_service
* DockerHub: https://hub.docker.com/repository/docker/petrjahoda/zapsi_service
### Siemens Service
* collects data from S7 devices
### OPC Service
* collects OPC data

### State Service
* process raw data and generates workplace states in realtime
* Github: https://github.com/petrjahoda/state_service
* DockerHub: https://hub.docker.com/repository/docker/petrjahoda/state_service
### Terminal Service
* process raw data and generates workplace states in realtime
* Github: https://github.com/petrjahoda/terminal_service
* DockerHub: https://cloud.docker.com/r/petrjahoda/terminal_service
### Alarm Service
* process raw data and generates email alarms in realtime
* Github: https://github.com/petrjahoda/alarm_service
* DockerHub: https://cloud.docker.com/r/petrjahoda/alarm_service
### System Service
* controls proper system behavior)
* Github: https://github.com/petrjahoda/system_service
* DockerHub: https://cloud.docker.com/r/petrjahoda/system_service   
        
### System Web Service
* system user interface
* Github:
* DockerHub:
### Display Web Service
* web pages for displaying realtime data, for use with big LCD screens
* Github: Github: https://github.com/petrjahoda/display_webservice
* DockerHub: https://cloud.docker.com/r/petrjahoda/display_webservice
    
© 2020 Petr Jahoda
