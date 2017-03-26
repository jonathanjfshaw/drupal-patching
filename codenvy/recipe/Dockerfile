FROM eclipse/php

#Install dependencies
ADD http://raw.githubusercontent.com/drupal/drupal/8.4.x/composer.lock /drupal/composer.lock

#Must end in a non-terminating command
CMD sudo service apache2 start && tail -f /dev/null
