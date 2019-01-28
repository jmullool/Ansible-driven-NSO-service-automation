# Ansible-driven-NSO-service-automation

Sample Ansible playbooks driving NSO services, including basic IOS configuration changes and full vBranch CPE automation. Cisco dcloud lab environment will also be avaialble.


## Business/Technical Challenge

Increasingly customer IT departments are standardizing on Ansible to drive their automation needs given it's increasing use in server deployments. Ansible is a very powerful open-source tool historically focused at server and application automation. The Ansible community has recently been increasingly contributing new "module" code supporting more and more network device types. Customers are now beginning to ask why not just use Ansible for both their server/app and network automation needs. Yet, Ansible is missing critical features such as network-wide transactional support, config rollbacks, an off-net Database store and algorithms to only push needed changes. Actually, these Ansible IT customers could benefit from capabilities of both Ansible for server/app automation and Cisco's Network Service Orchestrator (NSO) for network automation.  

Customer Example:  Public Sector Customer
 
Customers Design Goals:  Customer is looking to re-architect their global campus/WAN network as well as optimize their operations to efficiently roll out new services and configuration changes. Thier design will support small, medium, and large sites, each of a “modular” and “repeatable” design.  The only variation will be in number of users supported, which will impact the choice of a small/medium/large design, driving a 1 or 2-tier topology, variation in port scale, hierarchy, etc. Services will remain identical, regardless of the size of the location. The primary transport will be IP/MPLS for WAN interconnection for any-to-any connectivity, globally. Target service offering will include both L3 and L2 segmentation to the edge/access service delivery points. Current operations leverages basic scripting with CLI but the customer IT team has just started to use Ansible to leverage the structured playbooks it offers and standardize on a single tool for both applicaitons and network. Yet, the customer is seeing gaps in the Ansible solution, which are key strengths of NSO.


## Proposed Solution

NSO provides certain values not included in Ansible. Incuding the use of YANG for service modeling, a "network wide" commit for services that span multiple devices, auto-generation of update and delete functions, a "source of truth" network DB to only push config chnages when needed and algorithms that provide idempotent operation behavior. In order to provide a "better together" solution, the NSO team has developed "NSO modules" for Ansible such that the customer IT departments can still use their Ansible playbook approach to drive both application and network services, but via very tight integration between Ansible and NSO. 

![alt text](https://github.com/jmullool/Ansible-driven-NSO-service-automation/pic1.tiff)

For our customer, NSO is being investigated as the development platform for all network automation, standardizing on the API’s offered from the NSO platform, rather than per-device.  Moving the plan forward, the combination of using Ansible on top of NSO is the north-star plan to automate, simplify, and reduce errors in operations for any CRUD operations throughout the network, and mainly on service offering deployments, specifically targeting L2 and L3 VPN as mentioned earlier.

The authors have built sample Ansible playbooks that leverage Ansible's NSO "modules" developed by Cisco's NSO Engineering team. This integration can access sample NSO services via NSO's JSON RPC API . All playbook and NSO service code will be posted on github along with a step-by-step lab guide documentation showing how to use the Ansible NSO modules wiht IOS, IOS-XR and vBranch/NFVIS devices. A Cisco dcloud lab environment is also available to quickly demonstrate the use of Ansible with NSO with the Cisco ENCS/vBranch product and various VNFs.  


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
