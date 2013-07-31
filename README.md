Project Bindaas For GSOC 2013
=============================

Bindaas(http://imaging.cci.emory.edu/wiki/display/BDS/Downloads)is a database middle ware developed by Emory University

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

Current important APIs.

POST methods.
```
var saveDemographicsUrl = 'http://localhost:9099/services/ccda/demographics/submit/mongo?api_key=5d36e104-bdfe-4ec1-975c-728154aa90f9',
saveAllergyUrl = 'http://localhost:9099/services/ccda/allergy/submit/mongo?api_key=5d36e104-bdfe-4ec1-975c-728154aa90f9',
saveImmunizationUrl = 'http://localhost:9099/services/ccda/immunization/submit/mongo?api_key=5d36e104-bdfe-4ec1-975c-728154aa90f9',
saveMedicationUrl = 'http://localhost:9099/services/ccda/medication/submit/mongo?api_key=5d36e104-bdfe-4ec1-975c-728154aa90f9',
saveLabUrl = 'http://localhost:9099/services/ccda/lab/submit/mongo?api_key=5d36e104-bdfe-4ec1-975c-728154aa90f9';
saveEncounterUrl = 'http://localhost:9099/services/ccda/encounter/submit/mongo?api_key=5d36e104-bdfe-4ec1-975c-728154aa90f9';
saveProblemUrl = 'http://localhost:9099/services/ccda/problem/submit/mongo?api_key=5d36e104-bdfe-4ec1-975c-728154aa90f9';
saveProcedureUrl ='http://localhost:9099/services/ccda/procedure/submit/mongo?api_key=5d36e104-bdfe-4ec1-975c-728154aa90f9';
saveVitalUrl = 'http://localhost:9099/services/ccda/vital/submit/mongo?api_key=5d36e104-bdfe-4ec1-975c-728154aa90f9';
```

GET methods.

Please add uid=:uid to get the corresponding data with the uid = :uid
```
var demographicsUrl = '/services/ccda/demographics/query/demographics?api_key=5d36e104-bdfe-4ec1-975c-728154aa90f9',
problemUrl = '/services/ccda/problem/query/problem?api_key=5d36e104-bdfe-4ec1-975c-728154aa90f9',
allergyUrl = '/services/ccda/allergy/query/allergy?api_key=5d36e104-bdfe-4ec1-975c-728154aa90f9',
immunizationUrl = '/services/ccda/immunization/query/immunization?api_key=5d36e104-bdfe-4ec1-975c-728154aa90f9',
medicationUrl = '/services/ccda/medication/query/medication?api_key=5d36e104-bdfe-4ec1-975c-728154aa90f9',
labUrl = '/services/ccda/lab/query/lab?api_key=5d36e104-bdfe-4ec1-975c-728154aa90f9',
encounterUrl = '/services/ccda/encounter/query/encounter?api_key=5d36e104-bdfe-4ec1-975c-728154aa90f9',
procedureUrl = '/services/ccda/procedure/query/procedure?api_key=5d36e104-bdfe-4ec1-975c-728154aa90f9',
vitalUrl = '/services/ccda/vital/query/vital?api_key=5d36e104-bdfe-4ec1-975c-728154aa90f9';
```