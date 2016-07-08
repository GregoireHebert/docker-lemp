## Know your machine IP (only when using docker-machine)

``` shell
$ docker-machine ip
```

## add At least 2 hosts

in your hosts file
`/etc/hosts`
or
`C:/windows/System32/drivers/etc/hosts`

add
```
127.0.0.1ORDOCKERMACHINEIP project1.dev
127.0.0.1ORDOCKERMACHINEIP project2.dev
```

## Build and up

``` shell
$ docker-compose -f main.yml up
```

or with -d to hide any message and let the containers run in background

``` shell
$ docker-compose -f main.yml up -d
```

## Where ?

Nginx is configured this way : 
Ask project1.dev and it will load html/project/
Ask bar.dev and it will load html/bar/

by default come with project1 and project2

to manage your databases add 8080 port to any project url
ex: project1.dev:8080


## TODO

add side config file to combine with the main one to add optionnal services/containers
ex : node, elk, specific database such as mongodb or cassandra
