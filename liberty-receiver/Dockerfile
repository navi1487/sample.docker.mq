FROM store/ibmcorp/websphere-liberty:webProfile7

MAINTAINER Jamie Coleman <jlcoleman@uk.ibm.com>

COPY server.xml /opt/ibm/wlp/usr/servers/defaultServer/
COPY 9.1.0.7-IBM-MQ-Java-InstallRA.jar /
COPY receiver.war /opt/ibm/wlp/usr/servers/defaultServer/dropins/
	
RUN installUtility install --acceptLicense defaultServer
RUN java -jar 9.1.0.7-IBM-MQ-Java-InstallRA.jar --acceptLicense /
