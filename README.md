# Ready Set Jet

#### BLUF

Find the docker image [here](dockerhub.com), on dockerhub!

## What is Ready Set Jet?

Ready Set Jet is a responsive web app made to tailor a user's sleep schedule according to their flights.

## Run it!

```sh
git clone https://github.com/HTCicek/ready-set-jet.git
cd ready-set-jet
docker-compose build && docker-compose up

# don't mind the connection messages from api_1:
# # docker-compose.yml command for backend sleeps until postgres is accepting connections in order to migrate.
```

Enter the web client on localhost:3000

## Web Client

Built with react, utilizing Semantic UI with Material design principles (and theme)!

Currently timezone calculations are performed in the client as well, using Moment.js

## Backend

Built with Ruby on Rails.

## DB

PostgreSQL, with seed data from [OpenFlights](https://openflights.org/data.html)

## TODO

- Separate Moment.js and timeywimey.js into their own service to minimize clientside calculations

