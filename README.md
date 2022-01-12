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

Day 4: Learn about Compute
- Create two test compute instances 
- Created putty access to one of the instance then attempted to ssh between instances 
- Fun fact: OCI default user, opc has no password created, hence if you messed up with the ssh keys, essentially you're locked out of the instance
 so create a password for the opc user , ssh keys needs better handling and understanding 
- I attempted to scp files between instances and got locked out due to ssh mismatch , tried to recover by attaching boot volume of instance to another and modifying the ssh key entries but nothing happening there
- Deleted locked out instance, restart again, this ssh handling needs more care and attention, best I think is to keep one set of public key and private key
- Created new compute and rectified all the ssh related errors I did earlier, scp files from one instance to another
-  created a public facing load balancer, added the instances to the backend

Day 5: Testing network accessibility of OCI instances
- Created a custom VNC via the portal and was unable to ssh to the compute instance within that VNC 
- Figured out that I didn't create a IGW, created one and associated it to a route table, was able to ssh and ping that instance public IP


