FROM httpd:2.4

RUN sed -i '/LoadModule rewrite_module/s/^#//g' /usr/local/apache2/conf/httpd.conf && \
   sed -i 's#AllowOverride [Nn]one#AllowOverride All#' /usr/local/apache2/conf/httpd.conf

#COPY demo.apache.conf /usr/local/apache2/conf/demo.apache.conf
COPY apache-config.conf /usr/local/apache2/conf/apache-config.conf
RUN echo "Include /usr/local/apache2/conf/apache-config.conf" >> /usr/local/apache2/conf/httpd.conf

# Set working directory
WORKDIR /var/www/html



