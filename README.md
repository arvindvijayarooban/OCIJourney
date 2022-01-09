# OCIJourney
Detailing my OCI learning journey


Day 1: Setting up Tenancy and basic IAM
- Create a Free OCI tenancy account

- Setup basic IAM accounts to test IAM access 
  - OCI-ADMIN (to avoid using the root account)
  - Network-Admin
  - Storage-Admin

- Create groups based on roles
  - ociadmins
  - developers
  - networkadmins
  - storageadmins

-Create separate compartments and test policy assigment

 - Assign policies to groups and test policies effect for the created users 
 - Read documentation on IAM policies, the common ones 

Day 2: Trial run on OCI basics

- Create a test VCN  using the wizard
- Create a test VM in development compartment
- SSH into the test VM, install apache (httpd) , edit the index.html file
- Create NSG rules to allow HTTP connection to test VM

Day 3: Networking related learning

- Create a Load Balancer, provide test VM as backend and load the httpd index page from load balancer IP
- Create a new compartment for OCI labs
- Create a network peering between two VCNs in OCI labs compartment
- Test connectivity between two VMs using their private ips based on the peering

