FROM eclipse/php

#Setup folder structure
WORKDIR /drupal
RUN sudo chown user .
RUN sudo chown user /drupal

#Install dependencies
ADD http://raw.githubusercontent.com/drupal/drupal/8.4.x/composer.lock /drupal
ADD http://raw.githubusercontent.com/drupal/drupal/8.4.x/composer.json /drupal
RUN sudo chown user composer.json
RUN sudo chmod 0777 composer.json
RUN sudo chown user /drupal/composer.json
RUN sudo chmod 0777 /drupal/composer.json
RUN sudo chmod 0777 /drupal
#RUN sudo composer install

#Ready for Che launch
WORKDIR /projects
#Must end in a non-terminating command
CMD tail -f /dev/null
