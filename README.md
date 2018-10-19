# aws-inventory

To be used to gather a comprehensive inventory of assets in an AWS Cloud implementation

## Pre-requisites
This program needs Python 3.4 or newer. 

Make sure that you have the latest boto3 version. Older versions may lead to signature error with the newest regions or to some malfunction.

You will also need a service account with an access key and a secret key. The policy documents can be used to create the permissions needed for the service account. Typically a read only role will be fine.

# How to use it
From a terminal or command prompt:
1. aws configure - input your access key and secret key
2. choose your default region
3. choose your default output
4. Browse to the directory where you have downloaded the script to
5. Execute the script in the following way:
    - python inventory.py - This will inventory ALL AWS services - not really necessary
    - Luckily, the script supports arguments - to only run for select services you would enter
    - python inventory SERVICE1 SERVICE 2 -- python inventory.py ec2 s3
6. The script will run and provide you with a json document of what it found.
7. You can then import it into Excel and get the data you need

# Regions #
Right now the default is to run in the US-EAST-1 region. If you need to collect inventory from more than one region, you would simply populate the aws_regions.json with all of the regions you will need to scan


