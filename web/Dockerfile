FROM httpd:2.4

WORKDIR /usr/local/apache2/
RUN echo "include conf/sites-enabled/*" >> conf/httpd.conf
RUN mkdir /work
RUN chown www-data:www-data /work
COPY conf/sites-enabled.conf /usr/local/apache2/conf/sites-enabled/default.conf

# Update package cache to be able to install packages
#RUN apt-get -qq update

#RUN apt-get -y install vim php5 php5-mysql