## Messenger App using Laravel and Vue.JS

[Youtube Tutorial link](https://www.youtube.com/watch?v=5sXmfwnxfjA&list=PLJpBh2VJhy5x2GKfkfIcn0r6P6uLat7xR)

#### [@WeCodeTutorials](https://twitter.com/WeCodeTutorials)
[![Logo](https://cdn.pbrd.co/images/HdwCut8.png)](https://www.youtube.com/channel/UCj9VatwdukZjNOnIKcpWcsA)

This project is made for my youtube tutorial on "Messenger App with Laravel, Vue.JS & Laravel Echo".

![App Example](https://media.giphy.com/media/8cARsYOk9DmCLZTZOb/giphy.gif)

## get it up and running.

After you clone this project, do the following:

```bash
# go into the project
cd Messenger-App-VueJS-and-Laravel

# create a .env file
cp .env.example .env

# install composer dependencies
composer update

# install npm dependencies
npm install

# generate a key for your application
php artisan key:generate

# create a local MySQL database (make sure you have MySQL up and running)
mysql -u root

> create database chat_db;
> exit;

# add the database connection config to your .env file
DB_CONNECTION=mysql
DB_DATABASE=chat_db
DB_USERNAME=root
DB_PASSWORD=

# run the migration files to generate the schema
php artisan migrate

# visit https://pusher.com and create a free app. then copy the keys into your .env file
PUSHER_APP_ID=your_pusher_app_id
PUSHER_APP_KEY=your_pusher_app_key
PUSHER_APP_SECRET=your_pusher_app_secret
PUSHER_APP_CLUSTER=your_pusher_cluster

# change the BROADCAST_DRIVER in your .env to pusher
BROADCAST_DRIVER=pusher

# seed your databse with some users and messages
php artisan db:seed

# run webpack and watch for changes
npm run watch
```

## Setup pusher

- Visit [Pusher website](https://pusher.com), sign up and create your first app (it's free).
- Next. copy the new keys to your `.env` file.
- Make sure the necessary settings are enabled
![Pusher app settings](https://user-images.githubusercontent.com/17595033/64108972-fb7b8a00-cd86-11e9-97ab-d2a3f7699b71.png)

Good Luck :)
