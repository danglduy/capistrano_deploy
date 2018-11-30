# Purpose
This repo is a capistrano-based deploy tool
# Prepare
- Install rbenv and ruby on client
- Install prerequisites on the server: rbenv, ruby, nginx-passenger, mysql/pg
# Deploy
- Generate SSH key on the client, add public key to "deploy" user on the server.
- Copy .env.example to .env. Set project and server information
- Run:
```Ruby 
# You gonna fail first time
bundle exec cap production deploy
```
- On the server: go to /home/deploy/[project name]/, copy master.key and 
database.yml to shared/config/ folder. Config database.yml following your database
setup.
- Run the command again
- Setup nginx-passenger for the project
