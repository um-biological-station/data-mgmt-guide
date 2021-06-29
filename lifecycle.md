# The Data Life Cycle
This process starts as soon as you begin planning the other parts of your project, often as early as your research proposal. It occurs in 5 phases which will likely happen somewhat simultaneously or more than once.
1. [PLAN](#plan-create-a-data-management-plan-dmp)
2. [COLLECT](#collect-make-observations-and-gather-data)
3. [ASSURE](#assure-quality-assurance--quality-control-qaqc)
4. [DESCRIBE](#describe-gather-metadata)
5. [PRESERVE](#preserve-share-your-data)   

As a scientist, you will likely analyze your published data. These steps make sure that you are not the only one who can do so.  

## PLAN: create a data management plan (DMP)
This could be a formal proposal or just a guideline for you and your team. Essentially, you are outlining your plans for the next 4 steps of the cycle. Review those steps first before creating a DMP. Regularly update your DMP throughout the process - it will provide most of your metadata.  

- Collect:
  - Based on the hypotheses and sampling plan, what data will be generated? Choose which data fields you will collect (these will be your table's column names).  
  - Decide how your data table(s) will be structured so that they best suit your collection process. 
  - *Consider whether a relational database or other data organization strategy might be most appropriate for your research.*
  - Provide descriptive documentation of collection rationale and methods, analysis methods, and any relevant contextual information. 
  - What sensors instruments will be used? 
  - What cyberinfrastructure will be required to support your research?
  - Does your institution or discipline have a DMP template? (see [DMPTool](https://dmptool.org/))
  - What types of personnel will be required to carry out your data management plan? The budget prepared for your research project should include estimated costs for data management.
  - What computational resources will be needed? How much data are you planning to generate?
  - How can you collect data so that it is already "clean"? (see [tidydata](https://cran.r-project.org/web/packages/tidyr/vignettes/tidy-data.html) standards)  
- Assure:
  - How can you quality check your data?
  - Is your data table structured in a way that is obvious to others?  
- Describe:
  - How will you produce a metadata record? Using what metadata standard? Using what tool? 
  - Will you create a record at the project's inception and update it as you progress with your research? 
  - Where will you deposit the metadata? Consider your community's standards when deciding on the metadata standard and data center.  
- Preserve:
  - Who is in charge of managing the data? 
  - How will version control be handled? How will data be backed up, and how often?
  - How will you ensure that your data can be recovered in the event of file loss?
  - Develop a plan for sharing data with the project team, with other collaborators, and with the broader science community. 
  - Under what conditions will data be released to each of these groups? 
  - What are the target dates for release to these groups? 
  - How will the data be released? 
  - Do you need to choose a repository to share it on? Consider what type of data you will generate and which community will make use of the data.
  - *Check with the repository about requirements for submission, including required data documentation, metadata standards, and any possible restrictions on use e.g. intellectual property rights). Repository specifications will help guide decisions about the remainder of the practices below.*

More resources:
- [Creating a DMP](https://old.dataone.org/sites/all/documents/education-modules/handouts/L03_DataManagement_Handout.pdf)
- [A more formal DMP outline](https://www.icpsr.umich.edu/web/pages/datamanagement/dmp/framework.html)
- [DMPTool](https://dmptool.org/)


## COLLECT: make observations and gather data
Your goal here is to produce clean, reusable data. More organization now means less work later. 

- Carefully consider your methods and data format before beginning collection. 
  - Set up data templates/tables ahead of time and collect data in digital form when possible. 
  - Use consistent organization.
- Keep your raw data, even if you clean it immediately. 
  - Raw data is what you collect in the field or direct output from instruments. It's important for data integrity.
- Collect as much metadata as possible. Site locations, data field units, etc. are all relevant to your final dataset.
  - Take a metadata template with you to the field. 
- Choose data fields that are one of the following types: numerical, text, categorical, boolean, or date. (You can also use lists as data, but this makes things a little trickier.)
  - Don't use any special symbols in your variables names or data. Certain software will misinterpret or disallow even symbols like these @ ~ % <, so you'll save yourself work by just sticking to letters, numbers, and basic punctuation.


## ASSURE: quality assurance / quality control (QA/QC)
Determine what quality standards you will hold your data to (see options below). Do basic quality assurance and control during data collection, entry, and analysis. *The cleaner your data collection is, the easier this will be.*

- Describe any conditions during collection that might affect the quality of the data. 
- Document all quality checks and cleaning steps, either with code (R notebook, Python script, etc.) or in a plain text file. Either way, your steps should be unambiguous to someone familiar with your dataset.
- Make sure your data table has no empty cells by defining standard missing values.
- Identify values that are estimated, double-check data that are entered by hand (preferably entered by more than one person), and use quality level flags (see here) to indicate potential problems. Indicate values that are potentially out of range with flags, as well.
- Check the format of the data to be sure it is consistent across the data set. 
- Perform statistical and graphical summaries (e.g. max/min, average, range) to check for questionable or impossible values and to identify outliers. 
- Communicate data quality using either coding within the data set that indicates quality, or in the metadata or data documentation. 
- Identify missing values. 
- Make sure that numeric precision is consistent within each data field.
- *Additional problems with the data may also be identified during analysis and interpretation of the data.*

More resources:
- [DataONE Quality Standards](https://old.dataone.org/best-practices/ensure-basic-quality-control)
- [tidydata Guidelines](https://cran.r-project.org/web/packages/tidyr/vignettes/tidy-data.html)
- Data Carpentry's [Data Analysis and Visualization in R for Ecologists](https://datacarpentry.org/R-ecology-lesson/index.html) (no R experience)
- Enviornmental Data Initiative's [Data Cleaning with R](https://cdn.rawgit.com/EDIorg/tutorials/master/data_cleaning/R_instructions_exercise.html) (assumes familiarity with R)
- Data Carpentry's [Data Organization in Spreadsheets for Ecologists](https://datacarpentry.org/spreadsheet-ecology-lesson/)


## DESCRIBE: gather metadata
Metadata - data about your data - is essential for future comprehension and repeatability of your work. Utilize the metadata format corresponding to the field that your research best fits into. Note that almost all formats/tools for enviornmental data result in a .XML (extensible markup language) file. This is standard - the .XML file should be considered with as much importance as your data table files.

- Collect meatdata throughout the entire data lifecycle. 
  - Some can be extracted from your DMP, assuming you kept it updated. 
  - Ideally, you'll have mostly complete metadata after filling out a metadata template during data collection.
- Compile and keep a list of important files: raw data, clean data, data cleaning scripts/instructions, methods documents, images of field notes, etc.
- Often, [EML (Ecological Metadata Language)](https://eml.ecoinformatics.org/) is the go-to format for environmental metadata.
- The metadata you need to collect may depend on the format you choose, but the essentials are still the same.
  - EDI's [metadata template](https://github.com/EDIorg/MetadataTemplates) - great for printing and taking to the field 
  - DataONE's [list of important metadata and best practices](https://dataoneorg.github.io/Education/bp_step/describe/) 
  - EDI's [best practices for EML](https://environmentaldatainitiative.org/five-phases-of-data-publishing/phase-3/metadata-best-practices/)
- Find a compiling or validation tool for your metadata file. It's the easiest way to guarantee that your metadata file meets the standards you chose.
  - EDI's [ezEML](https://ezeml.edirepository.org/eml/) - compiling EML without R
  - EDI's [EML assemblyline](https://ediorg.github.io/EMLassemblyline/articles/overview.html) - R package for compiling EML


## PRESERVE: share your data
Your data isn't very useful if only you can see it. Use technology to make your dataset accessible, reusable, and repeatable. After metadata is compiled and you don't plan on making any more changes to your files, it's time to preserve your data.
*Your work may provide data that the scientific community desperately needs in the future. Imagine if virologists hadn't saved their 2019 data on coronaviruses...*

- Consider legal and policy restrictions that might affect how your data can be distributed.
  - Check your institution's policies on privacy and confidentiality.
  - Data are not copyrightable. Ensure that you have the appropriate permissions when using data that has multiple owners or copyright layers. Information documenting the context of data collection may be under copyright.
  - Data is able to be licensed. The manner in which you license your data can determine its ability to be consumed by other scholars. If your data fall into any of the following categories, there are additional considerations regarding sharing: rare, threatened or endangered species; cultural items returned to their
country of origin; Native American and Native Hawaiian human remains and objects; any research involving human subjects. 
  - If you use data from other sources, you should review your rights to use the data and be sure you have the appropriate licenses and permissions.
- Use file formats that are easy to open and accessible to all (ie. ".txt" or ".csv", not ".docx" or ".xlsx").
- Identify data with long-term value. 
  - It's not necessary to archive all of the data products generated from your research. 
  - Consider the size of your files, which data will be most useful for future data users (typically raw data), and which data versions would be most difficult to reproduce.
- Choose keywords using a controlled vocabulary (CV) to make your data easier to find.  example: [LTER Controlled Vocabulary](https://vocab.lternet.edu/vocab/vocab/index.php)
- Share data with your team. Create at least one backup on Google Drive, OneCloud, etc. 
- If appropriate, also submit to a long-term archive (i.e. data repository). They provide the tools that helps others find, use, and cite your data.
  - DataONE [member repositories](https://www.dataone.org/network/#list-of-member-repositories) - a list of 40+ reputable environmental data repositories
  - EDI's [repository](https://environmentaldatainitiative.org/submit-your-data/) - especially good if you want 1-on-1 assistance with metadata compilation and/or data publishing


-----------

*Source: DataONE (Data Observation Network for Earth) [Data Management Primer](https://old.dataone.org/sites/all/documents/DataONE_BP_Primer_020212.pdf)*


[<--  Back](index.md)
