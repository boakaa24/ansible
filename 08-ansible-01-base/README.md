1.
```
TASK [Print fact] **************************************************************
ok: [localhost] => {
    "msg": 12
```
2. 
```
TASK [Print fact] **************************************************************
ok: [localhost] => {
    "msg": "all default fact"
```
3.
```
root@andrew-VirtualBox:~/git_rep/ansible/playbook# docker ps
CONTAINER ID   IMAGE            COMMAND       CREATED          STATUS             PORTS     NAMES
1145d6df75f5   ubuntu:18.04     "bash"        21 minutes ago   Up 21 minutes                ubuntu
0bcb1186252e   centos:centos7   "/bin/bash"   2 hours ago      Up About an hour             centos7
```
4.
```
ok: [ubuntu] => {
    "msg": "deb"
```
```
ok: [centos7] => {
    "msg": "el"
```
6.
```
ok: [ubuntu] => {
    "msg": "deb default fact"
```
```
ok: [centos7] => {
    "msg": "el default fact"
```
7.
```
 ansible-vault encrypt /root/git_rep/ansible/playbook/group_vars/deb/examp.yml
 ansible-vault encrypt /root/git_rep/ansible/playbook/group_vars/el/examp.yml
 ```
 9.
 ```
 ansible-doc -t connection -l
 ```
 10.
```
 loc:
    hosts:
      localhost:
        ansible_connection: local
```
11.
```
ok: [localhost] => {  
    "msg": "all default fact"
```
