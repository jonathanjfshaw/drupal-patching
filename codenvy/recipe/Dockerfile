FROM eclipse/php

#Setup folder structure
#WORKDIR /drupal

#Install dependencies
#ADD http://raw.githubusercontent.com/drupal/drupal/8.4.x/composer.lock /drupal
#ADD http://raw.githubusercontent.com/drupal/drupal/8.4.x/composer.json /drupal
#RUN sudo composer install --no-scripts --no-autoloader
#COPY . ./
RUN sudo composer global config minimum-stability dev
ENV PATH=$PATH:~/.composer/vendor/bin
RUN sudo echo -e $PATH
RUN sudo -E echo -e $PATH
RUN sudo composer global require consolidation/cgr
RUN sudo ~/.composer/vendor/bin/cgr drupal/console:dev-master
#RUN sudo cgr drush/drush:dev-master

RUN sudo service mysql start
RUN sudo service apache2 start

#Ready for Che launch
WORKDIR /projects
#Must end in a non-terminating command
CMD tail -f /dev/null
