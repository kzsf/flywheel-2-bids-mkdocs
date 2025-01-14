# Flywheel2BIDS

Scripts to get data from Flywheel and convert to BIDS format.

## How to Use
#### 1. Clone the repository locally
* Clone the repository on your local computer by running the following command in your terminal: 

 `git clone https://github.com/PostonLab/flywheel_2_BIDS.git`

* Change directories into the repository and locate the config.yml file. 

`cd path_to_cloned_repository` 
#### 2. Set up config.yml file 
* The `config.yml` file is a file used to customize the converter.py script to handle your specific project. Edit the config.yml file to fit your project needs. You will need to create a Flywheel API key to complete this step. 
* For detailed instructions on how to set up the [config file](configfile.md) or create a [Flywheel API key](API_key.md), please refer to their respective pages.  
#### 3. Run Converter.py
* The `converter.py` file is a python script that downloads your specified data from Flywheel (using parameters set in the config.yml file) and outputs the data in BIDS format.
* To run the converter:
    
    - In your terminal, `cd` into the repository where the converter.py file is located.

    - Next, run the following command to run the script: 

    `python converter.py` 

* If everything worked, the output will be BIDS formatted scans located in the `output_dir` parameter set in the config.yml file.