# UOCIS322 - Project 6 #
Brevet time calculator with AJAX, MongoDB, and a RESTful API!

## What is in this repository

You have a minimal example of `docker-compose` in `DockerRestAPI`, using which you can create RESTful API-based services (as demonstrated in class). 


Recall that you created the following functionalities:

1. Add two buttons `Submit` and `Display` in the ACP calculator page.

2. Upon clicking the `Submit` button, the control times should be inserted into a MongoDB database.

3. Upon clicking the `Display` button, the entries from the database should be displayed in a new page.

4. Handle error cases appropriately. For example, `Submit` should return an error if no control times are input. One can imagine many such cases: you'll come up with as many cases as possible.

### Functionality you will add

This project has following four parts. Change the values for host and port according to your machine, and use the web browser to check the results.

    * "http://<host:port>/listAll" should return all open and close times in the database
    * "http://<host:port>/listOpenOnly" should return open times only
    * "http://<host:port>/listCloseOnly" should return close times only

* You will also design two different representations: one in csv and one in json. For the above, JSON should be your default representation for the above three basic APIs. 
    * "http://<host:port>/listAll/csv" should return all open and close times in CSV format
    * "http://<host:port>/listOpenOnly/csv" should return open times only in CSV format
    * "http://<host:port>/listCloseOnly/csv" should return close times only in CSV format

    * "http://<host:port>/listAll/json" should return all open and close times in JSON format
    * "http://<host:port>/listOpenOnly/json" should return open times only in JSON format
    * "http://<host:port>/listCloseOnly/json" should return close times only in JSON format

* You will also add a query parameter to get top "k" open and close times. For examples, see below.

    * "http://<host:port>/listOpenOnly/csv?top=3" should return top 3 open times only (in ascending order) in CSV format 
    * "http://<host:port>/listOpenOnly/json?top=5" should return top 5 open times only (in ascending order) in JSON format
    * "http://<host:port>/listCloseOnly/csv?top=6" should return top 5 close times only (in ascending order) in CSV format
    * "http://<host:port>/listCloseOnly/json?top=4" should return top 4 close times only (in ascending order) in JSON format

* You'll also design consumer programs (e.g., in jQuery) to use the service that you expose. `website` inside `DockerRestAPI` is an example of that. It is uses PHP. You're welcome to use either PHP or jQuery to consume your services. NOTE: your consumer program should be in a different container like example in `DockerRestAPI`.


