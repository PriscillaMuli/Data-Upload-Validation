# **Description**

For the data uploaded, it is necessary to validate that the data is present on the server.  
I utilized the GeneNetwork API endpoints as documented in this resource: https://github.com/genenetwork/gn-docs/blob/master/api/GN2-REST-API.md with https://staging.genenetwork.org/ as the domain

The API endpoints listed in this document give the data back, mostly in Json format, which can be used to compare with data in the original files and verify that the data is the same.

Utilizing the endpoints, I used the curl command-line tool to fetch data from the API.

The specific code used for fetching data from the API endpoints was:

       curl -k https://staging.genenetwork.org/api/v_pre1/datasets/bxd
 
The “-k” option in this command permits insecure SSL connections, while the provided API endpoint “datasets/bxd’ fetches information about the specific BXD dataset. 

The information retrieved by accessing the specified API endpoint included fields such as create time, ProbeFreeze ID, publicity, confidentiality, full name, short name, long abbreviation, short abbreviation and data scale, confirming the data has been successfully uploaded.
