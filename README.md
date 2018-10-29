# Apache installation and configuration ubuntu

### Installing necessary packages:
  1. To install apache:<br>
      sudo apt-get install apache2
  2. To install libraries for mod wsgi for python3:<br>
      sudo apt-get install libapache2-mod-wsgi-py3
  3. To install mysql necessaries:<br>
      sudo apt-get install mysql-server mysql-client
  4. Configure mysql-server:<br>
      sudo mysql_secure_installation
  5. Install mod_wsgi:<br>
      pip3.6 install mod_wsgi
      

### Steps to deploy the example flask app
  1. Creating wsgi.load file:<br>
      mod_wsgi-express module-config<br>
      ***copy the output of the command***<br>
      nano /etc/apache2/mods-available/wsgi.load<br>
      ***paste the copied text and save***<br>
  2. Make sure mod is enabled:<br>
      a2enmod wsgi
  3. Restart the apache server whenever necessary:<br>
      service apache2 restart
  4. Create a directory inside /var called www:<br>
      i.e., mkdir /var/www
  5. Copy the FlaskApp folder which contains the FlaskApp module and the wsgi file<br>
  6. Copy the FlaskApp.conf file inside the apache_conf_eg folder to /etc/apache2/sites-available/<br>
  7. Edit the above mentioned files as per the requirements.<br>
### Note:
        The ip address in the FlaskApp.conf file should be same as the server's ip.  Here the local host's ip is used.
