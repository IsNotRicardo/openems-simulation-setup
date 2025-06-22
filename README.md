# OpenEMS Simulation Setup

This repository contains all the files needed to run the simulation of the "Energy Optimization for Factories & Manufacturing units", developed using [OpenEMS](https://github.com/OpenEMS/openems). Each directory contains different files, explained in the sections below

## Setup

A guide on how to setup the OpenEMS Edges and the OpenEMS Backend can be found [here](https://docs.google.com/document/d/1jlzYWELOZlOSCAUN_QZrmKhfBdIGzFCbjZBVsHW-s-Q/edit?tab=t.0#heading=h.dgj6niftdjn1).

## Postman

This directory contains the Postman collection in JSON which automatically creates all the components in the OpenEMS Edges that are needed to run the simulation. Once imported into Postman, the collection itself contains two directories: **Create components** and **Delete components**. As the names suggest, running each specific folder will create or remove the necessary components, respectively.

## Simulation Edges

This directory contains the Docker compose file which creates the Docker containers for all OpenEMS Edges used in the simulation. The number of Edges can be changed at will, and more information about them can be found in the guide in the abovementioned guide.

## Simulation Server

This directory contains the Docker compose file which creates the Docker containers for the OpenEMS Backend and InfluxDB. It also contains the `metadata.json` file, which is where the connection credentials of all the Edges are stored. This file or the information contained in it should be included in the Backend container files, as instructed in the guide at the beginning.
