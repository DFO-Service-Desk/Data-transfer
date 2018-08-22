# Data-transfer

Describe and track the data transfer from DFO Service Desk to clients.

Account: sdfo000/sdf500 (~mirror)
To synchronized the files between account use rsync linux command:

  rsync -az source/ login@serveur.org:/destination/

## Scripts location:

### Maestro:
Data transfer of custom products via Maestro are in the directory :

  ~/.suites/[project]

### Scripts:
All the scripts that create product and transfer data are in the directory (note that the .log files of the hcron jobs are in there):

  ~/operation/[project]

## hron jobs:
The hcron jobs starting and running the Maestro suites and the scripts for data transfer (see above) are launched via :

  ~/.hcron/hcron1.science.gc.ca/events/[project]




