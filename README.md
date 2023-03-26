<!-- #laradock--laravel -->

# LARADOCK - LARAVEL 
***
## LARADOCK 

Laradock :  a full PHP phát triển môi trường của Docker . 

SETUP : 

### **DOCUMENT** : 

#### **List current running Containers**
<br> Cách dùng : 
	
	docker ps 

<br> Tưong tu nhu sau : 	
			
#### **Close all running Containers**
<br> Cách dùng : 

	docker-compose stop 

###### OR

	docker -compose  

Tuong tư nhu sau : 

#### **Delete all existing Containers**
<br> Cach dung : 

	docker-compose down

#### **Enter a Container**

-  First list the currently running containers with docker ps

- Enter any container using: 

<br>
    
	docker-compose exec {container-name} bash

#### **Build/Re-build Containers**

Cach dung : 

Cách 1 : dung de build tat ca .

	docker-compose build


Cách 2 : dung de build mot ***Container*** ban cần :	

	docker-compose build {container-name}

Tuơng tu nhu sau : 



#### **View the Log files**