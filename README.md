### How to Get the Data Using git-annex
Please follow the steps below to obtain the data needed for reproducing our study.
The data is stored on the cloud service Sciebo, accessible to members of the University of Cologne: https://uni-koeln.sciebo.de/s/jmRcT2Jsd3NaLFe?path=%2Fdata. To fetch the data using git-annex, the Sciebo folder must be synced locally, that is, via the Sciebo desktop app.

1. Download the Sciebo app here: https://hochschulcloud.nrw/de/download/index.html. Log in and navigate to the folder, making sure that is synced locally. The path to the local folder should look like this: ```[YOUR PATH]/sciebo/reproduction_artefacts/data```

4. Clone the repository to get a local copy of the repository including symlinks. Copy this into your terminal.


   ``` git clone <https://github.com/RoseHst/Reproduction-Listening-to-Accents>.git```


5. In the cloned repository, initialize the sciebo remote by pointing it to the correct folder, so that git-annex knows where the actual data is.

   ``` git annex initremote sciebo-remote type=directory directory=~[YOUR PATH]/sciebo/reproduction_artefacts/data encryption=none ```

6. Fetch the data: This replaces the symlinks with the actual files.


   ```git annex get .```
