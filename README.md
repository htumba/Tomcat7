Configura tu Tomcat 7.0.40 en OpenShift
============================

Este repositorio git te ayudara a configurar y correr rapidamente una instalacion tomcat en Openshift
esta basado en este: https://github.com/openshift/openshift-tomcat-quickstart

Crea una aplicacion DIY en OpenShift
----------------------------

Crea una cuenta en http://openshift.redhat.com/ , no olvides crear un namespace e instalar las herramientas cliente.

Puedes ver el video de como instalar las herramientas cliente aqui : http://www.youtube.com/watch?v=WER08V3eeHE

Crea la app DIY 

    rhc app create -a tomcat -t diy-0.1

Subiendo y ejecutando Tomcat
----------------------------
Ejecuta los siguientes comandos en la herramienta git para copiar el repositorio:

    cd tomcat
    git remote add upstream -m master git://github.com/htumba/Tomcat7.git
    git pull -s recursive -X theirs upstream master
    git push
	

Eso es todo, chequea tu flamante tomcat en:

    http://tomcat-$yournamespace.rhcloud.com

La cuenta por defecto para administracion es tomcat/openshift
No olvides configurar los usuarios en conf/tomcat-users.xml

License
-------

This code is dedicated to the public domain to the maximum extent
permitted by applicable law, pursuant to CC0
http://creativecommons.org/publicdomain/zero/1.0/
