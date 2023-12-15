# JWST Pipeline Caveat Notebooks

The repository contains notebooks or scripts intended to aid the community in mitigating issues that affect, or recently affected, data products available in the MAST archive.

Please direct all questions and comments about the information contained within to the [JWST Help Desk](https://jwsthelp.stsci.edu).

If you have a specific issue using one of the example scripts or notebooks, you can include a link to that file with the help desk call. 


Some issues can be fixed by reprocessing data on your computer, using the latest [JWST pipeline](https://github.com/spacetelescope/jwst) release and/or [calibration reference data](https://jwst-crds.stsci.edu/)(CRDS) context. 

It takes a few weeks to integrate a new calibration pipeline build into a full Science & Operations Center (S&OC) software build, test the S&OC build, fix subsystem interface issues, and finally install the S&OC build in operations. After that, fixes in the new pipeline software and/or reference data will be reflected in new (or replaced) products in MAST. 

[The software vs DMS build table in the JWST pipeline repository](https://github.com/spacetelescope/jwst) indicates when jwst builds were released, which reference data (CRDS) context they were tested with, and when the was first used in S&OC operations. Some JWST releases (particularly S&OC release candidates) are never installed in operations. That page also provides detailed instructions on how to create a fresh conda environment, install the version of the pipeline you would like to use, and how to configure the CRDS environment that is appropriate for that release.


## Deprecation of Notebooks

If JWST DMS infrastructure has been updated, and the workarounds in a specific notebook are no longer neccessary or recommended, then the notebook will be deprecated. The process for deprecating a notebook includes the following:

*  Ensure that any DMS software or reference file updates have been released publicly
*  Update the notebook to include a new cell at the top of the notebook which contains:
    * A sentence in large font explaining that the workaround is no longer needed and the notebook is deprecated
    * The calibration software version that contains the fix
    * The CRDS context that should be used
    * A timeline that reprocessing will occur that will update the files in the JWST Archive
 

*  Submit a PR that includes the updated files
*  Make sure that the JDOX table and information has been updated appropriately
*  After PR acceptance, the notebook should stay available for a period of 1 month, or until after reprocessing in the Archive as completed,  so that folks can still view it easily 
    * After the specified time, create and submit a PR that removes the notebook from the repository

