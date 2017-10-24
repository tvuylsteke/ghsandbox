# FastTrack for Azure Architectural Discussion Framework - Backup, Archive and Disaster Recovery Solution

## Table Of Contents

* [App & Data Migration](#app---data-migration)
* [Distributed Architecture](#distributed-architecture)
* [High Availability and Business Continuity / Disaster Recovery](#high-availability-and-business-continuity---disaster-recovery)
* [Monitoring &amp; Management](#monitoring--amp--management)
* [Performance &amp; Scalability](#performance--amp--scalability)
* [Security](#security)
* [Understand the Portfolio of applications are supported for Disaster Recovery](#understand-the-portfolio-of-applications-are-supported-for-disaster-recovery)

## App & Data Migration   
* **What does your on-premises infrastructure look like? Hyper-V, VMware, Baremetal, etc?**

    Determine the supportability in DR migration. This will dictate the path that should be taken with Azure Site Recovery. For more information, see [Site Recovery Workload](https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-workload)

* **What types of Operating Systems are in place today for your applications?**

    Understand what Operating Systems will be supported for migration. Depending on the OS, the VHD may need to be lifted and shifted as Azure Site Recovery may not support the OS. For more information, see [Support For Replicated Machine OS Versions](https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-support-matrix-to-azure#support-for-replicated-machine-os-versions)

* **What types of workloads are you looking to backup? Do those workloads need to be filesystem or application consistent?**

    Depending on Filesystem or Application consistency, that will dictate the backup solution to leverage (Azure Backup Agent, Azure Backup Server, or Azure Backup for IaaS). For more information, see [Which Azure Backup Components Should I Use](https://docs.microsoft.com/en-us/azure/backup/backup-introduction-to-azure-backup#which-azure-backup-components-should-i-use)

## Distributed Architecture   

* **Are you looking at Disaster Recovery between on-premises to Azure or Azure to Azure?**

    Determine the desired Disaster Recovery scenario, and how Azure Site Recovery can be used for Disaster Recovery. [[What Can I Replicate](https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-overview#what-can-i-replicate)]

* **For backups, are you protecting workloads in Azure or only on-premises?**

    Understand the need for Locally Redundant Storage (LRS) vs Geograpically Redundant Storage (GRS) for retaining data. Consider the wider scenario to meet attestations of "offsite" data, this will decrease risk of a large failure. [[Set Storage Replication](https://docs.microsoft.com/en-us/azure/backup/backup-azure-vms-first-look-arm#create-a-recovery-services-vault-for-a-vm#set-storage-replication)]

## High Availability and Business Continuity / Disaster Recovery   

| **Question**| **Purpose**| **Relevant Documentation**   |  
|---|---|---|  
| What is your defined Recovery Point Objective (RPO), Recovery Time Objective (RTO) and Service Level Agreement (SLA)?| RPO can influence bandwidth requirements.| N/A - Discovery Question - leads to potential solution options  |  
| Are you looking for a HOT or WARM Disaster Recovery solution?| Azure Site Recovery should not be used for Hot workloads. If a hot solution is required, thought should be given to distributing and scaling the architecture to the cloud naturally via App Modernization or running the workloads actively in multiple regions.|  |  
|Is failback required from Azure to on-premises?| Depending on the solution architecture, additional infrastructure may be needed to handle failback.| [https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-how-to-reprotect ][6]  |  
| Who is the individual that makes the decision to commit to a failover?| If it is unclear who is responsible for the processes and procedures for Disaster Recovery, then this will need to be defined as a first priority to take the next steps in moving forward with a successful Azure Site Recovery implementation.| Review Disaster Recovery Plan and update list of stakeholders who will and are authorized to make the call to initiate a failover.  |  
| Do you have a defined Disaster Recovery plan today?|Determine how this fits with Recovery Plans in Azure. This can help automate, orchestrate and document failover steps to ensure a successful Disaster Recovery solution.| [https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-runbook-automation ][7]  |  
| Do you test and validate your Disaster Recovery plans today?|Determine whether Disaster Recovery is initiated only in the event of a disaster. Consider utilising an environment to conduct effective testing within Azure.| [https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-test-failover-to-azure ][8]  |  
| Do you have a current Xen Infrastructure for which you want to provide a DR capability?| Understand that Azure Site Recovery can provide an option to protect Xendesktop Infrastructure.<br><br>See further details in the associated Citrix whitepaper. | [https://www.citrix.com/content/dam/citrix/en_us/documents/white-paper/xenapp-and-xendesktop-using-microsoft-azure-site-recovery.pdf][9]  |  

## Monitoring &amp; Management   

| **Question**| **Purpose**| **Relevant Documentation**   |  
|---|---|---|  
| What metrics do you gather today around Backups?| Deterine whether configuring reports for Azure Backup can act as a replacement for those metrics that are captured in the current environment.| [https://docs.microsoft.com/en-us/azure/backup/backup-azure-configure-reports ][10]  |  

## Performance &amp; Scalability   

| **Question**| **Purpose**| **Relevant Documentation**   |  
|---|---|---|  
| Consider Disaster Recovery between on-premises and Azure. Have you run the capacity planning tools?| This is the first step that should taken in right-sizing Azure Site Recovery for an environment both on-premises and in Azure.| [https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-capacity-planner ][11] [https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-deployment-planner ][12]  |  
| Consider the existing backup solution. How is data handled today? Off-site, offload to cloud, etc?|Determine bandwidth feasibility on data size. Additionally, offline backups to Azure via Import/Export service may need to be considered based upon the volume of data.| [https://docs.microsoft.com/en-us/azure/backup/backup-azure-backup-import-export ][13]  |  

## Security   

| **Question**| **Purpose**| **Relevant Documentation**   |  
|---|---|---|  
| What are your requirements for encryption?<br><br>Is there a requirement for customer-managed keys vs. Microsoft-managed keys?|Determine whether the extra management overhead and complexity is required for customer-managed keys, or whether Microsoft-managed keys would be suitable.| [https://docs.microsoft.com/en-us/azure/storage/storage-service-encryption-customer-managed-keys ][14] |  
|Who has access to backups today?| Consider those RBAC rules that are needed to the backups and associated locks. This will help protect a backup solution being removed accidentally or maliciously.| [https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-lock-resources ][15] [https://docs.microsoft.com/en-us/azure/backup/backup-rbac-rs-vault ][16]  |  
| Do you leverage Multi Factor Authentication (MFA) today?| Multi Factor Authentication should  be enforced to prevent malicious activity on Azure subscriptions.| [https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-subscription-governance ][17]<br><br>[https://docs.microsoft.com/en-us/azure/multi-factor-authentication/multi-factor-authentication ][18]  |  
  
## Understand the Portfolio of applications are supported for Disaster Recovery  

| **Question**| **Purpose**| **Relevant Documentation**   |  
|---|---|---|  
| What workloads do you plan to protect?|Gain an understanding of what needs to be secured. Use the associated documentation to determine those which are supported.| [https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-workload#workload-summary][19]  |  

[1]: https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-workload
[2]: https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-support-matrix-to-azure#support-for-replicated-machine-os-versions
[3]: https://docs.microsoft.com/en-us/azure/backup/backup-introduction-to-azure-backup#which-azure-backup-components-should-i-use
[4]: https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-overview#what-can-i-replicate
[5]: https://docs.microsoft.com/en-us/azure/backup/backup-azure-vms-first-look-arm#create-a-recovery-services-vault-for-a-vm#set-storage-replication
[6]: https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-how-to-reprotect
[7]: https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-runbook-automation
[8]: https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-test-failover-to-azure
[9]: https://www.citrix.com/content/dam/citrix/en_us/documents/white-paper/xenapp-and-xendesktop-using-microsoft-azure-site-recovery.pdf
[10]: https://docs.microsoft.com/en-us/azure/backup/backup-azure-configure-reports
[11]: https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-capacity-planner
[12]: https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-deployment-planner
[13]: https://docs.microsoft.com/en-us/azure/backup/backup-azure-backup-import-export
[14]: https://docs.microsoft.com/en-us/azure/storage/storage-service-encryption-customer-managed-keys
[15]: https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-lock-resources
[16]: https://docs.microsoft.com/en-us/azure/backup/backup-rbac-rs-vault
[17]: https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-subscription-governance
[18]: https://docs.microsoft.com/en-us/azure/multi-factor-authentication/multi-factor-authentication
[19]: https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-workload#workload-summary