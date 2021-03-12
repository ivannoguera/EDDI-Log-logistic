# EDDI

This repository includes a function for the parametric calculation of the **Evaporative Demand Drought Index (EDDI)** based on the Log-logistic distribution. This function represents an methodological alternative for EDDI calculation, instead of the original formulation of EDDI based on a non-parametric approach proposed by Hobbins et al. (2016).

The function `<eddi>` is based on spei funtion provided by Santiago Beguería and Sergio M. Vicente-Serrano 
(https://github.com/sbegueria/SPEI).


## Details

The function `<eddi>` is provided to compute the **Evaporative Demand Drought Index (EDDI)** by means of a parametric approach. The sign of the EDDI is reversed by default (i.e., increase in ETo results in decreases in EDDI values). The repository also includes other auxiliary low-level functions such as `<kern>`, `<cdfglo>` or `<pglo>`, as well as the functions `<thornthwaite>`, `<hargreaves>` and `<penman>` for computing potential evapotranspiration (see more details in https://github.com/sbegueria/SPEI).


## References

* Noguera, I.; Vicente-Serrano, S.M.; Domínguez-Castro, F.; Reig, F. 2021. Assessment of parametric approaches to calculate the Evaporative Demand 
Drought Index (EDDI). *Int. J. Climatol*. 2021. Under Review.

* Noguera I, Domínguez-Castro F, Vicente-Serrano SM. 2021. Flash Drought Response to Precipitation and Atmospheric Evaporative Demand in Spain. 
*Atmosphere*. MDPI AG, **12(2)**: 165. https://doi.org/10.3390/atmos12020165.

* Hobbins MT, Wood A, McEvoy DJ, Huntington JL, Morton C, Anderson M, Hain C. 2016. The evaporative demand drought index. Part I: Linking drought evolution to variations in evaporative demand. *Journal of Hydrometeorology*, **17(6)**: 1745–1761. https://doi.org/10.1175/JHM-D-15-0121.1.

Other references:

* S.M. Vicente-Serrano, S. Beguería, J.I. López-Moreno. 2010. A Multi-scalar drought index sensitive to global warming: The Standardized Precipitation Evapotranspiration Index – SPEI. *Journal of Climate* **23**: 1696, DOI: 10.1175/2009JCLI2909.1.

* Beguería S, Vicente-Serrano SM, Reig F, Latorre B. 2014. Standardized precipitation evapotranspiration index (SPEI) revisited: parameter fitting, evapotranspiration models, tools, datasets and drought monitoring. *International Journal of Climatology* **34(10)**: 3001-3023.

