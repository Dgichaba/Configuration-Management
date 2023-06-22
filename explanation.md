# Ansible playbook Explanation
## Description
By default, Ansible executes each task in order, one at a time, against all machines matched by the host pattern. Each task executes a module with specific arguments. When a task has executed on all target machines, Ansible moves on to the next task. You can use strategies to change this default behavior. Within each play, Ansible applies the same task directives to all hosts. If a task fails on a host, Ansible takes that host out of the rotation for the rest of the playbook.

## Roles
### Vars
Variable in playbooks are very similar to using variables in any programming language. It helps you to use and assign a value to a variable and use that anywhere in the playbook. One can put conditions around the value of the variables and accordingly use them in the playbook.

In my case, I have 3 variables one storing the client image anothr the backend image and the last for the app folder
### Tasks
Playbooks are collections of one or more plays that are performed in a certain order. A play is an ordered sequence of tasks performed against hosts from your inventory. The task to be done is defined by plays. Each play has a list of hosts to configure and responsibilities to complete.

I had several tasks as highlighed below:
* Clone the repository
* Update the cache
* Install packages
* Add Docker official GPG key
* Add docker repository
* Install docker packages
* Install the Docker module for Python, required by ansible
* Pull the client image
* Pull the backend image
* Create app folder
* Copy docker-compose file
* Start containers

