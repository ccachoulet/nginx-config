
# Nginx configuration file for several domains which redirects to only 1, with force https and no www

## nginx.conf 
path: /etc/nginx/nginx.conf
### Contents of the nginx.conf file
The nginx.conf file must contain the imports of your site configurations located in the site-available folder
### To perform the import you must add:
``` include /etc/nginx/sites-available/yoursite; ```
The above code should be added in the http

## site configuration
path: /etc/nginx/sites-available/yoursite

### Create your site file
move to the site-available folder and once inside type ```touch nameofthesite``` Open the file with nano or vim and paste the code present above

Restart the nginx service with the command ``` sudo service nginx restart ``` Once done check your config with the ```nginx -t``` command 
If all goes well he should return :
```nginx: the configuration file /etc/nginx/nginx.conf syntax is ok```
```nginx: configuration file /etc/nginx/nginx.conf test is successful``` 
