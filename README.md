# Levo-calendar

## How it works
On node js express application startup, a socket.io object is initialized. The socket.io object is used for instant communication between all connected browser clients.

Data is saved in sqlite3 database and accessible via 3 end points:
```localhost:8080/events/create-new-event'```
```localhost:8080/events/edit-event'```
```localhost:8080/events/delete-event'```

The frontend listens for socket.io notification whilst the express application is configured to fire at instances where data is changed. As such, on successful event updates, the data reflects immediately in the frontend.

There are checks in place for conflicts i.e. if a user is already a participant in another meeting scheduled at the selected time, the event cannot be added and users will be notified of the conflict.

## Getting Started

### Installing

* Navigate to `\backend` and nitialize dependencies with `npm i` 
* Set up sqlite schema with `npm run setup`
* Create a new .env file. Set value for `HOLIDAY_API_KEY`
* Start express server at port 8080 with `npm start`

* Navigate to `\frontend` and nitialize dependencies with `npm i` 
* Start at port 3000 with `npm start`


