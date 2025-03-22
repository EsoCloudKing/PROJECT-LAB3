# Vulnerability Management Lab Utilizing Tenable Solutions

## Overview
This project focuses on creating a Vulnerability Management Lab using Tenable solutions to identify, assess, and remediate security vulnerabilities in modern IT environments. The lab will incorporate tools such as Tenable Nessus for vulnerability scanning for advanced analytics and reporting. It emphasizes best practices in vulnerability prioritization, remediation strategies, and compliance adherence. By simulating real-world scenarios, this lab provides a hands-on platform to strengthen proactive security measures, ensuring robust risk management and enhanced resilience against potential threats.

   **LAB SCHEMATIC DIAGRAM AND OVERVIEW**
 
   ![VMGT Draw](https://github.com/user-attachments/assets/ec525596-fa2e-4aaa-9dab-40e33738e0d0)

 
 ## Objective
The purpose of this Lab is to configure and implemented a comprehensive vulnerability management system to identify, assess, and mitigate security vulnerabilities in an IT infrastructure.
It will Cover the entire vulnerability management lifecycle, including vulnerability detection, assessment, prioritization, remediation, and reporting.

## Achievements
- Understanding what vulnerability management is.
-	Successfully Detected and Mitigated Critical Vulnerabilities, reducing the risk of exploitation.
- Enhanced the security posture of the lab environment through continuous monitoring and remediation.
- Understanding of compliance standards like DISA/STIG, CIS, PCI DSS etc.

    ### Tools Used For this Project
  - __Draw.io:__ for diagram mapping.
  - __Azure Vms:__
  - __Tenable Vulnerability Management__
  - __Powreshell:__ Allowing remote access to Host (Azure Vms)

     ## LAB STEPS
    
   **1: SET UP AND CONFIGURE ENVIROMENT**
 
- Provision, Configure a VM in Azure  and Prepare the VM for vulnerability scanning: In this step Azure vm was created, connected to via RDP.
Windows firewall was turned off, remote assess was configured via powershell with this Bash command line (Set-ItemProperty -Path
"HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System" -Name "LocalAccountTokenFilterPolicy" -Value 1 -Type DWord -Force).

![vm2](https://github.com/user-attachments/assets/6d61d91f-b7ae-4e10-bd09-e94fb9d8158e)



 **2: CONFIGURE TENABLE ENVIROMENT**

 - Set up a credentialed Tenable scan to identify all fundamental vulnerabilities, including compliance with DISA Windows 10 STIG v3r2 standards.

     ![copy Tennable](https://github.com/user-attachments/assets/a0dfd5ec-725b-4cae-8b4e-d1b13c9bbb0d)


 **3: BASELINE SCAN** 
 
- Conduct an initial scan to establish a baseline for vulnerabilities and compliance.
- Examine and interpret the scan results, paying particular attention to any failed STIGs. For this context of this Lab, will focus on the following vulnerabilities to Fail/Remediate.

  ![base scan 2](https://github.com/user-attachments/assets/d9d41a2b-33fb-4a33-a1d4-8e6fb975b7cd)


  

  **4: INTRODUCE VULNERABILITES** 
  Simulate Vulnerabilities:

- In this step, vulnerabilities like outdated software (e.g., download old Firefox version 110) were introduced or improperly configured settings (e.g., enabling the Guest Account) to intentionally trigger non-compliance with STIG ID WN10-SO-000010 by activating the Guest Account, unistalling previous windows update on our windows 10 VM.

-Then, a second scan was Performd to detect changes.

![vulnerabilities](https://github.com/user-attachments/assets/cd39746f-bc2a-485f-bd1a-68b5b02eb861)




  **5: REMEDIATION (Resolve Vulnerabilities and Ensure Compliance)**
  
- Uninstall outdated software to eliminate security risks.

- Adjust registry settings to expand the security event log size, enhancing event tracking and auditing capabilities.

- Deactivate the Guest account and rename it to reduce exposure to potential unauthorized access.

  - Deleted malicious file, closed some open ports etc.

- Apply the latest Windows updates to integrate critical security patches and maintain compliance with current standards.

  **Perform a final scan** to confirm remediation and ensure compliance.

  The documented outcomes of the performed scans are as follows:

  ![excell2](https://github.com/user-attachments/assets/5eddc6c9-51ab-4a78-aec9-7d6b58d30da1)

  
- Scan 1 (Baseline Establishment): The initial scan establishes a vulnerability baseline, serving as the foundation of our security posture assessment.

- Scan 2 (Threat Introduction): A sharp spike is detected after introducing several high-risk elements: a deprecated Firefox version, a malicious file with a known MD5 hash signature, disabled automatic Windows updates, and deleted critical patches.

- Scan 3 (Initial Remediation): Mitigation efforts show success—a decline in vulnerabilities emerges after removing Firefox, eradicating the malicious file, and applying necessary Windows updates.

- Scan 4 (Full Patching): A further drop is recorded post full-system patching and complete remediation of outdated components.

- Scan 5 (Final Remediation): The remediation process concludes with vulnerabilities returning to the original baseline threshold, restoring system integrity after persistent remediation activities.


  ## CONCLUSION

  This lab strengthened my expertise in the folowing;

- Vulnerability management and compliance,
- Equipping me with hands-on experience in leveraging Tenable solutions to safeguard systems and applications.
- Furthermore, it showcased my capability to effectively identify, assess, and remediate vulnerabilities across diverse IT infrastructures and networks.
  
 
      
