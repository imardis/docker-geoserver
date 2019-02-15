FROM oscarfonts/geoserver:2.14.1
MAINTAINER Thomas Prebble <t.prebble@bangor.ac.uk>
ENV GEOSERVER_VERSION 2.14.1
ENV GEOSERVER_INSTALL_DIR /usr/local/geoserver

WORKDIR ${GEOSERVER_INSTALL_DIR}/WEB-INF/lib

RUN echo "<% response.sendRedirect(\"/geoserver\"); %>" > /usr/local/tomcat/webapps/ROOT/index.jsp

RUN wget https://github.com/ngageoint/elasticgeo/releases/download/2.14.0-RC1/elasticgeo-2.14.0.zip \
     && unzip -o elasticgeo-2.14.0.zip \
     && rm elasticgeo-2.14.0.zip

EXPOSE 8080