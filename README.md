Starknet Full Node Pathfinder Ansible Deployment
=========

An Ansible role to deploy a Starknet full node using Pathfinder and Docker Compose.

Role Variables
--------------

* `starknet_pathfinder_l1_rpc` - The  url of an ethereum API RPC endpoint for the desired chain (mainnet and goerli are supported) 
* `starknet_pathfinder_install_dir` - The directory in which to install ... (Default: pathfinder)

Dependencies
------------

- [tobias_richter.apt_upgrade](https://github.com/tobias-richter/ansible-apt-upgrade)
- [geerlingguy.pip](https://github.com/geerlingguy/ansible-role-pip) to install pip on the machine
- [geerlingguy.docker](https://github.com/geerlingguy/ansible-role-docker) to install docker and docker compose on the machine

Example Playbook
----------------

  - hosts: servers
    roles:
       - role: starknet-pathfinder-ansible
    vars:
      starknet_pathfinder_l1_rpc: 'https://eth-goerli.g.alchemy.com/v2/...<ALCHEMY_API_KEY>...'           
   

License
-------

BSD 3-Clause License


