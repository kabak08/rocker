FROM rocker/rstudio-stable:latest
## Work-around to make Docker Hub use the Dockerfile 
## from https://github.com/rocker-org/rocker-versioned/tree/master/rstudio

RUN sudo apt-get update -y
RUN sudo apt-get install vim -y
RUN sudo apt-get install unixodbc unixodbc-dev -y
RUN mkdir /etc/connections
RUN wget https://packages.microsoft.com/debian/8/prod/pool/main/m/msodbcsql/msodbcsql_13.1.9.1-1_amd64.deb
RUN sudo apt-get install msodbcsql_13.1.9.1-1_amd64.deb




COPY ./odbc/odbc.ini /etc/odbc.ini
COPY ./odbc/odbcinst.ini /etc/odbc.ini
COPY ./connections/DB2connection /etc/connection/DB2connection



#COPY install.packages.R /tmp
#RUN Rscript /tmp/install.packages.R
