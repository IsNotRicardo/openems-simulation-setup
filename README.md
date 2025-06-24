# OpenEMS Simulation Setup

This repository contains all the files needed to run the simulation of the "Energy Optimization for Factories & Manufacturing units", developed using [OpenEMS](https://github.com/OpenEMS/openems). Each directory contains different files, explained in the sections below

## Setup

A guide on how to setup the OpenEMS Edges and the OpenEMS Backend can be found [here](https://docs.google.com/document/d/1jlzYWELOZlOSCAUN_QZrmKhfBdIGzFCbjZBVsHW-s-Q/edit?tab=t.0#heading=h.dgj6niftdjn1).

## Bruno

This directory contains the Bruno collection which automatically creates all the components in the OpenEMS Edges that are needed to run the simulation. The collections contains two directories: **Create components**, **Delete components** and **Additional configurations**. The latter contains options to customize the simulation.

## Postman

This directory contains the Postman collection in JSON which automatically creates all the components in the OpenEMS Edges that are needed to run the simulation. Once imported into Postman, the collection will contain the same directories as Bruno.

## Simulation Edges

This directory contains the Docker compose file which creates the Docker containers for all OpenEMS Edges used in the simulation. The number of Edges can be changed at will, and more information about them can be found in the guide in the abovementioned guide.

## Simulation Server

This directory contains the Docker compose file which creates the Docker containers for the OpenEMS Backend and InfluxDB. It also contains the `metadata.json` file, which is where the connection credentials of all the Edges are stored. This file or the information contained in it should be included in the Backend container files, as instructed in the guide at the beginning.
