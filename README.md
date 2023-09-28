**Cloud Consumption Interface (CCI) OnPrem Technical Preview**

CCI serves as a cloud experience layer for Supervisor IaaS services. To end-users, it presents itself as a graphical web console, a common IaaS API endpoint, and a command-line interface (CLI) for self-service access to vSphere-based cloud resources. Simultaneously, it empowers infrastructure service providers to define regions, resource envelopes, and resources accessible through self-service by consumers. CCI seamlessly integrates into the vSphere+ platform, supercharged by the capabilities of Aria Automation. As of today, the CCI Initial Availability (IA) exists solely as a cloud service, and it has garnered enthusiastic feedback. Simultaneously, it has generated demand for an OnPrem version catering to cloud-disconnected environments. In response to this growing need, VMware shares a technical preview of the CCI OnPrem appliance. This preview release is intended to offer insights into the technology's capabilities and to collect invaluable feedback from users.

Comprehensive instructions can be accessed through the following link:

https://core.vmware.com/resource/cci-onprem-tech-preview 

**Please be aware that you are currently in the main branch. To obtain the most up-to-date installation scripts, kindly select the latest available branch for download!**


**License**

This is a preview version of software that is used to gather customer feedback and help shape VMware product roadmap. This software may only be applied to a newly installed Aria Automation instance that is not used for any production workloads. VMware is providing this software to you, that you may use at your sole discretion, “AS IS”, and without any warranty, condition, support, or service level agreement of any kind. The specific Aria Automation instance that gets modified with this software will not be eligible for warranty, support or service level agreements of any kind. VMware reserves the right to stop development of this capability at any time. Providing usage of this capability implies no commitment by VMware that it will be offered commercially in the future. VMware can also request you stop usage of this capability at any time. VMware can also use the feedback you provide for any purpose, and you must abide by existing NDA agreements that you have signed with VMware that require you not to disclose VMware confidential information pertaining to roadmap and product development details to a third party. VMware’s, its affiliates’ and its suppliers’ aggregate liability for any claim arising out of your use of this software will not exceed $5,000 USD.

**Notes**

The kubectl binary is not available for direct download from the appliance in this release. Users can obtain the kubectl binary by following these links to download it from the web:

Linux: https://www.mgmt.cloud.vmware.com/ccs-ui/cci-k8s-plugin/linux/kubectl-cci.zip

Windows: https://www.mgmt.cloud.vmware.com/ccs-ui/cci-k8s-plugin/windows/kubectl-cci.zip

ARM Mac: https://www.mgmt.cloud.vmware.com/ccs-ui/cci-k8s-plugin/darwin-arm64/kubectl-cci.zip

AMD64 Mac: https://www.mgmt.cloud.vmware.com/ccs-ui/cci-k8s-plugin/darwin-amd64/kubectl-cci.zip


Single SignOn (SSO): This preview does not support SSO feature. Any actions on the supervisor namespace and its workloads (like VM, TKG etc.) will be performed with vCenter admin credentials and will not correspond to the CCI user. This limitation will be addressed in subsequent releases.

**Scripts**

The following scripts are designed for installing CCI on a fresh Aria Automation appliance for testing purpose only. We recommend a single-node deployment with a minimum version of 8.13. These deployment and rollback scripts require no additional parameters to run. Comprehensive installation instructions can be found in the provided link. 

./deploy_cci_on_aria_auto_appliance.sh

./rollback_cci_deployment.sh

./populate_sample_data.sh --org-id <UUID> --user <USER> --storage-class <STORAGE_PROFILE>

Example: ./populate_sample_data.sh --org-id ffc03a8d-22ed-4fac-a64a-22dd4d611794 --user fritz@vmware.com --storage-class wcpglobal-storage-profile


 ./deploy_cci_on_aria_auto_appliance.sh script should be run first. If there are any errors when executing the deployment script

 ./rollback_cci_deployment.sh script should be run to undo the deployment script changes.

For the populate_sample_data.sh script, the USER passed should be the username used for logging into Aria Automation.

**Questions & Feedback**

We value your input and insights as we continue to refine and expand the capabilities of CCI. If you have any questions or would like to share your feedback, please don't hesitate to reach out to us at cci@vmware.com. 
