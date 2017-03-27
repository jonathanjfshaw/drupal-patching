FROM eclipse/php

#Setup folder structure
#WORKDIR /drupal

#Install dependencies
#ADD http://raw.githubusercontent.com/drupal/drupal/8.4.x/composer.lock /drupal
#ADD http://raw.githubusercontent.com/drupal/drupal/8.4.x/composer.json /drupal
#RUN sudo composer install --no-scripts --no-autoloader
#COPY . ./
ENV PATH=$PATH:~/.composer/vendor/bin
RUN sudo composer global config minimum-stability dev
RUN sudo composer global require "hirak/prestissimo:^0.3"
RUN sudo composer global require consolidation/cgr
RUN sudo ~/.composer/vendor/bin/cgr --stability dev drupal/console:dev-master
RUN sudo ~/.composer/vendor/bin/cgr --stability dev drush/drush:dev-master

RUN sudo service mysql start
RUN sudo service apache2 start

#Ready for Che launch
WORKDIR /projects
#Must end in a non-terminating command
CMD tail -f /dev/null
