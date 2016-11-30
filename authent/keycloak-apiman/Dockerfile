FROM jboss/keycloak-postgres
ADD apiman.json  /opt/jboss/keycloak/
ENTRYPOINT [ "/opt/jboss/docker-entrypoint.sh" ]
CMD ["-b", "0.0.0.0", "-Dkeycloak.import=/opt/jboss/keycloak/apiman.json"]
