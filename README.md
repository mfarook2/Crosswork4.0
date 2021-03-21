# Crosswork4.0
## Integrated Health Monitoring and Provisioning of NSO services using Crosswork Change Automation and Health Insights

The use case makes health monitoring of the NSO service a seemless part of the lifecycle of a NSO service.It involves:
  - Provisioning of NSO Service
  - Automatically identifies the objects for the provisioned NSO service, derives the relevant set of KPIs and configures the KPIs on the endpoints of the NSo service.


## Installation
1. 	Install the following NSO packages in the ncs-run directory on the nso server

| NSO Service Package  | Description |
| ------------- | ------------- |
| l3vpn.tar.gz  | A l3vpn NSO Service. |
| enable-kpi-profiles.tar.gz  | NSO service which detects the network objects where the kpis have to be applied and automatically configures and provisions the kpis on the endpoints of the NSO service.  |
| aux-info.tar.gz | Stores meta-data of the NSO l3vpn service for alert correlation.  |

2.	Edit NSO_SERVICE_PATH in file kpi.py in the enable-kpi-profiles packages directory to show the path where all the packages are located in the ncs running directory.
3.	Import the 2 plays and the playbook into Crosswork.

| Playbook and Plays | Description |
| ------------- | ------------- |
| l3vpn_play.tgz  | l3vpn play which corresponds to the NSO l3vpn service. |
| enable_kpi_profile_play.tgz  | Enable-kpi-profiles play corresponds to the NSO enable-kpi-service.  |
| l3vpn_and_kpi_profile_playbook.tgz  | Playbook containing l3vpn play and enable-kpi-profiles play  |

4. 	adas
5. 	asd
6. 	asd
7. 	asda
8. 	das
