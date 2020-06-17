# Opcon Web Services Templates for HYCU multi-cloud data protection
Templates for the OpCon Web Services Connector to interact with HYCU Multi-cloud Data Protection system (https://www.hycu.com).

Through HYCU, these templates will allow OpCon to perform Full or Incremental Backups as well as Archives (Yearly, Monthly and weekly) on AWS, Azure, Google Cloud, VMware and Nutanix.

# Disclaimer
No Support and No Warranty are provided by SMA Technologies for this project and related material. The use of this project's files is on your own risk.

SMA Technologies assumes no liability for damage caused by the usage of any of the files offered here via this Github repository.

# Prerequisites
- Opcon V19.1
- SMA OpCon Web Services Connector for Windows or Linux V20.0.3

- a HYCU Data Protection system and an Adminitrator account on this system.
- Create on Opcon on global property (mandatory) for Hycu API url: 
    - [[myHycuServer]]: your Hycu API url (https://xxx.xxx.xxx.xxx:8443)
- Create two Optionnal global properties (crypted) for Hycu user & password:
    - [[HycuUser]]
    - [[HycuPwd]]
- Create other Optionnals global properties for recurent used Hycu uuids:
    - [[Hycu-Hypervisor-Uuid]] : for Hycu Hypervisor Uuid
    - [[Hycu-Target01-Uuid]] : for your 1st Hycu Target...

# Instructions
- Download the zip file that contains the template files (.json), selecting your release [here](https://github.com/SMATechnologies/hycu-webservciestemplate/releases)
- Extract the zip on your local machine
- Create your Opcon job Type = Windows or Linux, Sub-type = **Web Services** and name it.
- Import Template, choose your template file (.json) from the extract location
- On Variable tab, check if variables are set according your environment. 
- Set any other variable required (OpCon Properties are supported).
- On Steps tab, Step1 in your job, check the body json, and modify it if need.
- On Steps tab, last step, Response subtab, adjust the poll times to match your hycu backup job durations.
- On Failure Criteria tab, set the OK return code to 200.
- Save your Job.

# License
Copyright 2019 SMA Technologies

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at [apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

# Contributing
We love contributions, please read our [Contribution Guide](CONTRIBUTING.md) to get started!

# Code of Conduct
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-v2.0%20adopted-ff69b4.svg)](code-of-conduct.md)
SMA Technologies has adopted the [Contributor Covenant](CODE_OF_CONDUCT.md) as its Code of Conduct, and we expect project participants to adhere to it. Please read the [full text](CODE_OF_CONDUCT.md) so that you can understand what actions will and will not be tolerated.
