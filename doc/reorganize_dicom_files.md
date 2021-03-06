## reorganize_dicom_files

This is a BIDS conversion utility to reorganize an existing MRI DICOM dataset. It works on a collection of DICOM files in a single directory or over multiple directories. It copies or moves the files according to the source BIDS structure that we started using from 2017 onwards at the DCCN. Note that it **does not convert** the DICOM files to NIfTI.

It is an executable Python script which you can run from the Linux command line. It creates a Bash shell script which you should save to file, check and where needed edit (i.e. rename subject identifiers) and subsequently execute using bash. Further details are provided if you execute it without any arguments:

```
This script searches through a directory for DICOM files and writes
them to the output screen in such a way that you can easily make a script
to reorganize them to a BIDS structure.

You should save the output to a script, edit the script and then execute it.

Use as
  ./reorganize_dicom_files -c <command> -o <outputdir> [inputdir]

Optional arguments
   -c <command>   command to execute, eg. mv or cp
   -x             do not check file extensions
```

Following this tool, you would probably continue with converting the DICOM files from the "source" structure into NIfTI files. For that you can have a look at my [convert_raw_to_bids](convert_raw_to_bids.md) script. 

Alternatives for converting DICOM files to BIDS/NIfTI are:  
  * [dac2bids](https://github.com/dangom/dac2bids)
  * [bidscoiner](https://github.com/marcelzwiers/bidscoiner) 
  * [heudiconv](https://github.com/nipy/heudiconv)
  * [pyBIDSconv](https://github.com/DrMichaelLindner/pyBIDSconv)
  
See also
  * [reorganize_brainvision_files](reorganize_brainvision_files.md)
  * [reorganize_ctf_files](reorganize_ctf_files.md)
  * [reorganize_nifti_files](reorganize_nifti_files.md)
  * [reorganize_presentation_files](reorganize_presentation_files.md)
  


