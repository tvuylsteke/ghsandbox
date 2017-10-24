# FastTrack for Azure Architectural Discussion Framework - Backup, Archive and Disaster Recovery Solution

## Table Of Contents

* [App & Data Migration](#app---data-migration)
* [Distributed Architecture](#distributed-architecture)
* [High Availability and Business Continuity / Disaster Recovery](#high-availability-and-business-continuity---disaster-recovery)
* [Monitoring &amp; Management](#monitoring--amp--management)
* [Performance &amp; Scalability](#performance--amp--scalability)
* [Security](#security)
* [Understand the Portfolio of applications are supported for Disaster Recovery](#understand-the-portfolio-of-applications-are-supported-for-disaster-recovery)

## 1 App & Data Migration   
* **What does your on-premises infrastructure look like? Hyper-V, VMware, Baremetal, etc?**

    Determine the supportability in DR migration. This will dictate the path that should be taken with Azure Site Recovery. For more information, see [Site Recovery Workload](https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-workload)

* **What types of Operating Systems are in place today for your applications?**

    Understand what Operating Systems will be supported for migration. Depending on the OS, the VHD may need to be lifted and shifted as Azure Site Recovery may not support the OS. For more information, see [Support For Replicated Machine OS Versions](https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-support-matrix-to-azure#support-for-replicated-machine-os-versions)

* **What types of workloads are you looking to backup? Do those workloads need to be filesystem or application consistent?**

    Depending on Filesystem or Application consistency, that will dictate the backup solution to leverage (Azure Backup Agent, Azure Backup Server, or Azure Backup for IaaS). For more information, see [Which Azure Backup Components Should I Use](https://docs.microsoft.com/en-us/azure/backup/backup-introduction-to-azure-backup#which-azure-backup-components-should-i-use)

## 2 App & Data Migration   
* **What does your on-premises infrastructure look like? Hyper-V, VMware, Baremetal, etc?**

    Determine the supportability in DR migration. This will dictate the path that should be taken with Azure Site Recovery. 
    
    * [Site Recovery Workload](https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-workload)

* **What types of Operating Systems are in place today for your applications?**

    Understand what Operating Systems will be supported for migration. Depending on the OS, the VHD may need to be lifted and shifted as Azure Site Recovery may not support the OS. 
    
    * [Support For Replicated Machine OS Versions](https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-support-matrix-to-azure#support-for-replicated-machine-os-versions)

* **What types of workloads are you looking to backup? Do those workloads need to be filesystem or application consistent?**

    Depending on Filesystem or Application consistency, that will dictate the backup solution to leverage (Azure Backup Agent, Azure Backup Server, or Azure Backup for IaaS). 
    
    * [Which Azure Backup Components Should I Use](https://docs.microsoft.com/en-us/azure/backup/backup-introduction-to-azure-backup#which-azure-backup-components-should-i-use)

## 3 App & Data Migration   
* **What does your on-premises infrastructure look like? Hyper-V, VMware, Baremetal, etc?**

    Determine the supportability in DR migration. This will dictate the path that should be taken with Azure Site Recovery. 
    
    &#10148; [Site Recovery Workload](https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-workload)

* **What types of Operating Systems are in place today for your applications?**

    Understand what Operating Systems will be supported for migration. Depending on the OS, the VHD may need to be lifted and shifted as Azure Site Recovery may not support the OS. 
    
    &#10148; [Support For Replicated Machine OS Versions](https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-support-matrix-to-azure#support-for-replicated-machine-os-versions)

* **What types of workloads are you looking to backup? Do those workloads need to be filesystem or application consistent?**

    Depending on Filesystem or Application consistency, that will dictate the backup solution to leverage (Azure Backup Agent, Azure Backup Server, or Azure Backup for IaaS). 
    
    &#10148; [Which Azure Backup Components Should I Use](https://docs.microsoft.com/en-us/azure/backup/backup-introduction-to-azure-backup#which-azure-backup-components-should-i-use)


## 4 App & Data Migration   

| **Question**| **Purpose**| **Relevant Documentation**   |  
|---|---|---|  
| **What does your on-premises infrastructure look like? Hyper-V, VMware, Baremetal, etc?**| Determine the supportability in DR migration. This will dictate the path that should be taken with Azure Site Recovery.| [https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-workload ][1]  |  
| **What types of Operating Systems are in place today for your applications? &nbsp;**| Understand what Operating Systems will be supported for migration. Depending on the OS, the VHD may need to be lifted and shifted as Azure Site Recovery may not support the OS. &nbsp;| [https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-support-matrix-to-azure#support-for-replicated-machine-os-versions ][2]  |  
| **What types of workloads are you looking to backup?<br><br>Do those workloads need to be filesystem or application consistent?**| Depending on Filesystem or Application consistency, that will dictate the backup solution to leverage (Azure Backup Agent, Azure Backup Server, or Azure Backup for IaaS).| [https://docs.microsoft.com/en-us/azure/backup/backup-introduction-to-azure-backup#which-azure-backup-components-should-i-use ][3]  |  

## App & Data Migration   

| **Question**| **Purpose**| **Relevant Documentation**   |  
|---|---|---|  
| What does your on-premises infrastructure look like? Hyper-V, VMware, Baremetal, etc?| Determine the supportability in DR migration. This will dictate the path that should be taken with Azure Site Recovery.| [https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-workload ][1]  |  
| What types of Operating Systems are in place today for your applications? &nbsp;| Understand what Operating Systems will be supported for migration. Depending on the OS, the VHD may need to be lifted and shifted as Azure Site Recovery may not support the OS. &nbsp;| [https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-support-matrix-to-azure#support-for-replicated-machine-os-versions ][2]  |  
| What types of workloads are you looking to backup?<br><br>Do those workloads need to be filesystem or application consistent?| Depending on Filesystem or Application consistency, that will dictate the backup solution to leverage (Azure Backup Agent, Azure Backup Server, or Azure Backup for IaaS).| [https://docs.microsoft.com/en-us/azure/backup/backup-introduction-to-azure-backup#which-azure-backup-components-should-i-use ][3]  |  