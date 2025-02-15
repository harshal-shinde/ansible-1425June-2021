### Make sure your containers are in running state
```
docker ps
```

### In case your container are in Exited state, you may see them with below command
```
docker ps -a
```

### In case they are Exited, you need to start them
```
docker start $(docker ps -aq)
```

### Running the ping playbook
```
ansible-playbook -i inventory ping.yml
```

### Running the install vim playbook
```
ansible-playbook -i inventory install-vim.yml
```

### Running the install vim playbook with verbosity enabled
```
ansible-playbook -i inventory install-vim.yml -vvvv
```

### Running the install nginx playbook
```
ansible-playbook -i inventory install-nginx-playbook.yml
```

### Check if you are able to access the custom web page from 'ubuntu1', 'ubuntu2', 'centos1' and 'centos2' ansible nodes respectively
```
curl http://localhost:8001
curl http://localhost:8002
curl http://localhost:8003
curl http://localhost:8004
```
Notice, the hostname variable gives different values depending on the ansible node.
