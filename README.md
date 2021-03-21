# Crosswork4.0
## Integrated Health Monitoring and Provisioning of NSO services using Crosswork Change Automation and Health Insights

The use case makes health monitoring of the NSO service a seemless part of the lifecycle of a NSO service. It involves:
  - Provisioning of NSO Service
  - Automatically identifies the objects for the provisioned NSO service, derives the relevant set of KPIs and configures the KPIs on the endpoints of the NSo service.


## Installation
1. 	[Install the following NSO packages](https://developer.cisco.com/docs/nso/guides/#!nso-5-5-administration-guide-nso-packages) in the ncs-run directory on the nso server

    | NSO Service Package  | Description |
    | ------------- | ------------- |
    | l3vpn.tar.gz  | A l3vpn NSO Service. |
    | enable-kpi-profiles.tar.gz  | NSO service which detects the network objects where the kpis have to be applied and automatically configures and provisions the kpis on the endpoints of the NSO service.  |
    | aux-info.tar.gz | Stores meta-data of the NSO l3vpn service for alert correlation.  |

2.	[Edit **NSO_SERVICE_PATH**](#edit_nso_service_path) in file **kpi.py** located in the **enable-kpi-profiles** packages directory to show the path where all the NSO packages are located in the ncs running directory.
3.	[Import](#import_playbook_and_play) the following plays and the playbook into Crosswork.

    | Playbook and Plays | Description |
    | ------------- | ------------- |
    | l3vpn_play.tgz  | l3vpn play which corresponds to the NSO l3vpn service. |
    | enable_kpi_profile_play.tgz  | Enable-kpi-profiles play corresponds to the NSO enable-kpi-service.  |
    | l3vpn_and_kpi_profile_playbook.tgz  | Playbook containing l3vpn play and enable-kpi-profiles play  |

4. 	[Run](#run_playbook) the playbook **l3vpn_and_kpi_profile** playbook. Import the parameters file **l3vpn_and_kpi_profile_parameters.json** file while running the playbook and modify the paramerters as required.
5. 	Executing the **l3vpn_and_kpi_profile** playbook results in:
    - Deploying the l3vpn service
    - Creation of a KPI profile with the KPI's relevant for the l3vpn service in Crosswork Health Insights.
    - Configuration of the KPIs on the endpoints of the l3vpn service which results in monitoring of the KPIs in Crosswork Health Insights

<a name="edit_nso_service_path"></a>
# ***Edit NSO_SERVICE_PATH***
![na-102](https://user-images.githubusercontent.com/12874987/111919200-fa33b000-8a45-11eb-9ed7-9b9ea8826851.jpg)

![na-101](https://user-images.githubusercontent.com/12874987/111919199-f738bf80-8a45-11eb-8174-0bda80af5b98.jpg)

<a name="import_playbook_and_play"></a>
# Import Playbook and Play
### ***Import Play***
From the Crosswork UI, select **Network Automation --> Play List**, and click on import plays
![image](https://user-images.githubusercontent.com/12874987/111920571-f7888900-8a4c-11eb-8b00-306c7c84853e.png)

### ***Import Playbook***
From the Crosswork UI, select **Network Automation --> Playbook List**, and click on import playbook
![image](https://user-images.githubusercontent.com/12874987/111922300-471f8280-8a56-11eb-9227-e7e6cb07b018.png)


<a name="run_playbook"></a>
# ***Run Playbook***
* From the Crosswork UI, select **Network Automation --> Run Playbook --> My Playbooks**, and select the playbook **l3vpn_and_kpi**
* In the **Parameters** step of the **Run Playbook** workflow, choose **Upload** parameters and choose the file **l3vpn_and_kpi_playbook_parameter.json**. Modify the values if required before executing the playbook

![image](https://user-images.githubusercontent.com/12874987/111923895-c749e600-8a5e-11eb-9fb7-07912e230af8.png)



