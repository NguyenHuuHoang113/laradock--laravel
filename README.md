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

	docker-compose  

<br> Tuong tư nhu sau : 

	C:\Users\Hoang\laradock> docker-compose stop
	[+] Running 5/5
		- Container laradock-phpmyadmin-1        Stopped                                                                  2.1s
		- Container laradock-php-fpm-1           Stopped                                                                  1.3s
		- Container laradock-workspace-1         Stopped                                                                  3.0s
		- Container laradock-mysql-1             Stopped                                                                  2.3s
		- Container laradock-docker-in-docker-1  Stopped                                                                  1.4s


#### **Delete all existing Containers**
<br> Cach dung : 

	docker-compose down

<br> Tuong tu nhu sau : 

	C:\Users\Hoang\laradock> docker-compose down
	[+] Running 8/8
		- Container laradock-phpmyadmin-1        Removed                                                                                                      1.3s
		- Container laradock-php-fpm-1           Removed                                                                                                      0.2s
		- Container laradock-workspace-1         Removed                                                                                                      1.8s
		- Container laradock-mysql-1             Removed                                                                                                      1.8s
		- Container laradock-docker-in-docker-1  Removed                                                                                                      1.2s
		- Network laradock_backend               Removed                                                                                                      0.1s
		- Network laradock_default               Removed                                                                                                      0.2s
		- Network laradock_frontend              Removed                                                                                                      0.1s


#### **Enter a Container**

-  First list the currently running containers with docker ps

- Enter any container using: 

<br>
    
	docker-compose exec {container-name} bash

Vi du :  Nhap  ***MySQL container***

	C:\Users\Hoang\laradock> docker-compose exec mysql bash
	bash-4.4# exit
	exit

> **NOTE** : exit dung de thoai khoi ***CONTAINER***
#### **Build/Re-build Containers**

Cach dung : 

Cách 1 : dung de build tat ca .

	docker-compose build


Cách 2 : dung de build mot ***Container*** ban cần :	

	docker-compose build {container-name}

Tuơng tu nhu sau : 

	C:\Users\Hoang\laradock> docker-compose build
	[+] Building 0.0s (0/0)
	[+] Building 0.0s (0/0)
	[+] Building 0.0s (0/0)
	[+] Building 0.0s (0/0)
	[+] Building 0.0s (0/1)
	[+] Building 0.0s (0/0)
	[+] Building 1.9s (2/2)
		=> [internal] load build definition from Dockerfile                                                                                                   0.0s
	[+] Building 0.4s (1/1)
	[+] Building 0.3s (1/1)
	[+] Building 0.1s (0/1)
		=> [internal] load build definition from Dockerfile                                                                                                   0.1s
		=> => transferring dockerfile:                                                                                                                        0.0s
	[+] Building 2.3s (2/2)
		=> [internal] load build definition from Dockerfile                                                                                                   0.0s
		=> => transferring dockerfile: 33B                                                                                                                    0.0s
		=> [internal] load .dockerignore                                                                                                                      0.0s
		=> => transferring context: 2B                                                                                                                        0.0s
	[+] Building 0.3s (1/1)
	[+] Building 0.0s (0/0)
	[+] Building 2.5s (2/2)
		=> [internal] load build definition from Dockerfile                                                                                                   0.0s
	[+] Building 1.2s (1/1)
	[+] Building 0.3s (0/1)
		=> [internal] load build definition from Dockerfile                                                                                                   0.3s
	[+] Building 0.0s (0/0)
	[+] Building 0.0s (0/0)
	[+] Building 0.4s (1/1)
		=> [internal] load build definition from Dockerfile                                                                                                   0.3s
	[+] Building 0.0s (0/0)
	[+] Building 2.8s (2/2)
	[+] Building 0.7s (1/1)
		=> [internal] load build definition from Dockerfile                                                                                                   0.3s
		=> => transferring dockerfile: 125B                   
	....



#### **Start Containers**
Cach dung : 

	docker-compose start

<br> Tuong tu nhu sau : 

	C:\Users\Hoang\laradock> docker-compose start
		[+] Running 5/5
			- Container laradock-docker-in-docker-1  Started                                                                  1.2s
			- Container laradock-mysql-1             Started                                                                  1.3s
			- Container laradock-workspace-1         Started                                                                  1.1s
			- Container laradock-phpmyadmin-1        Started                                                                  0.7s
			- Container laradock-php-fpm-1           Started                                                                  0.5s


## **LARAVEL**

Laravel is a web application framework with expressive, elegant syntax .


#### CREATE A PROJECT :

<br> Cach dung : 


	composer create-project --prefer-dist laravel/laravel <YOURNAME_PROJECT>

<br> Tuong tu nhu sau : 

	C:\Users\Hoang>composer create-project laravel/laravel example-app
	Creating a "laravel/laravel" project at "./example-app"
	Info from https://repo.packagist.org: #StandWithUkraine
	Installing laravel/laravel (v10.0.4)
	- Installing laravel/laravel (v10.0.4): Extracting archive
	Created project in C:\Users\Hoang\example-app
	> @php -r "file_exists('.env') || copy('.env.example', '.env');"
	Loading composer repositories with package information
	Updating dependencies
	Lock file operations: 106 installs, 0 updates, 0 removals
	....
	C:\Users\Hoang\example-app>php artisan serve

	INFO  Server running on [http://127.0.0.1:8000].

	Press Ctrl+C to stop the server


> NOTE : php artisan serve là một lệnh của Laravel được sử dụng để khởi động một server phát triển cục bộ để chạy ứng dụng Laravel . 



#### CREATE ROUTES : 