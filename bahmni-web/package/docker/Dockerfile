FROM infoiplitin/bahmni-iplit-web:latest

# this command to build bahmni-web image locally before starting service on any server
# docker compose down
# docker compose build bahmni-web
# docker compose up -d


USER root

# RUN /bin/sh -c 'chmod -R +w /usr/local/apache2/htdocs'

COPY bahmni-web/resources/clinicalPrint.css /usr/local/apache2/htdocs/bahmni/styles/

# COPY bahmni-web/resources/visitSummary.html /usr/local/apache2/htdocs/bahmni/clinical/common/views/
# COPY bahmni-web/resources/visitTabPrint.html /usr/local/apache2/htdocs/bahmni/clinical/common/views/

COPY bahmni-web/resources/bahmniLogo.png /usr/local/apache2/htdocs/bahmni/images/
COPY bahmni-web/resources/bahmniLogoFull.png /usr/local/apache2/htdocs/bahmni/images/
COPY bahmni-web/resources/visitPrintHeader.png /usr/local/apache2/htdocs/bahmni/images/

COPY bahmni-web/resources/index.html /usr/local/apache2/htdocs/
COPY bahmni-web/resources/bahmniLogoFull.png /usr/local/apache2/htdocs/bahmni-logo.png

# COPY bahmni-web/resources/whiteLabel.json /usr/local/apache2/htdocs/bahmni_config/openmrs/apps/home/

COPY bahmni-web/resources/diagnosis.html /usr/local/apache2/htdocs/bahmni/clinical/consultation/views/

COPY bahmni-web/resources/addTreatment.html /usr/local/apache2/htdocs/bahmni/clinical/consultation/views/treatmentSections/

COPY bahmni-web/resources/visitSummary.html /usr/local/apache2/htdocs/bahmni/clinical/common/views/

