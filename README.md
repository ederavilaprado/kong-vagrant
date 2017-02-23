# kong-vagrant
Kong + Vagrant used to aid in the local development of apis (who works behind kong in production env)

Machine IP: 192.168.33.10

## How to

**Start/Create**
```bash
$ vagrant up
```

**Connect SSH**
```bash
$ vagrant ssh
```

**Suspend, so you can continue your work later from where you stoped**
```bash
$ vagrant suspend
```

**Destroy**
```bash
$ vagrant destroy
```

**Connect to postgres**  
tip: inside the machine `vagrant ssh` you don't need to provide the ip
```
$ psql -U me -d kong -h 192.168.33.10
```

## Pros

- Clean dev environment
- Postgres accessible outside


## Thanks to

- https://github.com/jackdb/pg-app-dev-vm
- https://github.com/Mashape/kong-vagrant
- https://github.com/PGBI/kong-dashboard
