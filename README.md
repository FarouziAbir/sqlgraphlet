# sqlgraphlet

## Table of contents
* [General info](#general-info)
* [Technologies](#technologies)
* [Setup](#setup)
* [Usage](#usage)
* [Datasets](#datasets)
* [Publication](#publication)

## General info
This project aim to provide an efficient solution for pattern of three and four vertices enumeration in large graphs using queries.

## Technologies
The project is programmed using python 3. The requirements are presented as follows:
* Cluster: 4, 8, 9, 16, 27 or 81 hosts, each host with 4 cpu cores, 4 GB of main memory and 500 GB of disk at least. The cluster should define a shared-nothing architecture
* OS: Linux Ubuntu server 18.06 or above
* Language: Python 3.0 or higher
* DBMS: Vertica DBMS or any other relational DBMS with partitioning control (please refer to this page for installation guidelines).
* Libraries: vertica_python client and Pandas

## Setup
After installing the requirements, update the following lines in the code with your inputs:

<code> conn_info = {'database': database_name, 'port': 5433, 'user': username, 'password': password}</code>

## Usage
On a terminal, use the following command to execute the code:

<code>python sqlgraphlet.py /link/to/graph_file delimiter #_of_machines #_of_colors</code> 


The delimiter can be comma, space or tab

The number of machines (#_of_machines) should be (#_of_colors)^2, (#_of_colors)^3 or (#_of_colors)^4

## Datasets
The data set to use should be the edge list. It should have two columns (source_id del destination_id), where del refers to the delimiter.

## Publication
Abir Farouzi, Xiantian Zhou, Ladjel Bellatreche, Mimoun Malki, & Carlos Ordonez. (2023). Parallel Patern Enumeration in Large Graphs. In preceeding: Database and Expert Systems Applications (DEXA). 
