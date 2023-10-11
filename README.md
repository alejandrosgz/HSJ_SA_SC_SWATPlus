# HSJ_SA_SA_SWATPlus

This repository contains data related to the manuscript *Using sensitivity analysis and soft calibration of geological regions to improve the representation of hydrological processes in a SWAT+ model*.


**To find the raw simulations used in this work, access to the *Zenodo* repository: https://zenodo.org/record/8432546 (last version --> Version 1).**



In this GitHub repository, the needed data to reproduce most of the work can be found.


The main folder of the repository contains the following files:

* **README** files --> This file, where the structure of the repository and a description of files/folders can be found.

* **HSJ_SA_SC_paper.qmd** --> Quarto document where the manuscript was written. It was optimized to rendering to Word.

* **template.docs** --> Template for rendering to Word.

* **HSJ_SA_SC_bib.bib** --> References file exported through Zotero.

* **LICENSE** --> License of the repository.


Two important folders are located in the main directory:

* **Script** folder: Where the *SA_SC_Script.R* file can be found, which contains all the code used to perform this work. The script is structured in different sections and code is commented, explaining the main steps. The main steps of the methodology of the work can be found in this file, but some code that was repeated (e.g., same code for analyzing the three soft calibration rounds) has not been repeated. Results obtained and plots created can be reproduced, since post-processed data of the simulations has been included in the repository. However, to perform all the steps of the analysis, the raw simulations should be downloaded from the Zenodo repository mentioned in this README file. 


* **Data** folder: Divided in several folders:

    + **Figs_PNG** --> Contains the plots included in the html and the manuscript.
    
    + **Simulations** --> Contains the simulation files created with SWATPlusR for the soft calibration. To perform the entire analysis for the different rounds, the Zenodo repository contains should be saved in this folder. The post processed files that this folder contains are:
      - *default_channels.rds* --> Default simulation of the channels.
      - *default_modelwb.rds* --> Default water balance variables for LSUs and basin.
      - *observed_list.rds* --> Observed streamflow data.
      - *streamflow_metrics_allsims.rds* --> Streamflow performance metrics obtained for all the soft calibration simulations.
   
    + **lsus_lithology_spatial_analysis** --> Files used for the geological landscape units (LSUs) characterization and zonification:
      - *modeled_basin.shp* and related files --> Upper Tagus River basin shapefile.
      - *lsus2.shp* and related files --> LSUS file, obtained from the model.
      - *tiff_permeabildiad_types_250m.tif* --> Raster layer with permeability classes.
      - *zonal_histogram_LSUs_lithology.csv* --> Zonal histogram of the permeability-lithology classed for each LSU.
      - *lsus_lithology_configuration.shp* and related files --> Shapefile created, where the main geological materials for each LSU are defined.
      
    + **TxtInOut_data** --> Contains the file *ls_unit.def*, used to obtain the Hydrologic response units (HRUs) for each LSU and for each geological region. Extracted from the model TxtInOut.
    
    + **Results_WB** --> Contains for each of the Soft calibration iterations, a folder where the aggregated water balance for each geological region can be found.
    
    + **csv_files** --> Contains the following files:
    
      - *lsus_configuration.csv* --> It is the attribute table of the shapefile *lsus_lithology_configuration.shp*.
      - *soft_data_results.csv* --> Contains the soft data variables values estimated in previous work.
      - *par_tab.txt* --> Values of the parameter ranges used for each soft calibration iteration.
      - *"sum_tab_stats.csv"* --> Statiscital summary of the streamflow simulation performance for each subbasins in each iteration and default model.
      - *wyld_evolution_comp.csv* --> Distribution of the runoff coeffficient values for the three soft calibration iterations
      - *bsfl_evolution_comp.csv* --> Distribution of groundwater contribution values for the three soft calibration iterations
      
    + **SA_Data** --> Contains the following files:
      
      - *lsus_configuration.csv* --> It is the attribute table of the shapefile *lsus_lithology_configuration.shp*.
      - *230414_sobol_sample.rds* --> Contains the parameter set used for the SA
      - *var_extracted* Folder --> Contains the data extracted from the raw simulations. Can be downladed from the Zenodo repository, not included for its weigth.
      - *var_aggregate* Folder --> Contains the post processed data of the SA (one file for each variable.
      
    
    
Other folders/files can be ignored.
    
    
For doubts about the structure or contain of the repository, or bugs notification, contact with corresponding author: alejandro.sanchezgomez97@gmail.com, alejandro.sanchezg@uah.es.

    
    


