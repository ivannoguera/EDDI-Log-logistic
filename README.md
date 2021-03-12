# EDDI

This repository includes a function for the parametric calculation of the **Evaporative Demand Drought Index (EDDI)** based on the Log-logistic distribution.

This funtion is based on spei funtion create by 
[spei.csic.es](http://spei.csic.es/).


## Details

Functions `<spei>` and `<spi>` are the workhorse of the SPEI library. Other functions such as `<kern>`, `<cdfglo>` or `<pglo>` are auxiliary low-level functions and they will not be used directly by the typical user. Functions for computing potential evapotranspiration are provided, too, for helping computing the SPEI. These are: `<thornthwaite>`, `<hargreaves>` and `<penman>`.


## Installation

Install the latest stable development version from GitHub:

```r
library(devtools)
install_github('sbegueria', 'SPEI')
```

Or get it from the [CRAN](https://cran.r-project.org) repository:

```r
install.packages('SPEI')
```

Please, note that the CRAN version may not be the very latest version of the package.


## References

You can cite this references if you use the SPEI library on your work:

* S.M. Vicente-Serrano, S. Beguería, J.I. López-Moreno. 2010. A Multi-scalar drought index sensitive to global warming: The Standardized Precipitation Evapotranspiration Index – SPEI. *Journal of Climate* **23**: 1696, DOI: 10.1175/2009JCLI2909.1.

* Beguería S, Vicente-Serrano SM, Reig F, Latorre B. 2014. Standardized precipitation evapotranspiration index (SPEI) revisited: parameter fitting, evapotranspiration models, tools, datasets and drought monitoring. *International Journal of Climatology* **34(10)**: 3001-3023.

Other (possibly useful) references:

* Vicente-Serrano, S.M., Beguería, S., López-Moreno, J.I., Angulo, M., El Kenawy, A. 2010. A new global 0.5° gridded dataset (1901-2006) of a multiscalar drought index: comparison with current drought index datasets based on the Palmer Drought Severity Index. *Journal of Hydrometeorology* **11**: 1033--1043.

* Beguería, S., Vicente-Serrano, S.M. y Angulo, M. 2010. A multi-scalar global drought data set: the SPEIbase: A new gridded product for the analysis of drought variability and impacts. *Bulletin of the American Meteorological Society* **91**: 1351--1354.

* Vicente-Serrano, S.M., Beguería, S. and Juan I. López-Moreno. 2011. Comment on “Characteristics and trends in various forms of the Palmer Drought Severity Index (PDSI) during 1900-2008” by A. Dai. *Journal of Geophysical Research-Atmosphere* **116**: D19112, doi:10.1029/2011JD016410.

* Vicente-Serrano, S.M., Santiago Beguería, Jorge Lorenzo-Lacruz, Jesús Julio Camarero, Juan I. López-Moreno, Cesar Azorin-Molina, Jesús Revuelto, Enrique Morán-Tejeda and Arturo Sánchez-Lorenzo. 2012. Performance of drought indices for ecological, agricultural and hydrological applications. *Earth Interactions* **16**: 1--27.

* Vicente-Serrano, S.M., Célia Gouveia, Jesús Julio Camarero, Santiago Beguería, Ricardo Trigo, Juan I. López-Moreno, César Azorín-Molina, Edmond Pasho, Jorge Lorenzo-Lacruz, Jesús Revuelto, Enrique Morán-Tejeda and Arturo Sanchez-Lorenzo. 2012. The response of vegetation to drought time-scales across global land biomes. *Proceedings of the National Academy of Sciences of the United States of America*, doi: 10.1073/pnas.1207068110.

* Vicente-Serrano, S.M., Gerard Van der Schrier, Santiago Beguería, Cesar Azorin-Molina, Juan-I. Lopez-Moreno. 2015. Contribution of precipitation and reference evapotranspiration to drought indices under different climates. Journal of Hydrology 426: 42--54.

* Vicente-Serrano, S.M., Beguería, S. 2016. Comment on "Candidate Distributions for Climatological Drought Indices (SPI and SPEI)" by James H. Stagge et al. *International Journal of Climatology* **36**: 2120--213.



## Version history

### Version 1.7.2, January 2018 (current on github).

1. Several code optimizations and improvements (by github user doug-friedman).
2. Added formal unit testing with testthat (doug-friedman).
3. Move documentation over to roxygen (doug-friedman).
4. Update `<spei>` function to allow processing data with frequency different than 12 (by github user MuDestructor).

### Version 1.7.1, June 2017.

1. Corrected an error in `<spei>` function, which was not working when distribution was Gamma or PeasonIII and using user provided parameters. (Fixed by Emanuele Cordano, emanuele.cordano@gmail.com -- ecor)
2. Added probability of monthly precipitation = 0 (pze) when using user provided parameters. (Fixed by Emanuele Cordano, emanuele.cordano@gmail.com -- ecor) 

### Version 1.7, June 2017 (current on CRAN).

1. Corrected a bug in the `<kern>` function which resulted in a multiplicative kernel instead of an additive one such the one expected in the `<spei>` and `<spi>` functions.
2. Some small corrections to the plotting function and to the examples.

### Version 1.6, September 2013.

1. Corrected an error in the function `<thornthwaite>` which resulted in wrong potential evapotranspiration estimates when a multivariate time series was used as input.
2. Corrected an error in the function `<spi>` which resulted in wrong handling of zero precipitation months when using the Gamma or PearsonIII distribution.
3. Minor fixes to the `<spi>` and `<plot.spei>` functions to correctly handle \code{spei} objects when they result from a call to `<spi>`.
4. Modification to the `<kern>` function, which now yields kernel coefficients averaging one.
5. Corrected an error in the functions `<spi>` and `<spei>` which resulted in ub-pwm method being used irrespective of the value of the \code{fit} parameter used, when using the 'Gamma' or 'PearsonIII' distributions.
6. Minor changes to the documentation.

### Version 1.5, May 2013.

1. Optimization of function `<spei>`, now using embed() for accumulating the data at the desired time scale.

### Version 1.4, May 2013.

1. Minor fixes to functions `<penman>` and `<pwm>`.
2. Documentation of the penman function defined by mistake ed as the saturation vapour pressure, while it should read 'actual vapour pressure'.
3. Function zzz.R added to display basic information about the SPEI package at startup.
4. Function `<SPEINews>` added to display the NEWS file.

### Version 1.3, March 2013.

1. Minor fixes to functions `<spei>` and `<penman>`.
2. Added new option for user-supplied SPEI parameters in the `<spei>` function. This overrides the fitting of a probability function to the data.
3. Added new dataset `<cabinda>` from Allen et al. (1998).

### Version 1.2, October 2012.

1. Fixed a bug causing several functions to fail when a time series not belonging to matrix class was provided.
2. Function `<plot.spei>` now distinguises between calls to spei and spi and labels the axis accordingly.

### Version 1.1, March 2012.

1. Functions `<spei>` and `<spi>` now yield an object of class "spei".
2. New functions for summarizing and plotting "spei" objects are provided.
3. An option to establish a reference period for the computation of the indices has been implemented in functions `<spei>` and `<spi>`.

### Version 1.0, January 2012.

First release of the SPEI package.


## To do list (work in progress)

- [ ] Complete the documentation for pwmLC.Rd.
- [ ] New options for computing reference evapotranspiration.
- [ ] Review method plot.spei() that produces wrong results in some cases.
- [ ] Implement parallel processing - see branch parallel.
- [ ] Analysis function - see branch corel_anal.
- [ ] Add a warning message to penman function to inform the user about the
      options being used. A verbose option will control wether or not to display
      this warning.
- [ ] A version of penman function for daily data (there is one version on my
      blog, http://santiago.begueria.es).
- [ ] Different versions of the Penman-Monteith ET0 calculation (FAO-56, ASDE,
      etc), as Miquel did.


## Any problems?

Feel free to [write an issue](https://github.com/sbegueria/SPEI/issues) if you have any questions or problems.


## Copyright and license

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 2 of the License, or (at your option) any later version.
