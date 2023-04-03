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

<br> Tương tự như sau : 	
			
#### **Close all running Containers**
<br> Cách dùng : 

	docker-compose stop 

###### OR

	docker-compose  

<br> Tương tự như sau  : 

	C:\Users\Hoang\laradock> docker-compose stop
	[+] Running 5/5
		- Container laradock-phpmyadmin-1        Stopped                                                                  2.1s
		- Container laradock-php-fpm-1           Stopped                                                                  1.3s
		- Container laradock-workspace-1         Stopped                                                                  3.0s
		- Container laradock-mysql-1             Stopped                                                                  2.3s
		- Container laradock-docker-in-docker-1  Stopped                                                                  1.4s


#### **Delete all existing Containers**
<br> Cách dùng : 

	docker-compose down

<br> Tương tự như sau : 

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

Ví dụ  :  Nhập  ***MySQL container***

	C:\Users\Hoang\laradock> docker-compose exec mysql bash
	bash-4.4# exit
	exit

> **NOTE** : nhập ***exit*** để thoát khỏi  ***CONTAINER***
#### **Build/Re-build Containers**

Cách dùng : 

Cách 1 : dùng để build tất cả  .

	docker-compose build


Cách 2 : dùng để build một  ***Container*** bạn cần :	

	docker-compose build {container-name}

Tương tự như sau : 

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

<br> Cách dùng : 

	docker-compose start

<br> Tương tự như sau : 

	C:\Users\Hoang\laradock> docker-compose start
		[+] Running 5/5
			- Container laradock-docker-in-docker-1  Started                                                                  1.2s
			- Container laradock-mysql-1             Started                                                                  1.3s
			- Container laradock-workspace-1         Started                                                                  1.1s
			- Container laradock-phpmyadmin-1        Started                                                                  0.7s
			- Container laradock-php-fpm-1           Started                                                                  0.5s


## **LARAVEL**

Laravel : một  web yêu cầu framework với expressive, elegant syntax .


#### CREATE A PROJECT :

<br> Cách dùng : 


	composer create-project --prefer-dist laravel/laravel <YOURNAME_PROJECT>

<br> Tương tự như sau  : 

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
***
## **ROUTING** : 

1.  **Basic Routing** : 

	<br> Cách dùng : 

		Route::get('URL', funtion(){
			Return ('command');
		} );

	<br>Tương tư như sau : ở đây tôi muốn hiện thị **Command** :"HELLO LARAVEL" :
		<br> - Đầu tiên , cần tạo cho một ***[PROJECT](#create-a-project)***.
		<br> - Tiếp theo , truy cập vào **route** --> **web.php** .
		<br> - Khai báo route . 
		<?php

		use Illuminate\Support\Facades\Route;

		/*
		|--------------------------------------------------------------------------
		| Web Routes
		|--------------------------------------------------------------------------
		|
		| Here is where you can register web routes for your application. These
		| routes are loaded by the RouteServiceProvider and all of them will
		| be assigned to the "web" middleware group. Make something great!
		|
		*/

		Route::get('/', function () {
			return view('welcome');
		});

		Route::get('/hello', function () {
			return 'hello laravel';
		});


	<br> - Chạy  ***php artisan serve*** để khởi chạy web

	<!-- hình ảnh  -->

2. **Available Router Methods** : 

	<br>Đây là những ROUTER cho phép bạn được khai báo : 

		Route::get($uri, $callback); <cho phép truy cập một tài nguyên được chỉ định bởi URI>
		Route::post($uri, $callback);<cho phép tạo mới một tài nguyên mới>
		Route::put($uri, $callback);<cho phép cập nhật một tài nguyên đã tồn tại>
		Route::patch($uri, $callback);<cho phép cập nhật một phần của một tài nguyên đã tồn tại>
		Route::delete($uri, $callback);<cho phép xóa một tài nguyên đã tồn tại>
		Route::options($uri, $callback);<cho phép lấy thông tin về các tùy chọn được hỗ trợ trên một tài nguyên nhất định>

	Bên cạnh đó , còn có ***"match"*** and ***"any"***
	<!-- lý thuyết về match  -->

3. **View route** : dùng để xem trình bày của bạn 
	<br> Cách dùng :

		Route::view('/URL', 'COMMAND');

	<br> Tương tự như sau : 
	

<!-- hình ảnh  -->

4. **The route list** : dùng để check list route 

	<br> Cách dùng : 

		php artisan route:list

	Tương tự như sau : 

		D:\welcom>php artisan route:list
		GET|HEAD   / ................................................................
		POST       _ignition/execute-solution ...................................... ignition.executeSolution › Spatie\LaravelIgnition › ExecuteSolutionController
		GET|HEAD   _ignition/health-check .......................................... ignition.healthCheck › Spatie\LaravelIgnition › HealthCheckController
		POST       _ignition/update-config .......................................... ignition.updateConfig › Spatie\LaravelIgnition › UpdateConfigController
		GET|HEAD   api/user ..........................................................
		POST       form-submit .......................................................
		GET|HEAD   sanctum/csrf-cookie ............................................... sanctum.csrf-cookie › Laravel\Sanctum › CsrfCookieController@show


5. **Middleware**: cung cấp một cơ chế thuận tiện để kiểm tra và lọc các yêu cầu HTTP khi chúng nhập vào ứng dụng của bạn

	Cách dùng : 

		php artisan make:middleware <Name_Middleware>

	<br> Tương tự như sau : 

		D:\chaomung> php artisan make:middleware testlaravel

		INFO  Middleware [D:\chaomung\app/Http/Middleware/testlaravel.php] created successfully.

6. **Controller** : một lớp PHP đại diện cho một tác vụ xử lý yêu cầu HTTP

	Cách dùng : 

		php artisan make:controller <Name_Controller> 

	Tương tự như sau : 
		Ví dụ tạo một cái controller có tên là ***testlaravel*** : 

		D:\chaomung> php artisan make:controller testlaravel

	INFO  Controller [D:\chaomung\app/Http/Controllers/testlaravel.php] created successfully.

	<br>

7. Artisan là một công cụ dòng lệnh trong Laravel, cho phép bạn tạo các task, migrations, models, controllers và các cấu trúc khác một cách nhanh chóng và dễ dàng . 





8. Respose :  một thông điệp trả lời của máy chủ web cho client 

	<br> Cách dùng : 


	- Tạo nội dung với HTML :

			return response('<h1>Hello World</h1>');

	- Tạo với View : 


			return view('welcome');

	- Tạo một response với một redirect : 

			return redirect('/home');


9. **Blade Templates** là một công cụ mạnh mẽ để quản lý các giao diện người dùng trong các ứng dụng web được viết bằng PHP
<br>
Cách dùng : 
<br>
	<!-- Switch Statements :cung cấp một cú pháp đơn giản và dễ đọc cho việc tạo các mẫu.
	Cú pháp : @directive

	<!-- Kế thừa mẫu: cho phép các mẫu được kế thừa, giúp giảm thiểu việc lặp lại mã. -->

	<!-- If Statements : hỗ trợ các câu lệnh điều kiện và vòng lặp để điều khiển cách hiển thị các phần của giao diện người dùng. -->

	<!-- Raw PHP : cho phép chèn mã PHP vào các mẫu để tạo các hành động động. --> 
	
	@auth
		// The user is authenticated...
	@endauth
	
	@guest
		// The user is not authenticated...
	@endguest


If Statements : 

	@if (count($records) === 1)
		I have one record!
	@elseif (count($records) > 1)
		I have multiple records!
	@else
		I don't have any records!
	@endif