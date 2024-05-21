# 2-tier-project-using-docker

### Step1 :- Build  the images:-   
#### docker  build  -t  "tomcat"  -f  Dockerfile.tomcat  .  
#### docker  build  -t  "mysql"  -f  Dockerfile.mysql  .  


### Step2 :- Run  the images:-   
#### docker run -d  -p  8080:8080  tomcat  
#### docker run -d  -p  3306:3306  mysql  


### step3 :- Edit The IP Addresd of  context.xml  file  
#### docker exec  -it  <contaner_id>  /bin/bash 
#### cd /usr/local/tomcat/conf  
#### sed  -i  's/old-ip/new-ip/g'  context.xml   


----------------------------------------------------------------------
### Now edit the security group and access your application from  Web  
