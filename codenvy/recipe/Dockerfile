FROM eclipse/php

#Setup folder structure
WORKDIR /drupal

#Install dependencies
ADD http://raw.githubusercontent.com/drupal/drupal/8.4.x/composer.lock /
ADD http://raw.githubusercontent.com/drupal/drupal/8.4.x/composer.json /
RUN composer install

#Ready for Che launch
WORKDIR /projects
#Must end in a non-terminating command
CMD tail -f /dev/null
