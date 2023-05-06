FROM bahmniindiadistro/clinic-config:latest

# this command to build bahmni-config image locally before starting service on any server
# docker compose down
# docker compose build bahmni-config
# docker compose up -d

USER root

RUN echo 'Running some bahmni_config commands'

# ADD bahmni-config/resources/whiteLabel.json /tmp/
COPY bahmni-config/resources/whiteLabel.json /etc/bahmni_config/openmrs/apps/home/

# RUN mv /etc/bahmni_config/masterdata/configuration/bahmniforms  /etc/bahmni_config/masterdata/configuration/bahmniforms-OLD
# RUN mv /usr/local/bahmni_config/masterdata/configuration/bahmniforms /usr/local/bahmni_config/masterdata/configuration/bahmniforms-OLD


# RUN rm /etc/bahmni_config/masterdata/configuration/bahmniforms/*.* #temporary fix
# RUN rm -rf /usr/local/bahmni_config/masterdata/configuration/bahmniforms

# RUN mkdir -p /tmp/bahmniforms
# COPY  bahmni-config/resources/bahmniforms/*.* /tmp/bahmniforms/

# RUN mkdir -p /etc/bahmni_config/masterdata/configuration/bahmniforms
COPY bahmni-config/resources/bahmniforms/*.* /etc/bahmni_config/masterdata/configuration/bahmniforms/

RUN mkdir -p /etc/bahmni_config/openmrs/apps/ipd
RUN mkdir -p /etc/bahmni_config/openmrs/apps/adt

COPY  bahmni-config/resources/apps/ipd/*.* /etc/bahmni_config/openmrs/apps/ipd/
COPY  bahmni-config/resources/apps/adt/*.* /etc/bahmni_config/openmrs/apps/adt/

# RUN cp -R /tmp/ipd  /etc/bahmni_config/openmrs/apps/
# RUN cp -R /tmp/adt  /etc/bahmni_config/openmrs/apps/

# ADD bahmni-config/resources/home-extension.json /tmp/
COPY bahmni-config/resources/home-extension.json /etc/bahmni_config/openmrs/apps/home/extension.json

# ADD bahmni-config/resources/clinical-visit.json /tmp/
COPY bahmni-config/resources/clinical-visit.json /etc/bahmni_config/openmrs/apps/clinical/visit.json

# ADD bahmni-config/resources/apps/registration/registrationCardLayout/print.html /tmp/registration/
COPY bahmni-config/resources/apps/registration/registrationCardLayout/print.html /etc/bahmni_config/openmrs/apps/registration/registrationCardLayout/

# ADD bahmni-config/resources/apps/registration/registrationCardLayout/bahmniLogo.png /tmp/registration/
COPY bahmni-config/resources/apps/registration/registrationCardLayout/bahmniLogo.png /etc/bahmni_config/openmrs/apps/registration/registrationCardLayout/images/

# ADD bahmni-config/resources/apps/registration/locale_en.json /tmp/registration/
COPY bahmni-config/resources/apps/registration/locale_en.json /etc/bahmni_config/openmrs/i18n/registration/locale_en.json
