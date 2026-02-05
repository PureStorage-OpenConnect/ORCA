# Oracle Rapid Clone Automation with Ansible

**ORCA** is a collection of Ansible playbooks which addresses the challenges of Oracle Database Copy Data Management (CDM). 
**ORCA** provides traditional and modern DevOps teams a Self Service solution enabling developers, QA engineers and business teams the abiliy to refresh non-Production databases without impacting Production systems.

**ORCA** utilises standard Ansible and Pure modules to manage Oracle database services and perform 'Crash Consistent' storage snapshots, enabling end-to-end automation of Oracle databases refreshes across mulitple non-Production databases within the Enterprise. 

## Zero Production Impact
Unlike other Copy Data Management (CDM) solutions, **ORCA** has zero Production Impact e.g.
1. No Production configuration changes e.g. OS or databases accounts
1. No Production agents or sofware installs
1. No additional Production backup workload e.g. RMAN jobs
1. No impact to Production databases e.g. requirement to put database into Hot Backup mode.

## Modern DevOPS Solution
**ORCA** is designed to be run from RedHat Ansible Tower or the Opens Source AWX Project.

ORCA is able to leverage the Ansible Tower and AWX Automation and Orchestration features below. If you are considering a CDM tool I strongly suggest you consider these features:

1. Modern WebUI, command line and REST API interfaces (for integration with other DevOps tools e.g Jenkins)
1. The ability to schedule and run job interactivley (Self Service)
1. Provide runtime variables and parameters 
1. Job notifications - Slack, email etc...
1. Code configuration management through Git intergration
1. Host and dynamic inventory management
1. Security and encrypted password management
1. User RBAC (RollBack Access Control)
1. Job Audit and reporting

### ORCA Features
1. Refresh Mulitple Oracle 19c/26ai Databases

## Getting Started

### Prerequisites

ORCA requires the PureStorage Python REST Client, details available at https://pypi.org/project/purestorage/

pip install purestorage

### Installation

Download **ORCA** from GitHub and localise vars/database.yaml to required source and target databases.

### Usage

Use from ansible control machine command line or via RedHat Tower / AWX.

### Database Clone v2
Refactored to use Pure Ansible module and Purity 6+ volume tags
`
$ ansible-playbook database_clone2.yaml
`
### Database Clone Original
Legacy version available for reference only.
Examples using Ansible URI module rather than prefered Ansible Pure modules
`
$ ansible-playbook database_clone.yaml
`

## Restrictions

- Source and Target database(s) reside on the same FlashArray

## Authors

Ron Ekins, Director Field Solution Architecture Pure Storage

Oracle ACE Director (https://ace.oracle.com/ords/ace/profile/ronekins)

## License

This module is available to use under the Apache 2.0 license, stipulated as follows:

Copyright 2018 Pure Storage, Inc.
Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at http://www.apache.org/licenses/LICENSE-2.0 Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on  an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.

## Link(s)

[RedHat Ansible] (https://www.ansible.com)

[RedHat Ansible Tower] (https://www.ansible.com/products/tower)

[RedHat Ansible AWX] (https://www.ansible.com/products/awx-project)

 

