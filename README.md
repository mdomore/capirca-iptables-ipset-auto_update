Ansible role for creating iptables rules from capirca definition files.

Capirca installation

If setuptools Python package is not installed on your system, install it: For example, the following commands installs the package with apt package manager.

sudo apt-get install python3-pip python3-setuptools

Next, to install capirca from source, clone the capirca repository and run its installer:

git clone https://github.com/google/capirca.git
cd capirca/
python3 setup.py install --user



You can also add ipset to manage fqdn access.

Ipset are updated with python scripts.