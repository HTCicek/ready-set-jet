# Ready Set Jet

#### BLUF

Find the docker images [here](https://hub.docker.com/repository/docker/htcicek/ready-set-jet), on dockerhub!

Watch the demo on [vimeo](https://vimeo.com/391058350)!

## What is Ready Set Jet?

Ready Set Jet is a responsive web app made to tailor a user's sleep schedule according to their flights.

## Run it

### docker (recommended)

```sh
# all you need is the docker-compose file

curl https://raw.githubusercontent.com/HTCicek/ready-set-jet/master/docker-compose.yml > docker-compose.yml
docker-compose up

# don't mind the connection messages from api_1:
# # docker-compose.yml command for backend sleeps until postgres is accepting connections in order to migrate.
```
Enter the web client on localhost:3000

### locally

```sh
git clone https://github.com/HTCicek/ready-set-jet.git

# backend setup
cd ready-set-jet/ready-set-jet-backend
rails db:create && rails db:migrate && rails db:seed
rails s -d

# frontend setup
cd ../ready-set-jet-frontent
yarn && yarn start
```

## Application Info

### Web Client

Built with react, utilizing Semantic UI with Material design principles (and theme)!

Currently timezone calculations are performed in the client as well, using Moment.js

### Backend

Built with Ruby on Rails.

### DB

PostgreSQL, with seed data from [OpenFlights](https://openflights.org/data.html)

## TODO

- Separate Moment.js and timeywimey.js into their own service to minimize clientside calculations

