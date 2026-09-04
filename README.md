# Basic Employee Onboarding (AD)(RBAC)

## Problem Statement
Northstar Medical Group is a fictional fast-growing healthcare company that delegated its identity lifecycle workflow to a third-party MSP. This worked fine while the company was small, but as Northstar grew, the gaps became obvious. There was no RBAC policy in place, so access was assigned ad-hoc with no consistent standard tied to job role. There were no audit trails to track who had access to what or why. Combined with the fact that Northstar handles protected health information, this created real HIPAA compliance risk that could expose the company to significant fines in an audit.


## Solution Overview
I built a basic employee onboarding pipeline in Active Directory to replace the ad-hoc process. This started with creating a new domain (NMG.com) as the foundation, then designing an organizational unit structure that separated departments so access could be managed by group rather than by individual. I set up an RBAC matrix using security groups tied to each OU, ensuring users were granted access only according to their role, nothing more and nothing less. To validate the model, I simulated a mock support ticket where a user had been provisioned the wrong level of access, then used the OU and group structure to trace the issue back to its root cause and correct it. The result is a provisioning process where adding a user to the right OU and group automatically secures their access, instead of relying on manual, inconsistent configuration.
## Video Walkthrough
https://www.youtube.com/watch?v=EBR0ddXkFZg

## Tools Used
* Windows Server
* Active Directory Domain Services
* VirtualBox
* UTM
* RBAC
* GitHub

## Project Timeline
* Day 1: Domain creation and domain controller promotion
* Day 2: Organizational unit and security group design
* Day 3: User provisioning and RBAC implementation
* Day 4: Incident response and resolution (NMG-0047)
* Day 5: Documentation and case study packaging

## Key Accomplishments
* Built NMG.com domain from scratch
* Provisioned 15-20 user accounts using the OU/group model, then diagnosed and resolved a live access ticket (NMG-0047) by identifying incorrect OU placement and missing security group membership as root cause
* Designed a 4-OU structure with matching security groups, replacing an unstructured, manually-managed environment


