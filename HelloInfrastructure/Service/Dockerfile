#date: 2016-01-30
#image:liberty+app 
#env:  linuxone

#base image
FROM libertybase

#Install liberty 
#RUN mkdir /opt/ibm/wlp
#copy liberty file to sepcify path
#COPY wlp /opt/ibm/wlp
#set liberty PATH
#ENV PATH /opt/ibm/wlp/bin:$PATH

# Configure WebSphere Liberty
#RUN /opt/ibm/wlp/bin/server create \
#    && rm -rf /opt/ibm/wlp/usr/servers/.classCache
# copy server.xml for app configuration
#ADD server.xml /opt/ibm/wlp/usr/servers/defaultServer/
# copy app to deploy it
# set default run command after start this  container
RUN chmod 777 /opt/ibm/wlp/bin/server
ADD HelloService.war /opt/ibm/wlp/usr/servers/linuxoneservice/apps/
# expose container port
EXPOSE 9080 9443
# set default run command after start this  container
CMD ["/opt/ibm/wlp/bin/server", "run", "linuxoneservice"]
