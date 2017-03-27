FROM eclipse/php

#Setup folder structure
#WORKDIR /drupal

#Install dependencies
#ADD http://raw.githubusercontent.com/drupal/drupal/8.4.x/composer.lock /drupal
#ADD http://raw.githubusercontent.com/drupal/drupal/8.4.x/composer.json /drupal
#RUN sudo composer install --no-scripts --no-autoloader
#COPY . ./
RUN sudo composer global require drupal/console:@stable
RUN sudo composer global require drush/drush:@stable

#Ready for Che launch
WORKDIR /projects
#Must end in a non-terminating command
CMD tail -f /dev/null
