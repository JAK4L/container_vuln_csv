# License
*THIS SCRIPT IS PROVIDED TO YOU "AS IS." TO THE EXTENT PERMITTED BY LAW, QUALYS HEREBY DISCLAIMS ALL WARRANTIES AND LIABILITY FOR THE PROVISION OR USE OF THIS SCRIPT. IN NO EVENT SHALL THESE SCRIPTS BE DEEMED TO BE CLOUD SERVICES AS PROVIDED BY QUALYS*

# Image and Container Vulnerability CSV creation

This is an example script on creating two CSV files from the Qualys Container Security API for both images and containers respectively.
This script is provided with no warrantee and is provided as an example on how to accomplish making these files in Python 2.7.x

*Info* : Python script creates CSV files for vulnerability data from Qualys Cloud Security w.r.t details provided in "./config.yml".
       Script debug info will be logged in ./debug/debug_file.txt

CSV File Info
*Vulnerability Image Report headers*
> Registry,Repository,ImageID,Tag,Hostname,Vulnerabiltiy ID,Severity,CVE Number,Published Date,Description,Patch Available

*Vulnerability Container Report headers*
>Registry,Repository,ImageID,Tag,Container,Hostname,Vulnerabiltiy ID,Severity,CVE Number,Published Date,Description,Patch Available


# Script configuration
*config.yml*
Provide script configuration information for API U/P, vulnerability severity ratings, and Qualys API URL
  username: "QualysUsername"
  password: "QualysPassword"
  vulnerabilities_to_report: string value of severity ratings to include (**acceptable entries 54321, 5432, 543, 54, or 5**)
  apiURL: "Qualys API URL base (https:// - > .com, no trailing '/')"

# Script Requirements
This script is written in Python 2.7.x (X > 10)
This script requires the following PIP modules to run
Modules: sys, requests, datetime, os, time, pyyaml, json, base64

Example Python module install
MAC/Linux "pip install requests"
Windows "python -m pip install requests"

# Debug
Debug file for script run, located in ./debug folder with time/date stamp per line. To disable debug, comment out all lines containing "debug"
