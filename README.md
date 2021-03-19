this scripts is used in production network for nso bpa reporting purpose after UAT completion to address customer issue while provisioning mols l2 and l3 services.



"inventory.py" script is having details of lab bpa servers as well as production bpa servers


among "GetPayloadByDate.py" and "GetLogsNpayloads.py" scripts, either one can be used to query bpa server by requesting api they exposed to give ordes details in json format


"data.json" filr the result data of that api query


then this data,json results are parsed  using "createCsvReport.py" script and results are exported to "report.csv" file for user readability purpose or order tracking.


------------------------

in script "GetPayloadByDate.py" and "GetLogsNpayloads" below line of code is to define date,time range and  service types for which we want data,

serviceTagName can be 
CEN-L2
MPLS
ISP
CEN-L3

or you could omit that key value pair if you want all service type data 



body = {
        "startDate":"{}-2020 00:00:00".format(start_date),
        "endDate":"{}-2020 23:59:59".format(end_date),
	"serviceTagName": "CEN-L2"
    }
    
    
start date and end date will be user input while running this script


-----

all scripts can be run standalone as well as the final scripts ( createCsvReport.py ) could have results of all the child scripts
using import statements.

it depend on user how he/she want to utilise it.


    
