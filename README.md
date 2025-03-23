# HapMatch: An mtDNA Haplogroup Matching App
Jake Daigle | Bioinformatics, Lund University | 2025
***
## About
This is a web app which was designed to calculate genetic distance, by way of tabulating mtDNA haplogroup-associated differences, between a user and a collection of ancient individuals (or between two selected modern/ancient individuals). The app can be accessed at https://hapmatch.streamlit.app and an example test user file (Test1.tsv) can be downloaded locally and then used in the app. The paper I've written on the development and design of this app can be viewed by anyone at https://docs.google.com/document/d/13dld4dewWlLuCM4SnPzFYnCnQ3oraN_7PlNIU-uvVwk/edit?usp=sharing.

The concept and motivation for this app's development was originally provided by Eran Elhaik of Lund University as a part of the BINP29: DNA Sequencing Informatics II course in the bioinformatics master's degree program at Lund University. 
## Usage
1. Select input mode:
  - User vs. Ancient: for comparing a modern individual against a database of ancient individuals.
  - User vs. User: for comparing two modern individuals against one another.
  - Ancient vs. Ancient: for comparing one individual from the ancient individual database against all others.
2. Select/upload the data for the individual(s) to be compared.
3. See genetic distances recorded in the table presented below.
4. (Optionally) Select a specific individual from the list (if available in current mode) to get more information about them.
5. (Optionally) Toggle on/off the map in the sidebar to see geographical locations of the most closely related individuals.
