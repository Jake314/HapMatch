# HapMatch: An mtDNA Haplogroup Matching App
Jake Daigle | Bioinformatics, Lund University | 2025
***
## About
This is a web app which was designed to calculate genetic distance, by way of tabulating mtDNA haplogroup-associated differences, between a user and a collection of ancient individuals (or between two selected modern/ancient individuals). The app can be accessed at https://hapmatch.streamlit.app and an example test user file (data/Test1.tsv) can be downloaded locally and then used in the app. The paper I've written on the development and design of this app can be viewed by anyone at https://docs.google.com/document/d/13dld4dewWlLuCM4SnPzFYnCnQ3oraN_7PlNIU-uvVwk/edit?usp=sharing.

If one so wishes to run the app locally (personal preference or if the server is down), the repository can be downloaded and the user can navigate to the directory a terminal and run `streamlit run HapMatch.py`. If the data folder is not present, the app will not work. If the .streamlit folder is not present, the app will work but won't look as nice.

The concept and motivation for this app's development were originally provided by Eran Elhaik of Lund University as a part of the BINP29: DNA Sequencing Informatics II course within the bioinformatics master's degree program at Lund University. 
## Usage
1. Select input mode:
  - User vs. Ancient: for comparing a modern individual against a database of ancient individuals.
  - User vs. User: for comparing two modern individuals against one another.
  - Ancient vs. Ancient: for comparing one individual from the ancient individual database against all others.
2. Select/upload the data for the individual(s) to be compared. Uploaded files should be formatted in the following ways:
  - Tab separated (tsv)
  - Contains a header line which starts with #
  - Contains columns labelled chromosome (or chrom), position (or pos), and genotype (or allele1)
3. See genetic distances recorded in the table presented below.
  - A + means both individuals carry the mutation, - means neither do, \ means only the reference does, and / means only the individual of interest does
4. (Optionally) Select a specific individual from the list (if available in current mode) to get more information about them.
5. (Optionally) Toggle on/off the map in the sidebar to see geographical locations of the most closely related individuals.

There is also an input box in the sidebar which lets a user input a read-limit to cap the amount of the reference file the program reads. This is only really useful for testing the functionality of the software when the process needs to run many times.
## Example
Open the app (wake up if necessary), upload data/Test1.tsv to the user file slot, enter haplogroup "X2c2" (must press enter) and click run.
![Screenshot 2025-03-24 113216](https://github.com/user-attachments/assets/c2e52e4b-b932-42a9-b86e-a105aef2029b) 
We see that one of the closets results (among others) is I5373. Neither individual has the A227G mutation (and at least one has a gap there), while both have the G1719A mutation (among others).
![image](https://github.com/user-attachments/assets/e90bb6a0-c23b-4b8f-948e-9915ad9a46a1)
By selecting I5373 to see more info, we can see that they are a male from Great Britain, and are labelled as being haplogroup X2b+226.

