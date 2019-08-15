Export Data Scripts
===================

Neil Katin, 2019-08-15

This folder has script experiments to export (and eventually update) data on survey123.

Currently the damage assessment public survey allows anyone to read the data.  This is nice and simple, but not what was expected.

Eventually we'll have to pass a login token with our REST requests, but right now we don't.

There are a few files here in the folder:

* ```retrieve_survey_info``` was the attempt to retrieve info using the arcgis python package.
  It used to be a bit longer, but I never got it to successfully retrieve rows of data from our tables.

