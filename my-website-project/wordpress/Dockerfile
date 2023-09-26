FROM wordpress

# printf statement mocks answering the prompts from the pecl install
RUN printf "\n \n" | pecl install redis && docker-php-ext-enable redis
RUN \ 
apt-get update && \
apt-get install libldap2-dev -y && \
rm -rf /var/lib/apt/lists/* && \
docker-php-ext-configure ldap --with-libdir=lib/x86_64-linux-gnu/ && \
docker-php-ext-install ldap

RUN /etc/init.d/apache2 restart