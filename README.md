# ansible-molecule-f5
Molecule example using F5 LTM. This repo only contains a simple role that provisions an F5 LTM pool. Within the role there is a `molecule/default` directory containing a single [Molecule](https://ansible.readthedocs.io/projects/molecule/) scenario to test the role, which runs against ephemeral infrastructure in AWS using Molecule's [EC2 driver](https://github.com/ansible-community/molecule-plugins/tree/main/doc/ec2). Note that the `create.yml` and `destroy.yml` files are provided by the driver.

Prerequisites to running this:
* Have collections and their dependencies installed: `collections/requirements.yml`
* Have Molecule installed
* Have AWS credentials available in environment
* In your AWS environment, you need to already have a VPC and subnet created that you want to use for this. These details go into `molecule.yml`.

Running a test:
* `cd roles/f5_pool`
* `molecule test`
