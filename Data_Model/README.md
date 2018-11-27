# Deploy simple load-balanced services

Ansible playbook in this directory will create network infrastructure for a one arm F5 load-balancer
and add new simple laod balannced services

## Data model

Infrastructure data model **infrastructure.yml*** contain network informations to create basic connectivity on each load-balancer
Each load-balancer must have :
  * an interface
  * a vlan id
  * a subnet. Self-IP address will be derived from subnet information (first ip of the subnet)

Service data model **services.yml**  contain informations to create new services.
Requested informations are :
  * Service names. Object names (VIP and pool) are derived from the service name
  * protocol
  * virtual IP (last octet information)
  * nodes list (last octet information)
  VIP and nodes are represented with only the last octet of the IP address. They will inherit subnet information from infrastructure data model
