# CSC519 - HW1

* Vagrantfile.server - The Vagrantfile used to setup server
* Vagrantfile.node1 - The Vagrantfile used to setup first node
* Vagrantfile.node2 - The Vagrantfile used to setup second node

As shown in demo, to run coffeemaker and the selenium tests successfully: 
* First run "ansible-playbook playbook.yml -i inventory -l main" and wait for application to start
	* Not mentioned in the demo, .my.cnf was updated to contain the config properties from mysql.cfg as well. 
	* playbook.yml was updated to retrieve password from an environment variable (instead of hardcoded as shown in demo, first running "export MYSQL_PASS=12345" on the server)
* Then, run "ansible-playbook playbook.yml -i inventory -l test" and wait for maven to complete tests
	* Not mentioned in the demo, to successfully enable port forwarding in the playbook, run "cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys" first to allow localhost to ssh itself

* Screencast - https://youtu.be/JMUPdHXVd_M