# ansible-handson
play Ansible


## How to do?

First, docker-compose up and ceate containers.  
One is ansible container, and the other is server container.  

```
    $ docker-compose up -d  
    $ docker-compose exec ansible /bin/bash  
    # ansible-playbook -i inventry.ini playbook.yml  
```

Then, confirm the file is created and there is text.  

```
    # ssh server  
    # vi hoge.text  
    you can see: `hogehoge`  
```

## References
- https://qiita.com/Naoto9282/items/39eeefa5de652b857372
