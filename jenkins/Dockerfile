FROM jenkins/jenkins:lts

USER root

# Installer PHP, Git, Composer
RUN apt-get update && apt-get install -y \
    php php-cli php-zip php-mbstring php-curl php-xml \
    unzip curl git

# Installer Composer globalement
RUN curl -sS https://getcomposer.org/installer | php && \
    mv composer.phar /usr/local/bin/composer

USER jenkins

# Préinstaller les plugins Jenkins
COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN jenkins-plugin-cli --plugin-file /usr/share/jenkins/ref/plugins.txt
