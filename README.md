this scripts is used in production network for nso bpa reporting purpose after UAT completion to address customer issue while provisioning mols l2 and l3 services.



"inventory.py" script is having details of lab bpa servers as well as production bpa servers


among "GetPayloadByDate.py" and "GetLogsNpayloads.py" scripts, either one can be used to query bpa server by requesting api they exposed to give ordes details in json format


"data.json" filr the result data of that api query


then this data,json results are parsed  using "createCsvReport.py" script and results are exported to "report.csv" file for user readability purpose or order tracking.


