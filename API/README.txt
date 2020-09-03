Research Project - Summer 2020 - Fantine Chabernaud -04/08/2020

Goal: Download data from the MVM repository and convert those files into a SQL-friendly format (here CSV).

1. Get data via API using the scirpt: "get_data_MVM_API"

    1.1 The main function (first cell) in the notebook calls via API data from MVM servers. It queries "GetSamplesBySite". It iteratively downloads the JSON files for each site. In order to get the site ID list, I previously manually downloaded the list from MVM website. I converted the list into csv so that it is readable by the function "get_site_id_list". 
    /!\ To avoid executing the script over 14990+ sites, restrict the list of stations to request.
    
    1.2 The last cell is just a draft to look at a specific file, to check its content.
    
    
2. Convert JSON files into CSV (readable by SQL database management system) using script: "json_to_csv". It selects some columns (not scalable) and rows related to "Product Name: Vattenkemi".

    2.1 The first cell is the main script. Run it once the JSOn files are in the folder "data_to_convert_input" and the output is one big csv file in the folder "converted_output".

    
