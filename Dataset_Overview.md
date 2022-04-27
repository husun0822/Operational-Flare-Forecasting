# Solar Flare Datasets: What we have and how we can access more

This readme document is written to give a general overview about the existing datasets we have right now and give some additional guidance and resources for obtaining new data. Please update the information here if you have new resources available.

### Existing Datasets (What we have so far):

Our data for solar flare forecast machine learning works are measured in Terabytes (TB), making it hard to keep a local copy of the entire database. But since the data are organized in a hierachical structure (based on active region #), one can always compile a smaller amount of data files to test models & do feature engineering locally on your own laptop.

The data is stored using our SOLSTICE disk and can be accessed via the U-M **GreatLakes** HPC. See [here](https://arc.umich.edu/greatlakes/user-guide/) if you are new to GreatLakes. To access the folder where the data locates once you logged onto the GreatLakes remote machine, simply type 
```
cd ../../nfs/clasp-solsticedisk/SUMS/
```
and now you are in the root folder of the database!

There are several relevant subdirectories under this root folder:
```
/SUMS/
│       
└───AIA 
│
└───GOES
│
└───SHARP
    │
    └─── header
    └─── image
│
└───SMARP
│
└───SPAT
```

* AIA: Atmospheric Imaging Assembly (AIA) Data, grouped by active region (.sav files)
* GOES: The flare event list based on the Geostationary Operational Environmental Satellite (GOES), covering the period of 1996-Jan to 2021-Nov (.csv file)
* SHARP: there are two subfolders here
    * header: Space-Weather HMI-Active Region Patch (SHARP) data, time-series data grouped by active region. (.csv files) See [here](https://agupubs.onlinelibrary.wiley.com/doi/full/10.1029/2019SW002214) for a paper by our group on using SHARP data to predict flares. And [here](http://jsoc.stanford.edu/doc/data/hmi/sharp/sharp.htm) for a very accessible tutorial on what is SHARP and how to query more SHARP data.
    * image: The low-resolution Helioseismic and Magnetic Imager (HMI) data grouped by active region. (.fits files)
     

     
