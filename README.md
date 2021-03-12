# EDDI

This repository includes a function for the parametric calculation of the **Evaporative Demand Drought Index (EDDI)** based on the Log-logistic distribution.

This function is based on spei funtion provided by Santiago Beguería and Sergio M. Vicente-Serrano 
(https://github.com/sbegueria/SPEI).


## Details

The function `<eddi>` is provided to compute the Evaporative Demand Drought Index (EDDI) by means of a parametric approach. The sign of the EDDI is reversed by default (i.e., increase in AED results in decreases in EDDI values). The repository also includes other auxiliary low-level functions such as `<kern>`, `<cdfglo>` or `<pglo>`, as well as the functions `<thornthwaite>`, `<hargreaves>` and `<penman>` for computing potential evapotranspiration (see more details in https://github.com/sbegueria/SPEI).


## References

You can cite this references if you use the SPEI library on your work:

* S.M. Vicente-Serrano, S. Beguería, J.I. López-Moreno. 2010. A Multi-scalar drought index sensitive to global warming: The Standardized Precipitation Evapotranspiration Index – SPEI. *Journal of Climate* **23**: 1696, DOI: 10.1175/2009JCLI2909.1.

* Beguería S, Vicente-Serrano SM, Reig F, Latorre B. 2014. Standardized precipitation evapotranspiration index (SPEI) revisited: parameter fitting, evapotranspiration models, tools, datasets and drought monitoring. *International Journal of Climatology* **34(10)**: 3001-3023.

Other references:

* S.M. Vicente-Serrano, S. Beguería, J.I. López-Moreno. 2010. A Multi-scalar drought index sensitive to global warming: The Standardized Precipitation Evapotranspiration Index – SPEI. *Journal of Climate* **23**: 1696, DOI: 10.1175/2009JCLI2909.1.

* Beguería S, Vicente-Serrano SM, Reig F, Latorre B. 2014. Standardized precipitation evapotranspiration index (SPEI) revisited: parameter fitting, evapotranspiration models, tools, datasets and drought monitoring. *International Journal of Climatology* **34(10)**: 3001-3023.

