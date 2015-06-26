#Droplet Provision Script

This script is designed to provision and configure a Digital Ocean droplet.
It installs the following:
  - Ruby & Ruby-dev
  - Nginx
  - Unicorn
  - Postgres (creates a root user and database)

It also installs the following gems:
  - pg
  - json
  
Finally, it creates a default `/var/www/app` directory for you to start with.

##Important!

  1. You will need to create an nginx config file in `/etc/nginx/conf.d/default.conf`
  2. You will need to edit your Unicorn configuration file in `/var/www/app/unicorn.rb`
  3. Sample configuration files are included in this repository.

##Running this script

  1. Log into your droplet.
  2. Open a a new file in a text editor and copy the contents of setup_droplet.sh into it. Example: `nano setup.sh`
  3. Update this file's permissions - `chmod u+x setup.sh`
  4. Run the script! `./setup.sh`
  5. That's it. Enjoy!

This script has been tested on Ubuntu 14.04.
