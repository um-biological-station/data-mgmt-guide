# The Data Life Cycle
This process starts as soon as you begin planning the other parts of your project, often as early as your research proposal. It occurs in 5 phases which will likely happen somewhat simultaneously or more than once.
1. Plan
2. Collect
3. Assure
4. Describe 
5. Preserve  

As a scientist, you will likely analyze your published data. These steps make sure that you are not the only one who can do so.


## Plan 
### create a data management plan (DMP)
This could be a formal proposal or just a guideline for you and your team. Essentially, you are outlining your plans for the next 4 steps of the cycle. Review those steps first before creating a DMP. Regularly update your DMP throughout the process - it will provide most of your metadata.  

Collect:
- Based on the hypotheses and sampling plan, what data will be generated? Choose which data fields you will collect (these will be your table's column names).  
- Decide how your data table(s) will be structured so that they best suit your collection process. 
-> *Consider whether a relational database or other data organization strategy might be most appropriate for your research.*
- Provide descriptive documentation of collection rationale and methods, analysis methods, and any relevant contextual information. 
- What sensors instruments will be used? 
- What cyberinfrastructure will be required to support your research?
- Does your institution have a DMP template?
- What types of personnel will be required to carry out your data management plan? The budget prepared for your research project should include estimated costs for data management.
- What computational resources will be needed? How much data are you planning to generate?
- How can you collect data so that it is already "clean"? (see [tidydata](https://cran.r-project.org/web/packages/tidyr/vignettes/tidy-data.html) standards)  

Assure:
- How can you quality check your data?
- Is your data table structured in a way that is obvious to others?  

Describe:
- How will you produce a metadata record? Using what metadata standard? Using what tool? 
- Will you create a record at the project's inception and update it as you progress with your research? 
- Where will you deposit the metadata? Consider your community's standards when deciding on the metadata standard and data center.  

Preserve:
- Who is in charge of managing the data? 
- How will version control be handled? How will data be backed up, and how often?
- How will you ensure that your data can be recovered in the event of file loss?
- Develop a plan for sharing data with the project team, with other collaborators, and with the broader science community. 
- Under what conditions will data be released to each of these groups? 
- What are the target dates for release to these groups? 
- How will the data be released? 
- Do you need to choose a repository to share it on? Consider what type of data you will generate and which community will make use of the data.
* Check with the repository about requirements for submission, including required data documentation, metadata standards, and any possible restrictions on use(e.g. intellectual property rights). 
Repository specifications will help guide decisions about the remainder of the practices below.*

More resources:
- [Creating a DMP](https://old.dataone.org/sites/all/documents/education-modules/handouts/L03_DataManagement_Handout.pdf)
- [A more formal DMP outline](https://www.icpsr.umich.edu/web/pages/datamanagement/dmp/framework.html)


## Collect
### make observations and gather data
data should be in a digital form


## Assure
### quality assurance / quality control (QA/QC)
- the quality of the data are assured through checks and inspections
- check precision and data field limitations
- is your data clean? it should be if you planned
  - what should tidy data look like
  - if your data needs more significant reorganizing or cleaning: Data Analysis and Visualization in R for Ecologists https://datacarpentry.org/R-ecology-lesson/index.html
   - cleaning with R if you already have R experience https://cdn.rawgit.com/EDIorg/tutorials/master/data_cleaning/R_instructions_exercise.html
   - if you prefer spreadhseets over R: Data Organization in Spreadsheets for Ecologists https://datacarpentry.org/spreadsheet-ecology-lesson/


## Describe
### gather metadata
- data are accurately and thoroughly described using the appropriate metadata standards
- EDI metadata worksheet but maybe clean up and simplify it a bit
- this should be collected throughout (use DMP)
- compile important files
  - EZeml? eml assembly line? depends on R proficiency (ecological data specific)
  - https://ezeml.edirepository.org/eml/
  - https://ediorg.github.io/EMLassemblyline/articles/overview.html


## Preserve
### share your data
- share with your team and if its ok, submitted to an appropriate long-term archive (i.e. data center)
- where to share/publish data:
  - Mfield (not Deepblue)
  - Environmental Data Initiative https://environmentaldatainitiative.org/submit-your-data/
- at the very least have a shared drive/folder/repository for long-term storage (a USB is not good enough! its post-pandemic so there's no longer an excuse for having tech with a single point of failure)


Source: [DataOne Data Management Primer](https://old.dataone.org/sites/all/documents/DataONE_BP_Primer_020212.pdf)
