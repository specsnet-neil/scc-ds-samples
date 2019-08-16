Export Data Scripts
===================

Neil Katin, 2019-08-15

This folder has script experiments to export (and eventually update) data on survey123.

Currently the damage assessment public survey allows anyone to read the data.  This is nice and simple, but not what was expected.

Eventually we'll have to pass a login token with our REST requests, but right now we don't.
[This page](https://developers.arcgis.com/dashboard)
shows how to get an access token from ESRI.

The most useful page was this
[REST api query page](https://developers.arcgis.com/rest/services-reference/query-feature-service-.htm)
that showed how to use the query REST API for a feature layer.

There are a few files here in the folder:

* ```retrieve_survey_info``` was the attempt to retrieve info using the arcgis python package.
  It used to be a bit longer, but I never got it to successfully retrieve rows of data from our tables.

* ```retrieve_layer0_metadata``` is a trivial script that fetches the main table metadata;
  it gives the full table definition.  it uses the REST api and is just a small wrapper around ```curl```

* ```retrieve_layer_data``` is another small wrapper that fetches all the row data.  It takes one argument -- either ```--data``` or ```--images``` to pick which layer to return data from.

All the scripts depend on a ```survey_params.py``` file that contains account and survey info I
didn't want to check into a public GIT repo.
Initialize the file from ```survey_params.py.sample```, fill in the survey ID and you should be good to go.


