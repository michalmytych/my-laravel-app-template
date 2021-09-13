# My Laravel App Template

It's just a newly created Laravel v8.54 with some customizations,
which I used a lot and found useful while developing my projects.
* __RepositoryServiceProvider__ - to use repository design pattern, which add another
useful layer between Controllers/Services and data layer.
  <br>
* __ApiServiceProvider__ - for managing external APIs clients.
<br>
* __HasUuid trait__ - to use UUIDs instead of auto-incremented integer ids at models.
<br>
* __HasFailedValidationApiResponse__ - extension for FormRequests, overriding 
```failedValidation``` method - forms response with message & errors array in json format.
  
### Set-up
Clone repository and ```cd``` into it:
```bash
git clone https://github.com/michalmytych/my-laravel-app-template.git \
cd my-laravel-app-template
```
Next, copy ```.env.example``` file as ```.env``` and add your database credentials/other variables:
```bash
cp .env.example .env
```
After that, clear config cache:
```bash
php artisan config:cache
```
Run default migrations:
```bash
php artisan migrate
```
Now, you can run server:
```bash
php artisan serve
```
