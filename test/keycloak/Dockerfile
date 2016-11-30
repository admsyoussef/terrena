FROM jboss/keycloak-mongo
RUN rm -rf /usr/local/share/jboss/standalone/configuration/standalone_xml_history/current
RUN keycloak/bin/add-user-keycloak.sh -u kcadmin -p password
