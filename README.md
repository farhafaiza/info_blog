
# info_blog

Info_Blog is an incomplete blog website. It's a website for the project of DBMS Lab.
Which have Features:
1. Login
2. Registration
3. CRUD Operations (Blog App) [Also can upload an image for a post]
Framework: Laravel 
A Full description of the website has been described in the video:
https://drive.google.com/file/d/1QDH0G5Hwl_voxXWN6yq2T6SsjrSBgE1e/view?usp=sharing
## Deployment

To deploy this project run

Create a laravel project
```bash
  composer create-project laravel/laravel=9.1 info_blog
```

Install laravel breeze package
```bash
  composer install
```
```bash
  npm install
```
```bash
  npm run dev
```
Create a database and update .env file with your database credentials and then run migration
```bash
  php artisan migrate
```
Create seed
```bash
  php artisan db:seed
```
Run the project
```bash
  php artisan serve
```


## Create Admin Panel
Create a modal for admin
```bash
  php artisan make:model Admin -m
```
1.Copy users columns to admin migration file

2.Copy all text from User model to Admin model and set the class name Admin.

3.Create all necessary routes for admin authentication

4.create Admin folder on controller

5.controller => Admin => Auth => copy AuthenticatedSessionController.php from user Auth

6.AuthenticatedSessionController.php =>

7.go to RouteServiceProvider and do it:

8.create admin folder on views, create auth folder on admin and copy-paste login view from user > auth

9.You can specify the admin login page

10.to view login link paste it in welcome page anywhere.

11.set action in admin login form.

12.Create a seed for admin.

13.go to DatabaseSeeder.php and do it:

14.seed the database

Creating guard:

1.go to Admin model and do it:

2.go to config => auth.php =>

3.go to middleware => RedirectIfAuthenticated.php =>

4.App => Http => Request => Auth => LoginRequest.php > duplicate and set name AdminLoginRequest.php > change the classname to AdminLoginRequest >

5.create admin dashboard by duplicating user dashboard

6.create HomeController

7.copy user layout view folder to admin

8.App => view => components => duplicate AppLayout.php to AdminLayout.php and change class name to AdminLayout

9.change layouts file view from user to admin

10.Create middleware for admin

11.go to App => Http => Kernel =>

## Acknowledgements

 - [Dashboard Templates](https://drive.google.com/file/d/1t293DeI19LvLuQlUBDLVesCZQjdnAtbb/view)
 - [Followed video](https://www.youtube.com/watch?v=7Q-mYjXEZTs&list=PLJfHaHU9dKhaA_QY2SH76u9GpF6WZnUx5&index=3)


## Tech Stack

**Client:** Laravel, HTML, Bootstrap

**Server:** VS code

