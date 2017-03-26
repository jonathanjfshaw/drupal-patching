FROM eclipse/php

# this file needs to be at the project root for this to work
ADD . /drupal
WORKDIR /drupal

#Install dependencies
ADD http://raw.githubusercontent.com/drupal/drupal/8.4.x/composer.lock /

#Must end in a non-terminating command
CMD sudo service apache2 start && tail -f /dev/null
