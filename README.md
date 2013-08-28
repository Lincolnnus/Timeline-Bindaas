Project Bindaas For GSOC 2013
=============================

Bindaas[http://imaging.cci.emory.edu/wiki/display/BDS/Downloads] is a database middle ware developed by Emory University

In this GSOC project, the bindaas server is served as the dataware house and the data are accessed via the bindaas api using the project bindaas middleware.

------------------------

To run the bindaas api 

<code>
	$> cd $BINDAAS_HOME/bin
	$> ./startup.sh
</code>

You can access the bindaas api via  http://localhost:8080/dashboard/administration and the default credentials are *admin/password*

You can browse the apis developed in this GSOC 2013 project and ensure that you have opened up database management system and selected the corresponding database.

In this project, we used mongodb and named the database as ccda. You may want to change these configuration accordingly.

You can copy the *.json bindaas-metadata(project/ccda.project) bindaas.h2.db into your bindaas directory and then run the bindaas API from your server.