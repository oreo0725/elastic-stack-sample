ARG ELK_VERSION

# https://github.com/elastic/logstash-docker
FROM docker.elastic.co/logstash/logstash-oss:${ELK_VERSION}

# Add your logstash plugins setup here
# Example: RUN logstash-plugin install logstash-filter-json

# https://www.elastic.co/blog/logstash-jdbc-input-plugin
RUN logstash-plugin install logstash-input-jdbc
RUN logstash-plugin install logstash-filter-json

ADD plugin/mssql-jdbc-7.2.1.jre8.jar /usr/share/logstash/mssql-jdbc.jar

# ADD pipeline/import-hourly.conf /usr/share/mssql/import-hourly.conf
