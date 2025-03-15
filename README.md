# Vulnerability Management Lab Utilizing Tenable Solutions

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

      **LAB SCHEMATIC DIAGRAM AND OVERVIEW**

    ## LAB STEPS
    **1: SET UP AND CONFIGURE ENVIROMENT**

    - Provision, Configure a VM in Azure  and Prepare the VM for vulnerability scanning: In this step Azure vm was created, connected to via RDP.
       Windows firewall was turned off, remote assess was configured via powershell with this Bash command line (Set-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System" -Name "LocalAccountTokenFilterPolicy" -Value 1 -Type DWord -Force)
      Azure vm image

 **2: CONFIGURE TENABLE ENVIROMENT**

 - Set up a credentialed Tenable scan to identify all fundamental vulnerabilities, including compliance with DISA Windows 10 STIG v3r2 standards.
     TENABLLE IMAGE

 **3: BASELINE SCAN** 
 
- Conduct an initial scan to establish a baseline for vulnerabilities and compliance.
- Examine and interpret the scan results, paying particular attention to any failed STIGs. For this context of this Lab, will focus on the following vulnerabilities to Fail/Remediate and STIGS to Pass/Fail/Remediate below:

  **Vulnerabilities:** List and Image(below)

 **STIGs Compliance:** List and Image(below)

  **4: INTRODUCE VULNERABILITES** 
  Simulate Vulnerabilities:

- In this step, vulnerabilities like outdated software (e.g., download Firefox version 110) were introduced or improperly configured settings (e.g., enabling the Guest Account) to intentionally trigger non-compliance with STIG ID WN10-SO-000010 by activating the Guest Account.

-Then, a second scan was Performd to detect changes.

Image troducing vulnerabilities below

  **5: REMEDIATION (Resolve Vulnerabilities and Ensure Compliance)**
  
- Remove outdated software to eliminate security risks.

- Adjust registry settings to expand the security event log size, enhancing event tracking and auditing capabilities.

- Deactivate the Guest account and rename it to reduce exposure to potential unauthorized access.

- Apply the latest Windows updates to integrate critical security patches and maintain compliance with current standards.

  **Perform a final scan** to confirm remediation and ensure compliance.

- the documented results of the scans can be found below: 
  excell Image and graph below

     ## CONCLUSION

  This lab strengthened my expertise in the folowing;

- Vulnerability management and compliance,
- Equipping me with hands-on experience in leveraging Tenable solutions to safeguard systems and applications.
- Furthermore, it showcased my capability to effectively identify, assess, and remediate vulnerabilities across diverse IT infrastructures and networks.
  
 
      
