Migrate AWS Classic LB to Application LB
=========================================

This Ansible playbook automates the migration of AWS classic load balancers to application load balancers with all the configurations and some other features.


## Table of Contents
* **[Prerequisites](#Prerequisites)**
* **[How does it work?](#Howdoesitwork)**
* **[How to use?](#"How to use?")**

## Prerequisites
Before running the Ansible code you should install the following packages with the specified versions or later on the Ansible server.

* Ansible 2.7.0+
* aws cli 1.16.28+
* Python 2.7.15+
* boto3 1.12.24+
* botocore 1.12.24+
* boto 2.49.0+
* openshift 0.7.2+
* yq 2.1.2+
* jq 1.5-1+

**NOTE:** The code is tested with the exact versions mentioned above on Linux Mint 19.

## How does it work?

The playbook contains different tasks that executes the following points

* Migrate the classic load balancers to application load balancers
* Attach instances to the new load balancers
* Add a subdomain for the newly created load balancers
* Allow http to https redirection on the load balancer level
* Add a basic WAF support

## How to use?

* Choose the needed tasks and comment the other in the main.yml file
* Edit the vars and add your suitable values their
* In case of using the WAF support you should edit it to match your needs.
