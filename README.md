# IEOR E4501 Project


## Group Name and Section

- Project Group 62
- Section 2


## Group Members and UNIs

- Jiaxian Hu, jh4311
- Yi Xiao, yx2530


## Dataset

The dataset of the project consists of calls to the [**311 phone number**][311 phone number] for non-emergency services in 2020, which is published on [**NYC OpenData**][NYC OpenData]. Pre-exported CSV file (around 1.5GB) can be found in this [shared folder][311-folder].

[311 phone number]: https://www.ny.gov/agencies/nyc-311
[NYC OpenData]: https://opendata.cityofnewyork.us
[311-folder]: https://drive.google.com/drive/folders/1BRd8_RSST69UaZRBeD_dtXGw9fuKoBZE


## Description of Codes Implemented

In the Jupyter notebook named **Top10.ipynb**, considering the size of the dataset, the CSV file is read into DataFrames by chunks with each chunk size of 10,000. While reading data from the CSV file, only calls with "Incident ZIP" of 10025 are kept and stored into a single DataFrame. Group the DataFrame of calls from ZIP code 10025 by "Complaint Type", and compute group size of each type. Sort incident types by number of incidents in descending order. Top 10 incident types along with number of incidents of each type are stored in the variable called "top10."

In the Jupyter notebook named **Parking.ipynb**, again, considering the size of the dataset, the CSV file is read into DataFrames by chunks with each chunk size of 10,000. The data is loaded for two times. The first time is for computing number of parking incidents and number of incidents for the whole dataset. The second time is for computing parking incidents and total incidents happened in region 10025. The parking propotions are then computed and compared accordingly.
