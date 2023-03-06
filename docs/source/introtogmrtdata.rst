Introduction to the GMRT data
==============================

GMRT can record data in continuum, spectral line and pulsar (incoherent/coherent array) 
modes.

Continuum and spectral line data
---------------------------------

These are data typically recorded with the full array and contain visibilities. 
The raw data are in the "lta" format. The continuum and spectral line data will 
both be in the same format. The data in lta format is converted to FITS format 
using the in-house codes *listscan* and *gvfits*. The FITS file is further converted 
into the measurement set (ms) format in order to analyse the data using CASA.

The GMRT online archive (GOA) allows you to download data in FITS and lta formats. 
Thus if you downloaded your data in FITS format you can skip the step of converting 
the format from lta to FITS.

The files downloaded from GOA having 'gsb' in their filenames are the data recorded with 
the narrow band backend which was called the GMRT Software Backend. The files with 'GWB' 
in their names are the data recorded using the GMRT Wideband Backend (GWB) which is the 
new wideband system (Upgraded GMRT).


Pulsar data
------------
