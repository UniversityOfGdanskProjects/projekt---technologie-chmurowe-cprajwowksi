FROM quay.io/keycloak/keycloak:21.0.2

ENV KEYCLOAK_ADMIN=admin \
    KEYCLOAK_ADMIN_PASSWORD=admin \
    KC_DB=postgres \
    KC_DB_URL_HOST=postgres-service \
    KC_DB_URL_PORT=5432 \
    KC_DB_USERNAME=keycloak \
    KC_DB_PASSWORD=password

WORKDIR /opt/keycloak/data/import

COPY ./keycloak-conf /opt/keycloak/data/import

CMD ["-v", "start-dev", "--import-realm"]
