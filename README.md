# Udacity Linux Server Configuration

This Linux configuration is used in conjunction with AWS to host and launch a Python Flask application using Apache2 WSGI mod and a Pstgresql Database.

## Login for grader
Log into server using SSH command:

`$ ssh grader@18.217.89.103 -p 2200 -i [SSH_FILE_PATH]`

You can access the application with this link
[http://ec2-18-217-89-103.us-east-2.compute.amazonaws.com](http://ec2-18-217-89-103.us-east-2.compute.amazonaws.com)

## Configurations made
* A new user 'grader' was added to the server and given sudo permissions. Root login and password authentication were then blocked, requiring a user to use SSH login
* SSH login was enable for user, grader
* UFW was enabled and configured to allow only specific port access
* Server port access changed from 22 to 2200
* PSQL installed and given restricted access
* Apache2 and Apache mod WSGI install to launch Flask applications
* Catalog Project added and enable via WSGI with proper database permissions and correct path variables
* Server redirects to Catalog app by default

## What was used
* Python (2.7)
* Apache2
* Apache Mod WSGI
* Amazon Lightsail
* PSQL (9.5.10)
* Flask (0.12.2)
* Psycopg2 (2.7.3.2)
* SQLAlchemy (1.1.15)

## Resources used
* [http://flask.pocoo.org/docs/0.12/deploying/mod_wsgi/](http://flask.pocoo.org/docs/0.12/deploying/mod_wsgi/)
* [https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps](https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps)
* [https://wiki.postgresql.org/wiki/PostgreSQL_Tutorials](https://wiki.postgresql.org/wiki/PostgreSQL_Tutorials)
* And Udacity's Linux Configuration Course material
