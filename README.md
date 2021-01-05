# Run Hello World webserver in nginx 

copy following commands to do clone repo, cd to pohovor, build, run and stop container: 
```
git clone https://github.com/tmiklu/pohovor.git && echo && cd pohovor && docker build -t web:latest . 1> /dev/null && \
docker run -d web:latest | while read line ; do docker exec -i $line curl -s localhost ; docker stop $line 1> /dev/null ; done ; \
echo
```

result in output: 
`Hello World` 

all
