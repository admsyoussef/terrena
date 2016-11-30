FROM apiman/on-wildfly10
RUN $JBOSS_HOME/bin/add-user.sh admin admin123! --silent
USER jboss
COPY postgresql-9.3-1102-jdbc41.jar /opt/jboss/wildfly/standalone/deployments/
COPY standalone-apiman.xml /opt/jboss/wildfly/standalone/configuration/
COPY apiman.properties /opt/jboss/wildfly/standalone/configuration/
COPY apiman-ds.xml /opt/jboss/wildfly/standalone/deployments/apiman-ds.xml
#CMD ["/opt/jboss/wildfly/bin/standalone.sh", "-b", "0.0.0.0", "-bmanagement", "0.0.0.0", "-c", "standalone-apiman.xml"]
ENTRYPOINT [ "/opt/jboss/wildfly/bin/standalone.sh" ]
CMD ["-b", "0.0.0.0", "-bmanagement", "0.0.0.0", "-c", "standalone-apiman.xml", "--debug"]
