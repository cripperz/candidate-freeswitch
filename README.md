# Playbook use to deploy Freeswitch

- Freeswitch deploy with version 1.4 cause problem with libyuv dependencie on Centos 6.x while version 7 does not have this problem.


## Roles

- **freeswitch-user**  Use to deploy user to remote host support ssh-key authentication support. ** Need to approve Bulk user add
- **freeswitch**  Use to Build and deploy freeswitch also install pre-binary require from source to target. 
- **freeswitch-iptables** config iptables *Need to Approve  
- **freeswitch-service** Use to Enable Service Start enable service  
- **freeswitch-user** Use to create user

## Design idea

My design idea try to split job function to small roles because it easy to read and maintain in the future.  

- Users add to diaplan you can config from playbook i use template to generate directory file ```$FS_HOME/conf/directory/default```
- Users add to system. 



## Usage

Edit host connection parameter at 'hosts' file then run. ( Below example ) 

```  ansible-playbook freeswitch-basic.yml --limit treebox-freeswith-candidate ```` 

If you want just deploy new source compile 

```  ansible-playbook freeswitch-basic.yml --limit treebox-freeswitch-candidate --tags=builds-deploy``` 

## Usage NOTE

- User variable you can edit in playbook 
- User 'password' in playbook ( freeswitch-basic.yml ) if empty ansible will generate for you. and you might to grep from log where
  log name 'ansible-work.log' locate this root playbook.

- Detail of role please look in foleder 'roles'


