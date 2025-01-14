# Config.yml File Setup

This is a reference for all template options when setting up your config.yml file.

* api_key: "`enter your` [Flywheel API key](API_key.md) `here`"
* participants_csv: "`enter the name of the csv file containing your participants list`"
* fw_project_path: "`enter the directory address of your flywheel project`"
* output_dir: "`enter the directory where you want to output the end product`"
* temp_dir: "`enter the directory of the intermediary files`"
* config_json: "`enter the directory of the dcm2bids_config.json file (necessary to run dcm2bids, an intermediary tool used to convert dicom files to BIDS format)`" 

    Detailed instructions on how to set up the `dcm2bids_config.json` file can be found here: <https://unfmontreal.github.io/Dcm2Bids/3.1.1/how-to/create-config-file/#configuration-file-example>

* num_threads: "`insert desired number of threads here`"

    If exceeding 10 in Gene, please use 'nice -n' as described in <https://gene.stanford.edu/docs/#temporary-files>.

* scan_names:

    `- enter the name of the scan of interest`

    `- subsequent_scan_name`

* exclude_strings: 

    `- enter the name of string patterns you wish to exclude from the download`
    
    `- subsequent_scan_name`

* BIDS_validate: `enter True/False. if set to "True", BIDS_validate will test whether the files were successfully converted to BIDS format.` 
* clean_up: `enter True/False. Set to False only if you want to keep the intermediate dicom files (not recommended!)`

## Example Setup
``` py linenums="1"
api_key: "your_API_key"  
participants_csv: "participants_ids.csv" 
fw_project_path: "mormino/Lucas_PETMR"
output_dir: "/mnt/poston/projects/parkinsons/postonlab/EvaETP_IVIM/test_fw_bids"
temp_dir: "/scratch"
config_json: "/mnt/poston/projects/parkinsons/postonlab/EvaETP_IVIM/flywheel_2_BIDS/dcm2bids_config.json"
num_threads: 5 
scan_names:
  - CLARiTI_Accelerated_Sagittal
  - DTI_108_7s_2thick_2space_DL
  - DTI_84_7s_2thick_2space_DL_pepolar 
  - CLARiTI_Accelerated_Sagittal
  - Accelerated Sagittal IR-FSPGR (SCAN)
exclude_strings:
  - SOURCE
BIDS_validate: True 
clean_up: True 
```