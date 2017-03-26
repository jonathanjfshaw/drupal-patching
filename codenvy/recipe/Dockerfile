FROM eclipse/php

#Setup folder structure
WORKDIR /projects/drupal

#Install dependencies
ADD http://raw.githubusercontent.com/drupal/drupal/8.4.x/composer.lock .

#Ready for Che launch
WORKDIR /projects
#Must end in a non-terminating command
CMD sudo service apache2 start && tail -f /dev/null
