#### Normal stacking stuff
* For QSO and LAE catalogues respectively: trimmed each catalogue to the COMAP fields (with small amount of padding), removed duplicates (objects within 5 arcsec and 0.001 z were considered close enough to be duplicates)
* Ran a stack on these catalogues for each frequency in our frequency bin 

#### DM Mass stuff
* Added mass as an acceptible unit in lim_stacker
* Generated halo mass map + cat from `COMAP_z2.39-3.44_1140Mpc_seed_13585.npz` and stacked on it.

#### Bootstrap stuff
* Created bootstraps for both QSOs and LAEs across 100-101 GHz (0.1 step) using obj counts from stacking at each respective frequency
* Plotted the results in `plotting.ipynb`

#### BGS stuff
* Integrated magnitudes functions into limlam mocker `magschechter`, `abundancematchmags`.
* Generated mock maps and mock catalogues for BGS.
* Stacked on BGS map + cat using LAE params. Result is centered around the mean value of the spectrum and not the peak? 
