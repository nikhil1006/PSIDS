# PSIDS (Pass Scheduler Information Display System)

* After the data is fetched from the input file the output file of the Pass scheduler takes the data file consisting of several fields such as (AOS, LOS, etc.,) and shows the respective countdowns for data on, data off in real time for multiple satellites In a browser interface.

* The data file for the pass scheduler information display system consists of several fields which are needed to be pre processed in any one of the analytical software tools.

## 1. Introduction

### 1.1 Pre-processing of the data file

* Keeping in mind the number of columns present in the data file, the data has been decided to be pre processed with *R Language* .

* The tool used for implementation of the *R language* is *Anaconda Open Source Distribution*.

### 1.2 Backend Module for The WEB browser Interface

* The Backend Module for the web browser interface is developed using _XAMPP_.

### 1.3 Web Browser Interface

* The web browser Interface for the Pass Scheduler Information Display System (PSIDS) is designed using HTML, CSS, and PHP keeping the ease and the simplicity they offer and their easy integration with XAMPP’s backend modules

## 2. Methodology

### 2.1 Operations for Pre-Processing of Data file

* The data file is pre processed using a specific R package called ```data.table```. data.table is an R package that provides an enhanced version of data.frames

* After all the pre-processing is done the data is stored in ```file.csv``` file and saved.

### 2.2 Operations for the Backend XAMPP Module

* The saved .csv data file containing the PSIDS information is converted into a MySql database ```station_info``` having a table ```pass_info```.

* The Backend for the web browser Interface is hosted in *Apache* and *Tomcat* servers of the XAMPP.

* The servers are hosted on localhosts hence making them easily accessible to even remote systems provided the source code is available.

### 2.3 Operations for the WEB browser interface

* The front end for the web browser interface is designed using HTML and CSS & web browser interface is in by default dark mode.

* The PSIDS web page displays 6 columns from the ```pass_info``` table of the ```station_info``` database.The columns that are on display are ```sat_id```, ```orbit_no```, ```dt_on```, ```dt_off```, ```m_tid```, ```b_tid```.

* he new Column called ```countdown``` is added which shows the real time countdown for the ```dt_on``` and ```dt_off``` columns with respect to the current *system time*.

## 3. Results & Screenshots

### 3.1 Results for Backend Module

<img src="https://photos.google.com/u/2/photo/AF1QipOkyqk5PHmSR2Be4AoXzyhpc5UNB9yzz5IvYucL" width=900/></img>

<p align="center"><i><b>Figure 3.1 pass_info data</b></i></p>

* The final records of the database which contains the data of the pass scheduler dataset file is as shown.

### 3.2 Results for WEB browser interface

<img src="https://github.com/nikhil1006/PSIDS/blob/master/Screenshot%20(887).png" width=900/></img>

<p align="center"><i><b>Figure 3.2 PSIDS web page</b></i></p>

<img src="https://github.com/nikhil1006/PSIDS/blob/master/PSIDS.gif" width=900/></img>

## Prerequisites
* you need *Anaconda Distribution* with *R kernel* installed & also *XAMPP* installed.
* you can download anaconda distribution from [here](https://www.anaconda.com/distribution/)
* you can download XAMPP from [here](https://www.apachefriends.org/download.html)

## Software Installations
* After downloading and setting up the anaconda environment run the following command in *anaconda prompt* to install *R kernel* in Jupiter notebook
```
$ conda install -c r r-essentials
```
* After downloading XAMPP, follow the installation steps as it is.

## Execution

* After installing XAMPP copy the ```data``` folder into your ```MySql``` folder and ```PSIDS.html``` file into your htdocs.
* Now open the *XAMPP control panel* and start the ```apache``` & ```MySql``` services.

## Built with
* *R language*
* *XAMPP, HTML, CSS, PHP, JS*

## Authors

* **Sathwik Vadlamani** - *Initial design work, Logic, debugging, pre-processing, doccumentation* - [nikhil1006](https://github.com/nikhil1006)
* **Shriram Ravindranathan** - *logic Debugging ,html & php coding* - [notshriram](https://github.com/notshriram)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Acknowledgments

* based on the inputs Given by ```N. Askok Kumar Sci/Eng - SE ``` & ```A. Venugopal Sci/Eng - SG GH, RDASG``` at 
 **Real-Time Data Archival Systems Division (RDASG), National Remote Sensing Center (NRSC), Indian Space Reasearch Organization (ISRO),Dept. of Space, Govt. of India.**
