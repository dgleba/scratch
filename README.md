

# FoxUSA/OpenNote  Offline Progressive Web App



https://github.com/FoxUSA/OpenNote/blob/master/docs/Install.md

_____________


## -

made d..compose.yml

sftp://pmdsdata4/srv/dkr/opennote407/docker-compose.yml


_____________

## -

I went here and setup single node.

http://pmdsdata4:5984/_utils/#/setup

see pic

_____________
## -

http://pmdsdata4:5984/_utils/#_config/nonode@nohost/cors

enable cors

change from "restrict to specific domains" to "all domains"


got error see pic, but then go back in and it is ok.

  error could not save cors. invalid utf-8 json.

go to another url and back and it is all OK.



_____________

## ---


http://pmdsdata4:5984/_utils/#_config/nonode@nohost
  
  ```
  and set require_valid_user to true.
  in two spots
  ```

  
_____________

##  - - -

if need be..

pmdsdata4:5984/_utils/#login


_____________


## db list in couch web page

http://pmdsdata4:5984/_utils/#/_all_dbs


## Sometimes I created the db myself

create db - opennote  


_____________


##  replication

works.

Example url..

http://usera:userap@pmdsdata4:5984/opennote


eg:
http://admin:password@127.0.0.1:6984/opennote

_____________

## visit site at..

works.

http://pmdsdata4:6080/OpenNote/#/

junk..

  ```note/c9102126-0be8-4b46-88f3-73ad9491b6fe?rev=1-646f56fd0c1e49489a99fc1eb49b1cb0```



----------------------------------------------------


## clean up all containers - stuff and data


```
docker kill $(docker ps -q)
docker rm --force $(docker ps -a -q)
docker volume rm $(docker volume ls -qf dangling=true)
docker network ls  
docker network ls | grep "bridge"   
docker network rm $(docker network ls | grep "bridge" | awk '/ / { print $1 }')
#
# Careful, is there any data in these volumes you need??
#
docker volume rm $(docker volume ls -qf dangling=true)
```

                                sudo rm minio407 -rf
    albe@pmdsdata4:/srv/dkr/data$    sudo rm -rf couch407/


----------------------------------------------------
