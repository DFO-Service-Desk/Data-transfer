# Data-transfer

Describe and track the data transfer from DFO Service Desk to clients.

**Account**: sdfo000/sdf500 (~mirror). To synchronized the files between account use rsync linux command:

  rsync -az source/ login@serveur.org:/destination/
  
**Best pratices**: Run your script in sdfo500 if needed but put a copy in the sdfo000 account following the next three steps. For the 3) hcron jobs, add a ~ at the end of the name to indicate that this job is not running at the moment.



## 1) Maestro:
Data transfer of custom products via Maestro are in the directory (is this apply) :

  ~/.suites/[project]

## 2) Scripts only:
All the scripts that create product and transfer data are in the directory (note that the .log files of the hcron jobs are in there *** including those of Maestro *** ):

  ~/operation/[project]

## 3) hron jobs:
The hcron jobs starting and running the Maestro suites and the scripts for data transfer (see above) are launched via :

  ~/.hcron/hcron1.science.gc.ca/events/[project]




