IBM Z Crypto Discovery and Inventory (zCDI) workflows for z/OS
==============================================================

This directory contains z/OSMF workflows that provision IBM Z Crypto Discovery and Inventory (zCDI) on the z/OS platform.

In z/OSMF, a **workflow** is a guided set of steps that help you perform an activity on z/OS®. The zCDI workflows are delivered as PAX archives that contain the workflow definition files (XML), scripts, JCL, and a properties file.


## Workflows

Run the workflows in the following order:

1. **zCDI RACF Setup Workflow** (`setupZcdiRacf.xml`)
   Creates the RACF security definitions that are required to run a zCDI Liberty server. The workflow has 8 phases.

2. **zCDI Db2 Schema Provisioning Workflow** (`setupZcdiDb2.xml`)
   Builds the zCDI Db2 for z/OS schema. The workflow has 3 phases.

3. **zCDI Liberty Server Provisioning Workflow** (`provisionZcdiServer.xml`)
   Provisions, configures, and starts the zCDI WebSphere Liberty server. The workflow has 7 steps.

Each workflow has an end-to-end user guide that describes the prerequisites, the properties file, and each phase or step in detail.


## Prerequisites

- z/OS system with z/OSMF configured and running
- RACF as the security manager
- WebSphere Liberty for z/OS installed
- Db2 for z/OS V13 or later
- A user ID with the authority that is required by each workflow (RACF SPECIAL for the RACF workflow, Db2 SYSADM or equivalent for the Db2 workflow)
