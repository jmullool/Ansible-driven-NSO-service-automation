# Ansible-driven-NSO-service-automation

Sample Ansible playbooks driving NSO service automation with dcloud lab environment


## Business/Technical Challenge

Increasingly Customer IT departments are standardizing on Ansible to drive their automation needs. Ansible is a very powerful open-source tool historically focused at server and application automation. The Ansible community has been increasingly contributing module code supporting new network device types. Customers are now beginning to ask why not just use Ansible for all their network automation needs versus using Cisco's Network Service Orchestrator (NSO) product. 

Customer:  Public Sector Customer
 
Customers Design Goals:  Customer is looking to re-architect their global campus/WAN network as well as optimize their operations and how efficiently they roll out new services and configuration changes.  Design will support small, medium, and large designs, each of a “modular” and “repeatable” design.  The size only varying in number of users supported, which will impact them to a small/medium/large design, as well as from a 1 to 2-tier topology, variation in port scale, hierarchy, etc, but services will remain identical, regardless of the size of the location.  Primary transport will be IP/MPLS for WAN interconnection for any-to-any connectivity, globally, and intra-campus is still being evaluated. Target service offering will include both L3 and L2 segmentation to the edge/access service delivery points. Current operations leverages basic scripting with CLI.  The customer has just started to use Ansible to leverage the structured playbooks it offers and standardize on a single tool for both applicaitons and network. Yet, the customer is seeing gaps in the Ansible solution, which are key strengths of NSO.


## Proposed Solution

NSO provides certain values not included in Ansible. Incuding the use of YANG for service modeling, a "network wide" commit for services that span multiple devices, auto-generation of update and delete functions, a "source of truth" network DB to only push config chnages when needed and algorithms that provide idempotent operation behavior. In order to provide a "better together" solution, the NSO team has developed "NSO modules" for Ansible such that the customer IT departments can still use their Ansible playbook approach to drive both application and network services, but via very tight integration between Ansible and NSO. 


For our customer, NSO is being investigated as the development platform all automation will be developed towards, standardizing on the API’s offered from the NSO platform, rather than per-device.  Moving the plan forward, the combination of using Ansible on top of NSO is the north-star plan to automate, simplify, and reduce errors in operations for any CRUD operations throughout the network, and mainly on service offering deployments, specifically targeting L2 and L3 VPN as mentioned earlier.

The authors have built sample Ansible playbooks that leverage NSO sample services via NSO's JSON RPC API. All playbook and service code will be posted on github along with a step-by-step lab guide docuementation showing how to use the NSO modules and a dcloud lab environment demonstrating their use with NSO along with products such as Cisco's ENCS product and various VNFs.  


### Cisco Products Technologies/ Services

Our solution will levegerage the following Cisco technologies

* Network Service Orchestrator (NSO
* Enterprise Network Compute System (ENCS)
* ISRv/CSR1000v
* ASR9Kv

## Team Members

* John Mullooly <jmullool@cisco.com> - Americas Service Provider
* Craig Hill <crhill@cisco.com> - Public Sector 


## Solution Components


<!-- This does not need to be completed during the initial submission phase  

Provide a brief overview of the components involved with this project. e.g Python /  -->


## Usage

<!-- This does not need to be completed during the initial submission phase  

Provide a brief overview of how to use the solution  -->



## Installation

How to install or setup the project for use.


## Documentation

Pointer to reference documentation for this project.


## License

Provided under Cisco Sample Code License, for details see [LICENSE](./LICENSE.md)

## Code of Conduct

Our code of conduct is available [here](./CODE_OF_CONDUCT.md)

## Contributing

See our contributing guidelines [here](./CONTRIBUTING.md)
