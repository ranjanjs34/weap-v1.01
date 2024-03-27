# weap-v1.0.1
# WEAP: Whole Exome Analysis Pipeline


Operating system(s): Ubuntu 20.04 and 22.04.


Programming language used: Bash 

Important: Check bash in your linux using the command:     

           which bash
           
Desired output:

           /usr/bin/bash

Other requirements: Java 11, Python3, GLIBC 2.31 or higher.

Executable Binaries are converted from bash using Shell Script Compiler (SHC). 

Developer: Ranjan Jyoti Sarma and Prof. N. Senthil Kumar

## 1.Downloading WEAP

i.	Install git using:


      sudo apt -y install git


ii.	Change the current directory to Desktop:


      cd  ~/Desktop


iii.	Download WEAP using git:


       git clone https://github.com/ranjanjs34/weap.git


iv.	After downloading, enter into the WEAP:


       cd WEAP
       
       
NOTE: Advanced users may keep WEAP in any convenient location. 


## 2.Setting Up WEAP:


Add execution permission to binary files configure and reference:


       sudo chmod  +x ./configure.bin



## 3.Downloading prerequisite tools [One Time]


To download the prerequisite tools, run the configure as :


       ./configure.bin


Enter the directory address where it downloads the pre-requisite tools:
for example: mkdir /home/$USER/Desktop/weap_dependency
Directory address to be provided in the Configuration as: /home/$USER/Desktop/weap_dependency


There should not be any ‘/’ at the end of the directory address. 



This Script will automatically download and install the required tools and will add to the path so that WEAP can recognize the internal commands. As Please download the ANNOVAR from https://www.openbioinformatics.org/annovar/annovar_download_form.php manually by registering, and follow the instruction providedon the scrren.



## 4.Downloading Reference Data [One Time]:


       ./genome_prep.bin
       ./pull_annovarDB.bin
       ./pull_gatkBundle.bin
This will download the reference genome, Variants with Allele frequency from genomAD project, dbSNP data from gatk bundle and datasets from ANNOVAR web resource to annotate the variants. 





## 5.How to Run WEAP for variant calling (WEAP will guide the users at each step for the input):

There should not be any ‘/’ at the end of the input and output directory address.

    
      ./WEAP.bin  #for parallel mode (Recommended for faster analysis)
      ./WEAP-Serial.bin   #for one task at a time
