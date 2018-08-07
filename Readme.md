# CRIS.py
   Analyze NGS data for CRISPR (or any engineered endonuclease) activity and screen for clones.
   Screen for NHEJ or multiple HDR events concurrently.

CRIS.py is a an easy to use python script which analyzes NGS data for user-defined sequences.  Users directly modify the python script and run the script in the directory containing target fastq files.  After running CRIS.py, a folder is created in the current directory containing the analysis.

## Installation and Requirements
CRIS.py requires **Python 2.7** and the **Pandas library**.  CRIS.py does not currently run with Python 3.
An easy method to install Python 2.7 and Pandas is through:
    Enthough Canopy available at: https://store.enthought.com/downloads/
    or Anaconda at https://www.anaconda.com/download/


## Usage

To use CRIS.py, directly modify the file CRIS.py in the Python editor.
Change text between quote (') marks to reflect your target amplicon.  CRIS.py reads DNA as a simple text sequence.  Therefore all DNA sequences entered must be on the same strand.
Parameters to modify are:
  1.  ID:   The name of the project, gRNA or gene.  This will be used to create the output folder.
  2.  ref_seq: This is the expected amplicon.  If using forward or merged reads, it will be the 'top' sequence.
  3.  seq_start: A unique 12-20bp sequence in your ref_seq amplicon.  Must be **5'** of the gRNA sequence
  4.  seq_end:  A unique 12-20bp sequence in your ref_seq amplicon.  Must be **3'** of the gRNA sequence.
  5.  fastq_files: These are the fastq files to search.  If you want to run on all fastq files in a directory, leave as "\*.fastq".  If running on only foward reads, use nomenclature of forward reads, ie \*R1_001.fastq
  6.  test_list: A series of names and sequences you wish to search for in fastq file.  Edit the name (ie g10) and the sequence for each desired test.  You can copy the line and add as many as you like.
  
![alt text] (https://github.com/patrickc01/CRIS.py/blob/master/CRISpy_example.jpg)

Save the program/ parameters.

Run the program. Run -> Run File
                 or click the Green triangle/play button.
                 
Check the printed 'Working directory' and verify that is where your fastq files are located.

Check results in newly created folder that has the same label as "ID".

## Output
A folder is created in the working directory with the name 'ID' from step 1.
In the folder are two files:  
1.  a CSV file:  Summary of all fastq files with test_sequences and top indels.
2.  a TXT file:  Summary of all fastq files with sequence information of exact top reads from each fastq file.

## Sample files
All data from paper are uploaded in [example_directory](https://github.com/patrickc01/CRIS.py/tree/master/example_data).  In each zip file are the fastq files and CRIS.py script used to analyze the NGS data.

## Tips
1.  Formatting is important.  Check that all entered text is surrounded by quotes 'like this'
2.  When analyzing data from the CSV file, first look at the SNP check and raw_wt_counter to verify you are getting all reads.
3.  You must close the .CSV file before running the script again.  CRIS.py can not edit a file that is already open in excel.


## Citing



## Acknowledgements
