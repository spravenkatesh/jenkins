# jenkins

## Jenkins Host key verification failed for jenkins SCM pipleine jobs.

* create appropriate SSH key pairs for communication between Jenkins and Github using `ssh-keygen` utility and store the keys under `/var/lib/jenkins/.ssh/` dir as `jenkins` user
* add the public key from `/var/lib/jenkins/.ssh/` to Github `SSH & GPG` keys section under settings
* login as `jenkins` user from host
* execute below command
  ```
  git ls-remote -h -- git@github.com:spravenkatesh/jenkins.git HEAD
  ```
* accept the standard SSH warning when first connecting to a new host via SSH by typing `yes`.
* this will add remote git repository SSH public key in known_hosts file
* verify under Jenkins job-configuration no error is seen at SCM block. 
* if docker plugin is used for deploying agents, allow jenkins to deploy containers by accepting SSH connection `accept first-connection`, if known_hosts is not copied while building image.
