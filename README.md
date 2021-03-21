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

2.	Edit **NSO_SERVICE_PATH** in file **kpi.py** in the **enable-kpi-profiles** packages directory to show the path where all the NSO packages are located in the ncs running directory.
3.	Import the following plays and the playbook into Crosswork.

    | Playbook and Plays | Description |
    | ------------- | ------------- |
    | l3vpn_play.tgz  | l3vpn play which corresponds to the NSO l3vpn service. |
    | enable_kpi_profile_play.tgz  | Enable-kpi-profiles play corresponds to the NSO enable-kpi-service.  |
    | l3vpn_and_kpi_profile_playbook.tgz  | Playbook containing l3vpn play and enable-kpi-profiles play  |

4. 	Run the playbook **l3vpn_and_kpi_profile** playbook. Import the parameters file **l3vpn_and_kpi_profile_parameters.json** file while running the playbook and modify the paramerters as required.
5. 	Executing the **l3vpn_and_kpi_profile** playbook results in:
    - Deploying of the l3vpn service
    - Creation of a KPI profile with the KPI's relevant for the l3vpn service in Crosswork Health Insights.
    - Configuration of the KPIs on the endpoints of the l3vpn service which results in monitoring of the KPIs in Crosswork Health Insights
6. [click here to jump to my anchor](#Install NSO pacakges)

eqwe
qe
qeqwe
qe
qe
qe
qe
q
eq
e
qe
qe

<a name="Install NSO pacakges"></a>
# yes it works
