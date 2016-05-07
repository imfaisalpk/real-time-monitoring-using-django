# Adding Real-Time to Django Applications

This is an implementation of event based programming on Django. Django is made to build web applications synchronously using HTTP but crossbar.io enables you to trigger realtime notifications from your synchronous Python Web stack since it comes with a HTTP Pusher service.

This app monitors and prints the usage statistics of all the clients connected to your server which runs on Django. Currently, it prints CPU, disk and memory stats. It uses WAMP PubSub model implemented using crossbar router and Django's signalling system to handle the client configs telling which stats to print.

## Install

1. **Install Django** : `pip install django`
2. **Install Crossbar** : `pip install crossbar[all]`

Of course, you need to have python already installed.

## Usage

 - *fire up a terminal*
 - *cd to the directory*
 - *run `crossbar start`*
 - *run `python client.py`*
 - *run `python manage.py runserver`*

Make sure you need to run crossbar + django on the same machine.
You can run *client.py* in any machine for which you want the stats.

For simplicity, I have used localhost as server but you can change it according to you in *client.py*.

## Screenshots

![One client connected](screenshots/img.jpg?raw=true "Client monitored stats")

## Future

This is only an implementation of asynchronous programming on django. I will be soon adding in some additional features and making it a full fledged network monitoring app.
