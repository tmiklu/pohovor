# Tasks 

## 1. Run Hello World in nginx container 

copy following commands to do clone repo, cd to pohovor, build, run and stop container: 
```
git clone https://github.com/tmiklu/pohovor.git && echo && cd pohovor && docker build -t web:latest . 1> /dev/null && \
docker run -d web:latest | while read line ; do docker exec -i $line curl -s localhost ; docker stop $line 1> /dev/null ; done ; \
echo
```

result in output: 
`Hello World` 

## 2. Find duplicate uid in /etc/passwd 

copy cmd and hit enter: 

`awk -F":" 'n=x[$3]{print n"\n"$1"\t"$3;} {x[$3]=$1"\t"$3;}' /etc/passwd` 

`awk -F\: 'a[$3]++{print $3}' /etc/passwd`

all
