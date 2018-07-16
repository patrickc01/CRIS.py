# CRIS.py
Analyze NGS data for CRISPR activity and screen clones

Getting Started
CRIS.py is a an easy to use python script which analyzes NGS data for user-defined sequences.  Users directly modify the python script and run they script in the directory containing target fastq files.  After running, a folder is created in the same directory containing the analysis

**Installation and Requirements**
CRIS.py requires **Python 2.7** and the **Pandas library**.  CRIS.py does not currently run with Python 3.
An easy method to install Python 2.7 and Pandas is through:
    Enthough Canopy available at: https://store.enthought.com/downloads/
    or Anaconda at https://www.anaconda.com/download/


**Usage**
To use CRIS.py, directly modify the file CRIS.py in the Python editor.
Change text between quote (') marks to reflect your target amplicon.  CRIS.py reads DNA as a simple text sequence.  Therefore all DNA sequences entered must be on the same strand (this means gRNAs that target the reverse strand will start with 'CC')
Parameters to modify are:
  ID:   The name of the project, gRNA or gene.  This will be used to create the output folder.
  ref_seq: This is the expected amplicon.  If using forward or merged reads, it will be the 'top' sequence.
  seq_start: A unique 12-20bp sequence in your ref_seq amplicon.  Must be **upstream** of the gRNA sequence
  seq_end:  A unique 12-20bp sequence in your ref_seq amplicon.  Must be **downstrea** of the gRNA sequence.
  fastq_files: These are the fastq files to search.  If you want to run on all fastq files in a directory, leave alone.
  test_list: A series of names and sequences you wish to search for in fastq file.

**Sample files**
All data from paper uploaded in sample_directory

Output

Ciiting



Acknowledgements
