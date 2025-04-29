# Astro-416-Final-mstruk

## Unsupervised Identification of Open Star Clusters in the Galactic Anticenter with Gaia DR3

##### Michael Struk


### Project Summary

This project uses unsupervised machine learning to identify open star clusters in Gaia DR3 data from the galactic anticenter. DBSCAN is applied to multidimensional feature spaces including stellar positions, parallaxes, proper motions, and radial velocities.

### Contents

`final_proj_drafting.ipynb` is the main analysis Jupyter Notebook

`field_reduced.csv` is the chosen field read into the notebook, queried with ADQL and saved

### Methods

We explore the results of using two feature matrices:

* Positional quantities - RA, Dec, & Parallax
* Positional and kinematic quantities - RA, Dec, Parallax, Proper motions (RA/Dec), & Radial Velocity

These features were standardized using z-score scaling, and DBSCAN was used for clustering. The hyperparameters of DBSCAN were tuned and optimized using the silhouette score, and refined using astrophysical diagnosis of distribution spread.

### Tools Used

This project employed many libraries, including:
* Numpy
* Matplotlib
* Pandas
* astropy
* astroquery
* Scikit-learn

and, more specifically, from Scikit-learn:
* `StandardScaler()` - used for z-score feature scaling
* `DBSCAN()` - the density-based clustering algorithm
* `silhouette_score()` - hyperparameter tuning and clustering quality metric


The astrophysical validation was performed with distribution and spread analysis and Color-Magnitude Diagrams (CMD). 


### Results

Both of the feature sets aided in successfully identifying physically meaningful open clusters. Including the kinematics increased restrictiveness for cluster association and improved cluster coherence but resulted in fewer clusters detected.
