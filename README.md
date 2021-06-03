# Data Management at the University of Michigan Biological Station
### a guide to help UMBS researchers and students on data management
Created by Alex Pawlik (apawlik@umich.edu) and Jason Tallant (jtallant@umich.edu)


## Why manage your data? 
- your research is most credible when backed by data that is reproducable and reusable
- you're saving science money and resources by making your data accessible to others (and sometimes your grant will require this anyway!)
- If you give your data to a colleague who has not been involved with your project, will they be able to make sense of it? Will they be able to use it effectively and properly? 
https://www.youtube.com/watch?v=N2zK3sAtr-4

*docs to be paraphrased and linked*
- Data management primer https://old.dataone.org/sites/all/documents/DataONE_BP_Primer_020212.pdf
- data managing and sharing https://ukdataservice.ac.uk/media/622417/managingsharing.pdf

## How to manage your data: Create a data management plan (DMP)
- could be a formal proposal or just a guideline for you and your team
- creating a data mgmt plan https://old.dataone.org/sites/all/documents/education-modules/handouts/L03_DataManagement_Handout.pdf
  - more formal DMP outline https://www.icpsr.umich.edu/web/pages/datamanagement/dmp/framework.html

metadata:
- EDI metadata worksheet but maybe clean up and simplify it a bit
- compile once data collection is finished

cleaning:
- what should tidy data look like
- if your data needs more significant reorganizing or cleaning: Data Analysis and Visualization in R for Ecologists https://datacarpentry.org/R-ecology-lesson/index.html
  * avoid this by making a good DMP and initially collecting data in a tidy way
  - cleaning with R if you already have R experience https://cdn.rawgit.com/EDIorg/tutorials/master/data_cleaning/R_instructions_exercise.html
  - if you prefer spreadhseets over R: Data Organization in Spreadsheets for Ecologists https://datacarpentry.org/spreadsheet-ecology-lesson/

compiling:
- which files are important
- finalize metadata 
  - EZeml? eml assembly line? depends on R proficiency (ecological data specific)
  - https://ezeml.edirepository.org/eml/
  - https://ediorg.github.io/EMLassemblyline/articles/overview.html

where to share/publish data:
- Mfield (not Deepblue)
- EDI? (ecological data specific)
- at the very least have a shared drive/folder/repository for long-term storage (a USB is not good enough! its 2021 and there's no longer an excuse for having tech with a single point of failure)


## Other resources:
- more specific topics in data mgmt education https://old.dataone.org/education-modules
- Mlibrary DMP resources https://guides.lib.umich.edu/engin-dmp
- example of descriptive and reusable data: weather observations from UMBS https://portal.edirepository.org/nis/mapbrowse?scope=edi&identifier=549
- EDI people
- jtallant@umich.edu and apawlik@umich.edu


*how much of this can be incorporated into an R notebook?*

